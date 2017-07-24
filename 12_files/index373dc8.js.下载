define("biz_wap/jsapi/core.js",[],function(e,o,n,i){
"use strict";
document.domain="qq.com";
var t=window.__moon_report||function(){},d=8,r={
ready:function(e){
var o=function(){
try{
e&&e();
}catch(o){
throw t([{
offset:d,
log:"ready",
e:o
}]),o;
}
};
"undefined"!=typeof top.window.WeixinJSBridge&&top.window.WeixinJSBridge.invoke?o():top.window.document.addEventListener?top.window.document.addEventListener("WeixinJSBridgeReady",o,!1):top.window.document.attachEvent&&(top.window.document.attachEvent("WeixinJSBridgeReady",o),
top.window.document.attachEvent("onWeixinJSBridgeReady",o));
},
invoke:function(e,o,n){
this.ready(function(){
return"object"!=typeof top.window.WeixinJSBridge?(i("请在微信中打开此链接！"),!1):void top.window.WeixinJSBridge.invoke(e,o,function(o){
try{
if(n){
n.apply(window,arguments);
var i=o&&o.err_msg?", err_msg-> "+o.err_msg:"";
console.info("[jsapi] invoke->"+e+i);
}
}catch(r){
throw t([{
offset:d,
log:"invoke;methodName:"+e,
e:r
}]),r;
}
});
});
},
call:function(e){
this.ready(function(){
if("object"!=typeof top.window.WeixinJSBridge)return!1;
try{
top.window.WeixinJSBridge.call(e);
}catch(o){
throw t([{
offset:d,
log:"call;methodName:"+e,
e:o
}]),o;
}
});
},
on:function(e,o){
this.ready(function(){
return"object"==typeof top.window.WeixinJSBridge&&top.window.WeixinJSBridge.on?void top.window.WeixinJSBridge.on(e,function(){
try{
o&&o.apply(window,arguments);
}catch(n){
throw t([{
offset:d,
log:"on;eventName:"+e,
e:n
}]),n;
}
}):!1;
});
}
};
return r;
});define("biz_common/dom/event.js",[],function(){
"use strict";
function e(){
return s&&(new Date).getTime()-s<200?!0:!1;
}
function t(t,n,i,a){
c.isPc||c.isWp?o(t,"click",a,n,i):o(t,"touchend",a,function(t){
if(-1==c.tsTime||+new Date-c.tsTime>200||e())return c.tsTime=-1,!1;
var i=t.changedTouches[0];
return Math.abs(c.y-i.clientY)<=5&&Math.abs(c.x-i.clientX)<=5?n.call(this,t):void 0;
},i);
}
function n(e,t){
if(!e||!t||e.nodeType!=e.ELEMENT_NODE)return!1;
var n=e.webkitMatchesSelector||e.msMatchesSelector||e.matchesSelector;
return n?n.call(e,t):(t=t.substr(1),e.className.indexOf(t)>-1);
}
function i(e,t,i){
for(;e&&!n(e,t);)e=e!==i&&e.nodeType!==e.DOCUMENT_NODE&&e.parentNode;
return e;
}
function o(e,n,o,a,r){
var s,d,u;
return"input"==n&&c.isPc,e?("function"==typeof o&&(r=a,a=o,o=""),"string"!=typeof o&&(o=""),
e==window&&"load"==n&&/complete|loaded/.test(document.readyState)?a({
type:"load"
}):"tap"==n?t(e,a,r,o):("unload"==n&&"onpagehide"in window&&(n="pagehide"),s=function(e){
var t=a(e);
return t===!1&&(e.stopPropagation&&e.stopPropagation(),e.preventDefault&&e.preventDefault()),
t;
},o&&"."==o.charAt(0)&&(u=function(t){
var n=t.target||t.srcElement,a=i(n,o,e);
return a?(t.delegatedTarget=a,s(t)):void 0;
}),d=u||s,a[n+"_handler"]=d,e.addEventListener?void e.addEventListener(n,d,!!r):e.attachEvent?void e.attachEvent("on"+n,d,!!r):void 0)):void 0;
}
function a(e,t,n,i){
if(e){
var o=n[t+"_handler"]||n;
return e.removeEventListener?void e.removeEventListener(t,o,!!i):e.detachEvent?void e.detachEvent("on"+t,o,!!i):void 0;
}
}
var r=navigator.userAgent,c={
isPc:/(WindowsNT)|(Windows NT)|(Macintosh)/i.test(navigator.userAgent),
isWp:/Windows\sPhone/i.test(r),
tsTime:-1
};
c.isPc||o(document,"touchstart",function(e){
var t=e.changedTouches[0];
c.x=t.clientX,c.y=t.clientY,c.tsTime=+new Date;
});
var s;
return window.addEventListener("scroll",function(){
s=(new Date).getTime();
},!0),{
on:o,
off:a,
tap:t
};
});define("appmsg/test.js",[],function(){
"use strict";
var t=[],e=function(){
"undefined"==typeof getComputedStyle&&document.body.currentStyle&&(window.getComputedStyle=function(t){
return t.currentStyle;
});
},n=function(){
for(var e="/mp/jsmonitor?idkey=",n=[],r=0,o=t.length;o>r;++r){
var i=t[r],d=i.idkey.toString()+"_"+i.order.toString()+"_"+i.num.toString();
n.push(d);
}
e+=n.join(";"),t.length>0&&((new Image).src=e);
},r=function(){
try{
e(),o(),n();
}catch(t){
console.log(t);
}
},o=function(){
var e=10,n=top.window.user_uin||0,r=0!==n&&Math.floor(n/100)%1e3<e;
if(r){
var o=document.getElementsByTagName("img"),i=o.length,d=document.getElementById("img-content"),u=d.offsetWidth,a=0,g=0,c=getComputedStyle(d);
a=parseInt(c.paddingLeft)+parseInt(c.paddingRight),u-=a,u||(u=window.innerWidth-30);
for(var f=0;i>f;++f){
var m=o[f].getAttribute("data-src");
if(m){
var s=1*o[f].getAttribute("data-w")||u,p=1*o[f].getAttribute("data-ratio");
p&&p>0&&s>u&&g++;
}
}
g>0&&t.push({
idkey:28307,
order:22,
num:g
});
}
};
return r;
});define("biz_wap/utils/mmversion.js",[],function(){
"use strict";
function n(){
var n=/MicroMessenger\/([\d\.]+)/i,t=s.match(n);
return t&&t[1]?t[1]:!1;
}
function t(t,r,i){
var e=n();
if(e){
e=e.split("."),t=t.split("."),/\d+/g.test(e[e.length-1])||e.pop();
for(var o,s,u=f["cp"+r],c=0,a=Math.max(e.length,t.length);a>c;++c){
o=e[c]||0,s=t[c]||0,o=parseInt(o)||0,s=parseInt(s)||0;
var p=f.cp0(o,s);
if(!p)return u(o,s);
}
return i||0==r?!0:!1;
}
}
function r(n){
return t(n,0);
}
function i(n,r){
return t(n,1,r);
}
function e(n,r){
return t(n,-1,r);
}
function o(){
return u?"ios":a?"android":"unknown";
}
var s=navigator.userAgent,u=/(iPhone|iPad|iPod|iOS)/i.test(s),c=/Windows\sPhone/i.test(s),a=/(Android)/i.test(s),f={
"cp-1":function(n,t){
return t>n;
},
cp0:function(n,t){
return n==t;
},
cp1:function(n,t){
return n>t;
}
};
return{
get:n,
cpVersion:t,
eqVersion:r,
gtVersion:i,
ltVersion:e,
getPlatform:o,
isWp:c,
isIOS:u,
isAndroid:a
};
});define("appmsg/max_age.js",["biz_wap/utils/ajax.js"],function(e){
"use strict";
function a(){
window.location.href.indexOf("clearStorage=1")>=0&&(localStorage.removeItem("max-age-storage-test"),
console.log("清除 localStorage"));
var e=1,a=top.window.user_uin||0,t=0!==a&&Math.floor(a/100)%1e3<e;
if(t&&(o({
type:"GET",
url:"/mp/reportcache?type=1&random="+Math.random()
}),(new Image).src="/mp/reportcache?type=2&uin="+uin,localStorage&&null==localStorage.getItem("max-age-storage-test"))){
console.log("localstorage为空");
try{
localStorage.setItem("max-age-storage-test",!0),console.log("localStorage设置成功");
}catch(r){}
o({
type:"GET",
url:"/mp/reportcache?type=3&random="+Math.random()
});
}
}
var o=e("biz_wap/utils/ajax.js");
return a;
});define("biz_common/dom/attr.js",[],function(){
"use strict";
function t(t,e,n){
return"undefined"==typeof n?t.getAttribute(e):t.setAttribute(e,n);
}
function e(t,e,n,r){
t.style.setProperty?(r=r||null,t.style.setProperty(e,n,r)):"undefined"!=typeof t.style.cssText&&(r=r?"!"+r:"",
t.style.cssText+=";"+e+":"+n+r+";");
}
return{
attr:t,
setProperty:e
};
});define("biz_wap/utils/ajax.js",["biz_common/utils/url/parse.js","biz_common/utils/respTypes.js"],function(require,exports,module,alert){
"use strict";
function joinUrl(e){
var t={};
return"undefined"!=typeof uin&&(t.uin=uin),"undefined"!=typeof key&&(t.key=key),
"undefined"!=typeof pass_ticket&&(t.pass_ticket=pass_ticket),"undefined"!=typeof wxtoken&&(t.wxtoken=wxtoken),
"undefined"!=typeof top.window.devicetype&&(t.devicetype=top.window.devicetype),
"undefined"!=typeof top.window.clientversion&&(t.clientversion=top.window.clientversion),
t.x5=isx5?"1":"0",t.f="json",Url.join(e,t);
}
function reportRt(e,t,o){
var r="";
if(o&&o.length){
var n=1e3,s=o.length,a=Math.ceil(s/n);
r=["&lc="+a];
for(var i=0;a>i;++i)r.push("&log"+i+"=[rtCheckError]["+i+"]"+encodeURIComponent(o.substr(i*n,n)));
r=r.join("");
}
var c,p="idkey="+e+"_"+t+"_1"+r+"&r="+Math.random();
if(window.ActiveXObject)try{
c=new ActiveXObject("Msxml2.XMLHTTP");
}catch(_){
try{
c=new ActiveXObject("Microsoft.XMLHTTP");
}catch(d){
c=!1;
}
}else window.XMLHttpRequest&&(c=new XMLHttpRequest);
c&&(c.open("POST",location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?",!0),c.setRequestHeader("cache-control","no-cache"),
c.setRequestHeader("Content-Type","application/x-www-form-urlencoded; charset=UTF-8"),
c.setRequestHeader("X-Requested-With","XMLHttpRequest"),c.send(p));
}
function Ajax(obj){
var type=(obj.type||"GET").toUpperCase(),url=joinUrl(obj.url),mayAbort=!!obj.mayAbort,async="undefined"==typeof obj.async?!0:obj.async,xhr=new XMLHttpRequest,timer=null,data=null;
if("object"==typeof obj.data){
var d=obj.data;
data=[];
for(var k in d)d.hasOwnProperty(k)&&data.push(k+"="+encodeURIComponent(d[k]));
data=data.join("&");
}else data="string"==typeof obj.data?obj.data:null;
xhr.open(type,url,async);
var _onreadystatechange=xhr.onreadystatechange;
xhr.onreadystatechange=function(){
if("function"==typeof _onreadystatechange&&_onreadystatechange.apply(xhr),3==xhr.readyState&&obj.received&&obj.received(xhr),
4==xhr.readyState){
xhr.onreadystatechange=null;
var status=xhr.status;
if(status>=200&&400>status)try{
var responseText=xhr.responseText,resp=responseText;
if("json"==obj.dataType)try{
resp=eval("("+resp+")");
var rtId=obj.rtId,rtKey=obj.rtKey||0,rtDesc=obj.rtDesc,checkRet=!0;
rtId&&rtDesc&&RespTypes&&!RespTypes.check(resp,rtDesc)&&reportRt(rtId,rtKey,RespTypes.getMsg()+"[detail]"+responseText+";"+obj.url);
}catch(e){
return void(obj.error&&obj.error(xhr));
}
obj.success&&obj.success(resp);
}catch(e){
throw __moon_report({
offset:MOON_AJAX_SUCCESS_OFFSET,
e:e
}),e;
}else{
try{
obj.error&&obj.error(xhr);
}catch(e){
throw __moon_report({
offset:MOON_AJAX_ERROR_OFFSET,
e:e
}),e;
}
if(status||!mayAbort){
var __ajaxtest=window.__ajaxtest||"0";
__moon_report({
offset:MOON_AJAX_NETWORK_OFFSET,
log:"ajax_network_error["+status+"]["+__ajaxtest+"]: "+url+";host:"+top.location.host,
e:""
});
}
}
clearTimeout(timer);
try{
obj.complete&&obj.complete();
}catch(e){
throw __moon_report({
offset:MOON_AJAX_COMPLETE_OFFSET,
e:e
}),e;
}
obj.complete=null;
}
},"POST"==type&&xhr.setRequestHeader("Content-Type","application/x-www-form-urlencoded; charset=UTF-8"),
xhr.setRequestHeader("X-Requested-With","XMLHttpRequest"),"undefined"!=typeof obj.timeout&&(timer=setTimeout(function(){
xhr.abort("timeout");
try{
obj.complete&&obj.complete();
}catch(e){
throw __moon_report({
offset:MOON_AJAX_COMPLETE_OFFSET,
e:e
}),e;
}
obj.complete=null,__moon_report({
offset:MOON_AJAX_TIMEOUT_OFFSET,
log:"ajax_timeout_error: "+url,
e:""
});
},obj.timeout));
try{
xhr.send(data);
}catch(e){
obj.error&&obj.error();
}
return xhr;
}
var Url=require("biz_common/utils/url/parse.js"),RespTypes=require("biz_common/utils/respTypes.js"),isx5=-1!=navigator.userAgent.indexOf("TBS/"),__moon_report=window.__moon_report||function(){},MOON_AJAX_SUCCESS_OFFSET=3,MOON_AJAX_NETWORK_OFFSET=4,MOON_AJAX_ERROR_OFFSET=5,MOON_AJAX_TIMEOUT_OFFSET=6,MOON_AJAX_COMPLETE_OFFSET=7;
return Ajax;
});define("appmsg/log.js",["biz_wap/utils/log.js"],function(i){
"use strict";
var s=i("biz_wap/utils/log.js");
return function(i,t){
s(i,t);
};
});define("biz_common/dom/class.js",[],function(){
"use strict";
function s(s,a){
return s.classList?s.classList.contains(a):s.className.match(new RegExp("(\\s|^)"+a+"(\\s|$)"));
}
function a(s,a){
s.classList?s.classList.add(a):this.hasClass(s,a)||(s.className+=" "+a);
}
function e(a,e){
if(a.classList)a.classList.remove(e);else if(s(a,e)){
var c=new RegExp("(\\s|^)"+e+"(\\s|$)");
a.className=a.className.replace(c," ");
}
}
function c(c,l){
s(c,l)?e(c,l):a(c,l);
}
return{
hasClass:s,
addClass:a,
removeClass:e,
toggleClass:c
};
});define("biz_wap/utils/device.js",[],function(){
"use strict";
function s(s){
{
var e=s.match(/MQQBrowser\/(\d+\.\d+)/i),r=s.match(/QQ\/(\d+\.(\d+)\.(\d+)\.(\d+))/i)||s.match(/V1_AND_SQ_([\d\.]+)/),i=s.match(/MicroMessenger\/((\d+)\.(\d+))\.(\d+)/)||s.match(/MicroMessenger\/((\d+)\.(\d+))/),t=s.match(/Mac\sOS\sX\s(\d+\.\d+)/),n=s.match(/Windows(\s+\w+)?\s+?(\d+\.\d+)/),a=s.match(/MiuiBrowser\/(\d+\.\d+)/i),d=s.match(/MI-ONE/),h=s.match(/MI PAD/),w=s.match(/UCBrowser\/(\d+\.\d+(\.\d+\.\d+)?)/)||s.match(/\sUC\s/),c=s.match(/IEMobile(\/|\s+)(\d+\.\d+)/)||s.match(/WPDesktop/),b=s.match(/(ipod).*\s([\d_]+)/i),u=s.match(/(ipad).*\s([\d_]+)/i),v=s.match(/(iphone)\sos\s([\d_]+)/i),p=s.match(/Chrome\/(\d+\.\d+)/),m=s.match(/Mozilla.*Linux.*Android.*AppleWebKit.*Mobile Safari/),f=s.match(/(android)\s([\d\.]+)/i);
s.indexOf("HTC")>-1;
}
if(o.browser=o.browser||{},o.os=o.os||{},window.ActiveXObject){
var l=6;
(window.XMLHttpRequest||s.indexOf("MSIE 7.0")>-1)&&(l=7),(window.XDomainRequest||s.indexOf("Trident/4.0")>-1)&&(l=8),
s.indexOf("Trident/5.0")>-1&&(l=9),s.indexOf("Trident/6.0")>-1&&(l=10),o.browser.ie=!0,
o.browser.version=l;
}else s.indexOf("Trident/7.0")>-1&&(o.browser.ie=!0,o.browser.version=11);
f&&(this.os.android=!0,this.os.version=f[2]),b&&(this.os.ios=this.os.ipod=!0,this.os.version=b[2].replace(/_/g,".")),
u&&(this.os.ios=this.os.ipad=!0,this.os.version=u[2].replace(/_/g,".")),v&&(this.os.iphone=this.os.ios=!0,
this.os.version=v[2].replace(/_/g,".")),n&&(this.os.windows=!0,this.os.version=n[2]),
t&&(this.os.Mac=!0,this.os.version=t[1]),s.indexOf("lepad_hls")>0&&(this.os.LePad=!0),
h&&(this.os.MIPAD=!0),e&&(this.browser.MQQ=!0,this.browser.version=e[1]),r&&(this.browser.MQQClient=!0,
this.browser.version=r[1]),i&&(this.browser.WeChat=!0,this.browser.mmversion=this.browser.version=i[1]),
a&&(this.browser.MIUI=!0,this.browser.version=a[1]),w&&(this.browser.UC=!0,this.browser.version=w[1]||0/0),
c&&(this.browser.IEMobile=!0,this.browser.version=c[2]),m&&(this.browser.AndriodBrowser=!0),
d&&(this.browser.M1=!0),p&&(this.browser.Chrome=!0,this.browser.version=p[1]),this.os.windows&&(this.os.win64="undefined"!=typeof navigator.platform&&"win64"==navigator.platform.toLowerCase()?!0:!1);
var M={
iPad7:"iPad; CPU OS 7",
LePad:"lepad_hls",
XiaoMi:"MI-ONE",
SonyDTV:"SonyDTV",
SamSung:"SAMSUNG",
HTC:"HTC",
VIVO:"vivo"
};
for(var g in M)this.os[g]=-1!==s.indexOf(M[g]);
o.os.phone=o.os.phone||/windows phone/i.test(s),this.os.getNumVersion=function(){
return parseFloat(o.os.version,"10");
},this.os.hasTouch="ontouchstart"in window,this.os.hasTouch&&this.os.ios&&this.os.getNumVersion()<6&&(this.os.hasTouch=!1),
o.browser.WeChat&&o.browser.version<5&&(this.os.hasTouch=!1),o.browser.getNumVersion=function(){
return parseFloat(o.browser.version,"10");
},o.browser.isFFCanOcx=function(){
return o.browser.firefox&&o.browser.getNumVersion()>=3?!0:!1;
},o.browser.isCanOcx=function(){
return!(!o.os.windows||!o.browser.ie&&!o.browser.isFFCanOcx()&&!o.browser.webkit);
},o.browser.isNotIESupport=function(){
return!!o.os.windows&&(!!o.browser.webkit||o.browser.isFFCanOcx());
},o.userAgent={},o.userAgent.browserVersion=o.browser.version,o.userAgent.osVersion=o.os.version,
delete o.userAgent.version;
}
var o={};
s.call(o,window.navigator.userAgent);
var e=function(){
var s=window.navigator.userAgent,e=null;
if(o.os.android){
if(o.browser.MQQ&&o.browser.getNumVersion()>=4.2)return!0;
if(-1!=s.indexOf("MI2"))return!0;
if(o.os.version>="4"&&(e=s.match(/MicroMessenger\/((\d+)\.(\d+))\.(\d+)/))&&e[1]>=4.2)return!0;
if(o.os.version>="4.1")return!0;
}
return!1;
}(),r=function(){
var s=document.createElement("video");
if("function"==typeof s.canPlayType){
if("probably"==s.canPlayType('video/mp4; codecs="mp4v.20.8"'))return!0;
if("probably"==s.canPlayType('video/mp4; codecs="avc1.42E01E"')||"probably"==s.canPlayType('video/mp4; codecs="avc1.42E01E, mp4a.40.2"'))return!0;
}
return!1;
}();
return o.canSupportVideo=r||e,o.canSupportVideoMp4=r,o.canSupportH5Video=e,o;
});define("biz_common/utils/string/html.js",[],function(){
"use strict";
return String.prototype.html=function(t){
var e=["&#96;","`","&#39;","'","&quot;",'"',"&nbsp;"," ","&gt;",">","&lt;","<","&yen;","¥","&amp;","&"];
t&&e.reverse();
for(var n=0,r=this;n<e.length;n+=2)r=r.replace(new RegExp(e[n],"g"),e[n+1]);
return r;
},String.prototype.htmlEncode=function(){
return this.html(!0);
},String.prototype.htmlDecode=function(){
return this.html(!1);
},String.prototype.getPureText=function(){
return this.replace(/<\/?[^>]*\/?>/g,"");
},String.prototype.htmlLite=function(t){
var e=["&#96;","`","&#39;","'","&quot;",'"',"&gt;",">","&lt;","<","&amp;","&"];
t&&e.reverse();
for(var n=0,r=this;n<e.length;n+=2)r=r.replace(new RegExp(e[n],"g"),e[n+1]);
return r;
},String.prototype.htmlEncodeLite=function(){
return this.htmlLite(!0);
},String.prototype.htmlDecodeLite=function(){
return this.htmlLite(!1);
},{
htmlDecode:function(t){
return t.htmlDecode();
},
htmlEncode:function(t){
return t.htmlEncode();
},
getPureText:function(t){
return t.getPureText();
},
htmlEncodeLite:function(t){
return t.htmlEncodeLite();
},
htmlDecodeLite:function(t){
return t.htmlDecodeLite();
}
};
});define("appmsg/index.js",["biz_common/utils/string/html.js","biz_wap/utils/device.js","biz_common/dom/class.js","appmsg/log.js","biz_wap/utils/ajax.js","biz_common/dom/attr.js","appmsg/max_age.js","biz_wap/utils/mmversion.js","appmsg/test.js","biz_common/dom/event.js","biz_wap/jsapi/core.js","page/appmsg_new/combo.css","page/appmsg_new/not_in_mm.css","page/appmsg/page_mp_article_improve_combo.css","page/appmsg/not_in_mm.css","biz_common/utils/url/parse.js","appmsg/cdn_img_lib.js","appmsg/share.js","biz_common/log/jserr.js","biz_wap/ui/lazyload_img.js","appmsg/async.js","appmsg/copyright_report.js","appmsg/outer_link.js","appmsg/review_image.js","appmsg/product.js","appmsg/iframe.js","appmsg/qqmusic.js","appmsg/voice.js","appmsg/weapp.js","appmsg/new_index.js","appmsg/wxtopic.js","appmsg/cdn_speed_report.js","appmsg/page_pos.js","appmsg/report_and_source.js","appmsg/report.js","appmsg/fereport.js","biz_wap/safe/mutation_observer_report.js","sougou/index.js"],function(e){
"use strict";
function t(){
function t(e,t){
var o={
lossy:"UklGRiIAAABXRUJQVlA4IBYAAAAwAQCdASoBAAEADsD+JaQAA3AAAAAA",
lossless:"UklGRhoAAABXRUJQVlA4TA0AAAAvAAAAEAcQERGIiP4HAA==",
alpha:"UklGRkoAAABXRUJQVlA4WAoAAAAQAAAAAAAAAAAAQUxQSAwAAAARBxAR/Q9ERP8DAABWUDggGAAAABQBAJ0BKgEAAQAAAP4AAA3AAP7mtQAAAA==",
animation:"UklGRlIAAABXRUJQVlA4WAoAAAASAAAAAAAAAAAAQU5JTQYAAAD/////AABBTk1GJgAAAAAAAAAAAAAAAAAAAGQAAABWUDhMDQAAAC8AAAAQBxAREYiI/gcA"
},i=new Image;
i.onload=function(){
var o=i.width>0&&i.height>0;
t(e,o);
},i.onerror=function(){
t(e,!1);
},i.src="data:image/webp;base64,"+o[e];
}
function r(){
var e=window.performance||window.msPerformance||window.webkitPerformance;
if(e.timing){
var t=e.timing;
n("[Appmsg] dns:"+(t.domainLookupEnd-t.domainLookupStart)+"^^^ ssl:"+(0==t.secureConnectionStart?0:t.connectEnd-t.secureConnectionStart)+"^^^ tcp:"+(t.connectEnd-t.connectStart)+"^^^ request:"+(t.responseStart-t.requestStart)+"^^^ getPackageTime:"+(t.responseEnd-t.responseStart)+"^^^ domCententLoaded:"+(t.domContentLoadedEventStart-t.domLoading)+"^^^ domComplete:"+(t.domComplete-t.domLoading)+"^^^ firstViewTime:"+(real_show_page_time-t.navigationStart)+"^^^ interactiveTime:"+(page_endtime-t.navigationStart))+"^^^ ua:"+window.navigator.userAgent,
setTimeout(function(){
t.loadEventEnd&&n("[Appmsg] onload:"+(t.loadEventEnd-t.loadEventStart));
},100);
}
"function"!=typeof String.prototype.trim&&(String.prototype.trim=function(){
return this.replace(/^\s+|\s+$/g,"");
}),""==document.getElementById("js_content").innerHTML.trim()&&((new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=24729_94_1"),
console.log(window.reprint_style,document.getElementById("js_content").innerText.length),
3==window.reprint_style&&document.getElementById("js_content").innerText.length>300&&((new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=24729_7_1");
var o=Math.random();
.001>o&&document.getElementById("js_read_area3")&&document.getElementById("js_read_area3").innerText&&document.getElementById("js_read_area3").innerText.indexOf("Pageview")>-1&&((new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=24729_95_1"),
window.__wxjs_is_wkwebview&&window.__addIdKeyReport("28307",67);
}
var _=document.getElementsByTagName("body");
if(!_||!_[0])return!1;
_=_[0],function(){
var e=(new Date).getHours(),t=function(e,t){
t=t||"",window.isSg?(t=["uin:sougou","resp:"+t].join("|"),(new Image).src="/mp/jsreport?key="+e+"&content="+t+"&r="+Math.random()+"&from=sougou"):(t=["uin:"+top.window.user_uin,"resp:"+t].join("|"),
(new Image).src="/mp/jsreport?key="+e+"&content="+t+"&r="+Math.random());
},o=function(e,t,o){
var i=e+"_"+t;
o=o||1,window.logs.idkeys[i]||(window.logs.idkeys[i]={
val:0
}),window.logs.idkeys[i].val+=o;
},i=e>=11&&17>=e&&Math.random()<1,n=function(e,o){
i&&t(e,o);
};
window.__report=t,window.__commonVideoReport=n,window.__addIdKeyReport=o;
}();
var h=/^http(s)?:\/\/mp\.weixin\.qq\.com\//g;
try{
if(top!=window&&(!top||top&&top.location.href&&h.test(top.location.href))&&!window.isSg)throw new Error("in iframe");
}catch(y){
var A="",v=new Image;
v.src=("http://mp.weixin.qq.com/mp/jsreport?key=4&content=biz:"+biz+",mid:"+mid+",uin:"+uin+"[key4]"+A+"&r="+Math.random()).substr(0,1024);
}
if(window.isInWeixinApp()&&/#rd$/.test(location.href)&&!window.isWeixinCached){
var b=-1!=location.href.indexOf("?")?"&":"?";
location.replace(location.href.replace(/#rd$/,b+"rd2werd=1#wechat_redirect"));
}
var x=e("biz_common/utils/url/parse.js");
e("appmsg/cdn_img_lib.js"),window.page_endtime=+new Date;
{
var I=!p.isWp&&-1==navigator.userAgent.indexOf("MicroMessenger");
-1!=navigator.userAgent.indexOf("WindowsWechat");
}
if(e("appmsg/share.js"),window.isSg||"mp.weixin.qq.com"==location.host){
var j=e("biz_common/log/jserr.js");
j({
key:0,
reporturl:"http://mp.weixin.qq.com/mp/jsreport?1=1",
replaceStr:/http(s)?:(.*?)js\//g
});
}
window.logs.webplog={
lossy:0,
lossless:0,
alpha:0,
animation:0,
total:0
};
var R=-1!=navigator.userAgent.indexOf("TBS/"),z=function(e,o){
t(e,function(e,t){
if(window.logs.webplog[e]=t?1:0,window.logs.webplog.total++,4==window.logs.webplog.total){
var i=window.logs.webplog,n=Math.random();
R&&1>=n&&(i.lossy=i.lossless=i.alpha=1,window.logs.webplog=i);
var a=i.lossy&i.lossless&i.alpha;
o(!!a);
}
});
},E=function(e){
for(var t=document.getElementsByTagName("img"),o=!1,i=0,n=t.length;n>i;i++){
var a=t[i].getAttribute("data-src");
a&&a.isGif()&&(o=!0);
}
(u||navigator.userAgent.indexOf("Br_trunk")>-1)&&o&&p.isIOS&&p.gtVersion("6.5.10",!0)?(console.log("当前版本可以启用img代理"),
l.invoke("imageProxyInit",{},function(t){
console.log(t),t.err_msg.indexOf(":ok")>-1?(f=t.serverUrl,window.__addIdKeyReport("28307",117)):t.err_msg.indexOf(":fail")>-1&&window.__addIdKeyReport("28307",118),
e();
})):e();
},q=function(e){
z("lossy",e),z("lossless",e),z("alpha",e),z("animation",e);
};
window.webp=!1,E(function(){
q(function(t){
function o(e){
e.width<40||e.height<40||-1==e.className.indexOf("img_loading")&&(e.className+=" img_loading");
}
function i(e){
if(!(e.width<40||e.height<40)){
var t=e.src;
if(e.className=e.className.replace("img_loading",""),-1==e.className.indexOf("img_loadederror")){
e.className+=" img_loadederror",e.src="data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==",
window.__addIdKeyReport("28307",51);
var i=function(){
window.__addIdKeyReport("28307",66),a(e),o(e);
var i=e.__retryload;
return i=0,t=t.https2http(),e.__retryload=i,e.src=x.addParam(t,"retryload",i,!0),
!1;
};
m.on(e,"click",i);
}
}
}
function a(e){
e.className=e.className.replace("img_loading",""),e.className=e.className.replace("img_loadederror","");
}
function r(e,t,o,i){
if(1*t.getAttribute("data-order")<5)return e;
var n=1e3*window.svr_time||+new Date;
n=new Date(n);
var a=n.getHours(),r=(60*a+n.getMinutes(),e),s=document.createElement("span");
s.className="gif_img_wrp",s.innerHTML='<span class="gif_img_tips" style="display:none;"><i class="gif_img_play_arrow"></i>动图</span><span class="gif_img_tips loading" style="display:none;"><i class="weui_loading gif_img_loading"></i>加载中</span>';
var d="click",p=function(){
if(s){
s.children.item(0).style.display="none",s.children.item(1).style.display="";
var e=t.onload;
t.onload=function(){
s&&(s.children.item(1).style.display="none",m.off(s,d,p),s=null),t.className+=" img_gif_onload",
e&&e.apply(t,arguments);
};
var o=t.onerror;
t.onerror=function(){
s&&(s.children.item(0).style.display="",s.children.item(1).style.display="none",
m.off(s,d,p),s=null),o&&o.apply(t,arguments);
},t.src=r,t.loadGif=!0,window.__addIdKeyReport("28307",15);
}
};
return t.autoTap=function(){
t.src=r,t.loadGif=!0,t.autoTap=null,m.off(s,d,p),window.__addIdKeyReport("28307",26);
},t.span=s,(window.user_uin&&100>(g/100|0)%100&&"MzI5NjExODQ4OA=="!==window.biz||location.href.indexOf("gif=1")>-1)&&(e=i.nogif(),
t.gray=!0,t.parentNode.insertBefore(s,t),s.appendChild(t),m.on(s,d,p),window.__addIdKeyReport("28307",16)),
e;
}
function d(e){
var t,o=getComputedStyle(e),i=new Image,n=o.backgroundImage.replace(/url\((['"])?(.*?)\1\)/gi,"$2"),a=o.backgroundSize,r=parseFloat(o.width.replace("px","")),s=parseFloat(o.height.replace("px","")),d=[r,s],p=[];
if(i.src=n,t=i.width>i.height?i.width/i.height:i.height/i.width,a=a.split(" "),p[0]=a[0],
p[1]=a.length>1?a[1]:"auto","cover"===a[0])d[0]>d[1]&&d[0]/d[1]>=t?(p[0]=d[0],p[1]="auto"):(p[0]="auto",
p[1]=d[1]);else if("contain"===a[0])d[0]<d[1]?(p[0]=d[0],p[1]="auto"):d[0]/d[1]>=t?(p[0]="auto",
p[1]=d[1]):(p[1]="auto",p[0]=d[0]);else for(var c=a.length;c--;)a[c].indexOf("px")>-1?p[c]=a[c].replace("px",""):a[c].indexOf("%")>-1&&(p[c]=d[c]*(a[c].replace("%","")/100));
return"auto"===p[0]&&"auto"===p[1]?(p[0]=i.width,p[1]=i.height):(t="auto"===p[0]?i.height/p[1]:i.width/p[0],
p[0]="auto"===p[0]?i.width/t:p[0],p[1]="auto"===p[1]?i.height/t:p[1]),{
width:p[0],
height:p[1]
};
}
window.webp=t,t&&window.localStorage&&window.localStorage.setItem&&window.localStorage.setItem("webp","1"),
window.logs.img={
download:{},
read:{},
load:{}
};
var p=document.getElementById("js_cover");
if(p){
var c=p.getAttribute("data-src");
c&&(c.isCDN()&&(c=c.imgChange640(),t&&(c=x.addParam(c,"tp","webp",!0)),c=x.addParam(c,"wxfrom","5",!0),
is_https_res||w?c=c.http2https():("http:"==location.protocol||-1!=navigator.userAgent.indexOf("MicroMessenger"))&&(c=c.https2http())),
setTimeout(function(){
p.onload=function(){
s(p,"height","auto","important"),s(p,"visibility","visible","important");
},p.setAttribute("src",c);
},0),window.logs.img.read[c]=!0,window.logs.img.load[c]=!0,p.removeAttribute("data-src"));
}
var l=e("biz_wap/ui/lazyload_img.js"),_=1;
window.logs.outer_pic=0;
for(var u=document.getElementsByTagName("img"),h=0,y=u.length;y>h;h++){
{
var A=u[h].getAttribute("data-src");
u[h].getAttribute("src");
}
A&&A.isGif()&&u[h].className.indexOf("__bg_gif")<0&&(u[h].className+=" __bg_gif"),
A&&o(u[h]);
}
for(var v=document.getElementsByClassName("__bg_gif"),h=0,y=v.length;y>h;++h)v[h].setAttribute("data-order",h);
var b=!1,I=function(){
if(!b){
b=!0;
for(var e=document.getElementsByClassName("__bg_gif"),t=function(e){
var t=document.createElement("span"),o=document.createElement("div");
o.style.position="relative",o.style.height=0,o.className="gif_bg_tips_wrp",t.className="gif_img_tips_group",
t.innerHTML='<span class="gif_img_tips"><i class="gif_img_play_arrow"></i>动图</span><span class="gif_img_tips loading" style="display:none;"><i class="weui_loading gif_img_loading"></i>加载中</span>',
o.appendChild(t);
var i=getComputedStyle(e),n=i.backgroundPosition,a=i.backgroundPositionX||n.split(" ")[0],r=i.backgroundPositionY||n.split(" ")[1]||backgroundPositionX,s=d(e),p=parseFloat(s.width),c=parseFloat(s.height);
if(120>p||120>c)return"autoTap";
var l,g,_=e.clientWidth,w=e.clientHeight,u=i.backgroundOrigin,f=i.backgroundImage.slice(4,-1).replace(/"/g,""),h=parseFloat(i.paddingLeft),y=parseFloat(i.borderLeftWidth),A=parseFloat(i.paddingRight),v=parseFloat(i.borderRightWidth),b=parseFloat(i.paddingTop),x=parseFloat(i.borderTopWidth),I=parseFloat(i.paddingBottom),j=parseFloat(i.borderBottomWidth),R=parseFloat(i.marginTop),z=parseFloat(i.marginLeft);
"padding-box"===u?(l=y+z,g=x+R):"border-box"===u?(_+=y+v,w+=x+j,l=z,g=R):"content-box"===u&&(_-=A+h,
w-=b+I,l=y+z+h,g=x+R+b);
var E;
if(a.indexOf("%")>=0){
var q=.01*parseFloat(a);
E=(_-p)*q;
}else a.indexOf("px")>=0&&(E=parseFloat(a));
var B;
if(r.indexOf("%")>=0){
var q=.01*parseFloat(r);
B=(w-c)*q;
}else r.indexOf("px")>=0&&(B=parseFloat(r));
var k=B+g+c,O=E+l;
O=Math.max(O,z),k=Math.min(k,w+5+g),O+=10,k-=35,t.style.top=k+"px",t.style.left=O+"px";
var T="click",S=function(){
if(t){
t.children.item(0).style.display="none",t.children.item(1).style.display="";
var o=new Image,i=f;
f.indexOf("mmbiz_gif")>=0?i=i.replace("/s640?","/0?"):(i=i.replace("/s640?","/0?"),
i+="&wx_fmt=gif"),o.src=i,o.onload=function(){
t&&(t.children.item(1).style.display="none",m.off(t,T,S),t=null),e.style.backgroundImage='url("'+i+'")',
e.loadGif=!0;
},o.onerror=function(){
t&&(t.children.item(0).style.display="",t.children.item(1).style.display="none",
m.off(t,T,S),t=null);
},window.__addIdKeyReport("28307",15);
}
};
return m.on(t,T,S),o;
},o=5,i=function(e){
var t=getComputedStyle(e),o=t.backgroundImage.slice(4,-1).replace(/"/g,""),i=o;
o.indexOf("/mmbiz_gif/")>=0?i=i.replace("/s640?","/0?"):(i=i.replace("/s640?","/0?"),
i+="&wx_fmt=gif"),e.style.backgroundImage='url("'+i+'")',e.loadGif=!0;
},n=0,a=e.length;a>n;++n){
var r=e[n].getAttribute("data-src");
if(!(r&&r.isGif()||e[n].loadGif))if(o>n)i(e[n]);else{
var s=t(e[n]);
"autoTap"===s?i(e[n]):e[n].parentNode.insertBefore(s,e[n]);
}
}
}
};
m.on(window,"load",I),setTimeout(function(){
I();
},1e4),function(){
var e="onorientationchange"in window?"orientationchange":"resize";
m.on(window,e,function(){
if(b){
for(var e=document.getElementsByClassName("gif_bg_tips_wrp");e.length>0;)e[0].parentNode.removeChild(e[0]);
b=!1,I();
}
});
}(),new l({
attrKey:"data-src",
imgOccupied:!0,
lazyloadHeightWhenWifi:function(){
var e,t=1,o=1;
e=window.svr_time?new Date(1e3*window.svr_time):new Date;
var i=e.getHours();
return i>=20&&23>i&&(t=.5,o=0),{
bottom:t,
top:o
};
},
inImgRead:function(e){
e&&(window.logs.img.read[e]=!0);
},
changeSrc:function(e,t,o){
if(!t)return"";
var i=t;
if(t.isCDN()){
i=i.imgChange640();
var a,s=top.window.navigator.userAgent,d=/TBS\/([\d\.]+)/i,p=s.match(d);
p&&p[1]&&(a=parseInt(p[1]));
var c=1e3,m=top.window.user_uin||0,l=0!==m&&Math.floor(m/100)%1e3<c;
l&&a>=43305&&i.isGif()?(i=x.addParam(i,"tp","wxpic",!0),window.__addIdKeyReport("28307",91)):window.webp&&(i=x.addParam(i,"tp","webp",!0),
window.__addIdKeyReport("28307",84)),i=x.addParam(i,"wxfrom","5",!0),is_https_res||w?(i=i.http2https(),
window.__addIdKeyReport("28307",77)):("http:"==location.protocol||-1!=navigator.userAgent.indexOf("MicroMessenger"))&&(i=i.https2http(),
window.__addIdKeyReport("28307",70));
}else try{
var d=new RegExp("^http(s)?://((mmbiz.qpic.cn/.*)|(m.qpic.cn/.*)|(mmsns.qpic.cn/.*)|(shp.qpic.cn/.*)|(wx.qlogo.cn/.*)|(mmbiz.qlogo.cn/.*)|((a|b)[0-9]*.photo.store.qq.com/.*)|(mp.weixin.qq.com/.*)|(res.wx.qq.com/.*))");
d.test(t)||(window.__addIdKeyReport("28307",9),window.logs.outer_pic++);
}catch(g){}
var _=/^http\:\/\/(a|b)(\d)+\.photo\.store\.qq\.com/g;
i=i.replace(_,"http://m.qpic.cn"),i=x.addParam(i,"wx_lazy","1",!0);
var u=i;
return f&&i.isGif()&&(window.__addIdKeyReport("28307",106),i=x.addParam(i,"tp","wxpic",!0),
i=f+"hevc?url="+encodeURIComponent(i)+"&type=gif",console.log("hevc changeSrc : "+i)),
t.isGif()&&(i=r(i,e,o,u)),window.logs.img.load[i]=!0,n("[Appmsg] image_load_event_change_src. originsrc:"+t+"  ^^^ newsrc : "+i),
e.start_load_time=+new Date,i;
},
onerror:function(e,t){
var o=t?t.__retryload||0:0;
if(1==o&&i(t),e&&!(o>_)){
if(!e.isCDN()){
if(!f)return;
if(-1==e.indexOf(f))return;
}
var a=0==e.indexOf("https://")?7:0;
if(window.__addIdKeyReport("28307",72+a),window.__addIdKeyReport("28307",75+1*o+a),
e.isWxpic()?(window.__addIdKeyReport("28307",93),window.__addIdKeyReport("28307",96+1*o)):e.isWebp()&&(window.__addIdKeyReport("28307",86),
window.__addIdKeyReport("28307",89+1*o)),f&&e.indexOf(f)>-1&&window.__addIdKeyReport("28307",108),
_>o){
if(o++,t.__retryload=o,1==o&&e.indexOf("http://")>-1?(e=e.http2https(),window.__addIdKeyReport("28307",60),
window.__addIdKeyReport("28307",77)):1==o&&e.indexOf("https://")>-1&&(window.__addIdKeyReport("28307",61),
window.__addIdKeyReport("28307",77)),f&&e.indexOf(f)>-1){
console.log("加载hevc 失败： "+e);
var r=e.split("hevc?url=")[1];
r=r.split("&type")[0],r=decodeURIComponent(r),r=r.replace("tp=wxpic",""),e=r.https2http(),
console.log("重试src: "+e);
}
t.start_load_time=+new Date,t.src=x.addParam(e,"retryload",o,!0);
}
window.__has_imgfailed||(window.__has_imgfailed=!0,window.__addIdKeyReport("28307",65)),
n("[Appmsg] image_load_event_on_error. src:"+e),t.setAttribute("data-fail",1);
var s=10;
/tp\=webp/.test(e)&&(s=11);
var d=new Image;
d.src="http://mp.weixin.qq.com/mp/jsreport?key="+s+"&content="+(encodeURIComponent(e)+"["+uin+"]")+"&r="+Math.random();
}
},
onload:function(e,t){
a(t),t.gray&&!t.loadGif&&((t.width||t.naturalWidth)<120||(t.height||t.naturalHeight)<120?t.autoTap&&t.autoTap():t.span&&t.span.children&&t.span.children.item(0)&&(t.span.children.item(0).style.display=""));
var o=t?t.__retryload||0:0;
if(!(o>_)){
n("[Appmsg] image_load_event_onload_image. src:"+e+"  ^^^  retryloadtimes: "+o),
t.setAttribute("data-fail",0);
var i=0==e.indexOf("https://")?7:0;
window.__addIdKeyReport("28307",71+i),window.__addIdKeyReport("28307",73+1*o+i),
e.isWxpic()?(window.__addIdKeyReport("28307",92),window.__addIdKeyReport("28307",94+1*o)):e.isWebp()&&(window.__addIdKeyReport("28307",85),
window.__addIdKeyReport("28307",87+1*o)),f&&e.indexOf(f)>-1&&window.__addIdKeyReport("28307",107),
window.__has_imgsucceed||(window.__has_imgsucceed=!0,window.__addIdKeyReport("28307",64)),
1==o&&e.indexOf("http://")>-1&&window.__addIdKeyReport("28307",50),1==o&&e.indexOf("https://")>-1&&window.__addIdKeyReport("28307",52);
var r=Math.random(),s=+new Date-t.start_load_time;
s&&0==e.indexOf("https://")&&.5>r?(window.__addIdKeyReport("27822",121,s),window.__addIdKeyReport("27822",122)):s&&5e-4>r&&(window.__addIdKeyReport("27822",124,s),
window.__addIdKeyReport("27822",125));
}
},
detect:function(e){
if(e&&e.time&&e.loadList){
var t=e.time,o=e.loadList;
window.logs.img.download[t]=o;
}
},
container:document.getElementById("page-content")
});
});
}),e("appmsg/async.js"),!window.isSg;
var B=e("appmsg/copyright_report.js");
!function(){
var e=document.getElementById("post-user"),t=document.getElementById("copyright_info"),o=[],i=document.getElementById("post-user-headimg");
if(e){
var r="57";
"26"==window.source&&(r="95"),"28"==window.source&&(r="96"),"29"==window.source&&(r="39"),
"15"==window.source&&(r="121"),o.push({
dom:e,
username:user_name_new||user_name,
profileReportInfo:window.profileReportInfo||"",
scene:r
}),i&&o.push({
dom:i,
username:user_name_new||user_name,
profileReportInfo:window.profileReportInfo||"",
scene:r
});
}
t&&source_encode_biz&&o.push({
dom:t,
source_encode_biz:source_encode_biz,
scene:"110"
});
var s=document.getElementById("js_share_headimg");
s&&(window.new_appmsg&&window.source_encode_biz?m.on(s,"click",function(){
return location.href="/mp/profile_ext?action=home&__biz="+window.source_encode_biz+"#wechat_redirect",
!1;
}):o.push({
dom:s,
username:source_username,
scene:0
}));
var d=document.getElementById("js_share_author");
d&&(window.new_appmsg&&window.source_encode_biz?m.on(d,"click",function(){
return location.href="/mp/profile_ext?action=home&__biz="+window.source_encode_biz+"#wechat_redirect",
!1;
}):o.push({
dom:d,
username:source_username,
scene:0
}));
for(var c=0,g=o.length;g>c;c++)!function(e){
m.on(e.dom,"click",function(){
if("copyright_info"==e.dom.id&&source_encode_biz){
B.card_click_report({
scene:"0"
});
var t="https://mp.weixin.qq.com/mp/profile_ext?action=home&__biz="+e.source_encode_biz+"&scene="+e.scene+"#wechat_redirect";
-1!=navigator.userAgent.indexOf("WindowsWechat")||-1!=navigator.userAgent.indexOf("Mac OS")?location.href=t:l.invoke("openUrlWithExtraWebview",{
url:t,
openType:1
},function(e){
-1==e.err_msg.indexOf("ok")&&(location.href=t);
});
}else{
if(n("[Appmsg] profile_click_before_loadprofile: username:"+e.username+", scene:"+e.scene),
a({
url:"/mp/appmsgreport?action=name_click",
data:{
url:location.href,
title:window.msg_title||"",
msgid:window.mid||"",
itemidx:window.idx||"",
__biz:window.biz||""
},
type:"POST",
dataType:"json",
async:!0,
success:function(){}
}),profileReportInfo){
var o=String(profileReportInfo).split("_");
3==o.length&&a({
url:"/mp/ad_biz_info?action=report&__biz="+window.biz+"&report_type=2&aid="+o[1]+"&tid="+o[2],
type:"GET",
dataType:"json",
async:!0,
success:function(){}
});
}
l.invoke("profile",{
username:e.username,
profileReportInfo:e.profileReportInfo||"",
scene:e.scene
},function(t){
window.__addIdKeyReport("28307","1"),n("[Appmsg] profile_click_after_loadprofile: username:"+e.username+", scene:"+e.scene+", profileReportInfo:"+e.profileReportInfo+", res.err_msg:"+t.err_msg);
});
}
return!1;
}),p.isWp&&e.dom.setAttribute("href","weixin://profile/"+e.username);
}(o[c]);
}(),function(){
location.href.match(/fontScale=\d+/)&&p.isIOS&&l.on("menu:setfont",function(e){
e.fontScale<=0&&(e.fontScale=100),document.getElementsByTagName("html").item(0).style.webkitTextSizeAdjust=e.fontScale+"%",
document.getElementsByTagName("html").item(0).style.lineHeight=160/e.fontScale;
});
}();
var k=e("appmsg/outer_link.js");
if(new k({
container:document.getElementById("js_content"),
changeHref:function(e,t){
if(!e||0!=e.indexOf("http://mp.weixin.qq.com/")&&0!=e.indexOf("https://mp.weixin.qq.com/")){
if(18==ban_scene)return"/mp/ban?action=check&__biz="+biz+"&mid="+mid+"&idx="+idx+"&scene="+ban_scene+"#wechat_redirect";
if(0!=e.indexOf("http://mp.weixinbridge.com/mp/wapredirect"))return"http://mp.weixinbridge.com/mp/wapredirect?url="+encodeURIComponent(e)+"&action=appmsg_redirect&uin="+uin+"&biz="+biz+"&mid="+mid+"&idx="+idx+"&type="+t+"&scene=0";
}else{
e=e.replace(/#rd\s*$/,""),e=e.replace(/#wechat_redirect\s*$/,""),e=e.replace(/[\?&]scene=21/,"");
var o="&";
-1==e.indexOf("?")&&(o="?"),e+=o+"scene=21#wechat_redirect";
}
return e;
}
}),!I){
var O=e("appmsg/review_image.js"),T=document.getElementById("js_cover"),S=[];
T&&S.push(T),new O({
container:document.getElementById("js_content"),
is_https_res:is_https_res,
imgs:S
});
}
e("appmsg/product.js"),function(){
try{
var e=document.getElementById("js_content");
if(!e||!e.querySelectorAll)return;
for(var t=e.querySelectorAll("*"),o="img_loading,list-paddingleft-2,selectTdClass,noBorderTable,ue-table-interlace-color-single,ue-table-interlace-color-double,__bg_gif,weapp_text_link,weapp_image_link".split(","),i=function(e){
if(e&&e.className){
for(var t=e.className.split(/\s+/),i=[],n=0,a=t.length;a>n;++n){
var r=t[n];
r&&-1!=o.indexOf(r)&&i.push(r);
}
e.className=i.join(" ");
}
},n=0,a=t.length;a>n;++n){
var r=t[n];
r.tagName&&"iframe"!=r.tagName.toLowerCase()&&i(r);
}
}catch(s){}
}(),window.fromWeixinCached||e("appmsg/iframe.js"),e("appmsg/qqmusic.js"),e("appmsg/voice.js"),
e("appmsg/weapp.js"),window.new_appmsg&&e("appmsg/new_index.js"),e("appmsg/wxtopic.js"),
e("appmsg/cdn_speed_report.js"),e("appmsg/page_pos.js"),setTimeout(function(){
window.article_improve_combo_css;
},0),setTimeout(function(){
m.tap(document.getElementById("copyright_logo"),function(){
location.href="http://kf.qq.com/touch/sappfaq/150211YfyMVj150326iquI3e.html";
}),d(),c(),e("appmsg/report_and_source.js"),function(){
if(I){
i.addClass(_,"not_in_mm");
var e=document.getElementById("js_pc_qr_code_img");
if(e){
var t=10000004,o=document.referrer;
if(0==o.indexOf("http://weixin.sogou.com")?t=10000001:0==o.indexOf("https://wx.qq.com")&&(t=10000003),
window.isSg)e.setAttribute("src",sg_qr_code.htmlDecode());else{
e.setAttribute("src","/mp/qrcode?scene="+t+"&size=102&__biz="+biz+"&mid="+mid+"&idx="+idx+"&sn="+sn+"&send_time="+send_time);
var n=new Image;
n.src="/mp/report?action=pcclick&__biz="+biz+"&uin="+uin+"&scene="+t+"&r="+Math.random();
}
document.getElementById("js_pc_qr_code").style.display="block";
}
var a=document.getElementById("js_profile_qrcode"),r=document.getElementById("js_profile_arrow_wrp"),s=document.getElementById("post-user");
if(a&&s&&r){
var d=function(){
var e=10000005,t=document.referrer;
0==t.indexOf("http://weixin.sogou.com")?e=10000006:0==t.indexOf("https://wx.qq.com")&&(e=10000007);
var o=document.getElementById("js_profile_qrcode_img");
if(o)if(window.isSg)o.setAttribute("src",sg_qr_code.htmlDecode());else{
o.setAttribute("src","/mp/qrcode?scene="+e+"&size=102&__biz="+biz+"&mid="+mid+"&idx="+idx+"&sn="+sn+"&send_time="+send_time);
var i=new Image;
i.src="/mp/report?action=pcclick&__biz="+biz+"&uin="+uin+"&scene="+e+"&r="+Math.random();
}
return a.style.display="block",r.style.left=s.offsetLeft-a.offsetLeft+s.offsetWidth/2-8+"px",
!1;
};
m.on(s,"click",d),m.on(a,"click",d),m.on(document,"click",function(e){
var t=e.target||e.srcElement;
t!=s&&t!=a&&(a.style.display="none");
});
}
}else{
var p=document.getElementById("js_report_article3");
!!p&&(p.style.display="");
}
}(),function(){
var e=location.href.indexOf("scrolltodown")>-1?!0:!1,t=document.getElementById("img-content");
if(e&&t&&t.getBoundingClientRect){
var o=t.getBoundingClientRect().height;
window.scrollTo(0,o);
}
}(),e("appmsg/report.js");
for(var t=document.getElementsByTagName("map"),o=0,n=t.length;n>o;++o)t[o].parentNode.removeChild(t[o]);
if(B.card_pv_report(),Math.random()<.01)try{
var a="https://js.aq.qq.com/js/aq_common.js",r=document.createElement("script");
r.src=a;
var s=document.getElementsByTagName("head")[0];
s.appendChild(r);
}catch(p){}
var l=document.getElementById("js_close_temp");
m.on(l,"click",function(){
l.parentNode.parentNode.removeChild(l.parentNode),i.removeClass(document.getElementById("js_article"),"preview_appmsg");
});
},1e3),function(){
if(o.os.ios&&"onorientationchange"in window){
var e=[],t="onorientationchange"in window?"orientationchange":"resize",i=function(){
return 90===Math.abs(window.orientation)?1:2;
};
e.push({
ori:i(),
scroll:window.pageYOffset||document.documentElement.scrollTop,
istouchmove:!1
});
var n=(new Date).getHours();
m.on(window,t,function(){
var t=e.length-2,o=i();
if(t>=0){
var a=e[t],r=a.ori;
r!==o||e[e.length-1].istouchmove||(n>=11&&17>=n&&window.__report(63),window.scrollTo(0,a.scroll));
}
e.push({
ori:o,
scroll:window.pageYOffset||document.documentElement.scrollTop,
istouchmove:!1
});
}),m.on(window,"scroll",function(){
var t=e.length-1;
e[t].ori==i()&&(e[t].scroll=window.pageYOffset||document.documentElement.scrollTop,
e[t].istouchmove=!0);
});
}
}(),n("[Appmsg] href:"+location.href+"^^^ ua:"+window.navigator.userAgent),window.addEventListener?window.addEventListener("load",r,!1):window.attachEvent&&window.attachEvent("onload",r),
e("appmsg/fereport.js"),function(){
window.addEventListener&&document.getElementsByTagName("body")[0].addEventListener("copy",function(){
(new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_18_1",
p.isIOS&&((new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_19_1"),
p.isAndroid&&((new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_20_1");
},!1);
}(),function(){
window.__observer&&window.__observer_data&&e("biz_wap/safe/mutation_observer_report.js");
}(),function(){
var e=[.875,1,1.125,1.25,1.375],t=window.location.href.match(/winzoom=(\d+(?:\.\d+)?)/);
if(t){
var o=parseFloat(t[1]);
if("undefined"!=typeof e.indexOf&&e.indexOf(o)>=0){
document.getElementById("page-content").style.zoom=o;
var i=document.getElementsByClassName("rich_media_title"),n=document.getElementsByClassName("rich_media_meta_list");
i&&i.length>1&&(i[0].style.zoom=1/o),n&&n.length>1&&(n[0].style.zoom=1/o);
}
}
}(),"undefined"!=typeof isSg&&e("sougou/index.js"),setTimeout(function(){
for(var e=function(){
(new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_49_1&lc=1&log0=[28307_49_appmsg_fe_filter]"+encodeURIComponent(location.href);
},t=(window.appmsg_fe_filter||"").split(","),o=function(t,o){
try{
if(!t)return;
if(t.querySelectorAll){
var i=t.querySelectorAll("*["+o+"]");
if(i&&i.length>0){
e();
for(var n=0;n<i.length;++n)i[n]&&i[n].removeAttribute&&i[n].removeAttribute(o);
}
return;
}
var a=t.childNodes;
if(t.hasAttribute&&t.hasAttribute(o)&&e(),t.removeAttribute&&t.removeAttribute(o),
a&&a.length)for(var n=0;n<a.length;++n)filterContenteditable(a[n]);
}catch(r){}
},i=document.getElementById("js_content"),n=0;n<t.length;++n)t[n]&&o(i,t[n]);
},0),setTimeout(function(){
var e=999,t=636,o="http://mmbiz.qpic.cn/mmbiz_png/7lG1x2vpicdic0p5bBthpD9lsJcINicsSzd6uKQQJyoj5oTl8lFIs9K0fIibgxCzms0enDLTRxTHLpDPCLpSvIExiag/0",i=(new Date).getHours();
if(!(11>i||i>16||Math.random()<.99)){
var n=new Image;
n.onload=function(){
var o=n.naturalWidth||n.width,i=n.naturalHeight||n.height;
(o!=e||i!=t)&&window.__addIdKeyReport("28307","wifi"===window.networkType?120:123),
window.__addIdKeyReport("28307","wifi"===window.networkType?121:124);
},n.src=o;
var a=new Image;
a.onload=function(){
var o=a.naturalWidth||a.width,i=a.naturalHeight||a.height;
(o!=e||i!=t)&&window.__addIdKeyReport("28307",126),window.__addIdKeyReport("28307",127);
},a.src="https://mmbiz.qpic.cn/mmbiz_png/7lG1x2vpicdic0p5bBthpD9lsJcINicsSzd6uKQQJyoj5oTl8lFIs9K0fIibgxCzms0enDLTRxTHLpDPCLpSvIExiag/0";
}
},3e3);
}
e("biz_common/utils/string/html.js");
var o=e("biz_wap/utils/device.js"),i=e("biz_common/dom/class.js"),n=e("appmsg/log.js"),a=e("biz_wap/utils/ajax.js"),r=e("biz_common/dom/attr.js"),s=r.setProperty,d=e("appmsg/max_age.js"),p=e("biz_wap/utils/mmversion.js"),c=e("appmsg/test.js"),m=e("biz_common/dom/event.js"),l=e("biz_wap/jsapi/core.js"),p=e("biz_wap/utils/mmversion.js");
window.new_appmsg?(e("page/appmsg_new/combo.css"),e("page/appmsg_new/not_in_mm.css")):(e("page/appmsg/page_mp_article_improve_combo.css"),
e("page/appmsg/not_in_mm.css"));
var g=top.window.user_uin||0,_=Math.floor(g/100)%1e3,w=0!==g&&1001>_,u=0!==g&&10>_;
(2608618616==g||612444339==g||2026636217==g)&&(u=!0);
var f="";
window.logs.pagetime.jsapi_ready_time=+new Date,window.logs.idkeys={},console.log("进入index.js init"),
n("[Appmsg] start run index.js init"),t();
});