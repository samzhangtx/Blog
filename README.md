# Blog
## 从URL输入到页面展示
<div>（1） 用户在浏览器中输入URL地址</div>
<div>（2） 浏览器解析域名得倒服务器ip地址:</p>
浏览器首先会从浏览器缓存中找是否存在地域名，如存在就直接取出对应的ip地址，如果没有就在系统缓存里找，如果还没有就会找路由缓存，ISP缓存，如果还没有就开启</p>
一个DNS服务器。DNS首先会访问顶级域名服务器，将对应的ip发给客户端，然后访问根域名解析器，将对应的ip发给客户端，最后访问本地域名服务器，得到最终的ip地址。
</di>
<div>(3) ip地址找对对应的服务器，找到相对应的端口（默认为80端口），然后相对应的端口去调用一个网站，进行路由匹配 路由匹配成功后。</div>
<div>(4) http 请求模版和数据，服务器处理收到的请求，将数据返回至浏览器，浏览器收到http相应</div>
<div>(5) 读取页面内容，浏览器进行渲染， 解析html源码，生成dom树，解析css样式、js交互，<div>
 

## 页面渲染流程
 <div>1、解析html标签构建DOM树</div>
 <div>2、解析css构建 css OM树</div>
 <div>3、把DOM和cssOM组合成渲染树（rendertree）</div>
 <div>4、在渲染树的基础上进行布局，计算每个节点的集合结构</div>
 <div>5、把每个节点绘制到屏幕上（painting）</div>
  
## 网页出现长时间的白屏可能的原因是什么？如何优化？
 <div>页面出现白屏原因排除网路等其他因素，那就是由阻塞解析和阻塞渲染造成的。
  <p>一般都是因为css加载或者js加载造成的。css加载会造成阻塞渲染，如果把引入css（link标签）放到head里面，因为加载时间过长，会出现白屏现象</p>
  <p>js加载会造成阻塞解析，如果把引入js放在前面，也可能会因为加载时间过长，出现白屏现象。</p>
## 如何优化
  <p>在引入js标签中添加，async或者defer实现异步加载可避免上面现象</p>
 </div>
