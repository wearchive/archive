define("appmsg/emotion/common.js",[],function(){
"use strict";
return{
EMOTIONS_COUNT:99,
EMOTION_LI_SIZE:36,
EMOTION_SIZE:22
};
});define("appmsg/emotion/slide.js",["appmsg/emotion/common.js","appmsg/emotion/dom.js","appmsg/emotion/nav.js"],function(n,t){
"use strict";
function o(){
function n(n){
n.preventDefault(),n.stopPropagation(),l||(g=!0,i=a(n),m.isMoved=!1,u=+new Date);
}
function t(n){
n.preventDefault(),n.stopPropagation(),!l&&g&&(r=a(n),h=r-i,e(),Math.abs(h)>6&&(m.isMoved=!0));
}
function o(){
l||(g=!1,s());
}
function a(n){
return n.touches&&n.touches.length>0?n.touches[0].clientX:n.clientX;
}
var i,r,u;
c.on("touchstart",n),c.on("mousedown",n),c.on("touchmove",t),c.on("mousemove",t),
c.on("touchend",o),c.on("mouseup",o);
}
function e(){
var n=m.WIDTH,t=-d*n+h,o=n/4;
t>o?t=o:u-o>t&&(t=u-o);
var e="translate3d("+t+"px, 0, 0)";
c.css({
webkitTransform:e,
transform:e
});
}
function s(){
var n=m.WIDTH,t=55,o=parseInt(h/n),e=h%n;
d-=o,Math.abs(e)>t&&(d-=Math.abs(e)/e*1),d>m.pageCount-1?d=m.pageCount-1:0>d&&(d=0),
h=0,a(d);
}
function a(n){
l=!0,f=-n*m.WIDTH,i(),e(),setTimeout(function(){
l=!1,r();
},T),v.activeNav(n);
}
function i(){
var n="all 0.3s ease";
c.css({
transition:n,
webkitTransition:n
});
}
function r(){
var n=c.el[0].style;
n.transition="",n.webkitTransition="";
}
var u,m=n("appmsg/emotion/common.js"),p=n("appmsg/emotion/dom.js"),t={},c=p("#js_slide_wrapper"),f=0,v=n("appmsg/emotion/nav.js"),l=!1,d=0,g=!1,h=0;
t.init=function(){
u=-m.wrapperWidth+m.WIDTH,o();
var n="translate3d(0, 0, 0)";
c.css({
webkitTransform:n,
transform:n
});
};
var T=300;
return t;
});define("pages/report.js",["biz_wap/utils/ajax.js","pages/version4video.js"],function(e){
"use strict";
function i(e){
var i=["/mp/pagereport?type=","undefined"==typeof e.type?1:e.type,"&comment_id=",e.comment_id||"","&voiceid=",e.voiceid||"","&action=",e.action,"&__biz=",top.window.biz||"","&mid=",top.window.mid||"","&idx=",top.window.idx||"","&uin=",top.window.uin||"","&key=",top.window.key||"","&pass_ticket=",top.window.pass_ticket||"","&t=",Math.random(),"#wechat_redirect"].join(""),t=new Image;
t.src=i;
}
function t(e){
_({
type:"POST",
url:"/mp/videoreport?#wechat_redirect",
timeout:2e4,
async:!1,
data:e.data
});
}
function o(e){
var i=JSON.parse(JSON.stringify(e.data));
i.musicid=i.musicid.join(";"),i.hasended=i.hasended.join(";"),i.commentid=i.commentid.join(";"),
i.mtitle=i.mtitle.join(";#"),i.detail_click=i.detail_click.join(";"),i.duration=i.duration.join(";"),
i.errorcode=i.errorcode.join(";"),i.play_duration=i.play_duration.join(";"),_({
type:"POST",
url:"/mp/musicreport?#wechat_redirect",
timeout:2e4,
async:!1,
data:i
});
}
function n(e){
document.domain="qq.com";
var i=window.cgiData&&window.cgiData.txvideo_openid?window.cgiData.txvideo_openid:"",t=encodeURIComponent(top.window.location.href.replace(/(\?|&)(key|uin)=([\S\s]*?)(&|$)/g,"$1").replace(/&$/,"")),o=["http://btrace.qq.com/kvcollect?BossId=2973&Pwd=1557019983&step=1009&vid=","undefined"!=typeof e.vid?e.vid:"","&platform=",a(),"&val=","undefined"!=typeof e.val?e.val:"","&val1=","undefined"!=typeof e.val1?e.val1:"","&vurl=",encodeURIComponent(e.vurl),"&t=",Math.random(),"&url=",t,"&wx_openid=",i].join(""),n=new Image;
n.src=o.substr(0,1024);
}
function d(e){
if(3==e.step||6==e.step||1999==e.step){
document.domain="qq.com";
var i=window.cgiData&&window.cgiData.txvideo_openid?window.cgiData.txvideo_openid:"",t=encodeURIComponent(top.window.location.href.replace(/(\?|&)(key|uin)=([\S\s]*?)(&|$)/g,"$1").replace(/&$/,"")),o=["http://btrace.qq.com/kvcollect?BossId=2973&Pwd=1557019983&step=",e.step,"&vid=","undefined"!=typeof e.vid?e.vid:"","&platform=",a(),"&loadwait=","undefined"!=typeof e.loadwait?e.loadwait:"","&val=","undefined"!=typeof e.val?e.val:"","&t=",Math.random(),"&url=",t,"undefined"!=typeof e.vt&&""!==e.vt&&6==e.step?"&vt="+e.vt:"","&wx_openid=",i].join(""),n=new Image;
n.src=o.substr(0,1024);
}
}
function a(){
var e=l.device;
return e.ipad?60101:e.is_android_phone?60301:e.iphone?60401:e.is_android_tablet?60501:"";
}
function r(){
var e=l.device;
return e.ipad?"v4010":e.is_android_phone&&l.isUseProxy()?"v5060":e.is_android_phone?"v5060":e.iphone&&l.isUseProxy()?"v3060":e.iphone?"v3060":e.is_android_tablet?"v6010":"";
}
function p(e){
var i={
mid:window.mid||"",
__biz:window.biz||"",
idx:window.idx||"",
musicid:[],
hasended:[],
commentid:[],
scene_type:e.type||0,
mtitle:[],
detail_click:[],
app_btn_kv:0,
app_btn_click:0,
app_btn_type:0,
duration:[],
play_duration:[],
errorcode:[]
};
return i;
}
function c(){
var e={
videoerror:0,
like_kv_vid:"",
like_click_vid:"",
like_kv_alginfo:"",
like_click_alginfo:"",
tad:"",
page:0,
like_click_type:0,
iplat:2,
ptype:1,
rtype:"",
getvinfo_ret:-1,
getvinfo_time:0,
v_err_code:0,
loadwait:0,
hasended:0,
last_ms:0,
duration_ms:0,
app_btn_kv:0,
app_btn_click:0,
app_btn_type:0,
mid:"",
__biz:"",
idx:"",
detail_click:0,
vtitle:"",
vid:"",
commentid:"",
scene_type:"",
replay:0,
full_screen:0,
quick_play:0,
ad_play_time:-1,
video_play_time:-1,
click_play_button:0,
traceid:"",
webviewid:"",
orderid:0,
play_time:0,
client_time_when_play:0,
drag_times:"",
pause_num:0,
h5_profile:0,
to_article:0,
desc_more_click:0,
desc_more_show:0,
fromid:0,
openid:window.cgiData&&window.cgiData.txvideo_openid?window.cgiData.txvideo_openid:"",
file_size:0,
rate:0,
resolution:0,
format:"",
vt:"",
video_ext:"unknown"
};
return e;
}
var _=e("biz_wap/utils/ajax.js"),l=e("pages/version4video.js");
return{
report:i,
videoreport:t,
getPlatformType:a,
getsdtfrom:r,
getinfoReport:n,
qqvideo_common_report:d,
musicreport:o,
getMusicReportData:p,
getVideoReportData:c
};
});define("pages/music_player.js",["biz_wap/utils/mmversion.js","biz_common/dom/event.js","biz_wap/jsapi/core.js","pages/version4video.js","biz_common/utils/monitor.js"],function(t){
"use strict";
function e(t){
this._o={
wxIndex:0,
type:0,
src:"",
mid:"",
songId:"",
autoPlay:!1,
duration:0,
needVioceMutex:!0,
title:"",
allowPause:!1,
singer:"",
epname:"",
coverImgUrl:"",
webUrl:"",
fileSize:0,
onStatusChange:function(){},
onTimeupdate:function(){},
onError:function(){},
onUpdateSeekRange:function(){}
},this._extend(t),this._status=-1,this._g={
mutexKey:"",
jsapiSrcId:"",
hasCheckPlay:!1,
playTimeoutId:null,
stateChangeCallback:{}
},this._fixAndroidSizeLimit(),0!==b.surportType&&(this._initData(),this._synPlayStatus());
}
function o(t){
w.invoke("musicPlay",{
app_id:"a",
title:"微信公众平台",
singer:"微信公众平台",
epname:"微信公众平台",
coverImgUrl:"http://res.wx.qq.com/mpres/htmledition/images/favicon.ico",
dataUrl:b.ev,
lowbandUrl:b.ev,
webUrl:"http://mp.weixin.qq.com/s?"
},function(e){
"function"==typeof t&&t(e);
});
}
function i(t){
n({
cur:t,
stopCur:!1
});
}
function n(t){
function e(){
if(b.mutexCount==s&&(s=0,b.mutexCount=0,"function"==typeof a)){
var t=0;
1==b.surportType?t=2e3:3==b.surportType&&(t=0),setTimeout(function(){
a();
},t);
}
}
if(0!=b.mutexCount)return void setTimeout(function(){
n(t);
},200);
var o=t.cur,i=t.stopCur===!0?!0:!1,a=t.callback,s=0;
for(var r in b.mutexPlayers)for(var u=0,p=b.mutexPlayers[r].length;p>u;u++)s++;
for(var r in b.mutexPlayers)for(var u=0,p=b.mutexPlayers[r].length;p>u;u++){
var _=b.mutexPlayers[r][u];
if(_&&_!==o){
var c=_.getSurportType(),d="";
2!=c||1!=_._status&&4!=_._status?1!=c&&3!=c||1!=_._status&&2!=_._status&&4!=_._status||(d="stop"):d=_._o.allowPause?"pause":"stop",
d&&"function"==typeof _[d]?_[d](i,function(){
b.mutexCount++,e();
}):(b.mutexCount++,e());
}else b.mutexCount++,e();
}
}
function a(){
return b.surportType;
}
function s(t){
return new e(t);
}
function r(){
b.surportType>0&&b.isAndroidLow&&window.addEventListener("canplay",function(t){
t.target&&"function"==typeof t.target.play&&t.target.play();
},!0);
}
function u(){
b.jsapiGlobalEvent={
error:c,
pause:l,
stop:d,
play:h,
preempted:d,
waiting:y
};
}
function p(t){
return"&"+b.wxtag+"="+t;
}
function _(){
w.on("onBackgroundAudioStateChange",function(t){
if(!!b.debug&&console.log("onBackgroundAudioStateChange log:"+JSON.stringify(t||{})),
t.src&&t.state){
var e=T(b.wxtag,t.src)||"";
e&&(e=p(e));
var o=b.mutexPlayers[t.src]||b.mutexPlayers[e];
if(o){
var i;
if(t.srcId)for(var n=0,a=o.length;a>n;n++)o[n]._g.jsapiSrcId==t.srcId&&(i=o[n]);else if(1==o.length)i=o[0];else for(var n=0,a=o.length;a>n;n++)if(-1!=o[n]._status&&0!=o[n]._status&&3!=o[n]._status){
i=o[n];
break;
}
if(i&&i._g.stateChangeCallback){
var s=t.state;
"ended"==s&&(s="stop"),"wait"==s&&(s="waiting");
var r=!1;
if("error"==s)for(var u in i._g.stateChangeCallback)i._g.stateChangeCallback.hasOwnProperty(u)&&"function"==typeof i._g.stateChangeCallback[u]&&(r=!0,
i._g.stateChangeCallback[u](-1,t.errMsg||""),i._g.stateChangeCallback[u]=null);else"function"==typeof i._g.stateChangeCallback[s]&&(b.debug&&console.log("excute stateChangeCallback :"+s),
r=!0,i._g.stateChangeCallback[s](0),i._g.stateChangeCallback[s]=null);
r||"function"!=typeof b.jsapiGlobalEvent[s]||b.jsapiGlobalEvent[s](t,i);
}
}
}
});
}
function c(t,e){
e.stop(!1),v(e._o.type,"wx_err_2",1);
}
function d(t,e){
e.stop(!1);
}
function l(t,e){
e.pause(!1,null,!0);
}
function h(t,e){
1!=e._status&&e.resume(!1,null,!0);
}
function y(t,e){
e.onload();
}
function f(){
for(var t=b.reportId.split(";"),e=0,o=t.length;o>e;e++)for(var i=t[e],n=b.keyConf[e],a=0,s=0,r=n.length;r>s;s++){
var u=n[s]||"";
u?/^offset_/.test(u)?a+=1*u.replace(/^offset_/,""):(b.reportData[u]={
id:i,
key:a,
count:0
},a++):a++;
}
}
function g(){
for(var t in b.mutexPlayers)if(b.mutexPlayers.hasOwnProperty(t))for(var e=0,o=b.mutexPlayers[t].length;o>e;e++){
var i=b.mutexPlayers[t][e];
if(i&&1==i._status&&(1==i._surportType||3==i._surportType)){
v(i._o.type,"unload_wx_pv",1);
break;
}
}
m();
}
function m(){
for(var t in b.reportData){
var e=b.reportData[t];
e.count>0&&x.setSum(e.id,e.key,e.count);
}
x.send(),f();
}
function v(t,e,o){
0==t||1==t?e="m_"+e:(2==t||3==t||4==t)&&(e="v_"+e),b.reportData[e]&&(o=o||1,b.reportData[e].count+=o,
b.debug&&console.log("addpv:"+e+" count:"+b.reportData[e].count));
}
function T(t){
var e=arguments[1]||window.location.search,o=new RegExp("(^|&)"+t+"=([^&]*)(&|$)"),i=e.substr(e.indexOf("?")+1).match(o);
return null!=i?i[2]:"";
}
function S(t,e,o){
function i(t,e){
for(;b.synPlayStatusArr.length>0;){
var o=b.synPlayStatusArr.shift();
o&&"function"==typeof o[t]&&o[t](e);
}
}
b.synPlayStatusArr.push({
_t:t,
onSuccess:e,
onError:o
}),b.synPlayStatusId&&clearTimeout(b.synPlayStatusId),b.synPlayStatusId=setTimeout(function(){
t._jsapi_getMusicPlayerState({
onSuccess:function(t){
i("onSuccess",t);
},
onError:function(t){
i("onError",t);
}
});
},0);
}
document.domain="qq.com";
var P=t("biz_wap/utils/mmversion.js"),A=t("biz_common/dom/event.js"),w=t("biz_wap/jsapi/core.js"),k=t("pages/version4video.js"),x=t("biz_common/utils/monitor.js"),b={
synPlayStatusId:null,
synPlayStatusArr:[],
inWechat:!k.device.inWechat||k.device.inWindowWechat||k.device.inMacWechat?!1:!0,
mutexCount:0,
ev:0!=window._empty_v.indexOf(window.location.protocol)?"http:"+window._empty_v:window._empty_v,
debug:location.href.indexOf("vconsole=1")>0||document.cookie&&document.cookie.indexOf("vconsole_open=1")>-1?!0:!1,
_playtype:1*T("_playtype")||0,
isAndroidLow:/android\s2\.3/i.test(navigator.userAgent),
isAndroid:P.isAndroid,
surportType:"addEventListener"in window?2:0,
mutexPlayers:{},
reportId:"28306",
wxtag:"__wxtag__",
keyConf:[["m_pv","m_wx_pv","m_h5_pv","m_unload_wx_pv","v_pv","v_wx_pv","v_h5_pv","v_unload_wx_pv","offset_22","force_h5","m_h5_err_total","m_h5_err_1","m_h5_err_2","m_h5_err_3","m_h5_err_4","m_h5_err_5","v_h5_err_total","v_h5_err_1","v_h5_err_2","v_h5_err_3","v_h5_err_4","v_h5_err_5","m_wx_pv_2","v_wx_pv_2","offset_5","m_wx_pv_1","offset_4","v_wx_pv_1","offset_2","m_wx_err_1","m_wx_err_2","v_wx_err_1","v_wx_err_2"]],
reportData:{}
};
return f(),u(),_(),A.on(window,"unload",g),r(),e.prototype._synPlayStatus=function(){
function t(t){
if(a&&clearTimeout(a),n.hasCheckPlay!==!0&&(n.hasCheckPlay=!0,o._surportType=3,b.surportType=3,
!!b.debug&&console.log("_synPlayStatus mutexKey:"+n.mutexKey),t.src&&(i.src==t.src||t.src.indexOf(n.mutexKey)>0))){
if(t.srcId){
if(t.srcId!=n.jsapiSrcId)return;
}else if(b.mutexPlayers[n.mutexKey].length>1&&b.mutexPlayers[n.mutexKey][0]!==o)return;
o._initJsapiData({
curTime:t.currentTime,
bufferedPercent:t.bufferedPercent,
starTime:+new Date-1e3*t.currentTime
});
var e=o.jsApiData;
t.paused?(e.pauseTime=e.starTime+1e3*e.curTime,o._onPause(),o._onTimeupdate(null,e.curTime)):(o._onPlay(),
o._analogUpdateTime()),o._getMusicPlayerState();
}
}
function e(){
a&&clearTimeout(a),n.hasCheckPlay!==!0&&(n.hasCheckPlay=!0,o._o.autoPlay&&o.play());
}
var o=this,i=this._o,n=this._g;
if(!b.inWechat||1*b._playtype>0)return n.hasCheckPlay=!0,void(o._o.autoPlay&&o.play());
var a;
S(o,t,e),a=setTimeout(function(){
e();
},5e3);
},e.prototype._fixAndroidSizeLimit=function(){
if(!(1*b._playtype>0)&&b.isAndroid){
var t=this._o;
!t.fileSize||t.fileSize>300||P.gtVersion("6.3.28",!0)||(v(-1,"force_h5",1),this._g._playtype=2);
}
},e.prototype._createAutoAndPlay=function(){
function t(){
v(e._o.type,"pv",1),v(e._o.type,"h5_pv",1),e._h5Audio=document.createElement("audio"),
e._H5bindEvent(),e._h5Audio.setAttribute("style","height:0;width:0;display:none"),
e._h5Audio.setAttribute("autoplay",""),e._status=0,e._initH5Data(),b.isAndroidLow?(e._h5Audio.src=e._o.src,
document.body.appendChild(e._h5Audio),e._h5Audio.load()):(document.body.appendChild(e._h5Audio),
setTimeout(function(){
e._h5Audio.src=e._o.src,e._h5Audio.play();
},0)),e._surportType=2;
}
var e=this;
b.inWechat?this._stopJsapiPlay(!0,function(){
t();
}):t();
},e.prototype._destoryH5Audio=function(){
this._h5Audio&&(-1!=this._status&&"function"==typeof this._h5Audio.pause&&this._h5Audio.pause(),
document.body.removeChild(this._h5Audio),this._h5Audio=null,this._status=-1);
},e.prototype._onLoading=function(t){
this._status=4;
try{
i(this);
}catch(t){}
"function"==typeof this._o.onStatusChange&&this._o.onStatusChange.call(this,t||{},this._status);
},e.prototype._onPlay=function(t){
this._status=1;
try{
i(this);
}catch(t){}
"function"==typeof this._o.onStatusChange&&this._o.onStatusChange.call(this,t||{},this._status);
},e.prototype._onPause=function(t){
this._status=2,"function"==typeof this._o.onStatusChange&&this._o.onStatusChange.call(this,t||{},this._status);
},e.prototype._onEnd=function(t){
this._status=3,"function"==typeof this._o.onStatusChange&&this._o.onStatusChange.call(this,t||{},this._status);
},e.prototype._onLoadedmetadata=function(t){
"function"==typeof this._o.onLoadedmetadata&&this._o.onLoadedmetadata.call(this,t||{});
},e.prototype._onUpdateSeekRange=function(t){
this.surportSeekRange()&&(t=Math.max(t,0),t=Math.min(t,100),"function"==typeof this._o.onUpdateSeekRange&&this._o.onUpdateSeekRange.call(this,t));
},e.prototype._onTimeupdate=function(t,e){
"function"==typeof this._o.onTimeupdate&&this._o.onTimeupdate.call(this,t||{},e);
},e.prototype._onError=function(t,e){
this._status=-1,"function"==typeof this._o.onError&&this._o.onError.call(this,t||{},e);
},e.prototype._H5bindEvent=function(){
var t=this,e=this._o;
this._h5Audio.addEventListener("play",function(e){
t._h5Audio&&(t._onPlay(e),t._onUpdateSeekRange(t._h5Data.downloadDuration||0));
},!1),this._h5Audio.addEventListener("ended",function(e){
t._h5Audio&&(t._onUpdateSeekRange(t._h5Data.downloadDuration),t._onEnd(e));
},!1),this._h5Audio.addEventListener("pause",function(e){
t._h5Audio&&(t._o.allowPause!==!0||0==t._h5Audio.currentTime?t._onEnd(e):t._onPause(e));
},!1),this._h5Audio.addEventListener("error",function(e){
var o=1*e.target.error.code||5;
(1>o||o>5)&&(o=5),v(t._o.type,"h5_err_total",1),v(t._o.type,"h5_err_"+o,1),t._onError(e,{
type:1,
code:o
}),t._destoryH5Audio();
},!1),"function"==typeof this._o.onTimeupdate&&this._h5Audio.addEventListener("timeupdate",function(o){
t._h5Audio&&((1==t._status||4==t._status)&&t._onUpdateSeekRange(t._getH5DownloadDuration()),
1==t._status&&t._onTimeupdate(o,t._h5Audio.currentTime),"undefined"!=typeof e.duration&&1*e.duration>0&&t._h5Audio.currentTime>=e.duration&&t._h5Stop());
},!1),"function"==typeof this._o.onLoadedmetadata&&this._h5Audio.addEventListener("loadedmetadata",function(e){
t._h5Audio&&t._onLoadedmetadata(e);
},!1);
},e.prototype._initData=function(){
this._createMutexKey(),b.mutexPlayers[this._g.mutexKey]?b.mutexPlayers[this._g.mutexKey].push(this):b.mutexPlayers[this._g.mutexKey]=[this];
},e.prototype._createMutexKey=function(){
var t=this._o.mid||"";
this._o.src?(this._g.mutexKey=this._o.src,this._g.jsapiSrcId=b.wxtag+"_"+this._o.wxIndex):(this._g.mutexKey=p(t),
this._g.jsapiSrcId=this._g.mutexKey+"_"+this._o.wxIndex);
},e.prototype._extend=function(t){
for(var e in t)this._o[e]=t[e];
},e.prototype._initH5Data=function(){
this._h5Data={
downloadDuration:0
};
},e.prototype._initJsapiData=function(t){
t=t||{},this.jsApiData&&(this.jsApiData.updateTimeoutId&&clearTimeout(this.jsApiData.updateTimeoutId),
this.jsApiData.getStatusId&&clearTimeout(this.jsApiData.getStatusId)),this.jsApiData={
getStatusId:null,
getStatusTime:t.getStatusTime||2500,
updateTimeoutId:null,
seeking:!1,
starTime:t.starTime||+new Date,
curTime:t.curTime||0,
pauseTime:t.pauseTime||0,
bufferedPercent:t.bufferedPercent||0,
duration:this._o.duration||void 0
};
},e.prototype._getMusicPlayerState=function(){
var t=this,e=t._o,o=t.jsApiData;
o&&o.getStatusId&&clearTimeout(o.getStatusId),t._jsapi_getMusicPlayerState({
onSuccess:function(i){
i.src==e.src&&(o.curTime=i.currentTime,o.starTime=+new Date-1e3*i.currentTime,o.bufferedPercent=i.bufferedPercent,
(1==t._status||2==t._status)&&(o.getStatusId=setTimeout(function(){
t._getMusicPlayerState();
},o.getStatusTime)),t._onUpdateSeekRange(o.bufferedPercent),1==i.paused&&1==t._status?(b.debug&&console.log("_getMusicPlayerState force syn"),
t._pauseJsapiPlay(!1)):0==i.paused&&2==t._status&&(b.debug&&console.log("_getMusicPlayerState force syn"),
t._resumeJsapiPlay(!1)));
},
onError:function(){
o.getStatusId=setTimeout(function(){
t._getMusicPlayerState();
},o.getStatusTime);
}
});
},e.prototype._analogUpdateTime=function(){
var t=this,e=t.jsApiData;
if(e&&e.updateTimeoutId&&clearTimeout(e.updateTimeoutId),1==t._status){
if(e.curTime=1*((+new Date-e.starTime)/1e3).toFixed(2),e.curTime>=e.duration)return t._stopJsapiPlay(!1),
!0;
t._onTimeupdate(null,e.curTime);
}
return e.updateTimeoutId=setTimeout(function(){
t._analogUpdateTime();
},1e3),!1;
},e.prototype._jsapi_getMusicPlayerState=function(t){
var e=this._o;
w.invoke("getBackgroundAudioState",{},function(o){
if(!!b.debug&&console.log("getBackgroundAudioState log:"+JSON.stringify(o||{})),
/:ok$/.test(o.err_msg)){
if(o.paused=1*o.paused,o.currentTime=o.currentTime?(1*o.currentTime).toFixed(2):0,
o.buffered){
var i=Math.floor(o.buffered/e.duration*100);
i=Math.max(i,0),i=Math.min(i,100),o.bufferedPercent=i;
}else o.bufferedPercent=0;
"function"==typeof t.onSuccess&&t.onSuccess(o);
}else"function"==typeof t.onError&&t.onError(o);
});
},e.prototype._jsapi_musicPlay=function(t){
if(this._h5Audio&&this._destoryH5Audio(),2==b._playtype)return void("function"==typeof t.onError&&t.onError({}));
var e=this,o=this._o;
w.invoke("musicPlay",{
app_id:"a",
title:o.title,
singer:o.singer,
epname:o.epname,
coverImgUrl:o.coverImgUrl,
dataUrl:o.src,
lowbandUrl:o.src,
webUrl:o.webUrl
},function(i){
!!b.debug&&console.log("playlog:"+JSON.stringify(i||{})),i.err_msg.indexOf("ok")>=0?(v(o.type,"pv",1),
v(o.type,"wx_pv",1),v(o.type,"wx_pv_1",1),e._surportType=1,b.surportType=1,e._initJsapiData(),
e._onPlay(),"undefined"!=typeof o.duration&&1*o.duration>0&&e._analogUpdateTime(),
e._onUpdateSeekRange(0),"function"==typeof t.onSuccess&&t.onSuccess(i)):"function"==typeof t.onError&&t.onError(i);
});
},e.prototype._jsapi_setBackgroundAudioState=function(t){
if(this._h5Audio&&this._destoryH5Audio(),1*b._playtype>0){
if("function"==typeof t.onError){
var e={};
e.err_code=1,t.onError(e);
}
}else{
var o=this,i=this._o,n=o._g;
w.invoke("setBackgroundAudioState",{
src:i.src,
lowbandUrl:i.src,
title:i.title,
epname:i.epname,
singer:i.singer,
srcId:n.jsapiSrcId,
coverImgUrl:i.coverImgUrl,
webUrl:i.webUrl
},function(e){
!!b.debug&&console.log("setBackgroundAudioState log:"+JSON.stringify(e||{})),e.err_msg.indexOf("ok")>=0?("function"==typeof t.onSuccess&&t.onSuccess("waiting"),
n.stateChangeCallback.play=function(e,o){
0==e&&"function"==typeof t.onSuccess?t.onSuccess("play"):0!=e&&"function"==typeof t.onError&&t.onError({
err_code:2,
err_msg:o||""
});
}):"function"==typeof t.onError&&(e=e||{},e.err_code=1,t.onError(e));
});
}
},e.prototype._jsapi_operateBackgroundAudio=function(t){
var e=this,o=(this._o,e._g),i=1*t.position||0;
w.invoke("operateBackgroundAudio",{
operationType:t.type,
currentTime:i
},function(e){
if(!!b.debug&&console.log("operateBackgroundAudio "+t.type+",position:"+i+", log:"+JSON.stringify(e||{})),
e.err_msg.indexOf("ok")>=0){
var n=t.type;
"seek"==n?(o.stateChangeCallback.seeking=function(e,o){
0==e&&"function"==typeof t.onSuccess?t.onSuccess("seeking"):0!=e&&"function"==typeof t.onError&&t.onError({
err_msg:o||""
});
},o.stateChangeCallback.seeked=function(e,o){
0==e&&"function"==typeof t.onSuccess?t.onSuccess("seeked"):0!=e&&"function"==typeof t.onError&&t.onError({
err_msg:o||""
});
}):o.stateChangeCallback[n]=function(e,o){
0==e&&"function"==typeof t.onSuccess?t.onSuccess():0!=e&&"function"==typeof t.onError&&t.onError({
err_msg:o||""
});
};
}else"function"==typeof t.onError&&t.onError(e);
});
},e.prototype._jsapiPlay=function(){
var t=this,e=this._o;
1==b.surportType?this._jsapi_musicPlay({
onError:function(){
t._h5Play();
}
}):this._jsapi_setBackgroundAudioState({
onSuccess:function(o){
"waiting"===o?(v(e.type,"pv",1),v(e.type,"wx_pv",1),v(e.type,"wx_pv_2",1),t._initJsapiData(),
t._surportType=3,b.surportType=3,t._onLoading()):"play"===o&&(t._initJsapiData(),
t._onPlay(),"undefined"!=typeof e.duration&&1*e.duration>0&&(t._analogUpdateTime(),
t._getMusicPlayerState()));
},
onError:function(o){
o&&1==o.err_code?t._jsapi_musicPlay({
onError:function(){
t._h5Play();
}
}):(t._h5Play(),v(e.type,"wx_err_1",1));
}
});
},e.prototype._getJsapiDownloadSec=function(){
this._getMusicPlayerState();
var t=Math.floor(this._o.duration*this.jsApiData.bufferedPercent/100);
return!!b.debug&&console.log("downloadSec:"+t),t;
},e.prototype._jsapiSeek=function(t){
function e(){
n.seeking=!1,o._onPlay(),n.starTime=+new Date-1e3*a,o._analogUpdateTime(),o._getMusicPlayerState();
}
var o=this,i=this._g,n=this.jsApiData,a=parseInt(t,10);
n.getStatusId&&clearTimeout(n.getStatusId),n.updateTimeoutId&&clearTimeout(n.updateTimeoutId),
n.seekWaitId&&clearTimeout(n.seekWaitId),n.seeking=!0;
var s;
this._jsapi_operateBackgroundAudio({
type:"seek",
position:a,
onError:function(){
!!b.debug&&console.log("seek callback fail"),n.seeking=!1,o._analogUpdateTime(),
o._getMusicPlayerState();
},
onSuccess:function(t){
"seeking"==t?(!!b.debug&&console.log("seeking callback success"),n.seeking=!0,o._onLoading(),
i.stateChangeCallback.play=function(){
!!b.debug&&console.log("seeked to play"),s&&clearTimeout(s),e();
}):"seeked"==t&&(!!b.debug&&console.log("seeked callback success"),(2==o._status||4==o._status)&&(s=setTimeout(function(){
!!b.debug&&console.log("setTimeout to play"),i.stateChangeCallback.play=null,o._resumeJsapiPlay(!0);
},1e3)));
}
}),o._getMusicPlayerState();
},e.prototype._resumeJsapiPlay=function(t,e){
function o(t){
var e=i.jsApiData;
e.starTime+=+new Date-e.pauseTime,e.pauseTime=0,i._onPlay(),i._analogUpdateTime(),
i._getMusicPlayerState(),"function"==typeof t&&t();
}
var i=this;
1==this._surportType?this._jsapiPlay():3==this._surportType&&(t?this._jsapi_operateBackgroundAudio({
type:"play",
onError:function(){
i._stopJsapiPlay(!1,function(){
i.play();
});
},
onSuccess:function(){
o(e);
}
}):o(e));
},e.prototype._pauseJsapiPlay=function(t,e,o){
function i(t){
var e=n.jsApiData;
1==n._status&&(e.pauseTime=+new Date,n._onPause()),n._analogUpdateTime(),n._getMusicPlayerState(),
e&&e.updateTimeoutId&&clearTimeout(e.updateTimeoutId),e.updateTimeoutId=null,t===!0&&e&&e.getStatusId&&clearTimeout(e.getStatusId);
}
var n=this;
return 2==n._status?(i(e),void("function"==typeof o&&o())):void(1==this._surportType?this._stopJsapiPlay(t,o):3==this._surportType&&(t?this._jsapi_operateBackgroundAudio({
type:"pause",
onSuccess:function(){
i(e),"function"==typeof o&&o();
},
onError:function(){
n._stopJsapiPlay(!0,o);
}
}):(i(e),"function"==typeof o&&o())));
},e.prototype._stopJsapiPlay=function(t,e){
function i(t){
n._initJsapiData(),n._onTimeupdate(null,0),n._onUpdateSeekRange(0),n._onEnd(),"function"==typeof t&&t();
}
{
var n=this;
n.jsApiData;
}
t?1==n._surportType?o(function(){
i(e);
}):n._jsapi_operateBackgroundAudio({
type:"stop",
onSuccess:function(){
i(e);
},
onError:function(){
i(e);
}
}):i(e);
},e.prototype._getH5DownloadSec=function(){
var t=Math.floor(this._o.duration*this._getH5DownloadDuration()/100);
return!!b.debug&&console.log("h5 downloadSec:"+t),t;
},e.prototype._getH5DownloadDuration=function(){
if(!this._h5Audio)return 0;
if(this._h5Data.downloadDuration>=100)return 100;
var t=this._h5Audio.buffered,e=t.end(t.length-1);
return this._h5Data.downloadDuration=parseInt(e/this._o.duration*100,10),this._h5Data.downloadDuration;
},e.prototype._h5Play=function(){
0!==b.surportType&&(this._h5Audio?(this._h5Audio.ended||this._h5Audio.paused)&&(v(this._o.type,"pv",1),
v(this._o.type,"h5_pv",1),this._initH5Data(),this._h5Audio.currentTime=0,this._h5Audio.play()):this._createAutoAndPlay());
},e.prototype._h5Resume=function(){
this._h5Audio&&this._h5Audio.play();
},e.prototype._h5Stop=function(){
this._h5Audio&&(this._initH5Data(),this._h5Audio.pause(),this._h5Audio.currentTime=0,
this._onUpdateSeekRange(0),this._onEnd());
},e.prototype._h5Seek=function(t){
if(this._h5Audio){
{
var e=(this._h5Data,parseInt(t,10));
this._getH5DownloadSec();
}
e=Math.min(e,this._o.duration),this._h5Audio.currentTime=e,this._h5Audio.play();
}
},e.prototype.surportSeekRange=function(){
return 1==b._playtype?!1:2==this._surportType||3==this._surportType?!0:!1;
},e.prototype.setSrc=function(t){
-1==t.indexOf("?")&&(t+="?"),t+=p(this._o.mid),this._o.src=t,this._g.mutexKey=this._o.src,
b.mutexPlayers[this._g.mutexKey]?b.mutexPlayers[this._g.mutexKey].push(this):b.mutexPlayers[this._g.mutexKey]=[this];
},e.prototype.getSrc=function(){
return this._o.src||"";
},e.prototype.setDuration=function(t){
this._o.duration=t||0;
},e.prototype.getSurportType=function(){
return this._surportType||0;
},e.prototype.getPlayStatus=function(){
return this._status;
},e.prototype.getCurTime=function(){
return 1!=this._surportType&&3!=this._surportType||!this.jsApiData?this._h5Audio?this._h5Audio.currentTime:0:this.jsApiData.curTime||0;
},e.prototype.getDuration=function(){
return this._o.duration||void 0;
},e.prototype.pause=function(t,e,o){
return o===!0||this._o.allowPause?void(1==this._surportType||3==this._surportType?this._pauseJsapiPlay(t===!1?!1:!0,!1,function(){
"function"==typeof e&&e();
},function(){
"function"==typeof e&&e();
}):2==this._surportType&&this._h5Audio&&"function"==typeof this._h5Audio.pause&&(this._h5Audio.pause(),
"function"==typeof e&&e())):void this.stop(t,e);
},e.prototype.stop=function(t,e){
return 1==this._surportType||3==this._surportType?void this._stopJsapiPlay(t===!1?!1:!0,e):(2==this._surportType&&this._h5Audio&&this._h5Stop(),
void("function"==typeof e&&e()));
},e.prototype.resume=function(t,e,o){
(o===!0||2==this._status&&this._o.allowPause)&&(b.inWechat&&2!=b._playtype?this._resumeJsapiPlay(t===!1?!1:!0):0!=b.surportType&&this._h5Resume());
},e.prototype.onload=function(){
this._onLoading();
},e.prototype.play=function(){
var t=this,e=this._g;
if(t._o.src)return 2==t._status&&t._o.allowPause?void t.resume():(e.playTimeoutId&&clearTimeout(e.playTimeoutId),
e.hasCheckPlay?void(b.inWechat?this._jsapiPlay():0!=b.surportType&&this._h5Play()):void(e.playTimeoutId=setTimeout(function(){
t.play();
},1e3)));
},e.prototype.seek=function(t){
{
var e=this;
this._g;
}
if(1==e._status||2==e._status)return 3==this._surportType?void this._jsapiSeek(t):2==this._surportType&&this._h5Audio?void this._h5Seek(t):void 0;
},e.prototype.monitor=function(t,e){
v(-1,t,e);
},{
init:s,
getSurportType:a
};
});define("pages/loadscript.js",[],function(){
"use strict";
function e(t){
e.counter||(e.counter=1);
var n="number"!=typeof t.retry?1:t.retry,o=document.createElement("script"),r=document.head||document.getElementsByTagName("head")[0]||document.documentElement,a=t.url+"&t="+Math.random(),d=t.callbackName,i="uninitialized",u="undefined"==typeof t.successCode?200:t.successCode,c="undefined"==typeof t.timeoutCode?500:t.timeoutCode,l="undefined"==typeof t.scriptErrorCode?400:t.scriptErrorCode,s=!1,f=null,m=function(e){
o&&!s&&(s=!0,f&&(clearTimeout(f),f=null),o.onload=o.onreadystatechange=o.onerror=null,
r&&o.parentNode&&r.removeChild(o),o=null,d&&-1==d.indexOf(".")&&(window[d]=null),
e!=u&&"loaded"!=i&&"function"==typeof t.onerror&&t.onerror(e));
};
if(d&&"function"==typeof t.callback){
var p=d;
-1==d.indexOf(".")&&(d=window[d]?d+e.counter++:d,window[d]=function(){
i="loaded",t.callback.apply(null,arguments);
}),a=a.replace("="+p,"="+d);
}
o.onload=o.onreadystatechange=function(){
var e=navigator.userAgent.toLowerCase();
(-1!=e.indexOf("opera")||-1==e.indexOf("msie")||/loaded|complete/i.test(this.readyState))&&m("loaded"==i?u:l);
},o.onerror=function(){
return n>0?(t.retry=n-1,f&&(clearTimeout(f),f=null),void e(t)):void m(l);
},t.timeout&&(f=setTimeout(function(){
m(c);
},parseInt(t.timeout,10))),i="loading",o.charset="utf-8",setTimeout(function(){
o.src=a;
try{
r.insertBefore(o,r.lastChild);
}catch(e){}
},0);
}
return e;
});define("appmsg/emotion/dom.js",["biz_common/dom/event.js"],function(t){
"use strict";
function e(t){
if("string"==typeof t){
document.querySelectorAll||!function(){
var t=document.createStyleSheet(),e=function(e,n){
var i,o=document.all,r=o.length,u=[];
for(t.addRule(e,"foo:bar"),i=0;r>i&&!("bar"===o[i].currentStyle.foo&&(u.push(o[i]),
u.length>n));i+=1);
return t.removeRule(0),u;
};
document.querySelectorAll=function(t){
return e(t,1/0);
};
}();
var e=document.querySelectorAll(t);
}else e=[t];
return{
el:e,
on:function(t,e){
return this.each(function(n){
i.on(n,t,e);
}),this;
},
hide:function(){
return this.each(function(t){
t.style.display="none";
}),this;
},
show:function(){
return this.each(function(t){
t.style.display="block";
}),this;
},
each:function(t){
return n(this.el,t),this;
},
width:function(){
return this.el[0].clientWidth;
},
css:function(t){
return this.each(function(e){
for(var n in t)e.style[n]=t[n];
}),this;
},
attr:function(t,e){
var n=this.el[0];
return e?(n.setAttribute(t,e),this):n.getAttribute(t);
},
append:function(t){
return t.el&&(t=t.el[0]),this.el[0].appendChild(t),this;
},
html:function(t){
this.each(function(e){
e.innerHTML=t;
});
}
};
}
function n(t,e){
for(var n=0,i=t.length;i>n;n++)e(t[n],n);
}
var i=t("biz_common/dom/event.js");
return e.el=function(t){
return document.createElement(t);
},e.later=function(t){
setTimeout(t,3);
},e.log=function(){},e.each=n,e;
});define("appmsg/comment_tpl.html.js",[],function(){
return'<#if(window.new_appmsg){#>\n    <div class="discuss_container" id="js_cmt_main" style="display:none">\n        <div class="mod_title_context">\n            <strong class="mod_title">精选留言</strong>\n            <!-- 没有付费才给写留言入口 -->\n            <#if(window._copyright_stat!=1 || window.need_pay!=1){#>\n            <p class="discuss_icon_tips tr" id="js_cmt_addbtn1" style="display:none">\n                <a href="javascript:;" id="js_cmt_write1">写留言</a>\n            </p>\n            <#}#>\n            <p class="tips_global tr title_bottom_tips" id="js_cmt_nofans1" style="display:none;">作者已设置关注后才可以留言</p>\n        </div>\n        <ul class="discuss_list" id="js_cmt_list"></ul>\n    </div>\n\n\n    <!-- 没有付费才给写留言入口 -->\n    <#if(window._copyright_stat!=1 || window.need_pay!=1){#>\n    <div class="mod_title_context">\n        <p class="discuss_icon_tips tc" id="js_cmt_addbtn2" style="display:none">\n            <a href="javascript:;" id="js_cmt_write2">写留言</a>\n        </p>\n    </div>\n    <#}#>\n\n    <div class="tips_global rich_split_tips tc" id="js_cmt_nofans2" style="display:none;">\n        作者已设置关注后才可以留言    </div>\n    <p class="rich_split_tips tc tips_global" id="js_cmt_tips" style="display:none;"></p>\n\n\n    <div class="weui-loadmore" id="js_cmt_loading">\n        <i class="weui-loading"></i>\n        <span class="weui-loadmore__tips">正在加载</span>\n    </div>\n\n    <div class="rich_split_tips tc discuss_end_tips" id="js_cmt_statement" style="display:none">\n        <div class="weui-loadmore weui-loadmore_line weui-loadmore_dot">\n            <span class="weui-loadmore__tips"></span>\n        </div>\n        <!--\n        以上留言由公众号审核产生，        <a href="http://kf.qq.com/touch/sappfaq/150211YfyMVj150313qmMbyi.html?scene_id=kf264">\n            了解留言功能详情        </a>\n        -->\n    </div>\n<#}else{#>\n    <div class="discuss_container" id="js_cmt_main" style="display:none">\n        <div class="rich_tips with_line title_tips discuss_title_line">\n            <span class="tips">精选留言</span>\n        </div>\n        <p class="discuss_icon_tips title_bottom_tips tr" id="js_cmt_addbtn1" style="display:none">\n            <!-- 没有付费才给写留言入口 -->\n            <#if(window._copyright_stat!=1 || window.need_pay!=1){#>\n            <a href="javascript:;" id="js_cmt_write1">写留言<img class="icon_edit" src="<#=window.comment_edit_icon#>" alt=""></a>\n            <#}#>\n        </p>\n        <p class="tips_global tc title_bottom_tips" id="js_cmt_nofans1" style="display:none;">该文章作者已设置需关注才可以留言</p>\n        <ul class="discuss_list" id="js_cmt_list"></ul>\n    </div>\n\n\n    <p class="discuss_icon_tips rich_split_tips tr" id="js_cmt_addbtn2" style="display:none">\n        <!-- 没有付费才给写留言入口 -->\n        <#if(window._copyright_stat!=1 || window.need_pay!=1){#>\n        <a href="javascript:;" id="js_cmt_write2">写留言<img class="icon_edit" src="<#=window.comment_edit_icon#>" alt=""></a>\n        <#}#>\n    </p>\n\n    <div class="tips_global rich_split_tips tc" id="js_cmt_nofans2" style="display:none;">\n        该文章作者已设置需关注才可以留言    </div>\n    <p class="rich_split_tips tc tips_global" id="js_cmt_tips" style="display:none;"></p>\n\n\n    <div class="rich_tips tips_global loading_tips" id="js_cmt_loading">\n        <img src="<#=window.comment_loading_img#>" class="rich_icon icon_loading_white" alt="">\n        <span class="tips">加载中</span>\n    </div>\n\n    <div class="rich_tips with_line tips_global" id="js_cmt_statement" style="display:none">\n        <span class="tips">以上留言由公众号筛选后显示</span>\n    </div>\n\n    <p class="rich_split_tips tc" id="js_cmt_qa" style="display:none;">\n        <a href="http://kf.qq.com/touch/sappfaq/150211YfyMVj150313qmMbyi.html?scene_id=kf264">\n            了解留言功能详情        </a>\n    </p>\n<#}#>\n\n';
});define("biz_wap/utils/fakehash.js",["biz_common/dom/event.js"],function(t){
"use strict";
function s(t){
t=t||location.hash.substr(1);
var s,o,e,i,r=!1,u=[];
for(s=0;s<h.length;s++)o=h[s],e=o[0],i=o[1],e!==n?("string"==typeof e&&e===t||e instanceof RegExp&&e.test(t))&&(i(a),
r=!0):u.push(i);
if(!r)for(s=0;s<u.length;s++)u[s](a,t);
a=t;
}
var o=t("biz_common/dom/event.js"),h=[],n="__default_hash__",a=location.hash.substr(1);
return o.on(window,"popstate",function(t){
var o=n;
t.state&&t.state.hash&&(o=t.state.hash),s(o);
}),o.on(window,"hashchange",s),o.on(window,"load",function(){
history.state&&history.state.hash&&s(history.state.hash);
}),{
val:function(){
return history.state&&history.state.hash||location.hash.substr(1);
},
push:function(t){
history.pushState?(history.pushState({
hash:t
},document.title,location.href),s(t)):location.hash=t;
},
on:function(t,s){
"function"==typeof t&&(s=t,t=n),h.push([t,s]);
}
};
});define("biz_common/utils/wxgspeedsdk.js",[],function(){
"use strict";
function e(e){
if(!e.pid||!e.speeds)return-1;
if(!e.speeds.length>0){
var n=e.speeds;
e.speeds=[],e.speeds.push(n);
}
for(var t=d(e),o=0;o<e.speeds.length;o++){
var r=e.speeds[o];
r.time=parseInt(r.time),r.sid>20&&r.time>=0&&i(t,r.sid,r.time);
}
}
function n(){
s(function(){
setTimeout(function(){
for(var e in p)r({
pid_uin_rid:e,
speeds:p[e]
},c);
p={};
},100);
});
}
function t(e){
s(function(){
if(!e.pid||!e.time)return-1;
var n=d(e);
i(n,9,e.time);
});
}
function o(e){
s(function(){
var n=d(e);
p[n]||(p[n]=[]);
var t=window.performance||window.msPerformance||window.webkitPerformance||{};
if(t&&t.timing){
var o=t.timing||{};
i(n,1,o.domainLookupEnd-o.domainLookupStart),i(n,2,"https:"==location.protocol&&0!=o.secureConnectionStart?o.connectEnd-o.secureConnectionStart:0),
i(n,3,o.connectEnd-o.connectStart),i(n,4,o.responseStart-o.requestStart),i(n,5,o.responseEnd-o.responseStart),
i(n,6,o.domContentLoadedEventStart-o.domLoading),i(n,7,0==o.domComplete?0:o.domComplete-o.domLoading),
i(n,8,0==o.loadEventEnd?0:o.loadEventEnd-o.loadEventStart),function(){
setTimeout(function(){
o.loadEventEnd&&(i(n,7,0==o.domComplete?0:o.domComplete-o.domLoading),i(n,8,0==o.loadEventEnd?0:o.loadEventEnd-o.loadEventStart));
},0);
}(p),p[n][9]||i(n,9,o.domContentLoadedEventStart-o.navigationStart),i(n,10,o.redirectEnd-o.redirectStart),
i(n,11,o.domainLookupStart-o.fetchStart),i(n,12,o.domLoading-o.responseStart);
}
});
}
function i(e,n,t){
p[e]=p[e]||[],p[e][n]=p[e][n]||[],0>t||(21>n?p[e][n][0]=t:p[e][n].push(t));
}
function d(e){
return e&&e.pid?e.pid+"_"+(e.uin||0)+"_"+(e.rid||0):void(console&&console.error("Must provide a pid"));
}
function r(e,n){
var t=e.pid_uin_rid.split("_");
if(3!=t.length)return void(console&&console.error("pid,uin,rid, invalid args"));
for(var o="pid="+t[0]+"&uin="+t[1]+"&rid="+t[2],i=n+o+"&speeds=",d="",r=[],s=1;s<e.speeds.length;s++)if(e.speeds[s]){
for(var a=0;a<e.speeds[s].length;a++){
var p=s+"_"+e.speeds[s][a];
i.length+d.length+p.length<1024?d=d+p+";":(d.length&&r.push(i+d.substring(0,d.length-1)),
d=p+";");
}
s==e.speeds.length-1&&r.push(i+d.substring(0,d.length-1));
}
for(var s=0;s<r.length;s++)(new Image).src=r[s];
}
function s(e){
"complete"==document.readyState?e():u.push(e);
}
function a(){
for(var e=0;e<u.length;e++)u[e]();
u=[];
}
var p={},c="https://badjs.weixinbridge.com/frontend/reportspeed?",u=[];
return window.addEventListener?window.addEventListener("load",a,!1):window.attachEvent&&window.attachEvent("onload",a),
{
saveSpeeds:e,
send:n,
setFirstViewTime:t,
setBasicTime:o
};
});define("a/sponsor.js",["biz_common/dom/event.js","biz_common/utils/report.js","biz_wap/jsapi/core.js","biz_wap/utils/mmversion.js","a/a_report.js","biz_common/utils/url/parse.js","new_video/player.js","biz_wap/utils/ajax.js"],function(e){
"use strict";
function t(e,t){
r("http://mp.weixin.qq.com/mp/ad_report?action=follow&type="+e+t.report_param);
}
function i(){
c({
url:" /mp/ad_video_report?action=video_play_report",
data:window.__video_report_data,
type:"POST",
success:function(){}
});
}
function o(e){
var o=e.adData,r=e.pos_type,_=o.traceid,c=e.a_info.type,u=o.adid,f=o.url,m=e.a_info.rl;
110==o.pt&&(f=f.replace("#","&AdType=80#"));
var w={};
e.report_param=e.report_param||"";
var y=e.adDetailBtn,v=e.adMoreBtn,h=(e.adMessage,e.adAbout),g=e.adImg,b=e.adVideo,j=0,T={
type:c,
report_type:2,
url:encodeURIComponent(f),
tid:_,
rl:encodeURIComponent(m),
__biz:biz,
pos_type:r,
pt:o.pt,
click_pos:""
},W=null,m=o.rl||"",k="";
if(m){
m=m.split("?"),m=m.length>1?m[1]:"";
var x=new RegExp("(^|&)viewid=([^&]*)(&|$)","i"),z=m.match(x);
z&&(k=unescape(z[2]));
}
window.__video_report_data={
aid:o.adid,
traceid:o.traceid,
user_uin:top.window.user_uin,
publisher_appid:o.publisher_appid||0,
appmsg_id:mid,
item_idx:idx,
viewid:k,
__biz:biz,
report_type:0,
play_type:0,
play_duration:0,
video_duration:0,
auto_play:1
};
var H=null,I=!0,O=!1;
if(b){
W=new p({
container:b,
cover:o.thumbUrl,
width:b.offsetWidth,
height:b.offsetWidth*parseInt(o.displayHeight)/parseInt(o.displayWidth),
muted:!0,
ad_muted_btn:!0,
always_hide_loading:!0,
src:o.videoUrl,
autoHide:!0,
blockTouchVideo:!0,
onError:function(i){
console.log("播放出错",i),t(123,e),b.parentNode.innerHTML='<span class="ct_mpda_main_img img_bg_cover" id="js_main_img" style="background-image:url('+o.thumbUrl+"); height:"+l.clientWidth/1.77+'px;"></span>',
window.__video_report_data.play_type=3;
},
onEnd:function(){
t(122,e),window.__video_report_data.play_type=1,window.__video_report_data.play_duration=window.__video_report_data.video_duration,
window.__video_report_data.report_type=2,W.play(),i();
},
onTimeupdate:function(e,t){
window.__video_report_data.play_type=2,window.__video_report_data.play_duration=1e3*t.currentTime,
window.__video_report_data.video_duration=1e3*W.__getDuration();
}
}),j=29,W._showPlayer(),W.setSrc(o.videoUrl,"auto");
var E=window.pageYOffset||document.documentElement.scrollTop||document.body.scrollTop,U=document.documentElement.clientHeight||window.innerHeight;
if(d.isAndroid)if(l.offsetTop>E&&l.offsetTop<E+U)window.__video_report_data.auto_play=0;else{
var M=function(){
W.__beginPlayHandler(),n.off(window,"touchstart",M),O=!0;
};
n.on(window,"touchstart",M);
}
var P=function(){
if(3==window.__video_report_data.play_type)return void n.off(window,"scroll",P);
if(0!=window.__video_report_data.auto_play||0!=window.__video_report_data.play_type)if(E=window.pageYOffset||document.documentElement.scrollTop||document.body.scrollTop,
U=document.documentElement.clientHeight||window.innerHeight,W.isPlay()&&(l.offsetTop>E+U||l.offsetTop+l.offsetHeight<E))W.pause();else if(!W.isPlay()&&!(l.offsetTop>E+U||l.offsetTop+l.offsetHeight<E)){
if(d.isAndroid&&!O)return;
0==window.__video_report_data.play_type&&1==window.__video_report_data.auto_play?(t(121,e),
d.isIOS&&W.triggerMuted(!0),W.__beginPlayHandler()):W.play();
}
};
n.on(window,"scroll",P),P(),H=function(){
window.setTimeout(function(){
W.triggerMuted(!0);
},1e3);
};
}
n.on(window,"touchend",function(e){
e.target!=h&&e.target!=y&&(h.style.display="none");
}),n.on(document.getElementById("js_ad_inner"),"click",function(i){
if(i.target.className.indexOf("js_muted_btn")>-1)"true"==W.video.getAttribute("muted")?(W.triggerMuted(!1),
I=!1):(W.triggerMuted(!0),I=!0),t(124,e);else{
if(W&&(!W.isPlay()||0==window.__video_report_data.play_type))return W.__beginPlayHandler(),
I||W.triggerMuted(!1),t(121,e),void(window.__video_report_data.play_type=2);
"js_main_img"==i.target.id||i.target.className.indexOf("video_mask")>-1?w[_+"_1"]||(w[_+"_1"]=!0,
T.click_pos=1,s(T,function(){
t(87+j,e),w[_+"_1"]=!1,!!H&&H(),d.isWp||d.isIOS?a.invoke("openUrlWithExtraWebview",{
url:f,
openType:1
},function(e){
-1==e.err_msg.indexOf("ok")&&(location.href=f);
}):location.href=f;
})):w[_+"_2"]||(w[_+"_2"]=!0,T.click_pos=2,s(T,function(){
t(88+j,e),w[_+"_2"]=!1,!!H&&H(),d.isWp||d.isIOS?a.invoke("openUrlWithExtraWebview",{
url:f,
openType:1
},function(e){
-1==e.err_msg.indexOf("ok")&&(location.href=f);
}):location.href=f;
}));
}
return!1;
}),n.on(v,"click",function(){
return w[_+"_3"]||(w[_+"_3"]=!0,T.click_pos=3,s(T,function(){
t(89+j,e),w[_+"_3"]=!1,!!H&&H(),d.isWp||d.isIOS?a.invoke("openUrlWithExtraWebview",{
url:f,
openType:1
},function(e){
-1==e.err_msg.indexOf("ok")&&(location.href=f);
}):location.href=f;
})),!1;
}),n.on(y,"click",function(){
return t(90+j,e),h.style.display="none"==window.getComputedStyle(h).display?"initial":"none",
!1;
}),n.on(h,"click",function(){
t(91+j,e);
var i="https://mp.weixin.qq.com/promotion/res/htmledition/mobile/html/trade_about.html?aid="+u+"&tid="+_+"#wechat_redirect";
return!!H&&H(),d.isWp||d.isIOS||d.isAndroid?a.invoke("openUrlWithExtraWebview",{
url:i,
openType:1
},function(e){
-1==e.err_msg.indexOf("ok")&&(location.href=i);
}):location.href=i,!1;
}),n.on(window,"resize",function(){
setTimeout(function(){
var e=l.clientWidth;
if(g)g.style.height=e/1.77+"px";else{
var t=b.offsetWidth,i=b.offsetWidth*parseInt(o.displayHeight)/parseInt(o.displayWidth);
W.setHeight(i),W.setWidth(t),l.style.width=t,l.style.height=i;
}
},0);
});
}
var n=e("biz_common/dom/event.js"),r=e("biz_common/utils/report.js"),a=e("biz_wap/jsapi/core.js"),d=e("biz_wap/utils/mmversion.js"),_=e("a/a_report.js"),p=(e("biz_common/utils/url/parse.js"),
e("new_video/player.js")),s=_.AdClickReport,l=(e("biz_common/utils/url/parse.js"),
document.getElementById("js_sponsor_ad_area")),c=e("biz_wap/utils/ajax.js");
return o;
});define("a/app_card.js",["biz_common/dom/event.js","biz_common/dom/class.js","a/a_report.js","biz_wap/utils/position.js","biz_common/utils/report.js","biz_wap/jsapi/core.js","biz_wap/utils/mmversion.js","a/appdialog_confirm.js","biz_common/utils/url/parse.js"],function(a,t,n,e){
"use strict";
function o(a){
h("http://mp.weixin.qq.com/mp/ad_report?action=follow&type="+a+z.report_param);
}
function d(a,t){
if(z.app_status=a,"downloading"==a){
t=t||0;
var n="";
104==z.data.pt?n='<i class="btn_processor" style="width:'+t+'%;"></i><span class="btn_processor_value">暂停('+t+"%)</span>":113==z.data.pt||114==z.data.pt?z.btn.innerHTML.indexOf("继续")>-1?(n=z.btn.innerHTML,
n=n.replace("继续","暂停")):n='<i class="btn_processor" style="width:'+t+'%;"></i><span class="btn_processor_value">暂停</span>':n='<i class="btn_processor" style="width:'+t+'%;"></i><span class="btn_processor_value">'+t+"%</span>",
z.btn.innerHTML=n,w.addClass(z.btn,"with_processor");
}else if("paused"==a){
var n="";
104==z.data.pt||113==z.data.pt||114==z.data.pt?(n=z.btn.innerHTML,n=n.replace("暂停","继续"),
z.btn.innerHTML=n):(w.removeClass(z.btn,"with_processor"),z.btn.innerHTML=x[a]);
}else w.removeClass(z.btn,"with_processor"),z.btn.innerHTML=x[a];
}
function i(a){
var t=a.js_app_rating,n=1*z.data.app_rating;
n>5&&(n=5),0>n&&(n=0);
var e=["","one","two","three","four","five"],o="",d=Math.floor(n);
if(o="star_"+e[d],n>d&&(n=d+.5,o+="_half"),t&&n>0){
var i=t.getElementsByClassName("js_stars"),l=t.getElementsByClassName("js_scores");
i&&l&&i[0]&&l[0]&&(i=i[0],l=l[0],i.style.display="inline-block",w.addClass(i,o));
}
}
function l(a){
"undefined"!=typeof b&&b.log&&b.log(a);
}
function s(){
b.on("wxdownload:progress_change",function(a){
a.download_id==z.download_id&&d("downloading",a.progress);
});
}
function r(){
z.download_id&&b.invoke("queryDownloadTask",{
download_id:z.download_id
},function(a){
if(l("queryDownloadTask : "+a.state+"; dowloadid = "+z.download_id),a&&a.state){
if("download_succ"==a.state&&(d("downloaded"),window.clearInterval(z.clock)),"downloading"==a.state)return;
("download_fail"==a.state||"default"==a.state)&&(window.clearInterval(z.clock),window.clearInterval(z.install_clock),
e("下载失败"),d("download"));
}
});
}
function p(){
b.invoke("getInstallState",{
packageName:z.data.pkgname,
download_id:z.download_id
},function(a){
var t=a.err_msg;
t.indexOf("get_install_state:yes")>-1&&(l("getInstallState @app, version : "+t),
window.clearInterval(z.install_clock),d(z.url_scheme?"gotodetail":"installed"));
});
}
function c(){
b.invoke("pauseDownloadTask",{
packageName:z.data.pkgname,
download_id:z.download_id
},function(a){
a.err_msg.indexOf("pause_download_task:ok")>-1&&d("paused");
});
}
function _(){
b.invoke("resumeDownloadTask",{
packageName:z.data.pkgname,
download_id:z.download_id
},function(a){
a.err_msg.indexOf("ok")>-1&&d("downloading");
});
}
function m(){
if(104==z.data.pt||113==z.data.pt||114==z.data.pt&&z.url_scheme)j.gtVersion("6.5.6",!0)?b.invoke("launchApplication",{
schemeUrl:z.url_scheme
},function(a){
-1==a.err_msg.indexOf("ok")&&(location.href=z.url_scheme);
}):location.href=z.url_scheme;else{
var t=z.data.url,n=a("biz_common/utils/url/parse.js");
(!t||0!=t.indexOf("http://mp.weixin.qq.com/tp/")&&0!=t.indexOf("https://mp.weixin.qq.com/tp/"))&&(t="http://mp.weixin.qq.com/mp/ad_app_info?t=ad/app_detail&app_id="+z.data.app_id+(z.appdetail_params||"")+"&channel_id="+z.channelid+"&md5sum="+z.data.md5sum+"#wechat_redirect"),
z.url_scheme&&(t=n.join(t,{
is_installed:"1"
})),location.href=t;
}
}
function u(a){
if(z.btn=a.btn,!z.btn)return!1;
z.data=a.adData,z.url_scheme=a.url_scheme,z.appdetail_params=a.appdetail_params||"";
var t={};
z.channelid=z.data.channel_id||"",z.report_param=a.report_param;
var n=20;
if(("103"==z.data.pt||"104"==z.data.pt)&&i(a),"104"==z.data.pt||"113"==z.data.pt||"114"==z.data.pt){
var u=z.data.androiddownurl;
if(u&&u.match){
var w=/&channelid\=([^&]*)/,g=u.match(w);
g&&g[1]&&(z.channelid=g[1],z.data.androiddownurl=u.replace(w,""));
}
z.channelid&&(z.channelid="&channelid="+z.channelid),a.via&&(z.via=["&via=ANDROIDWX.YYB.WX.ADVERTISE",a.via].join("."));
}
b.ready(function(){
("113"==z.data.pt||"114"==z.data.pt||"104"==z.data.pt)&&(b.invoke("getInstallState",{
packageName:O
},function(a){
var t=a.err_msg;
l("getInstallState @yingyongbao : "+t);
var n=t.lastIndexOf("_")+1,e=t.substring(n);
1*e>=T&&t.indexOf("get_install_state:yes")>-1&&(I=!0);
}),b.invoke("getInstallState",{
packageName:z.data.pkgname
},function(a){
var t=a.err_msg;
l("getInstallState @"+z.data.pkgname+" : "+t);
var n=t.lastIndexOf("_")+1,e=t.substring(n);
1*e>=z.data.versioncode&&t.indexOf("get_install_state:yes")>-1&&d(z.url_scheme?"gotodetail":"installed");
})),f.on(z.btn,"click",function(i){
if("installed"==z.app_status)return d("installed"),!1;
if("gotodetail"==z.app_status)return o(74),m(),!1;
if("downloading"==z.app_status)return o(71),c(),!1;
if("paused"==z.app_status)return o(72),_(),!1;
if("downloaded"==z.app_status)return o(73),b.invoke("installDownloadTask",{
download_id:z.download_id,
file_md5:z.data.md5sum
},function(a){
var t=a.err_msg;
l("installDownloadTask : "+t),t.indexOf("install_download_task:ok")>-1?z.install_clock=setInterval(p,1e3):e("安装失败！");
}),!1;
var u=function(){
if("103"==z.data.pt||"111"==z.data.pt||"112"==z.data.pt){
o(23);
var t="http://"+location.host+"/mp/ad_redirect?url="+encodeURIComponent(z.data.appinfo_url)+"&ticket="+(z.data.ticket||window.ticket)+"#wechat_redirect";
z.url_scheme&&0==z.url_scheme.indexOf("http")||b.invoke("downloadAppInternal",{
appUrl:z.data.appinfo_url
},function(a){
a.err_msg&&-1!=a.err_msg.indexOf("ok")||(location.href=t);
});
}else{
if(I)return o(16),void(location.href="tmast://download?oplist=1,2&pname="+z.data.pkgname+z.channelid+z.via);
o(15);
var i=[z.data.adid,z.data.traceid,(z.data.pkgname||"").replace(/\./g,"_"),z.data.source,n,a.engine].join("."),c=function(a,t,n){
b.invoke("addDownloadTaskStraight",{
task_name:a.data.appname,
task_url:a.data.androiddownurl,
extInfo:t,
file_md5:a.data.md5sum
},function(e){
var o=e.err_msg;
o.indexOf("ok")>-1?n&&n(e):b.invoke("addDownloadTask",{
task_name:a.data.appname,
task_url:a.data.androiddownurl,
extInfo:t,
file_md5:a.data.md5sum
},n);
});
};
c(z,i,function(a){
var t=a.err_msg;
l("addDownloadTask : "+t),t.indexOf("ok")>-1?(z.download_id=a.download_id,l("download_id : "+z.download_id),
d("downloading"),z.clock=setInterval(r,1e3),z.install_clock=setInterval(p,1e3),s()):e("调用下载器失败！");
});
}
},f=function(){
return j.isIOS?void u():void y({
app_name:z.data.appname,
app_img_url:z.data.icon_url,
onOk:function(){
u(),o(I?106:100);
},
onCancel:function(){
o(I?107:101);
}
});
};
return j.isIOS&&z.url_scheme&&0==z.url_scheme.indexOf("http")&&(location.href=z.url_scheme),
window.setTimeout(function(){
if("download"==z.app_status&&z.data.rl&&z.data.traceid){
if(!t[z.data.traceid]){
t[z.data.traceid]=!0;
var n,e,o,d,l=!!i&&i.target;
l&&(n=v.getX(l,"js_ad_link")+i.offsetX,e=v.getY(l,"js_ad_link")+i.offsetY,o=document.getElementsByClassName("js_ad_link")[0]&&document.getElementsByClassName("js_ad_link")[0].clientWidth,
d=document.getElementsByClassName("js_ad_link")[0]&&document.getElementsByClassName("js_ad_link")[0].clientHeight),
k({
type:z.data.type,
report_type:2,
click_pos:0,
url:encodeURIComponent(z.data.androiddownurl),
tid:z.data.traceid,
rl:encodeURIComponent(z.data.rl),
__biz:biz,
pos_type:a.pos_type||0,
pt:z.data.pt,
pos_x:n,
pos_y:e,
ad_w:o||0,
ad_h:d||0
},function(){
t[z.data.traceid]=!1,f();
});
}
}else f();
},0),!1;
});
});
}
var f=a("biz_common/dom/event.js"),w=a("biz_common/dom/class.js"),g=a("a/a_report.js"),k=g.AdClickReport,v=a("biz_wap/utils/position.js"),h=a("biz_common/utils/report.js"),b=a("biz_wap/jsapi/core.js"),j=a("biz_wap/utils/mmversion.js"),y=a("a/appdialog_confirm.js"),x={
download:"下载",
downloading:"下载中",
paused:"继续",
downloaded:"安装",
gotodetail:"进入",
installed:"已安装"
},I=!1,O="com.tencent.android.qqdownloader",T=1060125,z={
app_status:"download",
btn:null,
download_id:0,
clock:null,
install_clock:null,
data:{},
channelid:"",
via:"",
report_param:"",
appdetail_params:""
};
return u;
});define("a/ios.js",["biz_common/dom/event.js","biz_common/utils/report.js","biz_wap/utils/ajax.js","biz_wap/jsapi/core.js"],function(t){
"use strict";
function e(t){
"undefined"!=typeof WeixinJSBridge&&WeixinJSBridge.log&&WeixinJSBridge.log(t);
}
function o(t,e){
n("http://mp.weixin.qq.com/mp/ad_report?action=follow&type="+t+e.report_param);
}
function i(t){
var i=t.btn;
if(!i)return!1;
var n=t.adData,p=!1,c={};
t.report_param=t.report_param||"";
var d="http://"+location.host+"/mp/ad_redirect?url="+encodeURIComponent(n.appinfo_url)+"&ticket="+(t.ticket||window.ticket)+"#wechat_redirect";
r.on(i,"click",function(){
if(e("click @js_app_action"),p)return e("is_app_installed"),o(n.is_appmsg?17:13,t),
void(location.href=n.app_id+"://");
var i=function(){
e("download"),o(n.is_appmsg?15:11,t),e("go : "+d),location.href=d;
};
return e("download"),n.rl&&n.traceid?c[n.traceid]||(c[n.traceid]=!0,a({
url:"/mp/advertisement_report?report_type=2&type="+n.type+"&url="+encodeURIComponent(n.appinfo_url)+"&tid="+n.traceid+"&rl="+encodeURIComponent(n.rl)+"&pt="+n.pt+t.report_param,
type:"GET",
timeout:1e3,
complete:function(){
e("ready to download"),c[n.traceid]=!1,i();
},
async:!0
})):i(),!1;
});
}
{
var r=t("biz_common/dom/event.js"),n=t("biz_common/utils/report.js"),a=t("biz_wap/utils/ajax.js");
t("biz_wap/jsapi/core.js");
}
return i;
});define("a/android.js",["biz_common/dom/event.js","biz_common/utils/report.js","biz_wap/utils/ajax.js","biz_wap/jsapi/core.js"],function(n,a,e,t){
"use strict";
function o(n){
"undefined"!=typeof s&&s.log&&s.log(n);
}
function i(n,a){
r("http://mp.weixin.qq.com/mp/ad_report?action=follow&type="+n+a.report_param);
}
function d(n){
function a(){
s.invoke("getInstallState",{
packageName:c.pkgname
},function(n){
var a=n.err_msg;
a.indexOf("get_install_state:yes")>-1&&(window.clearInterval(T),k=!0,d.innerHTML=x.installed);
});
}
function e(){
b&&s.invoke("queryDownloadTask",{
download_id:b
},function(a){
if(a&&a.state){
if("download_succ"==a.state){
o("download_succ"),i(c.is_appmsg?18:14,n),window.clearInterval(y),I=!1,j=!0,d.innerHTML=x.downloaded;
var e=document.createEvent("MouseEvents");
e.initMouseEvent("click",!0,!0,window,0,0,0,0,0,!1,!1,!1,!1,0,null),d.dispatchEvent(e);
}
if("downloading"==a.state)return;
("download_fail"==a.state||"default"==a.state)&&(o("fail, download_state : "+a.state),
window.clearInterval(y),I=!1,t("下载失败"),d.innerHTML=x.download);
}
});
}
var d=n.btn;
if(!d)return!1;
var r={},c=n.adData,u="",m="",_=c.androiddownurl;
if(_&&_.match){
var p=/&channelid\=([^&]*)/,f=_.match(p);
f&&f[1]&&(u="&channelid="+f[1],c.androiddownurl=_.replace(p,""));
}
n.via&&(m=["&via=ANDROIDWX.YYB.WX.ADVERTISE",n.via].join("."));
var w=!1,v="com.tencent.android.qqdownloader",g=1060125,k=!1,I=!1,j=!1,b=0,y=null,T=null,x={
download:"下载",
downloading:"下载中",
downloaded:"安装",
installed:"已安装"
};
d.innerHTML=x.download,s.ready(function(){
s.invoke("getInstallState",{
packageName:v
},function(n){
var a=n.err_msg;
o("getInstallState @yingyongbao : "+a);
var e=a.lastIndexOf("_")+1,t=a.substring(e);
1*t>=g&&a.indexOf("get_install_state:yes")>-1&&(w=!0);
}),s.invoke("getInstallState",{
packageName:c.pkgname
},function(n){
var a=n.err_msg;
o("getInstallState @"+c.pkgname+" : "+a);
var e=a.lastIndexOf("_")+1,t=a.substring(e);
1*t>=c.versioncode&&a.indexOf("get_install_state:yes")>-1&&(k=!0,d.innerHTML=x.installed);
}),d.addEventListener("click",function(){
if(o("click @js_app_action"),!I){
if(k)return!1;
if(j)return s.invoke("installDownloadTask",{
download_id:b,
file_md5:c.md5sum
},function(n){
var e=n.err_msg;
o("installDownloadTask : "+e),e.indexOf("install_download_task:ok")>-1?T=setInterval(a,1e3):t("安装失败！");
}),!1;
var _=function(){
return w?(i(c.is_appmsg?16:12,n),void(location.href="tmast://download?oplist=1,2&pname="+c.pkgname+u+m)):void s.invoke("addDownloadTask",{
task_name:c.appname,
task_url:c.androiddownurl,
extInfo:n.task_ext_info,
file_md5:c.md5sum
},function(a){
var r=a.err_msg;
o("addDownloadTask : "+r),r.indexOf("add_download_task:ok")>-1?(i(c.is_appmsg?15:11,n),
I=!0,b=a.download_id,o("download_id : "+b),d.innerHTML=x.downloading,y=setInterval(e,1e3)):t("调用下载器失败！");
});
};
return c.rl&&c.traceid?r[c.traceid]||(r[c.traceid]=!0,l({
url:"/mp/advertisement_report?report_type=2&type="+c.type+"&url="+encodeURIComponent(c.androiddownurl)+"&tid="+c.traceid+"&rl="+encodeURIComponent(c.rl)+"&__biz="+biz+"&pt="+c.pt+"&r="+Math.random(),
type:"GET",
timeout:1e3,
complete:function(){
r[c.traceid]=!1,_();
},
async:!0
})):_(),!1;
}
});
});
}
var r=(n("biz_common/dom/event.js"),n("biz_common/utils/report.js")),l=n("biz_wap/utils/ajax.js"),s=n("biz_wap/jsapi/core.js");
return d;
});define("a/profile.js",["biz_common/dom/event.js","biz_common/utils/report.js","a/a_report.js","biz_wap/utils/ajax.js","biz_common/utils/url/parse.js","biz_wap/utils/position.js","biz_wap/jsapi/core.js"],function(t){
"use strict";
function e(t,e){
a("http://mp.weixin.qq.com/mp/ad_report?action=follow&type="+t+e.report_param);
}
function n(t){
console.log(t),location.href=t;
}
function i(t){
var i=t.adData,s=t.pos_type||0,l={};
t.report_param=t.report_param||"",function(){
function r(t){
{
var e=_.dataset;
"https:"==top.location.protocol?1500:1200;
}
if(e.rl&&e.url&&e.type&&e.tid){
var n=e.tid,o=e.type,a=e.url,r=e.rl;
if(!l[n]){
l[n]=!0;
var d,m,u,j,b=!!t&&t.target;
b&&(d=c.getX(b,"js_ad_link")+t.offsetX,m=c.getY(b,"js_ad_link")+t.offsetY,u=document.getElementsByClassName("js_ad_link")[0]&&document.getElementsByClassName("js_ad_link")[0].clientWidth,
j=document.getElementsByClassName("js_ad_link")[0]&&document.getElementsByClassName("js_ad_link")[0].clientHeight),
p({
type:o,
report_type:2,
click_pos:0,
url:encodeURIComponent(a),
tid:n,
rl:encodeURIComponent(r),
__biz:biz,
pos_type:s,
pt:i.pt,
pos_x:d,
pos_y:m,
ad_w:u||0,
ad_h:j||0
},function(){
l[n]=!1,f();
});
}
}else f();
}
var _=t.btnAddContact,m=t.btnViewProfile;
if(_&&_.dataset){
var u=function(o,s){
var p=o.err_msg,r=i.is_appmsg?6:1;
-1!=p.indexOf("ok")?(m.style.display="inline-block",_.style.display="none",r=i.is_appmsg?9:4):"add_contact:added"==p?r=i.is_appmsg?7:2:"add_contact:cancel"==p?r=i.is_appmsg?8:3:(--s,
s>=0?d.invoke("addContact",{
scene:scene,
webtype:"1",
username:i.usename
},function(t){
u(t,s);
}):(p="addContact:fail|msg:"+p+"|uin:"+uin+"|biz:"+biz,a("http://mp.weixin.qq.com/mp/jsreport?key=13&content="+p+"&r="+Math.random()),
n(i.url))),e(r,t);
},f=function(){
e(i.is_appmsg?10:5,t),d.invoke("addContact",{
scene:scene,
webtype:"1",
username:i.usename
},function(t){
u(t,1);
});
};
o.on(_,"click",r);
}
}(),function(){
var e=t.btnViewProfile;
e&&o.on(e,"click",function(){
var e=t.btnAddContact.dataset,o={
source:4,
tid:e.tid,
idx:idx,
mid:mid,
appuin:biz,
pt:i.pt,
aid:t.aid,
ad_engine:t.ad_engine,
pos_type:s
},a=r.join(i.url,o);
return n(a),!1;
});
}();
}
{
var o=t("biz_common/dom/event.js"),a=t("biz_common/utils/report.js"),s=t("a/a_report.js"),p=s.AdClickReport,r=(t("biz_wap/utils/ajax.js"),
t("biz_common/utils/url/parse.js")),c=t("biz_wap/utils/position.js"),d=t("biz_wap/jsapi/core.js");
"https:"==top.location.protocol?5:0,window.__report;
}
return i;
});define("a/cpc_a_tpl.html.js",[],function(){
return'<div id="js_cpc_area"  class="js_ad_link appmsg_card_context appmsg_card_active mpda_cpc_context pages_reset" data-type="<#=type#>" data-ticket="<#=ticket#>" data-url="<#=url#>" data-rl="<#=rl#>"  data-aid="<#=aid#>" data-pt="<#=pt#>" data-tid="<#=traceid#>" data-gid="<#=group_id#>" data-apurl="<#=apurl#>" data-is_cpm="<#=is_cpm#>">\n    <div class="appmsg_card_bd mpda_cpc_bd" style="background-image:url(<#=image_url#>)"></div>\n    <div class="appmsg_card_ft mpda_cpc_ft">\n        <span class="dropdown_opr_tips">\n            广告\n            <span class="dropdown_opr_popover">xxxxx</span>\n        </span>\n        <a href="javascript:void(0);" class="link_tips">\n            <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAAoCAMAAAC7IEhfAAAAh1BMVEUAAAD19fX19fX////09PT09PT09PT09PT19fX09PT29vb29vb4+Pj////19fX09PT19fX09PR1htvJz+t6i9zS1+6wuefs7fLn6fKSn+GFlN5/j93w8fTZ3O+8xOmMmuCiruScqOOYpOLGzOvByOqrteamseWAkN7g4/De4e/N0uzM0uyAkN1rIPf0AAAAEXRSTlMAf/ML6NnTv6qlclIjFoLyg7LPVaEAAAFSSURBVDjLlZXZcoMwDEWNgRAIkPgGCEuWZu/2/99XlxYjUBgP9wUjnUGWLAsxVByFgS+lH4RRLCaVpAtFtEiTl5jrSDWSdFzOrTz1Qt5qzDlqQs4w7FJNaknDU46TLK41+kpZ9J+R69lAzyWB7cETyR35uc6qYtdXPtHghnMFWj1zY0k1uGDcUUN11QBNac5diJhx+wbZp37cgYcxxiJi4AEo2kWNkzFGImTgFti2iwsyYwxFMAm+Z+SLgfCH++vBWwbcjMMXku7ugqoDHwDeSA+Ldf9y1b5TB+rUi33vWwufZotL2YEf11IR+SSZM3A0yYwVkPI0eoOTYEgK/o2qO8GcgRE5wvMfsKuBkoExaYr8tyDH4knLQppCpOPuwmnHwHTYuF+1xrI752QyvgplftAYkzPjcs25rvYBMHOk2IfUrLFnH6QzRjNXsrEPe/vv4weFgFW8AqzRsgAAAABJRU5ErkJggg==" alt="">\n            去逛逛\n        </a>\n    </div>\n</div>\n';
});define("a/sponsor_a_tpl.html.js",[],function(){
return'<div class="ct_mpda_area <#if(window.new_appmsg){#>appmsg_card_context<# } #>" id="js_ad_area">\n    <div class="ct_mpda_placeholder">\n        <p class="ct_mpda_tips">广告，也可以是生活的一部分</p>\n    </div>\n    <div class="ct_mpda_inner js_ad_link" id="js_ad_inner" data-type="<#=type#>" data-ticket="<#=ticket#>" data-url="<#=url#>" data-rl="<#=rl#>" data-aid="<#=aid#>" data-pt="<#=pt#>" data-tid="<#=traceid#>" data-gid="<#=group_id#>" data-apurl="<#=apurl#>" data-is_cpm="<#=is_cpm#>">\n        <div class="ct_mpda_hd">\n            <# if(pt==108 || pt==109 || pt==110){ #>\n            <span class="ct_mpda_main_img img_bg_cover" id="js_main_img" style="background-image:url(<#=image_url#>)"></span>\n            <# }else if(pt==116 || pt==117){ #>\n            <div id="js_video_container"></div>\n            <# } #>\n        </div>\n        <div class="ct_mpda_bd" id="js_ad_message">\n            <span class="ct_mpda_logo img_bg_cover" style="background-image:url(<#=biz_info.head_img#>)"></span>\n            <div class="ct_mpda_desc_box">\n                <p class="ct_mpda_title"><#=biz_info.nick_name#></p>\n                <p class="ct_mpda_details" id="js_ad_detail">提供的广告</p>\n            </div>\n            <# if(pt== 108||pt==116){ #>\n            <a class="ct_mpda_btn_more" id="js_ad_more">查看详情</a>\n            <# }else if(pt==109){ #>\n            <a class="ct_mpda_btn_more" id="js_ad_more">下载应用</a>\n            <# }else if(pt==110||pt==117){ #>\n            <a class="ct_mpda_btn_more" id="js_ad_more">了解公众号</a>\n            <# } #>\n            <a class="ct_mpda_btn_about" id="js_btn_about">关于广告</a>\n        </div>\n    </div>\n</div>\n';
});define("a/a_tpl.html.js",[],function(){
return'<div class="rich_media_extra" id="gdt_area">\n    <# if(pos_type==0){ #>\n        <#if(window.new_appmsg){#>\n        <div class="mod_title_context">\n            <strong class="mod_title">广告</strong>\n        </div>\n        <#}else{#>\n        <div class="rich_tips with_line title_tips">\n            <span class="tips">广告</span>\n        </div>\n        <# } #>\n    <# } #>\n    <div class="js_ad_link extra_link <# if(pt==107){ #>preview_img_primary<# } #>" data-type="<#=type#>" data-ticket="<#=ticket#>" data-url="<#=url#>" data-rl="<#=rl#>"  data-aid="<#=aid#>" data-pt="<#=pt#>" data-tid="<#=traceid#>" data-gid="<#=group_id#>" data-apurl="<#=apurl#>" data-is_cpm="<#=is_cpm#>">\n        <# if(pt==1){ #>\n        <#=hint_txt#>\n        <img class="icon_arrow_gray" src="<%@GetResFullName($images_path$icon/common/icon_arrow_gray.png)%>">\n        <img class="icon_loading_white icon_after" style="display:none;" id="loading_<#=traceid#>" src="<%@GetResFullName($images_path$icon/common/icon_loading_white.gif)%>">\n        <# }else if(pt==2||pt==107){ #>\n        <!--第三方logo-->\n        <# if (logo.indexOf("http://mmsns.qpic.cn/") == 0){ #>\n        <div class="brand_logo"><img data-src="<#=logo#>" alt="logo图片" class="js_alazy_img"></div>\n        <# } #>\n        <img class="appmsg_banner js_alazy_img" data-src="<#=image_url#>">\n        <# if(watermark_type!=0){ #><i class="promotion_tag" id="js_promotion_tag"><# if(watermark_type==1){ #>商品推广<# }else if (watermark_type==2){ #>活动推广<# }else if (watermark_type==3){ #>\n            应用下载\n        <# } #>\n            </i>\n        <# } #>\n        <# }else if(pt==7){ #>\n        <!-- 图文 -->\n        <div class="preview_group preview_card">\n            <div class="preview_group_inner card_inner">\n                <div class="preview_group_info">\n                    <strong class="preview_group_title2"><#=hint_txt#></strong>\n                    <div class="preview_group_desc"><#=ad_desc#></div>\n                    <img data-src="<#=image_url#>" alt="" class="preview_card_avatar js_alazy_img">\n                </div>\n                <i class="promotion_tag">活动推广</i>\n            </div>\n        </div>\n        <# }else if(pt==115){ #>\n        <div class="preview_group mod_follow_with_img">\n            <div class="wx_flex_layout">\n                <div class="wx_flex_bd">\n                    <img class="fwi_thumb js_alazy_img" data-src="<#=image_url#>" alt="">\n                </div>\n                <div class="wx_flex_ft">\n                    <span class="radius_avatar"><img data-src="<#=biz_info.head_img#>" alt="" class="js_alazy_img"></span>\n                    <strong class="fwi_nickname"><#=biz_info.nick_name#></strong>\n                    <a id="js_view_profile_<#=pos_type#>" <# if(biz_info.is_subscribed == 0){ #>style="display:none"<# } #> class="wx_min_plain_btn primary js_ad_btn">查看</a>\n                    <a id="js_add_contact_<#=pos_type#>" data-url="<#=url#>" data-type="<#=type#>" data-tid="<#=traceid#>" data-rl="<#=rl#>" <# if(biz_info.is_subscribed ==1){ #>style="display:none"<# } #> class="wx_min_plain_btn primary js_ad_btn">关注</a>\n                </div>\n            </div>\n        </div>\n        <# }else if(pt==100){ #>\n        <div class="preview_group follow <# if(!!biz_info.show_comm_attention_num){ #>with_tips<# } #>">\n            <div class="preview_group_inner">\n                <div class="preview_group_info append_btn">\n                    <strong class="preview_group_title"><#=biz_info.nick_name#></strong>\n                    <div class="preview_group_desc"><#=hint_txt#></div>\n                    <# if(!!biz_info.show_comm_attention_num){ #>\n                    <div class="preview_group_desc weak_tips">有<#=biz_info.comm_attention_num#>个好友关注</div>\n                    <# } #>\n                    <# if(!!biz_info.head_img){ #>\n                    <img data-src="<#=biz_info.head_img#>" alt="" class="preview_group_avatar br_radius js_alazy_img" >\n                    <# }else{ #>\n                    <img class="preview_group_avatar br_radius" src="http://mmbiz.qpic.cn/mmbiz/a5icZrUmbV8p5jb6RZ8aYfjfS2AVle8URwBt8QIu6XbGewB9wiaWYWkPwq4R7pfdsFibuLkic16UcxDSNYtB8HnC1Q/0" alt="<#=biz_info.nick_name#>" >\n                    <# } #>                                 \n                </div>\n                <div class="preview_group_opr">\n                    <a id="js_view_profile_<#=pos_type#>" <# if(biz_info.is_subscribed == 0){ #>style="display:none"<# } #> class="btn btn_inline btn_primary btn_line js_ad_btn">查看</a>\n                    <a id="js_add_contact_<#=pos_type#>" data-url="<#=url#>" data-type="<#=type#>" data-tid="<#=traceid#>" data-rl="<#=rl#>" <# if(biz_info.is_subscribed ==1){ #>style="display:none"<# } #> class="btn btn_inline btn_line  btn_primary js_ad_btn">关注</a>\n                </div>\n            </div>\n        </div>\n        <# }else if(pt==102){ #>\n        <div class="preview_group">\n            <div class="preview_group_inner">\n                <div class="preview_group_info append_btn">\n                    <strong class="preview_group_title"><#=app_info.app_name#></strong>\n                    <div class="preview_group_desc"><#=hint_txt#></div>\n                    <img data-src="<#=app_info.icon_url#>" alt="" class="preview_group_avatar br_radius js_alazy_img">\n                </div>\n                <div class="preview_group_opr">\n                    <a id="js_app_action_<#=pos_type#>" class="btn btn_inline btn_primary js_ad_btn btn_download">下载</a>\n                </div>\n            </div>\n        </div>\n        <# }else if(pt==101){ #>\n        <div class="preview_group preview_card">\n            <div class="preview_group_inner card_inner">                            \n                <div class="preview_group_info append_btn">\n                    <strong class="preview_group_title"><#=app_info.app_name#></strong>\n                    <div class="preview_group_desc"><#=hint_txt#></div>\n                    <img data-src="<#=app_info.icon_url#>" alt="" class="preview_card_avatar js_alazy_img">                               \n                </div>\n                <div class="preview_group_opr">\n                    <a id="js_app_action_<#=pos_type#>" class="btn btn_inline btn_primary js_ad_btn">下载</a>\n                </div>\n            </div>                        \n        </div>\n        <# }else if(pt==103||pt==104){ #>\n        <div class="preview_group obvious_app">\n            <div class="preview_group_inner">\n                <div class="pic_app">\n                    <img data-src="<#=image_url#>" alt="" class="js_alazy_img">\n                </div>\n                <div class="info_app">\n                    <p class="name_app"><#=app_info.app_name#></p>\n                    <# if(pt==103){ #>\n                    <p class="profile_app" style="display:none;"><span class="fun_exp"><#=app_info._category#></span><em>|</em><span class="compacity"><#=app_info._app_size#></span></p>\n                    <# } else if(pt==104){ #>\n                    <p class="profile_app" style="display:none;"><span class="fun_exp"><#=app_info._app_size#></span><em>|</em><span class="compacity"><#=app_info._down_count#></span></p>\n                    <# } #>\n                    <!--星级评分-->\n                    <p class="grade_app" id="js_app_rating_<#=pos_type#>">\n                        <!--\n                            半星：star_half\n                            一星：star_one\n                            一星半：star_one_half\n                            二星：star_two\n                            三星：star_three\n                            四星：star_four\n                            五星：star_five\n                        -->\n                        <span class="js_stars stars" style="display:none;"></span>\n                        <!--暂无评分\n                        <span class="scores">3.5</span>\n                        -->\n                        <span class="js_scores scores"></span>\n                    </p>\n                    <div class="dm_app">\n                        <a id="js_appdetail_action_<#=pos_type#>" class="ad_btn btn_download js_ad_btn">下载</a>\n                        <p class="extra_info">来自<# if(pt==103){ #>App Store<# }else{ #>腾讯应用宝<# } #></p>\n                    </div>\n                </div>\n            </div>            \n        </div>\n        <# }else if(pt==105){ #>\n        <div class="mpda_card cardticket">\n            <div class="cardticket_hd cell">\n                <div class="cell_hd">\n                    <span class="radius_avatar">\n                        <img class="avatar js_alazy_img" data-src="<#=card_info.card_logo_url#>" >\n                    </span>\n                </div>\n                <div class="cell_bd cell_primary"><#=card_info.card_title#></div>\n                <div class="cell_ft">\n                    <a class="btn btn_plain_primary btn_inline js_ad_btn" id="js_card_action_<#=pos_type#>">领券</a>\n                </div>\n            </div>\n            <div class="cardticket_ft">\n                <div class="cardticket_theme"></div>\n                <p class="cardticket_source tips_global"><#=card_info.card_brand_name#></p>\n            </div>\n        </div>\n        <# }else if(pt==106){ #>\n        <!-- 小店广告 -->\n        <div class="preview_group preview_card preview_shop_card">\n            <div class="preview_group_inner shop_card_inner">\n                <div class="preview_group_info">\n                    <strong class="preview_shop_card_title"><#=mp_shop_info.name#></strong>\n                    <div class="preview_shop_card_desc">\n                        <span class="preview_card_desc_meta btn_plain_primary preview_shop_card_btn_buy js_ad_btn" id="js_shop_action_<#=pos_type#>">购买</span>\n                        <span class="preview_card_desc_meta preview_shop_card_oldprice">&yen;<#=mp_shop_info.ori_price/100#></span>\n                        <span class="preview_card_desc_meta preview_shop_card_price">&yen;<#=mp_shop_info.cur_price/100#></span>\n                    </div>\n                    <img data-src="<#=mp_shop_info.img#>" alt="" class="preview_card_avatar js_alazy_img">\n                </div>\n            </div>\n        </div>\n        <# }else if(pt==111||pt==113||pt==112||pt==114){ #>\n        <!-- 背景高斯模糊带描述文字、带背景图的app下载 -->\n        <div class="preview_group download_app_with_desc js_download_app_card">\n            <div class="preview_group_inner" style="background-image:url(<#=image_url#>)">\n                <div class="preview_group_hd">\n                    <div class="preview_group_hd_inner">\n                        <img data-src="<#=app_info.icon_url#>" alt="" class="preview_card_avatar js_alazy_img">\n                        <strong class="preview_group_title"><#=app_info.app_name#></strong>\n                        <a id="js_appdetail_action_<#=pos_type#>" class="preview_group_btn js_ad_btn">下载</a>\n                        <!-- <a id="js_app_action_<#=pos_type#>" class="preview_group_btn">继续</a>\n                        <a id="js_app_action_<#=pos_type#>" class="preview_group_btn">打开</a> -->\n                        <!-- <a id="js_app_action_<#=pos_type#>" class="preview_group_btn with_processor"><i class="btn_processor" style="width:35%;"></i><span class="btn_processor_value">35%</span></a> -->\n                    </div>\n                </div>\n                <# if(pt==111||pt==113){ #>\n                <div class="preview_group_bd">\n                    <div class="preview_group_desc"><#=hint_txt.split(\'|\')[0]#></div>\n                    <div class="preview_group_desc"><#=hint_txt.split(\'|\')[1] || ""#></div>\n                </div>\n                <div class="preview_group_ft"><div class="preview_group_download_info"><span class="download_size" ><#=app_info.app_size#></span>&nbsp;来自<# if(pt==111){ #>App Store<# }else{ #>腾讯应用宝<# } #></div></div>\n                <# } #>\n            </div>            \n        </div>\n        <# } #>\n    </div>\n</div>\n';
});