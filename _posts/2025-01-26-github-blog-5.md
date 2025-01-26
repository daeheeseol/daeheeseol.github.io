---
title: Github Blog by Chirpy theme (3) sitemap.xml 및 robots.txt 생성
description: Chirpy theme로 Github Blog 만들기 (2025-01 기준)
author: SemiDS
date: 2025-01-16 20:00:00 +0900
categories: [Github Blog, sitemap]
tags: [Github, Chirpy]
pin: true
---

## (1). sitemap.xml 생성
블로그 내 콘텐츠들을 Google에서 검색시 노출이 되게 하려면, sitemap.xml 파일을 생성하고 이를 Google Search Console에 등록해주는 과정이 필요합니다. (Naver는 서치어드바이저)  
Jekyll에서 sitemap.xml 파일을 간편하게 만들기 위해서 아래와 같은 2가지 방법을 사용할 수 있습니다. 

>- jekyll-sitemap plugin
>- sitemap.xml 생성을 위한 script
{: .prompt-tip }

### (1)-1. jekyll-sitemap plugin
`_config.yaml`파일과 동일한 경로에 있는 `Gemfile`에 아래 코드를 추가합니다. 

```shell
gem "jekyll-sitemap"
```
그리고, `_config.yaml`에 아래와 같이 plugin 코드 부분을 추가합니다.
```shell
plugins:
    - jekyll-sitemap
```
### (1)-2. sitemap.xml 생성을 위한 script
`_config.yaml`파일과 동일한 경로에 `sitemap.xml` 파일을 만들고 아래 코드를 입력합니다.
```ruby
{% raw %}
---
layout: null
---
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9 http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd" xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    {% for post in site.posts %}
    <url>
        <loc>{{ site.url }}{{ post.url }}</loc>
        {% if post.lastmod == null %}
        <lastmod>{{ post.date | date_to_xmlschema }}</lastmod>
        {% else %}
        <lastmod>{{ post.lastmod | date_to_xmlschema }}</lastmod>
        {% endif %}

        {% if post.sitemap.changefreq == null %}
        <changefreq>weekly</changefreq>
        {% else %}
        <changefreq>{{ post.sitemap.changefreq }}</changefreq>
        {% endif %}

        {% if post.sitemap.priority == null %}
        <priority>0.5</priority>
        {% else %}
        <priority>{{ post.sitemap.priority }}</priority>
        {% endif %}

    </url>
    {% endfor %}
</urlset>
{% endraw %}
```

## (2) robots.txt 생성
`_config.yaml`파일과 동일한 경로에 `robots.txt` 파일을 만들고 아래와 같이 입력하면 됩니다. 
```
{% raw %}
User-agent: *
Allow: /
Sitemap: {{ '/sitemap.xml' | relative_url | prepend: site.url }}
{% endraw %}
```

---
위와 같은 방법으로 `sitemap.xml`과 `robots.txt`파일을 생성한 후에 local에서 build 해보면 `_site` 경로 내 `sitemap.xml`과 `robots.txt` 파일이 생성 되는걸 확인할 수 있습니다.

참고로, `Chirpy theme`의 경우는 `sitemap.xml`과 `robots.txt`를 자동으로 생성해주는 기능이 이미 내장되어 있기 때문에, `Chirpy theme`를 사용해서 만든 블로그라면 따로 생성을 따로 해주지 않아도 자동으로 생성 됩니다.

![1](/assets/img/posting/2025-01-26-github-blog-1_1.png)
