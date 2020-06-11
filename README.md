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
  //整体缩小 兼容到ie9
  function BrowserType()
  {
  var userAgent = navigator.userAgent; //取得浏览器的userAgent字符串
  var isIE = userAgent.indexOf("compatible") > -1 && userAgent.indexOf("MSIE") > -1 ; //判断是否IE浏览器
  var isEdge = userAgent.indexOf("Edge") > -1; //判断是否IE的Edge浏览器
  var isFF = userAgent.indexOf("Firefox") > -1; //判断是否Firefox浏览器

  if (isIE)
  {
  var reIE = new RegExp("MSIE (\\d+\\.\\d+);");
  reIE.test(userAgent);
  var fIEVersion = parseFloat(RegExp["$1"]);
  if(fIEVersion == 7)
      { return "IE7";}
      else if(fIEVersion == 8)
      { return "IE8";}
      else if(fIEVersion == 9)
      { return "IE9";}
      else if(fIEVersion == 10)
      { return "IE10";}
      else if(fIEVersion == 11)
      { return "IE11";}
      else
      { return "0"}//IE版本过低
      }//isIE end
      if (isEdge) { return "Edge";}
      if (isFF) { return "Firefox";}
  }
  var ll = BrowserType();
  function onResize(){
      var ww= window.innerWidth;
      var hh= window.innerHeight;
      var zoom2 = ww<1400? 1400:ww;
      if(zoom2>=1920){
        zoom2 = 1920;
      }
      if(ll!=='Firefox'){
          $('.wrap_inner').css({'zoom':(zoom2/1920).toFixed(2)})
      }else{
        $('.wrap_inner').css('transform','scale('+(zoom2/1920).toFixed(2)+')')
        $('.wrap_inner').css('-webkit-transform','scale('+(zoom2/1920).toFixed(2)+')')
        $('.wrap_inner').css('-ms-transform','scale('+(zoom2/1920).toFixed(2)+')')
      }
      $('.wrap').css('height',(zoom2/1920).toFixed(2)*4020)

  }
  onResize();
  window.onresize = onResize;
```
