---
layout: post
title:  "Welcome to Jekyll!"
date:   2014-09-11 16:58:41
categories: jekyll update
---

距离上个 Blog 域名（`http://yun.be`）被域名商 hold 已经快三年了，今天终于又重新开启个人独立域名 Blog，这次告别了 WordPress，换到 Github + Github Page +  Markdown+Jekyll 环境。关于配置过程网上很多就不按照流程复述了，仅提供一些 tips：

- 使用 [Github Mac](https://mac.github.com/)可以节省很多事，按照 [Github Page 页面](https://pages.github.com/)流程来即可；
- 本地配置的时候记得修改 gem 源，命令前尽量都加上 sudo
     
      1.  sudo gem sources --remove http://rubygems.org/  
      2.  sudo gem sources -a http://ruby.taobao.org/ 
      3.  sudo gem install jekyll

- 不建议 Jekyll Bootstrap；
- 资源站：[Jekyll 中文网](http://jekyllcn.com/)、 [Jekyll Theme](http://jekyllthemes.org/)；
- 评论可使用 [Disque](https://disqus.com/)；
- 如想添加 favicon 图标，直接找一个喜欢的 icon 然后重命名为 favicon.ico 扔根目录下即可，如果不放心可以在 `_layouts` 的 `page.html` 及 `post.html` 的 head 标签内 加一句 `<link rel="shortcut icon" href="favicon.ico">`



You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve --watch`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help



