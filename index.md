---
layout: default
---	
<div class="s_left sa_articleinfo">
{% for post in site.posts limit:5 %}
	<h1><a href="{{ post.url }}">{{ post.title }}</a>&#160;<small><span class="ds-thread-count" data-thread-key="{{ post.id }}"></span>评论&#160;{{ post.date | date:"%b %e, %Y" }}</small></h1>
		<blockquote>{{ post.description }}</blockquote>
		<p><a href="{{ post.url }}">阅读全文 &raquo; </a></p>
		{% for tag in post.tags %}
		<span class="sa_articletag"><a  href="/tag/#{{ tag }}">{{ tag }}</a></span>
		{% endfor %}
		<span class="clearfix"></span>
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
<ul class="clearfix sa_authorinfo">
<li><span class="s">{{ site.posts.size }}</span>文章</li>
<li><span class="s">{{ site.tags.size }}</span>标签</li>
<aside id="socials">
<li id="weibo"><a class="ir" href="http://weibo.com/mjjinc" title="新浪微博" rel="external">kooker 新浪微博</a></li>
<li id="github"><a class="ir" href="https://github.com/kooker" title="github" rel="external">github</a></li>
<li id="mp3"><a class="ir" href="http://hibcs.kooker.jp/mp3" title="MP3分享列表" rel="external">MP3分享列表</a></li>
<li id="rss"><a class="ir" href="{{ site.production_url }}/atom.xml" title="RSS" rel="external">RSS</a></li>
<!-- <li id="diandian"><a class="ir" href="http://hi.kooker.jp/" title="Hi kooker" rel="external">Hi kooker</a></li> -->
</aside>
</ul>
</div>
</div>
                    
<div class="sa_hotarticles">
<div class="sa_right_title_b">友情链接</div>
<ul>
<li><a href="http://www.kooker.jp" title="">技术支持</a></li>
<li><a href="http://www.zhishou.org/" title="灰常灰常有钱途的MJJer" target="_blank">气总</a></li>
<li><a href="http://blog.yihao.me/" title="大脚小P" target="_blank">Yihao's</a></li>
<li><a href="http://www.sexdiy.org/" title="MJJ疯人院李院长梅子雨MM" target="_blank">李可先</a></li>
<li><a href="http://www.83sun.com/" title="疯子拿把枪的总部" target="_blank">欢仔</a></li>
<li><a href="http://alistorm.com/" title="阿里士多支那博客" target="_blank">阿里士多</a></li>
<li><del datetime="2012-08-08T00:38:38+08:00"><a href="http://www.neweye.org/" title="妞爱MM" target="_blank" rel="nofollow">Neweye</a></del></li>
</ul>
</div>

<div class="sa_hotarticles">
<div class="sa_right_title_b">最近访客</div>
<ul class="ds-recent-visitors"></ul>
</div>

</div><!-- End  sa_right-->