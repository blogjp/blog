---
layout: post
title: SaBlog-X 2.0 Nginx URL Rewrite
tags: ['Nginx']
description: 替换掉全部包含文件的路径 SABLOG_ROOT.
---
替换掉全部包含文件的绝对路径 `SABLOG_ROOT.`<br />
将下面 rewrite 规则加入站点配置中，重启Nginx

    # 归档
        rewrite ^/date/([0-9]+)/([0-9]+)/page/([0-9]+)?/?$ /index.php?action=article&setdate=$1&setday=$2&page=$3 last;
        rewrite ^/date/([0-9]+)/([0-9]+)/?$ /index.php?action=article&setdate=$1&setday=$2 last;
        rewrite ^/date/([0-9]+)/page/([0-9]+)?/?$ /index.php?action=article&setdate=$1&page=$2 last;
        rewrite ^/date/([0-9]+)/?$ /index.php?action=article&setdate=$1 last;
    # 无分类翻页
        rewrite ^/page/([0-9]+)?/?$ /index.php?action=article&page=$1 last;
    # 分类
        rewrite ^/category/([0-9]+)/?([0-9]+)?/?$ /index.php?action=article&cid=$1&page=$2 last;
        rewrite ^/category/([^/]+)/?([0-9]+)?/?$ /index.php?action=article&curl=$1&page=$2 last;
    # 归档、高级搜索
        rewrite ^/(archives|list|article|links)/?$ /index.php?action=$1 last;
    # 全部评论、标签列表、带分页
        rewrite ^/(comments|tagslist|article)/?([0-9]+)?/?$ /index.php?action=$1&page=$2 last;
    # 搜索结果
        rewrite ^/search/([0-9]+)/?([0-9]+)?/?$ /index.php?action=article&searchid=$1&page=$2 last;
    # tags
        rewrite ^/tag/([^/]+)/?([0-9]+)?/?$ /index.php?action=article&tag=$1&page=$2 last;
    # 文章
        rewrite ^/archives/([0-9]+)/?([0-9]+)?/?$ /index.php?action=show&id=$1&page=$2 last;
    # RSS
        rewrite ^/rss/([0-9]+)?/?$ /rss.php?cid=$1 last;
        rewrite ^/rss/([^/]+)/?$ /rss.php?url=$1 last;
    # 用户
        rewrite ^/uid/([0-9]+)/?([0-9]+)?/?$ /index.php?action=article&uid=$1&page=$2 last;
        rewrite ^/user/([^/]+)/?([0-9]+)?/?$ /index.php?action=article&user=$1&page=$2 last;
    # 自定义链接
        rewrite ^/([^/]+)/?([0-9]+)?/?$ /index.php?action=show&alias=$1&page=$2 last;
    # 地图文件
        rewrite  ^/sitemap\.xml$  /sitemap.php last;
