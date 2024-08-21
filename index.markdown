---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
  <main>
    <h3>用脚步丈量世界</h3>
    <ul>
        <li>2015年开始从几百米跑到5K</li>
        <li>2015/11/08完成人生首个半马 <a href="/marathon/2015上海马拉松.html">2015上海马拉松</a>，02:25:16，达标大众三级</li>
        <li>2016/09/17完成人生首个全马<a href="/marathon/2016北京马拉松.html">2016北京马拉松</a>，05:05:57</li>
        <li>2017/12/10首次完成全马破四2017广州马拉松，03:53:56，达标大众一级</li>
        <li>2018/03/25完成北京武汉广州重庆四站，成为<span style="color:red;">首届中国马拉松大满贯跑者</span>，拿到大满贯奖牌</li>
        <li>2021/04/11成功突破330，2021无锡马拉松，03:18:14，达标大众精英</li>
        <li>2023/08/27历时8年成功破三BQ近半小时，2023哈尔滨马拉松，02:56:20</li>
        <li>2023/10/04在连续四天戈壁122KM之后直飞芝加哥背靠背大PB完成SUB250，2023芝加哥马拉松，<span style="color:red;">02:49:52</span></li>
        <li>2024/04/15完成六大满贯最后一站，2024波士顿马拉松，02:56:53，成为<span style="color:red;">全球六大满贯跑者</span>，拿到六星奖牌</li>
        <li>2024/08/10完成2024巴黎奥运会马拉松大众组，实现奥运梦想，03:11:16，成为<span style="color:red;">奥运跑者</span></li>
    </ul>

    <h3>TODO</h3>
    <ul>
        <li>戈壁A+</li>
        <li>UTMB/UTMB</li>
        <li>FUJI 168</li>
        <li>WSER/100M</li>
        <li>八百流沙</li>
        <li>环青海湖七天七马</li>
        <li>南极马拉松</li>
        <li>珠峰马拉松</li>
        <li>雅典马拉松</li>
        <li>悉尼马拉松</li>
        <li>首尔马拉松</li>
        <li>新加坡马拉松</li>
        <li>朝鲜马拉松</li>
        <li>越南马拉松</li>
        <li>777</li>
        <li>------省会-------</li>
        <li>拉萨马拉松</li>
        <li>乌鲁木齐马拉松</li>
        <li>长沙马拉松</li>
        <li>西安马拉松</li>
        <li>吉林马拉松</li>
        <li>石家庄马拉松</li>
        <li>南昌马拉松</li>
        <li>桂林马拉松</li>
        <li>昆明马拉松</li>
        <li>呼和浩特马拉松</li>
        <li>台北马拉松</li>
        <li>------备选-------</li>
        <li>深圳马拉松</li>
        <li>成都马拉松</li>
        <li>郑开马拉松</li>
        <li>沈阳马拉松</li>
        <li>海口马拉松</li>
        <li>贵阳马拉松</li>
        <li>衡水湖马拉松</li>
        <li>香港马拉松</li>
        <li>吉木萨尔马拉松</li>
        <li>-------------</li>
        <li>泰国马拉松</li>
    </ul>
  </main>


<h3>百马王子进度</h3>

{% assign total_marathons = 100 %}
{% assign total_marathon = site.marathon | size %}
{% assign total_trail = site.trail | size %}
{% assign total_gebi = site.gebi | size %}
{% assign total_play = site.play | size %}
{% assign completed_marathons_temp = total_marathon | plus: total_trail %}
{% assign completed_marathons_temp2 = completed_marathons_temp | plus: total_gebi %}
{% assign completed_marathons = completed_marathons_temp2 | plus: total_play %}

{% assign progress_percentage = completed_marathons | times: 100 | divided_by: total_marathons %}

<div class="progress-bar-container" style="width: 100%; background-color: #f3f3f3; border-radius: 5px; overflow: hidden;">
  <div class="progress-bar" style="width: {{ progress_percentage }}%; height: 30px; background-color: #4caf50;"></div>
</div>
<p>{{ completed_marathons }} / {{ total_marathons }} 场马拉松已完成</p>