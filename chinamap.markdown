---
layout: default
title: 比赛地图
permalink: /chinamap/
---

<h1>比赛地图</h1>
<div id="map" style="height: 600px;"></div>
<!-- Include Leaflet.js CSS and JS -->
<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
  // Initialize the map
  var map = L.map('map').setView([35.8617, 104.1954], 4); // Centered on China

  // Add OpenStreetMap tile layer
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '© OpenStreetMap contributors'
  }).addTo(map);

  // Province coordinates
  var provinces = {
    "北京": [39.9042, 116.4074],
    "天津": [39.3434, 117.3616],
    "河北": [38.0373, 114.4687],
    "山西": [37.8798, 112.5589],
    "内蒙": [40.8175, 111.7656],
    "辽宁": [41.8057, 123.4328],
    "吉林": [43.8868, 125.3245],
    "黑龙江": [45.7415, 126.6425],
    "上海": [31.2304, 121.4737],
    "江苏": [32.0603, 118.7969],
    "浙江": [30.2741, 120.1551],
    "安徽": [31.8612, 117.2857],
    "福建": [26.0998, 119.2965],
    "江西": [28.6749, 115.9100],
    "山东": [36.6683, 117.0204],
    "河南": [34.7652, 113.6840],
    "湖北": [30.5454, 114.3423],
    "湖南": [28.1127, 112.9834],
    "广东": [23.1291, 113.2644],
    "广西": [22.8155, 108.3275],
    "海南": [20.0174, 110.3486],
    "重庆市": [29.5630, 106.5516],
    "四川": [30.5728, 104.0668],
    "贵州": [26.5783, 106.7135],
    "云南": [25.0422, 102.7064],
    "西藏": [29.6473, 91.1175],
    "陕西": [34.3416, 108.9402],
    "甘肃": [36.0594, 103.8263],
    "青海": [36.6234, 101.7782],
    "宁夏": [38.4872, 106.2309],
    "新疆": [43.7928, 87.6271],
    "香港": [22.3193, 114.1694],
    "澳门": [22.1987, 113.5439],
    "台湾": [25.0329, 121.5654]
  };

  // Marker data from Jekyll data file
  var competitions = [
    {% for competition in site.marathon %}
    {
      "name": "{{ competition.name }}",
      "place": "{{ competition.place }}",
      "date": "{{ competition.date }}"
    }{% if forloop.last == false %},{% endif %}
    {% endfor %}
  ];

  // Track which provinces have markers
  var provincesWithMarkers = {};

  // Add markers to the map
  competitions.forEach(function(competition) {
    var parts = competition.place.split('/');
    var city = parts[0];
    var province = parts[1];

    if (!provincesWithMarkers[province]) {
      var coords = provinces[province];
      if (coords) {
        L.marker(coords).addTo(map)
          .bindPopup('<b>' + competition.name + '</b><br>' + city + ', ' + province + '<br>' + competition.date);
        provincesWithMarkers[province] = true;
      }
    }
  });
</script>

