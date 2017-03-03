> 今天做项目发现了一个奇怪的现象：每个ajax请求都会请求两次，分别是由jQuery和页面发起的。后来细查通过控制台发现每个请求`Request Method`不一样，分别的`POST`和`OPTIONS` ……后来通过百度了解到原来是跨域的问题。正文从此开始！

## HTTP访问控制(CORS)

当一个资源请求其它域名的资源时会发起一个跨域HTTP请求(cross-origin HTTP request)。域名A（http://foo.com）的某个web页面通过`<img>`标签引入了域名B（http://bar.com）的某个图片资源（http://bar.com/img.jpg），域名A的web页面就会导致浏览器发起一个跨域HTTP请求。目前使用跨域HTTP加载各类资源（JSON、CSS、图片，JavaScript以及其他资源）已成为一种普遍流行的方式。