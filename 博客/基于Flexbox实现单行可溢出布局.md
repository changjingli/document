> 布局的传统解决方案，基于[盒状模型](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model)，依赖 [display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)属性 + [position](https://developer.mozilla.org/en-US/docs/Web/CSS/position)属性 + [float](https://developer.mozilla.org/en-US/docs/Web/CSS/float)属性。它对于那些特殊布局非常不方便，比如，[垂直居中](https://css-tricks.com/centering-css-complete-guide/)就不容易实现。2009年，W3C提出了一种新的方案----Flex布局，可以简便、完整、响应式地实现各种页面布局。目前，它已经得到了所有浏览器的支持，这意味着，现在就能很安全地使用这项功能。

看这标题是不是有点懵？没关系，一图胜千言，上图！

![overflow](E:\cjl\document\博客\overflow.gif)

通常这种单行布局都是使用列表 + `float` + `overflow-y: scroll`，最后动态计算宽度实现的。这种布局方式有一个很大的问题就是依赖JS，在被禁用JS的浏览器里布局就会被打回原形。<u>现在提倡前后端分离，个人也是比较倾向于`HTML/CSS`与`JavaScript`分离。</u>布局的事，JavaScript还是少参与为妙。

今天我们的案例便使用flex布局来实现。