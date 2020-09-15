https://r12a.github.io/app-conversion/  
https://blog.csdn.net/prisonersdilemma/article/details/90027873  
https://blog.csdn.net/baidu_36065997/article/details/72887553  
https://www.jianshu.com/p/8fa0fb53c183  
http://ionden.com/a/plugins/ion.rangeSlider/demo_interactions.html  
https://www.cnblogs.com/EnSnail/p/6294897.html  
https://www.cnblogs.com/shimily/articles/8032450.html  
  
  
  
  
https://tggear.qq.com/#/home  
https://egooa.egooidea.com/?tdsourcetag=s_pcqq_aiomsg#/login?redirect=%2Ftasks  
http://qcp.qq.com  
http://font-spider.org  
https://github.com/egoo-wh/egoo  
https://note.youdao.com/signIn/index.html?&callback=https%3A%2F%2Fnote.youdao.com%2Fweb%2F%23%2Ffile%2FWEBaf8c67  
https://lol.qq.com/cguide/Guide/Base/FECommon.html#整体通用规范  
https://www.toptal.com/developers/css/sprite-generator  
https://ossweb-img.qq.com/images/js/dom2img/demo/index.html  
http://www.lrcgc.com/diy  
http://tool.chinaz.com/Tools/unixtime.aspx  
https://tgideas.qq.com/doc/  

  
https://study.163.com/course/courseLearn.htm?courseId=1004938024#/learn/video?lessonId=1279460263&courseId=1004938024  
https://study.miaov.com  
https://study.miaov.com/study/show/chapter/83#117  
https://wenda.so.com/q/1461186827723935  

```
// 屏幕自适应
var adaptViewport = (function () {
  function detectIE() {
    var ua = window.navigator.userAgent;
    var msie = ua.match(/MSIE (\d+)/g);
    if (msie != null) {
      return parseInt(msie[0].match(/\d+/g)[0]);
    }
    // IE 11
    var trident = ua.indexOf('Trident/');
    if (trident > 0) {
      var rv = ua.indexOf('rv:');
      return parseInt(ua.substring(rv + 3, ua.indexOf('.', rv)), 10);
    }
    return false;
  }
  var minWidth = 1380; // 最小宽度
  var designWidth = 1920; // 设计稿宽度
  var isFirefox = navigator.userAgent.indexOf("Firefox") != -1
  var ieVersion = detectIE();
  var zoom = 1;
  function resize(){
    // doc.clientWidth不包含滚动栏宽度
    var ww = document.documentElement.clientWidth || window.innerWidth;
    var realWid = Math.max(ww, minWidth);
    zoom = realWid/designWidth;
    if (ieVersion && ieVersion < 9) { return; }
    // firefox不支持zoom. ie9,10,11 zoom表现奇怪
    if (isFirefox || ieVersion >= 9) {
      if (zoom !== 1) {
        if (!$('.wrap').parent().hasClass('wrap-scale')) {
          $('.wrap').wrap('<div class="wrap-scale"></div>')
          $('.wrap-scale').css('position', 'relative');
          $('.wrap').data('originHeight', $('.wrap').outerHeight())
        }
        var transformOrigin = '0% 0%';
        $('.wrap').css({'width': designWidth,'transform':'scale('+zoom+')', 'transform-origin': transformOrigin, 'margin-left': 0})
        $('.wrap-scale').css({'width': (realWid > minWidth ? 'auto' : minWidth), 'height': $('.wrap').data('originHeight')*zoom, 'overflow': 'hidden'})
      }
    } else {
      $('.wrap').css({'width': designWidth, 'zoom': zoom});
    }
  }
  resize();
  window.onresize = resize;
  // 当切换tab等情形导致.wrap高度改变时，调用此函数。
  function resizeWrapScale() {
    $('.wrap-scale').css({'height': $('.wrap').outerHeight()*zoom})
  }
  return { zoom: zoom, resizeWrapScale: resizeWrapScale}
})();
```
```
  (function() {
  if(/Android|webOS|iPhone|iPad|iPod|BlackBerry/i.test(navigator.userAgent)){var a=document.referrer,b={"baidu.com":"seo_baidu","sogou.com":"seo_sogou","sm.cn":"seo_sm","so.com":"seo_360","bing.com":"seo_bing","google.com":"seo_google"},c;for(c in b){if(-1!=a.indexOf(c)){a=b[c];if(window.sessionStorage){sessionStorage.setItem("channel",a)}else{var d=d||0,b="";0!=d&&(b=new Date,b.setTime(b.getTime()+1000*d),b="; expires="+b.toGMTString());document.cookie="channel="+escape(a)+b+"; path=/"}break}}window.location.href="https://dnf.qq.com/cp/a20200618fightmanm/index.html"+location.search};
  })();
```
