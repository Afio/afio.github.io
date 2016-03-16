---
layout: post
title:  "Welcome to Jekyll!"
date:   2014-09-11 16:58:41
categories: jekyll update
header-img: "img/post-bg-01-jekyll.jpeg"
---

<script>
        var imgUrl = "http://7xrxiu.com1.z0.glb.clouddn.com/wechat.JPG";
        var lineLink = "http://afio.im";
        var descContent = '蛤蛤蛤蛤';
        var shareTitle = 'In case of memory fade away';
        var appid = 'Jekyll is a static blogging engine';
           
        function shareFriend() {
            WeixinJSBridge.invoke('sendAppMessage',{
                "appid": appid,
                "img_url": imgUrl,
                "img_width": "200",
                "img_height": "200",
                "link": lineLink,
                "desc": descContent,
                "title": shareTitle
            }, function(res) {
                //_report('send_msg', res.err_msg);
            })
        }
        function shareTimeline() {
            WeixinJSBridge.invoke('shareTimeline',{
                "img_url": imgUrl,
                "img_width": "300",
                "img_height": "300",
                "link": lineLink,
                "desc": descContent,
                "title": shareTitle
            }, function(res) {
                   //_report('timeline', res.err_msg);
            });
        }
        function shareWeibo() {
            WeixinJSBridge.invoke('shareWeibo',{
                "content": descContent,
                "url": lineLink,
            }, function(res) {
                //_report('weibo', res.err_msg);
            });
        }
        // 当微信内置浏览器完成内部初始化后会触发WeixinJSBridgeReady事件。
        document.addEventListener('WeixinJSBridgeReady', function onBridgeReady() {
            // 发送给好友
            WeixinJSBridge.on('menu:share:appmessage', function(argv){
                shareFriend();
            });
            // 分享到朋友圈
            WeixinJSBridge.on('menu:share:timeline', function(argv){
                shareTimeline();
            });
            // 分享到微博
            WeixinJSBridge.on('menu:share:weibo', function(argv){
                shareWeibo();
            });
        }, false);
</script>


<h3>About Jekyll</h3>

<a href="http://jekyllrb.com/" target="_blank">Jekyll</a> is a static blogging engine, which can transform your plain text into static websites and blogs and serves and perform faster.

If want to be focusing on writing and publishing your content, use Jekyll, and allows you to concoct your sites in any way you can dream up.

So I reset up blog with Jekyll + Github + Github Page +  Markdown configuration, say goodbye to WordPress.

Actually, you don't need to install Jekyll in your local system, just click `Fork` button in your favor Jekyll github repositories. Then clone to your own repo and custom `the _config.yml`, In this file you can specify the blog name, the permalink format, host, Port number, and etc.

And there are some tips:

- Use Github Mac

- <a href="http://jekyllcn.com/" target="_blank">Jekyllcn</a> was a awesome site

- If you have to set up in your locally Mac, use domestic gem

      1.  sudo gem sources --remove http://rubygems.org/
      2.  sudo gem sources -a http://ruby.taobao.org/
      3.  sudo gem install jekyll

-  You can add `<link rel="shortcut icon" href="favicon.ico”>` in `_layouts` >`page.html` & `post.html`  head label to get an favicon icon, and don’t forget to drag the file to root cd.


**Happy Jekyll’ing!**


<h3>Official introduction</h3>

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
