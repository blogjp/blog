---
layout: default
title: 标签
permalink: /tags/
---
<div class="s_left">
{% for tag in site.tags %}
<a name="{{ tag | first }}"><h2>&#160;&#160;{{ tag | first }}<sup>{{ tag.last.size }}</sup></h2></a>
    <ul>
    {% for post in tag.last %}
      <li class="sa_abstract"><a href="{{ post.url }}">{{ post.title }}</a> <span class="ds-thread-count" data-thread-key="{{ post.id }}"></span>评论</li>
    {% endfor %}
    </ul>
{% endfor %}
</div>

<div class="sa_right clearfix">
<div class="s_i_r_title"><span>作者信息</span></div>
<div class="sa_articleinfo">
<div class="clearfix">
<div class="sa_avatar"><img src="{{ site.production_url }}/images/author.jpg"></div>
<div class="sa_text">
<p><span>{{ site.author.name }} {{ site.author.info }}</span></p>
<p>{{ site.author.description }}</p>
<p style="min-height:10px;"></p>
</div>
<ul id="socials" class="clearfix sa_authorinfo">
<li id="weibo"><a class="ir" href="http://weibo.com/mjjinc" title="新浪微博" rel="external">kooker 新浪微博</a></li>
<li id="github"><a class="ir" href="https://github.com/kooker" title="github" rel="external">github</a></li>
<li id="diandian"><a class="ir" href="http://hi.kooker.jp/" title="Hi kooker" rel="external">Hi kooker</a></li>
</ul>
</div>
</div>

<div class="sa_hotarticles">
<div class="sa_right_title_b">最近访客</div>
<ul class="ds-recent-visitors"></ul>
</div>

<div class="sa_hotarticles">
<div class="sa_right_title_b">友情链接</div>
<ul>
<li><a href="http://cdn.kooker.jp" title="">技术支持</a></li>
<li><a href="http://www.zhishou.org/" title="灰常灰常有钱途的MJJer" target="_blank">气总</a></li>
<li><a href="http://blog.yihao.me/" title="大脚小P" target="_blank">Yihao's</a></li>
<li><a href="http://www.sexdiy.org/" title="MJJ疯人院李院长梅子雨MM" target="_blank">李可先</a></li>
<li><a href="http://www.83sun.com/" title="疯子拿把枪的总部" target="_blank">欢仔</a></li>
<li><a href="http://alistorm.com/" title="阿里士多支那博客" target="_blank">阿里士多</a></li>
<li><del datetime="2012-08-08T00:38:38+08:00"><a href="http://www.neweye.org/" title="妞爱MM" target="_blank" rel="nofollow">Neweye</a></del></li>
</ul>
</div>

</div><!-- End  sa_right-->