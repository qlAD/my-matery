# My-matery

[中文文档](README_CN.md) | [Access Example (Meteor's Blog)](https://qlad.gitee.io/)

> Thanks:
> [zhangpanqin/my-hexo-theme-matery](https://github.com/zhangpanqin/my-hexo-theme-matery)
> [godweiyang/hexo-matery-modified](https://github.com/godweiyang/hexo-matery-modified)

## Features

-Simple and beautiful, the content of the article is beautiful and easy to read
-Responsive design, blog can be displayed well on desktop, tablet, mobile phone and other devices
-Homepage carousel articles and daily dynamic switching of `Banner` pictures
-Waterfall list of blog posts
-Timeline archive page
-**Word Cloud** tab page and **Radar Chart** category page
-Rich about me pages (including about me, article statistics, my projects, my skills, photo albums, etc.)
-Customizable data link page
-Support article top and article reward
-Support `MathJax`
-`TOC` directory
-You can add copyright information when copying article content
-Password verification can be set when reading articles
-Integrated [Gitalk](https://gitalk.github.io/), [Gitment](https://imsun.github.io/gitment/), [Valine](https://valine.js.org /) and [Disqus](https://disqus.com/) comment module (`Gitalk` is recommended)
-Integrated functions such as [Busuanzi Statistics](http://busuanzi.ibruce.info/), Google Analytics (`Google Analytics`) and article word count statistics
-Support music playback and video playback on the homepage
-Support `emoji` emoticons, use `markdown emoji` grammar writing to directly generate corresponding **jumping emoticons.
-Support [DaoVoice](http://www.daovoice.io/), [Tidio](https://www.tidio.com/) online chat function.

## Download

This topic **recommend you to use Hexo 5.0.0 and above**. If you already have your own [Hexo](https://hexo.io/zh-cn/) blog, I suggest you upgrade Hexo to the latest stable version.

Go to your `themes` folder and use the `git clone` command to download:

```bash
git clone https://github.com/qlAD/my-matery.git
```

## Configuration

### Switch theme

Modify the value of `theme` in `_config.yml` under the Hexo root directory: `theme: my-matery`

#### Other suggestions for modification of `_config.yml` file:

-Please modify the value of `url` in `_config.yml` to your website's main `URL` (for example: `http://xxx.github.io`).
-It is recommended to modify the page bar value of `per_page` to a multiple of `6`, such as: `12`, `18`, etc., so that the article list can be better displayed on each screen.
-If you are a Chinese user, it is recommended to change the value of `language` to `zh-CN`.

### New categories page

The `categories` page is used to display all categories of pages. If there is no `categories/index.md` file in your blog's `source` directory, then you need to create a new one. The command is as follows:

```bash
hexo new page "categories"
```

Edit the page file you just created `/source/categories/index.md`, at least the following content is required:

```yaml
---
title: categories
date: 2018-09-30 17:25:30
type: "categories"
layout: "categories"
---
```

### New label tags page

The `tags` page is used to display all tags. If there is no `tags/index.md` file in your blog's `source` directory, then you need to create a new one. The command is as follows:

```bash
hexo new page "tags"
```

Edit the page file `/source/tags/index.md` you just created. At least the following content is required:

```yaml
---
title: tags
date: 2018-09-30 18:23:38
type: "tags"
layout: "tags"
---
```

### Create a new about page about me

The `about` page is used to display **about me and my blog** information. If there is no `about/index.md` file in the `source` directory of your blog, then you need to create a new one. The command is as follows:

```bash
hexo new page "about"
```

Edit the page file `/source/about/index.md` you just created. At least the following content is required:

```yaml
---
title: about
date: 2018-09-30 17:25:30
type: "about"
layout: "about"
---
```

### New message board contact page

The `contact` page is used to display **message board** information. If there is no `contact/index.md` file in your blog `source` directory, then you need to create a new one. The command is as follows:

```bash
hexo new page "contact"
```

Edit the page file `/source/contact/index.md` you just created. At least the following content is required:

```yaml
---
title: contact
date: 2018-09-30 17:25:30
type: "contact"
layout: "contact"
---
```

> **Note**: This message board function relies on a third-party comment system, please **activate** your comment system to be effective.

### New friendship link friends page

The `friends` page is a page used to display **friendship links** information. If there is no `friends/index.md` file in your blog's `source` directory, then you need to create a new one. The command is as follows:

```bash
hexo new page "friends"
```

Edit the page file `/source/friends/index.md` you just created. At least the following content is required:

```yaml
---
title: friends
date: 2018-12-12 21:25:30
type: "friends"
layout: "friends"
---
```

At the same time, create a new `_data` directory under the `source` directory of your blog, and a new `friends.json` file in the `_data` directory. The contents of the file are as follows:

```json
[
    {
    "avatar": "https://***",
    "name": "Guoguang",
    "introduction": "Information Security Chief",
    "url": "https://www.sqlsec.com/",
    "title": "Go and learn"
    },
    
    {
    "avatar": "Picture Address",
    "name": "Name",
    "introduction": "Introduction",
    "url": "Friendly Link Address",
    "title": "Button text"
    },
    
        {
    "avatar": "Picture Address",
    "name": "Name",
    "introduction": "Introduction",
    "url": "Friendly Link Address",
    "title": "Button text"
    },
]
```
#### The renderings are as follows

![友联](https://www.hualigs.cn/image/602aa15495d04.jpg)


### New 404 page

If there is no 404.md file in your blog’s source directory, then you need to create a new one

```bash
hexo new page 404
```

Edit the page file `/source/404/index.md` you just created. At least the following content is required:

```yaml
---
title: 404
date: 2018-09-30 17:25:30
type: "404"
layout: "404"
description: "Oops~, I broke down! Can't find the page you want :("
---
```

### Menu navigation configuration

#### Configure the name, path url and icon icon of the basic menu navigation.

1. Menu navigation name can be Chinese or English (such as: `Index` or `Home`)
2. Icon icon can be found in [Font Awesome](https://fontawesome.com/icons)

```yaml
menu:
  Index:
    url: /
    icon: fas fa-home
  Tags:
    url: /tags
    icon: fas fa-tags
  Categories:
    url: /categories
    icon: fas fa-bookmark
  Archives:
    url: /archives
    icon: fas fa-archive
  About:
    url: /about
    icon: fas fa-user-circle
  Friends:
    url: /friends
    icon: fas fa-address-book
```

#### Secondary menu configuration method

If you need a secondary menu, you can operate as follows on the basis of the original basic menu navigation
     
1. Add the keyword `children` under the first level menu that needs to add the second level menu (for example: add `children` under the `About` menu)
2. Create the name, path url and icon icon of the secondary menu under `children`.
3. Pay attention to adding `-` before each secondary menu module.
4. Pay attention to the indentation format

```yaml
menu:
  Index:
    url: /
    icon: fas fa-home
  Tags:
    url: /tags
    icon: fas fa-tags
  Categories:
    url: /categories
    icon: fas fa-bookmark
  Archives:
    url: /archives
    icon: fas fa-archive
  About:
    url: /about
    icon: fas fa-user-circle-o
  Friends:
    url: /friends
    icon: fas fa-address-book
  Medias:
    icon: fas fa-list
    children:
      -name: Music
        url: /music
        icon: fas fa-music
      -name: Movies
        url: /movies
        icon: fas fa-film
      -name: Books
        url: /books
        icon: fas fa-book
      -name: Galleries
        url: /galleries
        icon: fas fa-image
```


### Code highlighting

Starting from Hexo5.0 version, it comes with support for `prismjs` code syntax highlighting, and this theme has been modified to support this.

If the plugin of `hexo-prism-plugin` has been installed in your blog, you need to execute `npm uninstall hexo-prism-plugin` to uninstall it, otherwise there will be `&#123;` and The escape character for `&#125;`.

Then, modify the value of `highlight.enable` in the file `_config.yml` in the root directory of Hexo to `false` and set the value of `prismjs.enable` to `true`. The main configuration is as follows:

```yaml
highlight:
  enable: false
  line_number: true
  auto_detect: false
  tab_replace:''
  wrap: true
  hljs: false
prismjs:
  enable: true
  preprocess: true
  line_number: true
  tab_replace:''
```

The default `prismjs` theme in the theme is `Tomorrow Night`, if you want to customize your own theme, you can go to [prismjs download page](https://prismjs.com/download.html) to customize and download your favorite theme `css `File, and then name this css theme file `prism.css`, and replace the `source/libs/prism/prism.css` file in the theme folder of `hexo-theme-matery`.

### search for

The Hexo plugin of [hexo-generator-search](https://github.com/wzpan/hexo-generator-search) is also used in this theme for content search. The installation command is as follows:

```bash
npm install hexo-generator-search --save
```

In the `_config.yml` file in the Hexo root directory, add the following configuration items:

```yaml
search:
  path: search.xml
  field: post
```

### Chinese link to pinyin (recommended installation)

If your article name is in Chinese, then the permalink generated by Hexo by default will also have Chinese, which is not conducive to `SEO`, and `gitment` comments do not support Chinese links. We can use [hexo-permalink-pinyin](https://github.com/viko16/hexo-permalink-pinyin) Hexo plug-in to generate permalinks in Chinese Pinyin when generating articles.

The installation command is as follows:

```bash
npm i hexo-permalink-pinyin --save
```

In the `_config.yml` file in the Hexo root directory, add the following configuration items:

```yaml
permalink_pinyin:
  enable: true
  separator:'-' # default:'-'
```

> **Note**: In addition to this plugin, the [hexo-abbrlink](https://github.com/rozbo/hexo-abbrlink) plugin can also generate non-Chinese links.

### Article word count plugin (recommended to install)

If you want to display the word count and reading time information in the article, you can install the [hexo-wordcount](https://github.com/willin/hexo-wordcount) plugin.

The installation command is as follows:

```bash
npm i --save hexo-wordcount
```

Then just activate the configuration related to the word count of each article in the `_config.yml` file under this topic:

```yaml
postInfo:
  date: true
  update: false
  wordCount: false # Set the word count of the article to true.
  totalCount: false # Set the total word count of site articles to true.
  min2read: false # Reading time.
  readCount: false # Number of reads.
```

### Add emoji support (optional)

This theme adds support for `emoji` expressions, using the Hexo plugin of [hexo-filter-github-emojis](https://npm.taobao.org/package/hexo-filter-github-emojis) To generate `emoji` expressions, convert the corresponding `markdown emoji` grammar (`::`, for example: `:smile:`) into a jumping `emoji` expression, the installation command is as follows:

```bash
npm install hexo-filter-github-emojis --save
```

In the `_config.yml` file in the Hexo root directory, add the following configuration items:

```yaml
githubEmojis:
  enable: true
  className: github-emoji
  inject: true
  styles:
  customEmojis:
```
Execute `hexo clean && hexo g` to regenerate the blog file, and then you can see your emoji written in `emoji` syntax at the corresponding position in the article.

### Add RSS subscription support (optional)

The Hexo plug-in of [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed) is also used in this theme to do `RSS`, the installation command is as follows:

```bash
npm install hexo-generator-feed --save
```

In the `_config.yml` file in the Hexo root directory, add the following configuration items:

```yaml
feed:
  type: atom
  path: atom.xml
  limit: 20
  hub:
  content:
  content_limit: 140
  content_limit_delim: ''
  order_by: -date
```

Execute `hexo clean && hexo g` to regenerate the blog file, and then you can see the `atom.xml` file in the `public` folder, indicating that you have successfully installed it.

### Add [DaoVoice](http://www.daovoice.io/) online chat function (optional)

Go to the [DaoVoice](http://www.daovoice.io/) official website to register and get the `app_id`, and fill the `app_id` into the theme's `_config.yml` file.

### Add [Tidio](https://www.tidio.com/) online chat function (optional)

Go to the [Tidio](https://www.tidio.com/) official website to register and obtain the `Public Key`, and fill the `Public Key` into the theme's `_config.yml` file.

### Modify the footer

Footer information may need to be customized, and it is not easy to make configuration information, so you may need to modify and process it yourself. The modification is in the `/layout/_partial/footer.ejs` file of the theme file, including the site, the theme used, and the number of visits.

### Modify social links

In the theme's `_config.yml` file, the configuration of `QQ`, `GitHub` and email are supported by default. You can add new, Modify the social link addresses you need, and add links to the following code:

```html
<% if (theme.socialLink.github) {%>
    <a href="<%= theme.socialLink.github %>" class="tooltipped" target="_blank" data-tooltip="Visit my GitHub" data-position="top" data-delay="50" >
        <i class="fab fa-github"></i>
    </a>
<%} %>
```

Among them, social icons (such as: `fa-github`) can be found in [Font Awesome](https://fontawesome.com/icons). The following are the logos of commonly used social icons for your reference:

-Facebook: `fab fa-facebook`
-Twitter: `fab fa-twitter`
-Google-plus: `fab fa-google-plus`
-Linkedin: `fab fa-linkedin`
-Tumblr: `fab fa-tumblr`
-Medium: `fab fa-medium`
-Slack: `fab fa-slack`
-Sina Weibo: `fab fa-weibo`
-Wechat: `fab fa-weixin`
-QQ: `fab fa-qq`
-Zhihu: `fab fa-zhihu`

> **Note**: The version of `Font Awesome` used in this theme is `5.11.0`.

### Modify the QR code picture for rewarding

In the `source/medias/reward` file of the theme file, you can replace it with your WeChat and Alipay reward QR code pictures.

### Configure music player (optional)

To support music playback, activate the music configuration in the theme's `_config.yml` configuration file:

```yaml
# Whether to display music on the homepage
music:
  enable: true
  title: # Non-bottom suction mode is valid
    enable: true
    show: listen to music
  server: netease # require music platform: netease, tencent, kugou, xiami, baidu
  type: playlist # require song, playlist, album, search, artist
  id: 503838841 # require song id / playlist id / album id / search keyword
  fixed: false # Turn on bottom suction mode
  autoplay: false # Whether to play automatically
  theme:'#42b983'
  loop:'all' # Audio loop playback, optional values:'all','one','none'
  order:'random' # Audio loop sequence, optional values:'list','random'
  preload:'auto' # preload, optional values:'none','metadata','auto'
  volume: 0.7 # The default volume, please note that the player will remember the user settings, the default volume will be invalid after the user manually sets the volume
  listFolded: true # Default list folding
```

> `server` can choose `netease` (Netease Cloud Music), `tencent` (QQ music), `kugou` (酷狗音乐), `xiami` (shimi music),
>
> `baidu` (Baidu Music).
>
> `type` can be `song` (song), `playlist` (song list), `album` (album), `search` (search keyword), `artist` (singer)
>
> Example of how to obtain `id`: Open NetEase Cloud Music in the browser, click on the music playlist I like, there will be a string of numbers behind the browser address bar, the `id` of the `playlist`
>
> Is this string of numbers.



## Post Front-matter

### Detailed Front-matter options

Everything in the Front-matter option is **not required**. But I still recommend at least filling in the values of `title` and `date`.

| Options   | Defaults              | Description                                             |
| ---------- | --------------------------- | ------------------------------------------------------------ |
| title      | Markdown's file title | Post title, it is highly recommended to fill in this option |
| date       | Date and time when the file created | Publish time, it is highly recommended to fill in this option, and it is best to ensure that it is globally unique |
| author     | `author` in root `_config.yml` | Post author                                    |
| img        | a value in `featureImages`  | Post feature image，For example: `http://xxx.com/xxx.jpg` |
| top        | `true`                      | Recommended post (whether the post is topped), if the `top` value is `true`, it will be recommended as a homepage post. |
| cover      | `false`                     | The `v1.0.2` version is added to indicate whether the post needs to be added to the homepage carousel cover. |
| coverImg   | null                        | The new version of `v1.0.2` indicates that the post needs to display the image path on the cover of the homepage. If not, the default image of the post is used by default. |
| password   | null                        | The post read the password. If you want to set the reading verification password for the article, you can set the value of `password`, which must be encrypted with `SHA256` to prevent others from seeing it. The premise is that the `verifyPassword` option is activated in the theme's `config.yml` |
| toc        | `true`                      | Whether TOC is turned on or not, you can turn off the TOC function for an article. The premise is that the `toc` option is activated in the theme's `config.yml` |
| mathjax    | `false`                     | Whether to enable math formula support, whether this article starts `mathjax`, and you need to open it in the theme `_config.yml` file. |
| summary    | null                        | Post summary, custom post summary content, if the attribute has a value, the post card summary will display the text, otherwise the program will automatically intercept part of the article as a summary |
| categories | null                        | Article classification, the classification of this topic represents a macroscopically large classification, only one article is recommended for one classification. |
| tags       | null                        | Post label, a post can have multiple labels |
| keywords   | Post Title                  | Post key Words With SEO                               |
| reprintPolicy       | cc_by              | Post reprint policy, value could be one of cc_by, cc_by_nd, cc_by_sa, cc_by_nc, cc_by_nc_nd, cc_by_nc_sa, cc0, noreprint and pay |

> **Note**: 
> 1. post's featured picture will take remainder if not writing the `img` property, and choose the featured picture of theme to let all of post's picture **have their own characteristics**.
> 2. The value of `date` should try to ensure that each article is unique, because `Gitalk` and `Gitment` recognize `id` in this topic are uniquely identified by the value of `date`.
> 3. If you want to set the ability to read the verification password for the article, you should not only set the value of the password with SHA256 encryption in Front-matter, but also activate the configuration in the theme `_config.yml`.
> 4. you can define reprint policy for a single article in the front-matter of the specific md file using this key: reprintPolicy

The following are examples of the post's `Front-matter`.

### The simplest example

```yaml
---
title: typora-vue-theme Theme introduction
date: 2018-09-07 09:25:00
---
```

### The most comprehensive example

```yaml
---
title: typora-vue-theme Theme introduction
date: 2018-09-07 09:25:00
author: Qi Zhao
img: /source/images/xxx.jpg
top: true
cover: true
coverImg: /images/1.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary: This is the content of your custom post summary. If there is a value for this attribute, the post card summary will display the text, otherwise the program will automatically intercept part of the post content as a summary.
categories: Markdown
tags:
  - Typora
  - Markdown
---
```
## Effect screenshot

![Home](https://www.hualigs.cn/image/602aa3f8be851.jpg)

![About](https://www.hualigs.cn/image/602aa3f8c0c97.jpg)

![End of text](https://www.hualigs.cn/image/602aa3f8a952a.jpg)


## Customized modification

Some custom information can be modified in the `_config.yml` of this topic. There are the following parts:

-Menu
- my dream
-Homepage music player and video player configuration
-Whether to display the recommended article name and button configuration
-`favicon` and `Logo`
- Personal information
-TOC directory
-Article reward information
-Add copyright information when copying article content
-MathJax
-Article word count and reading time
-Click the'love' effect on the page
- My project
-My skills
- my album
-`Gitalk`, `Gitment`, `Valine` and `disqus` comment configuration
-[Busuanzi Statistics](http://busuanzi.ibruce.info/) and Google Analytics (`Google Analytics`)
-Collection of default featured images. When the article does not have a feature map, this topic will select the corresponding feature map based on the remainder of the `hashcode` value of the article title

**I think personal blogs should have their own style and characteristics**. If you are not satisfied with the many functions and theme colors in this theme, you can customize and modify them in the theme. Many more free functions and detailed modifications are difficult to complete in the theme's `_config.yml`, and you need to modify the source code. carry out. Here is a list of places that might be useful to you:


There are 24 featured images in the `/source/medias/featureimages` folder by default. You can add or reduce them, and you need to make synchronization changes in `_config.yml`.
