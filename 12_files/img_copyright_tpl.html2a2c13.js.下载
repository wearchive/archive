define("pages/weapp_tpl.html.js",[],function(){
return'<!-- <span class="weapp_card flex_context">\n    <span class="weapp_card_hd">\n        <span class="radius_avatar weapp_card_avatar">\n            <img src="<#=avatar#>">\n        </span>\n    </span>\n    <span class="weapp_card_bd flex_bd">\n        <strong class="weapp_card_nickname"><#=nickname#></strong>\n        <span class="weapp_card_logo"><img class="icon_weapp_logo_mini" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAcCAMAAABF0y+mAAAAb1BMVEUAAAB4it11h9x2h9x2h9x2htx8j+R8i+B1h9x2h9x3h92Snv91htt2h9x1h9x4h9x1h9x1h9x2idx1h9t2h9t1htt1h9x1h9x1htx2h9x1h912h9x4h913iN17juOOjuN1iNx2h9t4h958i+B1htvejBiPAAAAJHRSTlMALPLcxKcVEOXXUgXtspU498sx69DPu5+Yc2JeRDwbCYuIRiGBtoolAAAA3ElEQVQoz62S1xKDIBBFWYiFYImm2DWF///G7DJEROOb58U79zi4O8iOo8zuCRfV8EdFgbYE49qFQs8ksJInajOA1wWfYvLcGSueU/oUGBtPpti09uNS68KTMcrQ5jce4kmN/HKn9XVPAo702JEdx9hTUrWUqVrI3KwUmM1NhIWMKdwiGvpGMWZOAj1PZuzAxHwhVSplrajoseBnbyDHAwvrtvKKhdqTtFBkL8wO5ijcsS3G1JMNvQ5mdW7fc0x0+ZcnlJlZiflAomdEyFaM7qeK2JahEjy5ZyU7jC/q/Rz/DgqEuAAAAABJRU5ErkJggg==" alt="">小程序</span>\n    </span>\n</span> -->\n<span class="weapp_card app_context appmsg_card_context">\n    <span class="weapp_card_bd">\n        <span class="weapp_card_profile flex_context">\n            <span class="radius_avatar weapp_card_avatar">\n                <img src="<#=avatar#>">\n            </span>\n            <span class="weapp_card_nickname flex_bd"><#=nickname#></span>\n        </span>\n        <span class="weapp_card_info">\n            <span class="weapp_card_title"><#=title#></span>\n            <span class="weapp_card_thumb_wrp" style="background-image:url(<#=imageUrl#>);"></span>\n        </span>\n    </span>\n    <span class="weapp_card_ft">\n        <span class="weapp_card_logo"><img class="icon_weapp_logo_mini" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAcCAMAAABF0y+mAAAAb1BMVEUAAAB4it11h9x2h9x2h9x2htx8j+R8i+B1h9x2h9x3h92Snv91htt2h9x1h9x4h9x1h9x1h9x2idx1h9t2h9t1htt1h9x1h9x1htx2h9x1h912h9x4h913iN17juOOjuN1iNx2h9t4h958i+B1htvejBiPAAAAJHRSTlMALPLcxKcVEOXXUgXtspU498sx69DPu5+Yc2JeRDwbCYuIRiGBtoolAAAA3ElEQVQoz62S1xKDIBBFWYiFYImm2DWF///G7DJEROOb58U79zi4O8iOo8zuCRfV8EdFgbYE49qFQs8ksJInajOA1wWfYvLcGSueU/oUGBtPpti09uNS68KTMcrQ5jce4kmN/HKn9XVPAo702JEdx9hTUrWUqVrI3KwUmM1NhIWMKdwiGvpGMWZOAj1PZuzAxHwhVSplrajoseBnbyDHAwvrtvKKhdqTtFBkL8wO5ijcsS3G1JMNvQ5mdW7fc0x0+ZcnlJlZiflAomdEyFaM7qeK2JahEjy5ZyU7jC/q/Rz/DgqEuAAAAABJRU5ErkJggg==" alt="">小程序</span>\n    </span>\n</span>\n';
});define("pages/voice_tpl.html.js",[],function(){
return'<div>\n    <#if(show_not_support===true){#>\n    <p>当前浏览器不支持播放音乐或语音，请在微信或其他浏览器中播放</p>\n    <#}#>\n    <div aria-labelledby="语音" id="voice_main_<#=voiceid#>_<#=posIndex#>" class="share_audio_context flex_context pages_reset" <#if(!musicSupport){#>style="display:none;"<#}#>>\n        <div id="voice_play_<#=voiceid#>_<#=posIndex#>" aria-labelledby="播放开关" class="share_audio_switch"><em class="icon_share_audio_switch" role="button"></em></div>\n        <div id="voice_detail_<#=voiceid#>_<#=posIndex#>" class="share_audio_info flex_bd">\n            <strong class="share_audio_title" aria-describedby="语音标题" role="link"><#=title#></strong>\n            <#if(!!nickname){#>\n            <p class="share_audio_tips">来自<#=nickname#></p>\n            <#}#>\n            <div id="voice_seekRange_<#=voiceid#>_<#=posIndex#>" class="share_audio_progress_wrp">\n                <div class="share_audio_progress">\n                    <div id="voice_progress_<#=voiceid#>_<#=posIndex#>" style="width:0%" class="share_audio_progress_inner"></div>\n                    <div id="voice_buffer_<#=voiceid#>_<#=posIndex#>" class="share_audio_progress_buffer" style="width:0%;"></div>\n                    <div id="voice_loading_<#=voiceid#>_<#=posIndex#>" class="share_audio_progress_loading" style="display:none;">\n                        <div class="share_audio_progress_loading_inner"></div>\n                    </div>\n                </div>\n                <span id="voice_playdot_<#=voiceid#>_<#=posIndex#>" class="share_audio_progress_handle" style="display:none;left:0%;"></span>\n            </div>\n            <div class="share_audio_desc" aria-labelledby="时长">\n                <em id="voice_playtime_<#=voiceid#>_<#=posIndex#>" class="share_audio_length_current" aria-hidden="true">00:00</em>\n                <em class="share_audio_length_total"><#=duration_str#></em>\n            </div>\n        </div>\n    </div>\n</div>\n';
});define("pages/voice_component.js",["biz_common/dom/event.js","biz_common/tmpl.js","pages/loadscript.js","pages/music_player.js","biz_common/dom/class.js","pages/report.js","biz_common/utils/monitor.js"],function(e,t,r,o){
"use strict";
function a(e){
this._o={
wxIndex:0,
type:0,
comment_id:"",
src:"",
mid:"",
songId:"",
autoPlay:!1,
duration:0,
debug:!1,
needVioceMutex:!0,
appPlay:!0,
title:"",
allowPause:!1,
singer:"",
epname:"",
coverImgUrl:"",
webUrl:[location.protocol,"//mp.weixin.qq.com/s?referFrom=#referFrom#&songid=#songId#&__biz=",window.biz,"&mid=",window.mid,"&idx=",window.idx,"&sn=",window.sn,"#wechat_redirect"].join(""),
playingCss:"",
playCssDom:"",
playArea:"",
progress:"",
detailUrl:"",
detailArea:"",
fileSize:0,
playtimeDom:"",
loadingDom:"",
bufferDom:"",
playdotDom:"",
seekRange:"",
seekContainer:""
},this._init(e);
}
function i(e,t,r,o){
b.num++,t.musicSupport=b.musicSupport,t.show_not_support=!1,b.musicSupport||1!=b.num||(t.show_not_support=!0);
var a=document.createElement("div"),i="";
if(i=_.tmpl(e,t),a.innerHTML=i,o===!0)r.appendChild(a.children[0]);else{
var n=r.parentNode;
if(!n)return;
n.lastChild===r?n.appendChild(a.children[0]):n.insertBefore(a.children[0],r.nextSibling);
}
}
function n(){
"undefined"==typeof window.reportVoiceid&&(window.reportVoiceid=[]),"undefined"==typeof window.reportMid&&(window.reportMid=[]);
}
function p(){
y.on(window,"unload",s);
}
function s(){
function e(e,t){
for(var r=0,o=e.length;o>r;r++)e[r]=t;
return e;
}
for(var t in b.reportData)v.musicreport({
data:b.reportData[t]
}),b.reportData[t].hasended=e(b.reportData[t].hasended,0),b.reportData[t].detail_click=e(b.reportData[t].detail_click,0),
b.reportData[t].errorcode=e(b.reportData[t].errorcode,0),b.reportData[t].play_duration=e(b.reportData[t].play_duration,0);
}
function c(e){
k.setSum(b.reportId,18,1),k.send();
var t=+new Date,r="//open.music.qq.com/fcgi-bin/fcg_music_get_song_info_weixin.fcg?song_id=#songid#&mid=#mid#&format=json&app_id=1034002693&app_key=cjjDaueOyPYRJFeTqG&device_id=weixin&file_type=mp3&qqmusic_fromtag=50&callback=get_song_info_back";
r=r.replace("#mid#",e.mid).replace("#songid#",e.id),h({
url:r,
timeout:3e4,
callbackName:"get_song_info_back",
callback:function(r){
var o=+new Date-t;
if(!r||"undefined"==typeof r.ret){
var a=1;
return d({
type:"error",
time:o,
code:a
}),void("function"==typeof e.onError&&e.onError({
errcode:a
}));
}
var i;
i=0==r.ret?r.play_url?0:6:1001==r.ret?1:1002==r.ret?2:1003==r.ret?3:1004==r.ret?4:5,
d({
type:"success",
time:o,
code:i
}),e.onSuc({
status:i,
play_url:r.play_url,
duration:r.song_play_time||0
});
},
onerror:function(r){
var o=+new Date-t,a=4;
switch(1*r){
case 400:
a=2;
break;

case 500:
a=3;
break;

default:
a=4;
}
d({
type:"error",
time:o,
code:a
}),"function"==typeof e.onError&&e.onError({
errcode:a
});
}
});
}
function d(e){
var t=Math.max(e.time,0);
if(t=Math.min(t,6e4),e.time>=0&&e.time<200?k.setSum(b.reportId,24,1):e.time>=200&&e.time<500?k.setSum(b.reportId,25,1):e.time>=500&&e.time<1e3?k.setSum(b.reportId,26,1):e.time>=1e3&&e.time<2e3?k.setSum(b.reportId,27,1):e.time>=2e3&&e.time<1e4?k.setSum(b.reportId,28,1):e.time>=1e4&&k.setSum(b.reportId,29,1),
k.setAvg(b.reportId,23,t),"error"==e.type){
switch(1*e.code){
case 1:
k.setSum(b.reportId,9,1);
break;

case 2:
k.setSum(b.reportId,10,1);
break;

case 3:
k.setSum(b.reportId,11,1);
break;

case 4:
k.setSum(b.reportId,12,1);
}
k.setSum(b.reportId,19,1);
}else if("success"==e.type){
switch(1*e.code){
case 1:
k.setSum(b.reportId,8,1);
break;

case 0:
k.setSum(b.reportId,17,1);
break;

case 2:
k.setSum(b.reportId,13,1);
break;

case 3:
k.setSum(b.reportId,14,1);
break;

case 4:
k.setSum(b.reportId,15,1);
break;

case 5:
k.setSum(b.reportId,16,1);
break;

case 6:
k.setSum(b.reportId,47,1);
}
k.setSum(b.reportId,20,1);
}
k.send();
}
function u(e){
return new a(e);
}
function l(e){
if(isNaN(e))return"00:00";
e=Math.ceil(e);
var t=Math.floor(e/3600),r=Math.floor((e-3600*t)/60),o=e-3600*t-60*r;
return 0!=t?(10>t&&(t="0"+t),t+=":"):t="",10>r&&(r="0"+r),10>o&&(o="0"+o),t+r+":"+o;
}
function m(e){
return e=(e||"").replace(/&#96;/g,"`").replace(/&#61;/g,"=").replace(/&#39;/g,"'").replace(/&quot;/g,'"').replace(/&lt;/g,"<").replace(/&gt;/g,">").replace(/&amp;/g,"&");
}
function g(e){
return e=(e||"").replace(/&/g,"&amp;").replace(/>/g,"&gt;").replace(/</g,"&lt;").replace(/"/g,"&quot;").replace(/'/g,"&#39;").replace(/=/g,"&#61;").replace(/`/g,"&#96;");
}
var y=e("biz_common/dom/event.js"),_=e("biz_common/tmpl.js"),h=e("pages/loadscript.js"),f=e("pages/music_player.js"),D=e("biz_common/dom/class.js"),v=e("pages/report.js"),k=e("biz_common/utils/monitor.js"),b={
reportId:"28306",
musicSupport:f.getSurportType(),
debug:location.href.indexOf("vconsole=1")>0||document.cookie&&document.cookie.indexOf("vconsole_open=1")>-1?!0:!1,
reportData:{},
posIndex:{},
qqMusiceSongId:"http://thirdparty.gtimg.com/#songId#.m4a?fromtag=38&songid=#songId#",
qqMusiceMid:"http://thirdparty.gtimg.com/C100#mid#.m4a?fromtag=38&songid=#songId#",
num:0
};
return n(),p(),a.prototype._init=function(e){
this._extend(e),this._g={
copyright:-1,
check_copyright:!1,
canDragBar:!1,
barDraging:!1,
canGoDetail:!0
},this._initQQmusicLyric(),this._initReportData(),this._initPlayer(),this._playEvent();
},a.prototype._initQQmusicLyric=function(){
var e=this._o;
e.webUrl=0==e.type||1==e.type?e.webUrl.replace("#songId#",e.songId||"").replace("#referFrom#","music.qq.com"):e.webUrl.replace("#songId#","").replace("#referFrom#","");
},a.prototype._initReportData=function(){
var e=this._o;
2==e.type||3==e.type||4==e.type?window.reportVoiceid.push(e.songId):(0==e.type||1==e.type)&&window.reportMid.push(e.songId),
"undefined"==typeof b.reportData[e.type]&&(b.reportData[e.type]=v.getMusicReportData(e),
b.posIndex[e.type]=0),this._g.posIndex=b.posIndex[e.type]++;
var t=b.reportData[e.type];
t.musicid.push(e.songId),t.commentid.push(e.comment_id),t.hasended.push(0),t.mtitle.push(e.title),
t.detail_click.push(0),t.duration.push(parseInt(1e3*e.duration)),t.errorcode.push(0),
t.play_duration.push(0);
},a.prototype._initPlayer=function(){
b.musicSupport&&(this._o.onStatusChange=this._statusChangeCallBack(),this._o.onTimeupdate=this._timeupdateCallBack(),
this._o.onError=this._errorCallBack(),this._o.onUpdateSeekRange=this._onUpdateSeekRange(),
this.player=new f.init(this._o));
},a.prototype.isInSeekrang=function(e){
var t=this._o.seekRange;
if(!t)return!1;
if(t===e)return!0;
for(var r=t.getElementsByTagName("*"),o=0,a=r.length;a>o;o++)if(r[o]===e)return!0;
return!1;
},a.prototype._playEvent=function(){
var e=this,t=this._o,r=this._g;
if(t.detailUrl&&t.detailArea&&y.on(t.detailArea,"click",function(o){
if(!r.barDraging&&r.canGoDetail){
var a=o.target||o.srcElement;
a&&e.isInSeekrang(a)||(2==t.type||3==t.type||4==t.type?(b.reportData[t.type].detail_click[r.posIndex]=1,
window.location.href=t.detailUrl):(0==t.type||1==t.type)&&e._checkCopyright(function(){
b.reportData[t.type].detail_click[r.posIndex]=1,window.location.href=t.detailUrl;
}));
}
}),b.musicSupport){
var o=0,a=4,i=5;
2==t.type?o=3:3==t.type?o=6:4==t.type?o=7:(0==t.type||1==t.type)&&(o=1),y.tap(t.playArea,function(){
return D.hasClass(t.playCssDom,t.playingCss)?(t.allowPause?e.player.pause():e.player.stop(),
v.report({
type:o,
comment_id:t.comment_id,
voiceid:t.songId,
action:i
})):1==o?e._checkCopyright(function(){
e.player.setSrc(r.play_url),r.duration&&e.player.setDuration(r.duration),e._playMusic(o,a);
}):e._playMusic(o,a),!1;
}),e._dragEvent();
}
},a.prototype._getCategory=function(){
var e=this._o.type;
return 2==e||3==e||4==e?2:0==e||1==e?1:-1;
},a.prototype._dragEvent=function(){
var e=this,t=this._o,r=this._g,o=t.seekRange;
if(o){
for(var a=0,i=o;i&&i!=document.body;)a+=i.offsetLeft,i=i.offsetParent;
var n=e.player.getDuration();
r.seekData={
offsetLeft:a,
duration:n,
rangeWidth:o.offsetWidth,
startTime:0,
dragTime:0,
downX:0,
moveX:0
},y.on(o,"mousedown",function(t){
r.canDragBar&&(e._pointerDownHandler({
x:t.pageX||t.clientX
}),t.preventDefault());
}),y.on(t.seekContainer,"mousemove",function(t){
r.canDragBar&&r.barDraging&&(e._pointerMoveHandler({
x:t.pageX||t.clientX
}),t.preventDefault(),t.stopPropagation());
}),y.on(document.body,"mouseup",function(t){
return r.canDragBar&&r.barDraging?(e._pointerUpHandler({
x:t.pageX||t.clientX
}),t.preventDefault(),t.stopPropagation(),!1):void 0;
}),y.on(o,"touchstart",function(t){
r.canDragBar&&(e._pointerDownHandler({
x:t.changedTouches[0].clientX
}),t.preventDefault());
}),y.on(o,"touchmove",function(t){
r.canDragBar&&r.barDraging&&(e._pointerMoveHandler({
x:t.changedTouches[0].clientX
}),t.preventDefault(),t.stopPropagation());
}),y.on(o,"touchend",function(t){
return r.canDragBar&&r.barDraging?(e._pointerUpHandler({
x:t.changedTouches[0].clientX
}),t.preventDefault(),t.stopPropagation(),!1):void 0;
});
}
},a.prototype._pointerDownHandler=function(e){
var t=this._g;
t.barDraging=!0,t.canGoDetail=!1,t.seekData.downX=e.x,t.seekData.startTime=this.player.getCurTime();
},a.prototype._pointerMoveHandler=function(e){
var t=this._g,r=t.seekData;
r.moveX=e.x;
var o=(r.moveX-r.offsetLeft)/r.rangeWidth;
o=Math.min(o,1),o=Math.max(o,0),r.dragTime=o*r.duration,r.dragTime!=r.startTime&&this._updateProgressBar(r.dragTime);
},a.prototype._pointerUpHandler=function(e){
var t=this._g,r=t.seekData;
r.dragTime||this._pointerMoveHandler({
x:e.x
}),t.barDraging=!1,this.player.seek(r.dragTime),t.seekData.startTime=0,t.seekData.dragTime=0,
t.seekData.downX=0,t.seekData.moveX=0,setTimeout(function(){
t.canGoDetail=!0;
},1e3);
},a.prototype._checkCopyright=function(e){
var t=this,r=this._o,o=this._g;
return o.play_url&&this._musicCopyrightWarnning(!1)===!1?void("function"==typeof e&&e()):void(o.check_copyright||(o.check_copyright=!0,
c({
id:r.songId,
mid:r.mid,
onSuc:function(r){
o.check_copyright=!1,o.copyright=1*r.status,t._musicCopyrightWarnning(!0)===!1&&"function"==typeof e&&(o.play_url=r.play_url,
o.duration=r.duration||0,e({
play_url:r.play_url,
duration:o.duration
}));
},
onError:function(){
o.check_copyright=!1;
}
})));
},a.prototype._musicCopyrightWarnning=function(e){
var t=this._g,r=!0,a="";
switch(1*t.copyright){
case 0:
r=!1;
break;

case 1:
r=!0,a="该歌曲版权已过期，无法播放。";
break;

case 2:
r=!0,a="抱歉，应版权方要求，当前国家或地区暂不提供此歌曲服务。";
break;

case 3:
r=!0,a="该歌曲版权已过期，无法播放。";
break;

case 4:
r=!0,a="抱歉，歌曲信息不正确。";
break;

case 5:
r=!0,a="系统错误，请稍后再试。";
break;

case 6:
r=!0,a="系统错误，请稍后再试。";
break;

default:
r=!0,a="系统错误，请稍后再试。";
}
return r===!0&&e===!0&&(a+="错误码："+t.copyright,setTimeout(function(){
o(a);
},0)),r;
},a.prototype._playMusic=function(e,t){
var r=this._o,o=this._g;
this.player.play(),b.reportData[r.type].hasended[o.posIndex]=1,v.report({
type:e,
comment_id:r.comment_id,
voiceid:r.songId,
action:t
});
},a.prototype._extend=function(e){
for(var t in e)this._o[t]=e[t];
},a.prototype._onUpdateSeekRange=function(){
var e=this,t=e._o,r=e._g;
return function(e){
this.surportSeekRange()&&t.bufferDom&&t.playdotDom?(r.canDragBar=!0,t.playdotDom.style.display="block",
t.bufferDom.style.width=1*e+"%"):(r.canDragBar=!1,t.playdotDom&&(t.playdotDom.style.display="none"));
};
},a.prototype._statusChangeCallBack=function(){
var e=this;
return function(t,r){
e._updatePlayerCss(this,r);
};
},a.prototype._timeupdateCallBack=function(){
var e=this,t=this._o,r=this._g;
return function(o,a){
e._updateProgress(a),0!=a&&(b.reportData[t.type].play_duration[r.posIndex]=parseInt(1e3*a));
};
},a.prototype._errorCallBack=function(){
var e=this,t=this._o,r=this._g;
return function(o,a){
b.reportData[t.type].errorcode[r.posIndex]=a.code,e._updatePlayerCss(this,3),e._reportH5Error(a);
};
},a.prototype._reportH5Error=function(e){
if("mp.weixin.qq.com"==location.host&&1==e.type||b.debug){
var t=["code:",e.code,";type:",this._o.type,";url:",window.location.href];
this.player&&t.push(";src:"+this.player.getSrc());
var r=new Image;
r.src=["https://badjs.weixinbridge.com/badjs?level=4&id=112&msg=",encodeURIComponent(t.join("")),"&uin=",window.uin||"","&from=",this._o.type].join("");
}
},a.prototype._updatePlayerCss=function(e,t){
!!b.debug&&console.log("status:"+t);
{
var r=this._o,o=r.playCssDom;
r.progress;
}
2==t?(D.removeClass(o,r.playingCss),r.playdotDom&&(e.surportSeekRange()?(r.playdotDom.style.display="block",
this._g.canDragBar=!0):(r.playdotDom.style.display="none",this._g.canDragBar=!1))):3==t?(D.removeClass(o,r.playingCss),
r.playdotDom&&(r.playdotDom.style.display="none",this._g.canDragBar=!1),this._updateProgress(0)):(1==t||4==t)&&(D.addClass(o,r.playingCss),
r.playdotDom&&(e.surportSeekRange()?(r.playdotDom.style.display="block",this._g.canDragBar=!0):(r.playdotDom.style.display="none",
this._g.canDragBar=!1))),r.loadingDom&&(r.loadingDom.style.display=4==t?"block":"none");
},a.prototype._updateProgress=function(e){
this._g.barDraging||this._updateProgressBar(e);
},a.prototype._updateProgressBar=function(e){
var t=this._o,r=this.player,o=r.getDuration();
if(o){
var a=this._countProgress(o,e);
t.progress&&(t.progress.style.width=a),t.playtimeDom&&(t.playtimeDom.innerHTML=l(e)),
t.playdotDom&&(t.playdotDom.style.left=a);
}
},a.prototype._countProgress=function(e,t){
return Math.min(t/e*100,100)+"%";
},{
init:u,
renderPlayer:i,
formatTime:l,
decodeStr:m,
encodeStr:g
};
});define("pages/qqmusic_tpl.html.js",[],function(){
return'<span id="qqmusic_main_<#=musicid#>_<#=posIndex#>" class="db qqmusic_area <#if(!musicSupport){#> unsupport<#}#>">\n    <span class="tc tips_global unsupport_tips" <#if(show_not_support!==true){#>style="display:none;"<#}#>>\n    当前浏览器不支持播放音乐或语音，请在微信或其他浏览器中播放    </span>\n    <span class="db qqmusic_wrp appmsg_card_context appmsg_card_active">\n        <span class="db qqmusic_bd">\n            <span id="qqmusic_play_<#=musicid#>_<#=posIndex#>" class="play_area">\n                <i class="icon_qqmusic_switch"></i>\n                <img src="<#=window.icon_qqmusic_default#>" alt="" class="pic_qqmusic_default">\n                <img src="<#=music_img#>" data-autourl="<#=audiourl#>" data-musicid="<#=musicid#>" class="qqmusic_thumb" alt="">\n            </span>\n            <a id="qqmusic_home_<#=musicid#>_<#=posIndex#>" class="access_area">\n                <span class="qqmusic_songname"><#=music_name#></span>\n                <span class="qqmusic_singername"><#=singer#></span>\n                <span class="qqmusic_source"><img src="<#=window.icon_qqmusic_source#>" alt=""></span>\n            </a>\n        </span>\n    </span>       \n</span>\n';
});define("new_video/ctl.js",["biz_wap/utils/ajax.js"],function(i){
"use strict";
var e=top.window.user_uin,t=Math.floor(top.window.user_uin/100)%20;
e||(t=-1);
var o=function(){
return t>=0;
};
top.window.__webviewid||(top.window.__webviewid=+new Date+"_"+Math.ceil(1e3*Math.random()));
var d=function(){
var i=top.window.mid,t=top.window.idx,o="";
o=i&&t?i+"_"+t:"";
var d=top.window.__webviewid,r=[e,o,d].join("_");
return r;
},r=function(e){
if(20>t)try{
var r=e.vid||"",w={};
w.__biz=top.window.biz||"",w.vid=r,w.clienttime=+new Date;
var n=top.window.mid,a=top.window.idx,p="";
n&&a?(w.type=1,p=n+"_"+a):(w.type=2,p=r),w.id=p,w.webviewid=d(),w.step=e.step||0,
w.orderid=e.orderid||0,w.ad_source=e.ad_source||0,w.traceid=e.traceid||0,w.ext1=e.ext1||"",
w.ext2=e.ext2||"",w.r=Math.random(),w.devicetype=top.window.devicetype,w.version=top.window.clientversion,
w.is_gray=o()?1:0;
var _=i("biz_wap/utils/ajax.js");
_({
url:"/mp/ad_video_report?action=user_action",
type:"post",
data:w
});
}catch(v){}
};
return{
report:r,
getWebviewid:d,
showAd:o
};
});define("a/testdata.js",[],function(){
"use strict";
var i=[{
hint_txt:"android_1450",
url:"pages/store/store?poi_id=471334801&amp;weixinadkey=369aae2cf4a83f97317e0d7cbf8235d0c236bf448338531cad09537aa0442dd2c88c5c80a20ab9a451e195bae80b907c&amp;gdt_vid=wx0qwki52mnztuau01&amp;weixinadinfo=1000028800.wx0qwki52mnztuau01.0.1",
original_id:"wxopen_ghid",
type:"0",
rl:"http://ad.wx.com:12638/cgi-bin/click?viewid=Z9AhqIKxf%2B",
apurl:"http://ad.wx.com:12638/cgi-bin/exposure?viewid=Z9AhqIKxf%2B",
traceid:"wx0qwki52mnztuau01",
group_id:"",
ticket:"24bkzv9mpuvk9",
aid:"1000028800",
pt:118,
image_url:"http://wximg.qq.com/wxp/generic/2016060014/f7ce9b0152fa676c493094b8d7535ac9.jpeg",
ad_desc:"",
biz_appid:"wxf4c20fc6adac2f78",
pos_type:4,
watermark_type:0,
logo:"",
is_cpm:1,
weapp_info:{
original_id:"gh_a3df530d38b1"
}
},{
hint_txt:"",
url:"https://mp.weixin.qq.com/mp/ad_biz_info?__biz=MjM5OTg2MjMxMg==&sn=a61272cba6fadd949d14e22c52c4f172&weixinadkey=ddfcad5b2aab7b8ed3d874223e60e05277f0e107a0eddf9193158d436bc1763fa451fa5866706619cbdae6f1486208d5&ticket=24bkzv9mpuvk9&gdt_vid=wx0nbqjrudeu6t3a00&weixinadinfo=10477522.wx0nbqjrudeu6t3a00.0.1#wechat_redirect",
type:"0",
rl:"http://ad.wx.com:12638/cgi-bin/click?viewid=TtvIAPFkbYCw0NLHyOCuhVUKcvSDeqikHgGHgV06N8wHRqLXjHbiPvzWZ42MQnxG2j%2FU%2BMrrVRLsSiV%2BVyFpLLTP%2FmNhZnfupgbvUnusHoJCZ6qy%2FNILY5M9P6HPuGWlIEdF%2FJa8%2B2nUKqv%2B0%2F2CALIGqmsMtw%2F1dt2CGRNS5UHYOq1Bt9UZ7E3XKghCMDE05E4kC%2FF4JILufWV7Pmm836lmc2vLKc3MvLo6ooJrKLcdW2vJH10vLxF%2BnESDG11SnLK2L7%2BEAlHZc8jskwkmE%2FqpwY1hfPUFzRWTxFIoBAOjn7EavIEM3%2BDO0v9jzXYBsADOrPwx7ZHeCW%2Bkz5sLGaz2P75MJ03uGvDwqvy7TWxs1G5Ds0nRbRrkarBh3QHfW81MyXPRK2v%2BlkDq3LDhWrvZVPotyrGEhPx3InTcFN6u8T%2BpyED5c6kl2HZ2pPgAQGQ3ygQDFeRgAhquTjEqvVZ06XQrEBkecElRz1%2B%2FjKcg6IBvgA1WMMLbnAFQ6YaHJi%2BJLpsDaa%2BQdqcBPAQxX0zBbUJYbmSR5RzrRYF0nivv8PMUGlcxqPhcc6Ro4zml7QeE4lP5mM9K2rrmph4tcUZdwCMCewElmy09lAhZq74X0a9AZvEc22Oj%2F7UY7Xw4wNvDD1R46ZGWX6Vp%2BmoyG0aZeEUplV0WVq66MSe9fxCg5s66xqLd9CZUTiEhVt258HKTM8dfpGxbpocBbMHYCXS8vtzx6Qi1L5b8LGtzc%2FOypgf22ZobjJp4ZZVSIhxdN0305g05XKEocbCwZpPBNVWaPzmIyaNceMOJAh6L6iEQcSsG8bD7QD%2BE2DBpMEUdtReUejhqI4ZcIMog3q51NA%3D%3D",
apurl:"http://ad.wx.com:12638/cgi-bin/exposure?viewid=TtvIAPFkbYCw0NLHyOCuhVUKcvSDeqikHgGHgV06N8wHRqLXjHbiPvzWZ42MQnxG2j%2FU%2BMrrVRLsSiV%2BVyFpLLTP%2FmNhZnfupgbvUnusHoJCZ6qy%2FNILY5M9P6HPuGWlIEdF%2FJa8%2B2nUKqv%2B0%2F2CALIGqmsMtw%2F1dt2CGRNS5UHYOq1Bt9UZ7E3XKghCMDE05E4kC%2FF4JILufWV7Pmm836lmc2vLKc3MvLo6ooJrKLcdW2vJH10vLxF%2BnESDG11SnLK2L7%2BEAlHZc8jskwkmE%2FqpwY1hfPUFzRWTxFIoBAOjn7EavIEM3%2BDO0v9jzXYBsADOrPwx7ZHeCW%2Bkz5sLGaz2P75MJ03uGvDwqvy7TWxs1G5Ds0nRbRrkarBh3QHfW81MyXPRK2v%2BlkDq3LDhWrvZVPotyrGEhPx3InTcFN6u8T%2BpyED5c6kl2HZ2pPgAQGQ3ygQDFeRgAhquTjEqvVZ06XQrEBkecElRz1%2B%2FjKcg6IBvgA1WMMLbnAFQ6YaHJi%2BJLpsDaa%2BQdqcBPAQxX0zBbUJYbmSR5RzrRYF0nivv8PMUGlcxqPhcc6Ro4zml7QeE4lP5mM9K2rrmph4tcUZdwCMCewElmy09lAhZq74X0a9AZvEc22Oj%2F7UY7Xw4wNvDD1R46ZGWX6Vp%2BmoyG0aZeEUplV0WVq66MSe9fxCg5s66xqLd9CZUTiEhVt258HKTM8dfpGxbpocBbMHYCXS8vtzx6Qi1L5b8LGtzc%2FOypgf22ZobjJp4ZZVSIhxdN0305g05XKEocbCwZpPBNVWaPzmIyaNceMOJAh6L6iEQcSsG8bD7QD%2BE2DBpMEUdtReUejhqI4ZcIMog3q51NA%3D%3D",
traceid:"wx0nbqjrudeu6t3a00",
group_id:"",
ticket:"24bkzv9mpuvk9",
aid:"10477522",
pt:100,
image_url:"http://vweixinthumb.tc.qq.com/109/20204/snsvideodownload?filekey=30270201010420301e02016d04025348041073f09322d2b39e1e439330a757f2d0690203010c9e0400&hy=SH&storeid=32303137303431323033303233303030303564653666313336666664393336663561333230613030303030303664&bizid=1023",
video_info:{
displayWidth:"4px",
displayHeight:"3px",
thumbUrl:"http://vweixinthumb.tc.qq.com/109/20204/snsvideodownload?filekey=30270201010420301e02016d04025348041073f09322d2b39e1e439330a757f2d0690203010c9e0400&hy=SH&storeid=32303137303431323033303233303030303564653666313336666664393336663561333230613030303030303664&bizid=1023",
videoUrl:"http://wxsnsdy.video.qq.com/105/20210/snsdyvideodownload?filekey=30270201010420301e02016904025348041007c00a8ebdfdd80d0aa77790123d0e660203145d190400&hy=SH&storeid=32303137303532353035323735333030303433663536313336666664393330343561333230613030303030303639&bizid=1023"
},
ad_desc:"",
biz_appid:"wxf4c20fc6adac2f78",
biz_info:{
user_name:"gh_f99505e7d9c5",
nick_name:"Skyscanner天巡",
is_subscribed:0,
head_img:"http://wx.qlogo.cn/mmhead/Q3auHgzwzM6QRHv4Qlh3uvsjicu2mgW5y5GnWmnL9ZeCJbeK9sNdTRQ/0",
biz_uin:2399862312
},
pos_type:0,
watermark_type:0,
logo:"",
is_cpm:1,
exp_info:{},
app_info:{}
}];
return{
data:i
};
});define("appmsg/reward_entry.js",["biz_common/dom/event.js","biz_wap/utils/ajax.js","biz_wap/jsapi/core.js","rt/appmsg/getappmsgext.rt.js"],function(e,t,n,r){
"use strict";
function a(e){
e&&(e.style.display="block");
}
function o(e){
e&&(e.style.display="none");
}
function i(){
p({
url:"/mp/getappmsgext?&f=json"+(window.send_time?"&send_time="+send_time:""),
data:{
__biz:biz,
appmsg_type:appmsg_type,
mid:mid,
sn:sn,
idx:idx,
scene:source,
title:encodeURIComponent(msg_title.htmlDecode()),
ct:ct,
devicetype:devicetype.htmlDecode(),
version:version.htmlDecode(),
is_need_reward:is_need_reward,
reward_uin_count:is_need_reward?3*w:0,
r:Math.random()
},
type:"post",
dataType:"json",
async:!0,
rtId:27613,
rtKey:50,
rtDesc:f,
success:function(e){
e&&(document.getElementById("js_reward_link")&&u.off(document.getElementById("js_reward_link"),"click",x),
s({
reward_total:e.reward_total_count,
reward_head_imgs:e.reward_head_imgs||[],
can_reward:e.can_reward,
timestamp:e.timestamp
}));
}
});
}
function d(e){
return function(t){
return"0"==window.wx_user_can_reward?void r("你已成为该公众号的黑名单用户，暂时无法赞赏。"):(t.preventDefault(),
void g.invoke("openUrlWithExtraWebview",{
url:e
},function(t){
t.err_msg.indexOf(":ok")>-1||(location.href=e);
}));
};
}
function s(e){
var t=window.innerWidth||document.documentElement.innerWidth,n=(Math.ceil((h-188)/42)+1)*Math.floor((t-15)/42);
_="http://mp.weixin.qq.com/mp/reward?act=getrewardheads&__biz="+biz+"&appmsgid="+mid+"&idx="+idx+"&sn="+sn+"&offset=0&count="+n+"&source=1#wechat_redirect";
var r="#wechat_redirect",s="https://mp.weixin.qq.com/bizmall/reward?act=showpage&__biz="+biz+"&appmsgid="+mid+"&idx="+idx+"&sn="+sn+"&timestamp="+e.timestamp+"&showwxpaytitle=1"+r,l=document.getElementById("js_reward_link");
l&&(g.on("activity:state_change",function(e){
if("onResume"==e.state_change||"onResume"==e.state){
var t=(new Date).valueOf();
if(-1!=navigator.userAgent.indexOf("Android")&&localStorage.getItem("lastOnresumeTime")&&t-parseInt(localStorage.getItem("lastOnresumeTime"))<=j)return;
localStorage.setItem("lastOnresumeTime",t),g.invoke("setNavigationBarColor",{
actionCode:"1"
}),i();
}
}),x=d(s),u.on(l,"click",x)),y=e.reward_head_imgs;
var w=c();
v.reward&&1==e.can_reward?(a(v.reward),u.on(window,"load",function(){
m&&(u.off(window,"scroll",m),u.on(window,"scroll",m));
})):o(v.reward);
var p=document.getElementById("js_reward_inner");
p&&w>0&&a(p);
var f=document.getElementById("js_reward_total");
f&&(f.innerText=e.reward_total,f.setAttribute("href",_));
}
function l(e,t){
var n=document.createElement("span");
n.className="reward_user_avatar";
var r=new Image;
return r.onload=function(){
window.logs&&window.logs.reward_heads_total++,r.onload=r.onerror=null;
},r.onerror=function(){
window.logs&&window.logs.reward_heads_total++,window.logs&&window.logs.reward_heads_fail++,
r.onload=r.onerror=null;
},r.src=t,n.appendChild(r),e.appendChild(n),n;
}
function c(){
if(y.length){
var e=document.getElementById("js_reward_list"),t=0,n=document.createDocumentFragment();
if(e){
for(var r=0,a=y.length;a>r&&(t++,l(n,y[r]),t!=3*w);++r);
t>w&&(e.className+=" tl"),e.innerHTML="",e.appendChild(n);
}
return t;
}
}
function m(){
var e=window.pageYOffset||document.documentElement.scrollTop;
e+h>v.reward.offsetTop&&(p({
type:"GET",
url:"/bizmall/reward?act=report&__biz="+biz+"&appmsgid="+mid+"&idx="+idx,
async:!0
}),u.off(window,"scroll",m),m=null);
}
var w,_,u=e("biz_common/dom/event.js"),p=e("biz_wap/utils/ajax.js"),g=e("biz_wap/jsapi/core.js"),f=e("rt/appmsg/getappmsgext.rt.js"),h=window.innerHeight||document.documentElement.clientHeight,v={
reward:document.getElementById("js_reward_area")
},y=[],j=500;
window.logs&&(window.logs.reward_heads_total=0,window.logs.reward_heads_fail=0);
var x=function(){};
return{
handle:function(e,t){
w=t,s(e);
},
render:function(e){
w=e,c();
}
};
});define("appmsg/comment.js",["biz_common/dom/class.js","appmsg/cmt_tpl.html.js","biz_common/utils/wxgspeedsdk.js","biz_common/dom/event.js","biz_wap/utils/ajax.js","biz_common/utils/string/html.js","biz_common/tmpl.js","biz_wap/utils/fakehash.js","appmsg/log.js","appmsg/comment_tpl.html.js","appmsg/my_comment_tpl.html.js","appmsg/emotion/emotion.js","appmsg/emotion/dom.js"],function(e,t,n,o){
"use strict";
function m(e,t){
e&&(e.style.display=t?t:"block");
}
function i(e){
e&&(e.style.display="none");
}
function s(){
setTimeout(function(){
m(X.toast);
},750),setTimeout(function(){
i(X.toast);
},1500);
}
function c(e){
return e.replace(/^\s+|\s+$/g,"");
}
function a(e,t){
if(!(Math.random()<.999)){
var n=window.location.protocol,o=9;
"https:"==n&&(o=18),z.saveSpeeds({
uin:uin,
pid:o,
speeds:[{
sid:29,
time:e
},{
sid:30,
time:t
}]
}),z.send();
}
}
function l(e,t){
if("undefined"!=typeof e){
var n=new Image;
n.src=A.idkey?"//mp.weixin.qq.com/mp/jsmonitor?idkey="+(A.idkey+"_"+e+"_1")+"&t="+Math.random():"http://mp.weixin.qq.com/mp/jsreport?key="+e+"&content="+(t||"")+"&r="+Math.random();
}
}
function d(){
var e=window.innerHeight||document.documentElement.clientHeight,t=window.pageYOffset||document.documentElement.scrollTop,n=document.documentElement.scrollHeight;
if(t+e+100>n&&H.off(window,"scroll",d),!!L&&console.log("onscroll,isLoading:"+Y+";offset:"+F+";scrollHeight:"+n+";scrollTop:"+t+";innerHeight:"+e),
!(Y||-1==F||F>0&&n-t-e>500)){
var o=+new Date;
Y=!0,i(X.tips),m(X.loading);
var s="/mp/appmsg_comment?action=getcomment&scene="+A.scene+"&__biz="+biz+"&appmsgid="+appmsgid+"&idx="+idx+"&comment_id="+M+"&offset="+F+"&limit="+P+(window.send_time?"&send_time="+send_time:"");
try{
W++,W>1&&l(A.moreList,encodeURIComponent(s)),K.indexOf(s)>-1&&l(A.repeatList,encodeURIComponent(s)),
K.push(s);
}catch(c){}
!!L&&console.log("[Appmsg comment] start get comment data:"+s),N("[Appmsg comment] start get comment data, url:"+s),
R({
url:s,
type:"get",
success:function(e){
var t=+new Date,n=t-o,m={};
try{
m=window.eval.call(window,"("+e+")");
}catch(i){}
var c=m.base_resp&&m.base_resp.ret;
if(0==c){
r(m);
var d=+new Date-t;
a(n,d);
}else l(A.errList,"type:resperr;url:"+encodeURIComponent(s)+";ret="+c);
N("[Appmsg comment] get comment success, text: "+e);
},
error:function(){
l(A.errList,"type:ajaxerr;url:"+encodeURIComponent(s)),N("[Appmsg comment] get comment ajax error");
},
complete:function(){
Y=!1,i(X.loading),H.off(window,"scroll",k);
}
});
}
}
function r(e){
var t,n=document.createDocumentFragment();
V++,V>1&&l(A.handleList,encodeURIComponent(JSON.stringify({
comment_id:M,
offset:F,
url:location.href
}))),"undefined"!=typeof e.only_fans_can_comment?window.can_fans_comment_only=e.only_fans_can_comment:"undefined"==typeof window.can_fans_comment_only&&(window.can_fans_comment_only=0),
1!=e.enabled?(x&&(x.style.display="none"),e.elected_comment=[],e.elected_comment_total_cnt=0):x&&(x.style.display="block"),
0==F?(J=e.logo_url,G=e.nick_name,t=e.elected_comment,t&&t.length?(g(t,n,"elected"),
X.list.appendChild(n),m(X.main),0==window.can_fans_comment_only||1==window.can_fans_comment_only&&1==e.is_fans?m(document.getElementById("js_cmt_addbtn1")):m(document.getElementById("js_cmt_nofans1"),"block"),
e.elected_comment_total_cnt<=10&&(m(document.getElementById("js_cmt_statement")),
m(document.getElementById("js_cmt_qa")))):(i(X.main),0==window.can_fans_comment_only||1==window.can_fans_comment_only&&1==e.is_fans?m(document.getElementById("js_cmt_addbtn2")):m(document.getElementById("js_cmt_nofans2"),"block")),
function(){
var e=location.href.indexOf("scrolltodown")>-1?!0:!1,t=(document.getElementById("img-content"),
document.getElementById("js_cmt_area"));
if(e&&t&&t.offsetTop){
var n=t.offsetTop;
window.scrollTo(0,n-25);
}
}()):(t=e.elected_comment,t&&t.length&&(g(t,n,"elected"),X.list.appendChild(n))),
0==e.elected_comment_total_cnt?(F=-1,i(document.getElementById("js_cmt_loading")),
i(document.getElementById("js_cmt_statement")),i(document.getElementById("js_cmt_qa"))):F+P>=e.elected_comment_total_cnt?(F=-1,
i(document.getElementById("js_cmt_loading")),m(document.getElementById("js_cmt_statement")),
m(document.getElementById("js_cmt_qa"))):F+=e.elected_comment.length;
}
function _(){
S.log("tag1");
var e=c(X.input.value);
if(S.log("tag2"),!B.hasClass(X.submit,"btn_disabled")){
if(S.log("tag3"),e.length<1)return f("留言不能为空");
if(S.log("tag4"),e.length>600)return f("字数不能多于600个");
S.log("tag5"),B.addClass(X.submit,"btn_disabled"),S.log("tag6");
var t=document.getElementById("activity-name");
S.log("tag7"),et!=e&&(tt=+new Date);
var n="/mp/appmsg_comment?action=addcomment&scene="+A.scene+"&comment_id="+M+"&__biz="+biz+"&idx="+idx+"&appmsgid="+appmsgid+"&sn="+sn;
R({
url:n,
data:{
content:e,
title:t&&c(t.innerText),
head_img:J,
nickname:G,
client_id:tt
},
type:"POST",
success:function(t){
S.log("tag8"),U.hidePannel();
var o={},i=document.createDocumentFragment();
try{
o=window.eval.call(window,"("+t+")");
}catch(c){}
switch(+o.ret){
case 0:
s(),g([{
content:e,
nick_name:G,
create_time:(new Date).getTime()/1e3|0,
is_elected:0,
logo_url:J,
like_status:0,
content_id:0,
like_num_format:0,
like_num:0,
is_from_friend:0,
is_from_me:1,
my_id:o.my_id
}],i,"mine"),X.mylist.insertBefore(i,X.mylist.firstChild),m(X.mylist.parentNode),
X.input.value="";
break;

case-6:
f("你留言的太频繁了，休息一下吧");
break;

case-7:
f("你还未关注该公众号，不能参与留言");
break;

case-10:
f("字数不能多于600个");
break;

case-15:
f("留言已关闭");
break;

default:
et=e,f("系统错误，请重试");
}
0!=o.ret&&l(A.addCommentErr,"type:resperr;url:"+encodeURIComponent(n)+";ret="+o.ret);
},
error:function(e){
S.log("shit;"+e.status+";"+e.statusText),l(A.addCommentErr,"type:ajaxerr;url:"+encodeURIComponent(n));
},
complete:function(){
""!=X.input.value&&B.removeClass(X.submit,"btn_disabled");
}
});
}
}
function p(){
if(0==Q){
var e="/mp/appmsg_comment?action=getmycomment&scene="+A.scene+"&__biz="+biz+"&appmsgid="+appmsgid+"&idx="+idx+"&comment_id="+M,t=document.getElementById("js_mycmt_loading");
Q=1,m(t),R({
url:e,
type:"get",
success:function(t){
var n={};
try{
n=window.eval.call(window,"("+t+")");
}catch(o){}
var i=n.base_resp&&n.base_resp.ret;
if(0==i){
var s=n.my_comment,c=document.createDocumentFragment();
s&&s.length&&(g(s,c,"mine"),X.mylist.appendChild(c),m(X.mylist.parentNode)),Q=2;
}else Q=0,l(A.errComment,"type:resperr;url:"+encodeURIComponent(e)+";ret="+i);
},
error:function(){
Q=0,l(A.errComment,"type:ajaxerr;url:"+encodeURIComponent(e));
},
complete:function(){
i(t);
}
});
}
}
function u(e){
var t=(new Date).getTime(),n=new Date;
n.setDate(n.getDate()+1),n.setHours(0),n.setMinutes(0),n.setSeconds(0),n=n.getTime();
var o=t/1e3-e,m=n/1e3-e,i=new Date(n).getFullYear(),s=new Date(1e3*e);
return 3600>o?Math.ceil(o/60)+"分钟前":86400>m?Math.floor(o/60/60)+"小时前":172800>m?"昨天":604800>m?Math.floor(m/24/60/60)+"天前":s.getFullYear()==i?s.getMonth()+1+"月"+s.getDate()+"日":s.getFullYear()+"年"+(s.getMonth()+1)+"月"+s.getDate()+"日";
}
function g(e,t,n){
var o,m="",i=document.createElement("div"),s="http://mmbiz.qpic.cn/mmbiz/ByCS3p9sHiak6fjSeA7cianwo25C0CIt5ib8nAcZjW7QT1ZEmUo4r5iazzAKhuQibEXOReDGmXzj8rNg/0";
$={};
for(var c,a=0;c=e[a];++a){
c.time=u(c.create_time),c.status="",c.logo_url=c.logo_url||s,c.logo_url=-1!=c.logo_url.indexOf("wx.qlogo.cn")?c.logo_url.replace(/\/132$/,"/96"):c.logo_url,
c.content=c.content.htmlDecodeLite().htmlEncodeLite(),c.nick_name=c.nick_name.htmlDecodeLite().htmlEncodeLite(),
c.like_num_format=parseInt(c.like_num)>=1e4?(c.like_num/1e4).toFixed(1)+"万":c.like_num,
c.is_from_friend=c.is_from_friend||0,c.is_from_me="mine"==n?1:c.is_from_me||0,c.reply=c.reply||{
reply_list:[]
},c.is_mine=n?!1:!0,c.is_elected="elected"==n?1:c.is_elected,c.reply.reply_list.length>0&&(c.reply.reply_list[0].time=u(c.reply.reply_list[0].create_time),
c.reply.reply_list[0].content=(c.reply.reply_list[0].content||"").htmlEncodeLite(),
c.reply.reply_list[0].reply_like_status=c.reply.reply_list[0].reply_like_status||0,
c.reply.reply_list[0].reply_like_num=c.reply.reply_list[0].reply_like_num||0,c.reply.reply_list[0].reply_like_num_format=parseInt(c.reply.reply_list[0].reply_like_num)>=1e4?(c.reply.reply_list[0].reply_like_num/1e4).toFixed(1)+"万":c.reply.reply_list[0].reply_like_num),
c.new_appmsg=window.new_appmsg,m+=O.tmpl(D,c);
try{
var d=c.nick_name+c.content,r=!1,_=A.repeatContentID;
$[d]&&(r=!0,_=A.repeatContent),Z.indexOf(c.content_id)>-1&&(r=!0,_=A.repeatContentID),
Z.push(c.content_id),$[d]=!0,r&&l(_,encodeURIComponent(JSON.stringify({
comment_id:M,
content_id:c.content_id,
offset:F,
length:e.length,
url:location.href
})));
}catch(p){}
}
for(i.innerHTML=m,y(i);o=i.children.item(0);)t.appendChild(o);
}
function y(e){
S.each(e.querySelectorAll("div.discuss_message_content"),function(e){
e.innerHTML=U.encode(e.innerHTML);
});
}
function f(e){
return setTimeout(function(){
o(e);
});
}
function w(){
var e="1"===T.getParam("js_my_comment");
e&&h(!0);
}
function h(e){
i(X.article),m(X.mine),window.scrollTo(0,0),p(),e||S.later(function(){
X.input.focus();
});
}
function j(){
i(X.mine),m(X.article),window.scrollTo(0,document.documentElement.scrollHeight),
X.input.blur();
}
function b(e){
var t=e.delegatedTarget||e.srcElement,n=null;
if(B.hasClass(t,"js_comment_praise")&&(n=t),n){
var o=parseInt(n.dataset.status),m=0==o?1:0,i=n.dataset.contentId,s="/mp/appmsg_comment?action=likecomment&scene="+A.scene+"&like="+m+"&__biz="+biz+"&appmsgid="+appmsgid+"&comment_id="+M+"&content_id="+i;
I(n),R({
url:s,
type:"GET"
});
}
}
function v(e){
var t=e.delegatedTarget,n=parseInt(t.dataset.status),o=n?0:1,m=t.dataset.contentId,i=t.dataset.replyId;
I(t),R({
url:"/mp/appmsg_comment?action=like_author_reply&scene="+A.scene,
type:"post",
data:{
comment_id:M,
content_id:m,
reply_id:i,
like:o
}
});
}
function I(e){
var t=B.hasClass(e,"praised"),n=e.querySelector(".praise_num"),o=n.innerHTML,m=o.indexOf("万"),i=parseInt(o)?parseInt(o):0;
t?(-1==m&&(n.innerHTML=i-1>0?i-1:""),B.removeClass(e,"praised"),e.dataset.status=0):(-1==m&&(n.innerHTML=i+1),
B.addClass(e,"praised"),e.dataset.status=1);
}
function E(e){
var t=e.delegatedTarget,n=t.getAttribute("data-my-id"),s="/mp/appmsg_comment?action=delete&scene="+A.scene+"&__biz="+biz+"&appmsgid="+appmsgid+"&comment_id="+M+"&my_id="+n;
confirm("确定删除吗？")&&R({
url:s,
success:function(e){
var s,c=t;
try{
e=JSON.parse(e);
}catch(a){
e={};
}
if(0==e.ret){
for(;c&&(c.nodeType!=c.ELEMENT_NODE||"li"!=c.tagName.toLowerCase());)c=c.parentNode;
c&&(c.parentNode.removeChild(c),s=document.getElementById("cid"+n),s&&s.parentNode.removeChild(s),
0==X.list.children.length&&(i(X.main),i(document.getElementById("js_cmt_statement")),
i(document.getElementById("js_cmt_qa")),m(document.getElementById("js_cmt_addbtn2"))),
0==X.mylist.children.length&&i(X.mylist.parentNode));
}else o("删除失败，请重试");
},
error:function(){
o("网络错误，请重试");
}
});
}
function k(){
try{
var e=X.loading.getBoundingClientRect(),t=Math.random()<1;
e.top<window.innerHeight&&Y&&t&&((new Image).src="//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_45_1&lc=1&log0",
H.off(window,"scroll",k));
}catch(n){}
}
function C(e){
var t=document.createElement("a");
t.setAttribute("href",e),this.el=t,this.parser=this.el,this.getParam=function(e){
var t=new RegExp("([?&])"+e+"=([^&#]*)([&#])?"),n=this.el.search.match(t);
return n?n[2]:null;
};
}
var B=e("biz_common/dom/class.js"),D=e("appmsg/cmt_tpl.html.js"),x=document.getElementById("js_cmt_area"),T=new C(window.location.href),z=e("biz_common/utils/wxgspeedsdk.js"),L=location.href.indexOf("vconsole=1")>0||document.cookie&&document.cookie.indexOf("vconsole_open=1")>-1?!0:!1,M=0;
if(window._has_comment=!0,"undefined"!=typeof window.comment_id?M=window.comment_id:window.cgiData&&"undefined"!=typeof window.cgiData.comment_id&&(M=window.cgiData.comment_id),
!!L&&console.log("comment_id:"+M+";uin:"+uin+";key:"+key),-1==navigator.userAgent.indexOf("MicroMessenger")&&(x&&(x.style.display="none"),
M=0,window._has_comment=!1),0==M||!uin||!key)return void(window._has_comment=!1);
var H=e("biz_common/dom/event.js"),R=e("biz_wap/utils/ajax.js"),O=(e("biz_common/utils/string/html.js"),
e("biz_common/tmpl.js")),q=e("biz_wap/utils/fakehash.js"),N=e("appmsg/log.js"),A={
scene:0,
idkey:"",
moreList:27,
repeatList:25,
errList:18,
handleList:26,
addCommentErr:19,
errComment:18,
repeatContent:24,
repeatContentID:23
};
window.__commentReportData&&window.__commentReportData.idkey&&(!!L&&console.log("init reportData"),
A=window.__commentReportData),function(){
if(x){
var t=e("appmsg/comment_tpl.html.js");
x.innerHTML=O.tmpl(t,{
new_appmsg:window.new_appmsg
});
}
}(),function(){
var t=e("appmsg/my_comment_tpl.html.js"),n=document.createElement("div");
n.innerHTML=O.tmpl(t,{
new_appmsg:window.new_appmsg
}),document.body.appendChild(n);
}();
var U=e("appmsg/emotion/emotion.js"),S=e("appmsg/emotion/dom.js"),F=(new Image,0),P=100,Y=!1,J="",G="我",Q=0,X={
article:document.getElementById("js_article"),
mine:document.getElementById("js_cmt_mine"),
main:document.getElementById("js_cmt_main"),
input:document.getElementById("js_cmt_input"),
submit:document.getElementById("js_cmt_submit"),
addbtn:document.getElementById("js_cmt_addbtn"),
list:document.getElementById("js_cmt_list"),
mylist:document.getElementById("js_cmt_mylist"),
morelist:document.getElementById("js_cmt_morelist"),
toast:document.getElementById("js_cmt_toast"),
tips:document.getElementById("js_cmt_tips"),
loading:document.getElementById("js_cmt_loading")
},Z=[],$={},K=(new Image,[]),W=0,V=0,et=null,tt=+new Date;
!function(){
d(),w(),U.init();
}(),q.on("comment",function(){
!!L&&console.log("FakeHash on comment"),h();
}),q.on(function(e){
"comment"==e&&j();
}),H.on(X.input,"input",function(){
var e=c(X.input.value);
e.length<1?B.addClass(X.submit,"btn_disabled"):B.removeClass(X.submit,"btn_disabled");
}),H.on(X.list,"tap",".js_comment_praise",b),H.on(X.mylist,"tap",".js_comment_praise",b),
H.on(X.list,"tap",".js_reply_praise",v),H.on(X.list,"tap",".js_del",E),H.on(X.mylist,"tap",".js_del",E),
H.on(X.list,"tap",".js_del",function(e){
e.preventDefault();
}),H.on(X.mylist,"tap",".js_del",function(e){
e.preventDefault();
}),H.on(X.submit,"tap",_),H.on(X.submit,"click",function(e){
e.preventDefault();
}),H.on(window,"scroll",d),H.on(window,"scroll",k),H.on(document.getElementById("js_cmt_write1"),"click",function(e){
e.preventDefault(),!!L&&console.log("push comment"),q.push("comment");
}),H.on(document.getElementById("js_cmt_write2"),"click",function(e){
e.preventDefault(),!!L&&console.log("push comment"),q.push("comment");
});
});define("appmsg/like.js",["biz_common/dom/event.js","biz_common/dom/class.js","biz_wap/utils/ajax.js","appmsg/log.js"],function(require,exports,module,alert){
"use strict";
function like_report(e){
log("[Appmsg] click like");
var tmpAttr=el_like.getAttribute("like"),tmpHtml=el_likeNum.innerHTML,isLike=parseInt(tmpAttr)?parseInt(tmpAttr):0,like=isLike?0:1,likeNum=parseInt(tmpHtml)?parseInt(tmpHtml):0;
ajax({
url:"/mp/appmsg_like?__biz="+biz+"&mid="+mid+"&idx="+idx+"&like="+like+"&f=json&appmsgid="+appmsgid+"&itemidx="+itemidx,
data:{
is_temp_url:window.is_temp_url||0
},
type:"POST",
success:function(res){
log("[Appmsg] like succ");
var data=eval("("+res+")");
0==data.base_resp.ret&&(isLike?(Class.removeClass(el_like,"praised"),el_like.setAttribute("like",0),
likeNum>0&&"100000+"!==tmpHtml&&(el_likeNum.innerHTML=likeNum-1==0?"赞":likeNum-1)):(el_like.setAttribute("like",1),
Class.addClass(el_like,"praised"),"100000+"!==tmpHtml&&(el_likeNum.innerHTML=likeNum+1)));
},
async:!0
});
}
var DomEvent=require("biz_common/dom/event.js"),Class=require("biz_common/dom/class.js"),ajax=require("biz_wap/utils/ajax.js"),log=require("appmsg/log.js"),el_toolbar=document.getElementById("js_toobar3");
if(el_toolbar&&el_toolbar.querySelector){
var el_like=el_toolbar.querySelector("#like3"),el_likeNum=el_toolbar.querySelector("#likeNum3"),el_readNum=el_toolbar.querySelector("#readNum3");
DomEvent.on(el_like,"click",function(e){
return like_report(e),!1;
});
}
});define("pages/version4video.js",["biz_common/dom/event.js","biz_wap/jsapi/core.js","biz_wap/utils/device.js","new_video/ctl.js"],function(e){
"use strict";
function i(e,i){
i=i||"",i=["uin:"+top.window.user_uin,"resp:"+i].join("|"),(new Image).src="/mp/jsreport?key="+e+"&content="+i+"&r="+Math.random();
}
function o(){
return document.domain="qq.com",-1!=top.location.href.indexOf("&_newvideoplayer=0")?!1:-1!=top.location.href.indexOf("&_newvideoplayer=1")?!0:1!=top.window.is_login?!1:top.window.use_tx_video_player?!1:r.canSupportVideo&&_.inWechat?_.is_ios||_.is_android&&_.is_x5?!0:!1:(top.window._hasReportCanSupportVideo||r.canSupportVideo||!_.inWechat||(top.window._hasReportCanSupportVideo=!0,
i(44)),!1);
}
function n(){
{
var e=top.location.href,i=window.location.href;
top.sn||"";
}
return-1==e.indexOf("&_videoad=0")||"5a2492d450d45369cd66e9af8ee97dbd"!=top.sn&&"f62e1cb98630008303667f77c17c43d7"!=top.sn&&"30c609ee11a3a74a056e863f0e20cae2"!=top.sn?-1!=e.indexOf("&_videoad=1")?!0:-1==e.indexOf("mp.weixin.qq.com/s")&&-1==e.indexOf("mp.weixin.qq.com/mp/appmsg/show")?!1:"54"==top.window.appmsg_type?!1:-1!=i.indexOf("&xd=1")?!1:top.window.__appmsgCgiData&&top.window.__appmsgCgiData.can_use_page&&(_.is_ios||_.is_android)?!0:p.showAd()?!0:!1:!1;
}
function t(){
var e=top.location.href;
if(!top.window.user_uin)return!1;
if(-1!=e.indexOf("&_proxy=1"))return!0;
if(-1!=e.indexOf("&_proxy=0"))return!1;
if(-1==e.indexOf("mp.weixin.qq.com/s")&&-1==e.indexOf("mp.weixin.qq.com/mp/appmsg/show"))return!1;
var i=(new Date).getHours();
return i>=9&&14>=i?!1:_.inWechat&&_.is_android&&_.is_x5&&_.wechatVer>="6.2.2"?!0:_.inWechat&&_.is_ios&&(-1!=w.indexOf("MicroMessenger/6.2.4")||_.wechatVer>="6.2.4")?!0:!1;
}
function s(){
return c.networkType;
}
var a=e("biz_common/dom/event.js"),d=e("biz_wap/jsapi/core.js"),r=e("biz_wap/utils/device.js"),p=e("new_video/ctl.js"),w=top.window.navigator.userAgent,c={
networkType:""
},_={};
return function(e){
var i=r.os;
_.is_ios=/(iPhone|iPad|iPod|iOS)/i.test(e),_.is_android=!!i.android,_.is_wp=!!i.phone,
_.is_pc=!(i.phone||!i.Mac&&!i.windows),_.inWechat=/MicroMessenger/.test(e),_.inWindowWechat=/WindowsWechat/i.test(e),
_.inMacWechat=/wechat.*mac os/i.test(e),_.is_android_phone=_.is_android&&/Mobile/i.test(e),
_.is_android_tablet=_.is_android&&!/Mobile/i.test(e),_.ipad=/iPad/i.test(e),_.iphone=!_.ipad&&/(iphone)\sos\s([\d_]+)/i.test(e),
_.is_x5=/TBS\//.test(e)&&/MQQBrowser/i.test(e);
var o=e.match(/MicroMessenger\/((\d+)(\.\d+)*)/);
_.wechatVer=o&&o[1]||0,a.on(window,"load",function(){
if(""==c.networkType&&_.inWechat){
var e={
"network_type:fail":"fail",
"network_type:edge":"2g/3g",
"network_type:wwan":"2g/3g",
"network_type:wifi":"wifi"
};
d.invoke("getNetworkType",{},function(i){
c.networkType=e[i.err_msg]||"fail";
});
}
},!1);
}(top.window.navigator.userAgent),"undefined"==typeof top.window._hasReportCanSupportVideo&&(top.window._hasReportCanSupportVideo=!1),
{
device:_,
isShowMpVideo:o,
isUseProxy:t,
isUseAd:n,
getNetworkType:s
};
});define("a/a.js",["biz_wap/utils/mmversion.js","biz_common/dom/event.js","biz_common/utils/url/parse.js","a/a_report.js","biz_wap/utils/ajax.js","biz_wap/utils/position.js","a/card.js","a/wxopen_card.js","a/mpshop.js","biz_wap/jsapi/core.js","biz_common/tmpl.js","a/a_tpl.html.js","a/sponsor_a_tpl.html.js","a/cpc_a_tpl.html.js","biz_common/utils/report.js","biz_common/dom/class.js","biz_wap/utils/storage.js","appmsg/log.js","appmsg/cdn_img_lib.js","a/profile.js","a/android.js","a/ios.js","a/app_card.js","a/sponsor.js"],function(require,exports,module,alert){
"use strict";
function report(e,a){
Report("http://mp.weixin.qq.com/mp/ad_report?action=follow&type="+e+a);
}
function checkNeedAds(){
var is_need_ad=1,_adInfo=null,screen_num=0,both_ad=0,inwindowwx=-1!=navigator.userAgent.indexOf("WindowsWechat");
if(!document.getElementsByClassName||-1==navigator.userAgent.indexOf("MicroMessenger")||inwindowwx)is_need_ad=0,
js_sponsor_ad_area.style.display="none",js_top_ad_area.style.display="none",js_bottom_ad_area.style.display="none",
js_cpc_area&&js_cpc_area.style&&(js_cpc_area.style.display="none");else{
var adLS=new LS("ad");
if(window.localStorage)try{
var key=[biz,sn,mid,idx].join("_"),_ad=adLS.get(key);
_adInfo=_ad.info;
try{
_adInfo=eval("("+_adInfo+")");
}catch(e){
_adInfo=null;
}
var _adInfoSaveTime=_ad.time,_now=+new Date;
_adInfo&&18e4>_now-1*_adInfoSaveTime&&1*_adInfo.advertisement_num>0?is_need_ad=0:adLS.remove(key),
log("[Ad] is_need_ad: "+is_need_ad+" , adData:"+JSON.stringify(_ad));
}catch(e){
is_need_ad=1,_adInfo=null;
}
}
return screen_num=Math.ceil(document.body.scrollHeight/(document.documentElement.clientHeight||window.innerHeight)),
both_ad=screen_num>=2?1:0,{
is_need_ad:is_need_ad,
both_ad:both_ad,
_adInfo:_adInfo
};
}
function afterGetAdData(e,a){
var t={},o=e.is_need_ad,p=e._adInfo;
if(0==o)t=p,t||(t={
advertisement_num:0
});else{
if(a.advertisement_num>0&&a.advertisement_info){
var i=a.advertisement_info;
t.advertisement_info=saveCopy(i);
}
t.advertisement_num=a.advertisement_num;
}
1==o&&(window._adRenderData=t),t=t||{
advertisement_num:0
};
var n=!1;
if(!t.flag&&t.advertisement_num>0){
var r=t.advertisement_num,_=t.advertisement_info;
window.adDatas.num=r;
for(var s=0;r>s;++s){
var d=null,c=_[s];
if(c.exp_info=c.exp_info||{},c.is_cpm=c.is_cpm||0,c.biz_info=c.biz_info||{},c.app_info=c.app_info||{},
c.pos_type=c.pos_type||0,c.logo=c.logo||"",100==c.pt||115==c.pt){
for(var l=c.exp_info.exp_value||[],m=!1,u=0,f=0;f<l.length;++f){
var g=l[f]||{};
if(1==g.exp_type&&(u=g.comm_attention_num,m=u>0),2==g.exp_type){
m=!1,u=0;
break;
}
}
c.biz_info.show_comm_attention_num=m,c.biz_info.comm_attention_num=u,d={
usename:c.biz_info.user_name,
pt:c.pt,
url:c.url,
traceid:c.traceid,
adid:c.aid,
ticket:c.ticket,
is_appmsg:!0
};
}else if(102==c.pt)d={
appname:c.app_info.app_name,
versioncode:c.app_info.version_code,
pkgname:c.app_info.apk_name,
androiddownurl:c.app_info.apk_url,
md5sum:c.app_info.app_md5,
signature:c.app_info.version_code,
rl:c.rl,
traceid:c.traceid,
pt:c.pt,
ticket:c.ticket,
type:c.type,
adid:c.aid,
is_appmsg:!0
};else if(101==c.pt)d={
appname:c.app_info.app_name,
app_id:c.app_info.app_id,
icon_url:c.app_info.icon_url,
appinfo_url:c.app_info.appinfo_url,
rl:c.rl,
traceid:c.traceid,
pt:c.pt,
ticket:c.ticket,
type:c.type,
adid:c.aid,
is_appmsg:!0
};else if(103==c.pt||104==c.pt||2==c.pt&&c.app_info){
var y=c.app_info.down_count||0,v=c.app_info.app_size||0,h=c.app_info.app_name||"",j=c.app_info.category,w=["万","百万","亿"];
if(y>=1e4){
y/=1e4;
for(var k=0;y>=10&&2>k;)y/=100,k++;
y=y.toFixed(1)+w[k]+"次";
}else y=y.toFixed(1)+"次";
v=formSize(v),j=j?j[0]||"其他":"其他",h=formName(h),c.app_info._down_count=y,c.app_info._app_size=v,
c.app_info._category=j,c.app_info.app_name=h,d={
appname:c.app_info.app_name,
app_rating:c.app_info.app_rating||0,
icon_url:c.app_info.icon_url,
app_id:c.app_info.app_id,
channel_id:c.app_info.channel_id,
md5sum:c.app_info.app_md5,
rl:c.rl,
pkgname:c.app_info.apk_name,
url_scheme:c.app_info.url_scheme,
androiddownurl:c.app_info.apk_url,
versioncode:c.app_info.version_code,
appinfo_url:c.app_info.appinfo_url,
traceid:c.traceid,
pt:c.pt,
url:c.url,
ticket:c.ticket,
type:c.type,
adid:c.aid,
is_appmsg:!0
};
}else if(105==c.pt){
var b=c.card_info.card_id||"",x=c.card_info.card_ext||"";
x=x.htmlDecode();
try{
x=JSON.parse(x),x.outer_str=c.card_info.card_outer_id||"",x=JSON.stringify(x);
}catch(I){
x="{}";
}
d={
card_id:b,
card_ext:x,
pt:c.pt,
ticket:c.ticket||"",
url:c.url,
rl:c.rl,
tid:c.traceid,
traceid:c.traceid,
type:c.type,
adid:c.aid,
is_appmsg:!0
};
}else if(106==c.pt){
var z=c.mp_shop_info.pid||"",E=c.mp_shop_info.outer_id||"";
d={
pid:z,
outer_id:E,
pt:c.pt,
url:c.url,
rl:c.rl,
tid:c.traceid,
traceid:c.traceid,
type:c.type,
adid:c.aid,
is_appmsg:!0
};
}else if(108==c.pt||109==c.pt||110==c.pt||116==c.pt||117==c.pt)d={
pt:c.pt,
ticket:c.ticket||"",
url:c.url,
traceid:c.traceid,
adid:c.aid,
is_appmsg:!0
},c.video_info&&(d.displayWidth=c.video_info.displayWidth,d.displayHeight=c.video_info.displayHeight,
d.thumbUrl=c.video_info.thumbUrl,d.videoUrl=c.video_info.videoUrl,d.rl=c.rl);else if(111==c.pt||113==c.pt||114==c.pt||112==c.pt){
var v=c.app_info.app_size||0,h=c.app_info.app_name||"";
v=formSize(v),h=formName(h),c.app_info.app_size=v,c.app_info.app_name=h,d={
appname:c.app_info.app_name,
app_rating:c.app_info.app_rating||0,
app_id:c.app_info.app_id,
icon_url:c.app_info.icon_url,
channel_id:c.app_info.channel_id,
md5sum:c.app_info.app_md5,
rl:c.rl,
pkgname:c.app_info.apk_name,
url_scheme:c.app_info.url_scheme,
androiddownurl:c.app_info.apk_url,
versioncode:c.app_info.version_code,
appinfo_url:c.app_info.appinfo_url,
traceid:c.traceid,
pt:c.pt,
url:c.url,
ticket:c.ticket,
type:c.type,
adid:c.aid,
source:source||"",
is_appmsg:!0
};
}else 118==c.pt&&(d=c,n=!0);
var T=c.image_url;
require("appmsg/cdn_img_lib.js"),T&&T.isCDN()&&(T=T.replace(/\/0$/,"/640"),T=T.replace(/\/0\?/,"/640?"),
c.image_url=ParseJs.addParam(T,"wxfrom","50",!0)),adDatas.ads["pos_"+c.pos_type]={
a_info:c,
adData:d
},localStorage&&localStorage.setItem&&c.app_info&&c.app_info.url_scheme&&localStorage.setItem("__WXLS__a_url_schema_"+c.traceid,c.app_info.url_scheme);
}
c.has_installed=!1,c&&(104==c.pt||113==c.pt||114==c.pt||2==c.pt)&&c.app_info.url_scheme&&JSAPI.invoke("getInstallState",{
packageName:c.app_info.apk_name
},function(e){
var a=e.err_msg;
a.indexOf("get_install_state:yes")>-1&&(c.has_installed=!0,document.getElementById("js_promotion_tag")&&(document.getElementById("js_promotion_tag").innerHTML="进入应用"));
});
var q=function(e){
var a=window.pageYOffset||document.documentElement.scrollTop||document.body.scrollTop;
"undefined"!=typeof e&&(a=e);
10>=a&&(js_top_ad_area.style.display="block",DomEvent.off(window,"scroll",q));
},C=function(){
var e=window.pageYOffset||document.documentElement.scrollTop||document.body.scrollTop,a=document.documentElement.clientHeight||window.innerHeight;
js_sponsor_ad_area.offsetTop<e+a&&(Class.addClass(document.getElementById("js_ad_area"),"show"),
DomEvent.off(window,"scroll",C));
},B=adDatas.ads;
for(var A in B)if(0==A.indexOf("pos_")){
var d=B[A],c=!!d&&d.a_info;
if(d&&c){
if(0==c.pos_type){
if(c.new_appmsg=window.new_appmsg,js_bottom_ad_area.innerHTML=TMPL.tmpl(a_tpl,c),
111==c.pt||112==c.pt||113==c.pt||114==c.pt){
var D=document.getElementsByClassName("js_download_app_card")[0],O=D.offsetWidth,S=Math.floor(O/2.875);
S>0&&(D.style.height=S+"px");
}
}else if(1==c.pos_type){
js_top_ad_area.style.display="none",c.new_appmsg=window.new_appmsg,js_top_ad_area.innerHTML=TMPL.tmpl(a_tpl,c),
DomEvent.on(window,"scroll",q);
var N=0;
window.localStorage&&(N=1*localStorage.getItem(A)||0),window.scrollTo(0,N),q(N);
}else if(3==c.pos_type){
var D=document.createElement("div");
D.appendChild(document.createTextNode(c.image_url)),c.image_url=D.innerHTML,c.new_appmsg=window.new_appmsg,
js_sponsor_ad_area.innerHTML=TMPL.tmpl(sponsor_a_tpl,c),js_sponsor_ad_area.style.display="block";
var H=js_sponsor_ad_area.clientWidth;
108==c.pt||109==c.pt||110==c.pt?document.getElementById("js_main_img").style.height=H/1.77+"px":116==c.pt||117==c.pt,
DomEvent.on(window,"scroll",C),C(0);
}else 4==c.pos_type&&_checkShowCpc()&&(js_cpc_area.innerHTML=TMPL.tmpl(cpc_a_tpl,c));
lazyLoadAdImg({
aid:c.aid,
type:c.pt
}),checkAdImg(c);
}
}
mmversion.isIOS&&c.app_info&&c.app_info.url_scheme&&0==c.app_info.url_scheme.indexOf("http")&&(document.getElementById("js_promotion_tag")&&(document.getElementById("js_promotion_tag").innerHTML="查看应用"),
document.getElementsByClassName("js_ad_btn")&&document.getElementsByClassName("js_ad_btn").length>0&&(document.getElementsByClassName("js_ad_btn")[0].innerHTML="查看")),
bindAdOperation();
}
is_temp_url&&document.getElementsByTagName("mpcpc").length>0&&_checkShowCpc()&&!n&&(js_cpc_area.innerHTML=TMPL.tmpl(cpc_a_tpl,{
type:"",
ticket:"",
url:"",
rl:"",
aid:"",
pt:"",
traceid:"",
group_id:"",
apurl:"",
is_cpm:"",
image_url:"https://mmbiz.qlogo.cn/mmbiz_png/4whpV1VZl28zEsn4C4aKo3TLTWAsFI9fnd6F4VubeMIlncQTBbCvickQLSgSZZz3UjTFnoGFprqiadcCLGYF7VyQ/0?wx_fmt=png"
}));
}
function _checkShowCpc(){
var e=(document.documentElement.clientHeight||window.innerHeight)/2,a=js_cpc_area.offsetTop,t=document.getElementById("js_content").offsetHeight;
return console.log(e,a,t,e>a||e>t-a),e>a||e>t-a?!1:!0;
}
function lazyLoadAdImg(e){
for(var a=document.getElementsByClassName("js_alazy_img"),t=0;t<a.length;t++){
var o=a[t];
a[t].onload=function(){
window.__addIdKeyReport("28307",54),o.src.indexOf("retry")>-1&&window.__addIdKeyReport("28307",69);
},a[t].onerror=function(){
if(-1==o.src.indexOf("retry"))o.src=ParseJs.addParam(o.src,"retry",1);else{
window.__addIdKeyReport("28307",98);
var a="other";
mmversion.isIOS?a="iphone":mmversion.isAndroid&&(a="android"),window.setTimeout(function(){
var t=window.networkType||"unknow";
ajax({
url:"http://mp.weixin.qq.com/tp/datacenter/report?cmd=report&id=900023&os="+a+"&uin=777&aid="+e.aid+"&image_url="+encodeURIComponent(o.src)+"&type="+e.type+"&network="+t,
type:"GET",
async:!0
});
},500);
}
window.__addIdKeyReport("28307",57);
},a[t].src=a[t].dataset.src;
}
}
function getHost(e){
if(!e)return"";
var a=document.createElement("a");
return a.href=e,a.hostname;
}
function checkAdImg(e){
if(e){
var a=["wximg.qq.com","wximg.gtimg.com","pgdt.gtimg.cn","mmsns.qpic.cn","mmbiz.qpic.cn","vweixinthumb.tc.qq.com","pp.myapp.com","wx.qlog.cn","mp.weixin.qq.com"],t=e.image_url||"",o=getHost(t);
return void(o&&-1==a.indexOf(o)&&window.__addIdKeyReport("28307",58));
}
}
function saveCopyArr(e){
for(var a=[],t=0;t<e.length;++t){
var o=e[t],p=typeof o;
o="string"==p?o.htmlDecode():o,"object"==p&&(o="[object Array]"==Object.prototype.toString.call(o)?saveCopyArr(o):saveCopy(o)),
a.push(o);
}
return a;
}
function saveCopy(e){
var a={};
for(var t in e)if(e.hasOwnProperty(t)){
var o=e[t],p=typeof o;
o="string"==p?o.htmlDecode():o,"object"==p&&(o="[object Array]"==Object.prototype.toString.call(o)?saveCopyArr(o):saveCopy(o)),
a[t]=o;
}
return a;
}
function formName(e){
for(var a=[" ","-","(",":",'"',"'","：","（","—","－","“","‘"],t=-1,o=0,p=a.length;p>o;++o){
var i=a[o],n=e.indexOf(i);
-1!=n&&(-1==t||t>n)&&(t=n);
}
return-1!=t&&(e=e.substring(0,t)),e;
}
function formSize(e){
return"number"!=typeof e?e:(e>=1024?(e/=1024,e=e>=1024?(e/1024).toFixed(2)+"MB":e.toFixed(2)+"KB"):e=e.toFixed(2)+"B",
e);
}
function seeAds(){
var adDatas=window.adDatas;
if(adDatas&&adDatas.num>0){
var onScroll=function(){
for(var scrollTop=window.pageYOffset||document.documentElement.scrollTop,i=0;total_pos_type>i;++i)!function(i){
var pos_key="pos_"+i,gdt_a=gdt_as[pos_key];
if(gdt_a=!!gdt_a&&gdt_a[0],gdt_a&&gdt_a.dataset&&gdt_a.dataset.apurl){
var gid=gdt_a.dataset.gid,tid=gdt_a.dataset.tid,apurl=gdt_a.dataset.apurl,is_cpm=1*gdt_a.dataset.is_cpm,ads=adDatas.ads,a_info=ads[pos_key].a_info||{},exp_info=a_info.exp_info||{},exp_id=exp_info.exp_id||"",exp_value=exp_info.exp_value||[],pos_type=adDatas.ads[pos_key].a_info.pos_type,gdt_area=el_gdt_areas[pos_key],offsetTop=gdt_area.offsetTop,adHeight=gdt_a.clientHeight,adOffsetTop=offsetTop+gdt_a.offsetTop;
adDatas.ads[pos_key].ad_engine=0;
try{
exp_value=JSON.stringify(exp_value);
}catch(e){
exp_value="[]";
}
if(-1!=apurl.indexOf("ad.wx.com")&&(adDatas.ads[pos_key].ad_engine=1),function(){
try{
var e=window.__report,a=ping_test_apurl[pos_key],t=new Date,o=t.getHours(),p=ping_test_apurl_random&&o>=12&&18>=o&&0==pos_type;
!a[0]&&p&&scrollTop+innerHeight>offsetTop&&(a[0]=!0,e(81)),!a[1]&&p&&scrollTop+innerHeight>offsetTop+40&&(a[1]=!0,
e(82));
}catch(i){}
}(),!ping_apurl[pos_key]&&(0==pos_type&&scrollTop+innerHeight>offsetTop||1==pos_type&&(10>=scrollTop||scrollTop-10>=offsetTop)||4==pos_type&&scrollTop+innerHeight>offsetTop||3==pos_type&&scrollTop+innerHeight>offsetTop)){
ping_apurl[pos_key]=!0;
try{
var report_arg="trace_id="+tid+"&product_type="+adDatas.ads[pos_key].a_info.pt+"&logtype=2&url="+encodeURIComponent(location.href)+"&apurl="+encodeURIComponent(apurl);
tid&&mmversion.gtVersion("6.3.22",!0)&&JSAPI.invoke("adDataReport",{
ad_info:report_arg
},function(){});
}catch(e){}
log("[Ad] seeAd, tid="+tid+", gid="+gid+", pos_type="+pos_type),ajax({
url:"/mp/advertisement_report?report_type=1&tid="+tid+"&adver_group_id="+gid+"&apurl="+encodeURIComponent(apurl)+"&__biz="+biz+"&pos_type="+pos_type+"&exp_id="+exp_id+"&exp_value="+exp_value+"&r="+Math.random(),
mayAbort:!0,
success:function(res){
log("[Ad] seeAd report success, tid="+tid+", gid="+gid+", pos_type="+pos_type);
try{
res=eval("("+res+")");
}catch(e){
res={};
}
res&&0!=res.ret?ping_apurl[pos_key]=!1:ping_apurl.pos_0&&ping_apurl.pos_1;
},
error:function(){
log("[Ad] seeAd report error, tid="+tid+", gid="+gid+", pos_type="+pos_type),(new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_27_1";
},
async:!0
});
}
var ping_cpm_apurl_obj=ping_cpm_apurl[pos_key];
if(is_cpm&&!ping_cpm_apurl_obj.hasPing){
var rh=.5;
scrollTop+innerHeight>=adOffsetTop+adHeight*rh&&adOffsetTop+adHeight*(1-rh)>=scrollTop?3==pos_type?(ping_cpm_apurl_obj.hasPing=!0,
ajax({
url:"/mp/advertisement_report?report_type=1&tid="+tid+"&adver_group_id="+gid+"&apurl="+encodeURIComponent(apurl+"&viewable=true")+"&__biz="+biz+"&pos_type="+pos_type+"&r="+Math.random(),
mayAbort:!0,
success:function(res){
try{
res=eval("("+res+")");
}catch(e){
res={};
}
res&&0!=res.ret&&(ping_cpm_apurl_obj.hasPing=!1);
},
async:!0
})):ping_cpm_apurl_obj.clk||(ping_cpm_apurl_obj.clk=setTimeout(function(){
ping_cpm_apurl_obj.hasPing=!0,ajax({
url:"/mp/advertisement_report?report_type=1&tid="+tid+"&adver_group_id="+gid+"&apurl="+encodeURIComponent(apurl+"&viewable=true")+"&__biz="+biz+"&pos_type="+pos_type+"&exp_id="+exp_id+"&exp_value="+exp_value+"&r="+Math.random(),
mayAbort:!0,
success:function(res){
try{
res=eval("("+res+")");
}catch(e){
res={};
}
res&&0!=res.ret&&(ping_cpm_apurl_obj.hasPing=!1);
},
async:!0
});
},1001)):3!=pos_type&&ping_cpm_apurl_obj.clk&&(clearTimeout(ping_cpm_apurl_obj.clk),
ping_cpm_apurl_obj.clk=null);
}
}
}(i);
};
DomEvent.on(window,"scroll",onScroll),onScroll();
}
}
function ad_click(e,a,t,o,p,i,n,r,_,s,d,c,l,m,u,f,g){
if(!has_click[p]){
has_click[p]=!0;
var y=document.getElementById("loading_"+p);
y&&(y.style.display="inline");
var v=g.exp_info||{},h=v.exp_id||"",j=v.exp_value||[];
try{
j=JSON.stringify(j);
}catch(w){
j="[]";
}
AdClickReport({
click_pos:1,
report_type:2,
type:e,
exp_id:h,
exp_value:j,
url:encodeURIComponent(a),
tid:p,
rl:encodeURIComponent(t),
__biz:biz,
pos_type:s,
pt:_,
pos_x:l,
pos_y:m,
ad_w:u,
ad_h:f
},function(){
if(has_click[p]=!1,y&&(y.style.display="none"),"5"==e)location.href="/mp/profile?source=from_ad&tousername="+a+"&ticket="+i+"&uin="+uin+"&key="+key+"&__biz="+biz+"&mid="+mid+"&idx="+idx+"&tid="+p;else{
if("105"==_&&c)return void Card.openCardDetail(c.card_id,c.card_ext,c);
if("106"==_&&c)return void(location.href=ParseJs.join(a,{
outer_id:c.outer_id
}));
if("118"==_)return void Wxopen_card.openWxopen(c);
if(g&&g.has_installed&&("104"==_||"113"==_||"114"==_||"2"==_&&-1==a.indexOf("itunes.apple.com"))&&g.app_info.url_scheme)return void JSAPI.invoke("launchApplication",{
schemeUrl:g.app_info.url_scheme
},function(e){
-1==e.err_msg.indexOf("ok")&&(location.href=g.app_info.url_scheme);
});
if(0==a.indexOf("https://itunes.apple.com/")||0==a.indexOf("http://itunes.apple.com/"))return g.app_info&&g.app_info.url_scheme&&0==g.app_info.url_scheme.indexOf("http")||JSAPI.invoke("downloadAppInternal",{
appUrl:a
},function(e){
e.err_msg&&-1!=e.err_msg.indexOf("ok")||(location.href="http://"+location.host+"/mp/ad_redirect?url="+encodeURIComponent(a)+"&ticket="+i+"#wechat_redirect");
}),!1;
if(-1==a.indexOf("mp.weixin.qq.com"))a="http://mp.weixinbridge.com/mp/wapredirect?url="+encodeURIComponent(a);else if(-1==a.indexOf("mp.weixin.qq.com/s")&&-1==a.indexOf("mp.weixin.qq.com/mp/appmsg/show")){
var t={
source:4,
tid:p,
idx:idx,
mid:mid,
appuin:biz,
pt:_,
aid:r,
ad_engine:d,
pos_type:s
},o=window.__report;
if(("104"==_||"113"==_||"114"==_)&&c||-1!=a.indexOf("mp.weixin.qq.com/mp/ad_app_info")){
var n="",l="";
c&&(n=c.pkgname&&c.pkgname.replace(/\./g,"_"),l=c.channel_id||""),t={
source:4,
tid:p,
traceid:p,
mid:mid,
idx:idx,
appuin:biz,
pt:_,
channel_id:l,
aid:r,
engine:d,
pos_type:s,
pkgname:n
};
}
a=URL.join(a,t),(0==a.indexOf("http://mp.weixin.qq.com/promotion/")||0==a.indexOf("https://mp.weixin.qq.com/promotion/"))&&(a=URL.join(a,{
traceid:p,
aid:r,
engine:d
})),!r&&o&&o(80,a);
}
location.href=a;
}
});
}
}
function bindAdOperation(){
seeAds();
for(var e=0;total_pos_type>e;++e)!function(e){
var a="pos_"+e,t=el_gdt_areas[a];
if(!t)return!1;
if(!t.getElementsByClassName&&t.style)return t.style.display="none",!1;
var o=t.getElementsByClassName("js_ad_link")||[],p=adDatas.ads[a];
if(p){
for(var i=p.adData,n=p.a_info,r=n.pos_type,_=p.ad_engine,s=0,d=o.length;d>s;++s)!function(e,a){
var t=o[e],p=t.dataset;
if(p&&3!=n.pos_type){
var i=p.type,s=p.url,d=p.rl,c=p.apurl,l=p.tid,m=p.ticket,u=p.group_id,f=p.aid,g=p.pt;
DomEvent.on(t,"click",function(e){
var t=!!e&&e.target;
return!t||!t.className||-1==t.className.indexOf("js_ad_btn")&&-1==t.className.indexOf("btn_processor_value")?(mmversion.isIOS&&n.app_info&&n.app_info.url_scheme&&0==n.app_info.url_scheme.indexOf("http")&&(location.href=n.app_info.url_scheme),
window.setTimeout(function(){
if(a){
a.adid=window.adid||a.adid;
var o="&tid="+a.traceid+"&uin="+uin+"&key="+key+"&ticket="+(a.ticket||"")+"&__biz="+biz+"&source="+source+"&scene="+scene+"&appuin="+biz+"&aid="+a.adid+"&ad_engine="+_+"&pos_type="+r+"&r="+Math.random();
n&&n.has_installed&&("104"==a.pt||"113"==a.pt||"114"==a.pt||"2"==a.pt)?report(114,o):"103"==a.pt||"111"==a.pt||"112"==a.pt?report(23,o):("104"==a.pt||"113"==a.pt||"114"==a.pt)&&report(25,o);
}
var p,y,v,h;
p=position.getX(t,"js_ad_link")+e.offsetX,y=position.getY(t,"js_ad_link")+e.offsetY,
v=document.getElementsByClassName("js_ad_link")[0]&&document.getElementsByClassName("js_ad_link")[0].clientWidth,
h=document.getElementsByClassName("js_ad_link")[0]&&document.getElementsByClassName("js_ad_link")[0].clientHeight,
ad_click(i,s,d,c,l,m,u,f,g,r,_,a,p,y,v,h,n),log("[Ad] ad_click: type="+i+", url="+s+", rl="+d+", apurl="+c+", traceid="+l+", ticket="+m+", group_id="+u+", aid="+f+", pt="+g+", pos_type="+r+", ad_engine="+_);
},0),!1):void 0;
},!0);
}
}(s,i);
if(i){
i.adid=window.adid||i.adid;
var c=n.exp_info||{},l=c.exp_id||"",m=c.exp_value||[];
try{
m=JSON.stringify(m);
}catch(u){
m="[]";
}
var f="&tid="+i.traceid+"&uin="+uin+"&key="+key+"&ticket="+(i.ticket||"")+"&__biz="+biz+"&source="+source+"&scene="+scene+"&appuin="+biz+"&aid="+i.adid+"&ad_engine="+_+"&pos_type="+r+"&exp_id="+l+"&exp_value="+m+"&r="+Math.random();
if(i.report_param=f,"100"==i.pt||"115"==i.pt){
var g=require("a/profile.js");
return void new g({
btnViewProfile:document.getElementById("js_view_profile_"+r),
btnAddContact:document.getElementById("js_add_contact_"+r),
adData:i,
pos_type:r,
report_param:f,
aid:i.adid,
ad_engine:_
});
}
if("102"==i.pt){
var y=require("a/android.js"),v=15,h=i.pkgname&&i.pkgname.replace(/\./g,"_");
return void new y({
btn:document.getElementById("js_app_action_"+r),
adData:i,
report_param:f,
task_ext_info:[i.adid,i.traceid,h,source,v,_].join("."),
via:[i.traceid,i.adid,h,source,v,_].join(".")
});
}
if("101"==i.pt){
var j=require("a/ios.js");
return void new j({
btn:document.getElementById("js_app_action_"+r),
adData:i,
ticket:i.ticket,
report_param:f
});
}
if("105"==i.pt)return void new Card({
btn:document.getElementById("js_card_action_"+r),
adData:i,
report_param:f,
pos_type:r
});
if("106"==i.pt)return void new MpShop({
btn:document.getElementById("js_shop_action_"+r),
adData:i,
report_param:f,
pos_type:r
});
if("103"==i.pt||"104"==i.pt||"111"==i.pt||"112"==i.pt||"113"==i.pt||"114"==i.pt){
var w=require("a/app_card.js"),v=15,h=i.pkgname&&i.pkgname.replace(/\./g,"_");
return void new w({
btn:document.getElementById("js_appdetail_action_"+r),
js_app_rating:document.getElementById("js_app_rating_"+r),
adData:i,
report_param:f,
pos_type:r,
url_scheme:i.url_scheme,
via:[i.traceid,i.adid,h,source,v,_].join("."),
ticket:i.ticket,
appdetail_params:["&aid="+i.adid,"traceid="+i.traceid,"pkgname="+h,"source="+source,"type="+v,"engine="+_,"appuin="+biz,"pos_type="+r,"ticket="+i.ticket,"scene="+scene].join("&"),
engine:_
});
}
if("108"==i.pt||"109"==i.pt||"110"==i.pt||"116"==i.pt||"117"==i.pt){
var k=require("a/sponsor.js");
new k({
adDetailBtn:document.getElementById("js_ad_detail"),
adMoreBtn:document.getElementById("js_ad_more"),
adAbout:document.getElementById("js_btn_about"),
adImg:document.getElementById("js_main_img"),
adMessage:document.getElementById("js_ad_message"),
adVideo:document.getElementById("js_video_container"),
adData:i,
a_info:n,
pos_type:r,
report_param:f
});
}
"118"==n.pt&&(i.report_param=f);
}
}
}(e);
}
var mmversion=require("biz_wap/utils/mmversion.js"),js_bottom_ad_area=document.getElementById("js_bottom_ad_area"),js_top_ad_area=document.getElementById("js_top_ad_area"),js_sponsor_ad_area=document.getElementById("js_sponsor_ad_area"),js_cpc_area=document.getElementsByTagName("mpcpc"),gdt_pos_4={};
js_cpc_area.length>0?(js_cpc_area=document.getElementsByTagName("mpcpc")[0],gdt_pos_4=js_cpc_area.getElementsByClassName("js_ad_link")):js_cpc_area=void 0;
var pos_type=window.pos_type||0,__report=window.__report,total_pos_type=5,el_gdt_areas={
pos_4:js_cpc_area,
pos_3:js_sponsor_ad_area,
pos_1:js_top_ad_area,
pos_0:js_bottom_ad_area
},gdt_as={
pos_4:gdt_pos_4,
pos_3:js_sponsor_ad_area.getElementsByClassName("js_ad_link"),
pos_1:js_top_ad_area.getElementsByClassName("js_ad_link"),
pos_0:js_bottom_ad_area.getElementsByClassName("js_ad_link")
};
window.adDatas={
ads:{},
num:0
};
var adDatas=window.adDatas,has_click={},DomEvent=require("biz_common/dom/event.js"),URL=require("biz_common/utils/url/parse.js"),AReport=require("a/a_report.js"),AdClickReport=AReport.AdClickReport,ajax=require("biz_wap/utils/ajax.js"),position=require("biz_wap/utils/position.js"),Card=require("a/card.js"),Wxopen_card=require("a/wxopen_card.js"),MpShop=require("a/mpshop.js"),JSAPI=require("biz_wap/jsapi/core.js"),ParseJs=require("biz_common/utils/url/parse.js"),TMPL=require("biz_common/tmpl.js"),a_tpl=require("a/a_tpl.html.js"),sponsor_a_tpl=require("a/sponsor_a_tpl.html.js"),cpc_a_tpl=require("a/cpc_a_tpl.html.js"),Report=require("biz_common/utils/report.js"),Class=require("biz_common/dom/class.js"),LS=require("biz_wap/utils/storage.js"),ParseJs=require("biz_common/utils/url/parse.js"),log=require("appmsg/log.js"),ping_apurl={
pos_0:!1,
pos_1:!1,
pos_3:!1,
pos_4:!1
},ping_cpm_apurl={
pos_0:{},
pos_1:{},
pos_3:{},
pos_4:{}
},ping_test_apurl={
pos_0:[],
pos_1:[],
pos_3:[],
pos_4:[]
},ping_test_apurl_random=Math.random()<.3,innerHeight=window.innerHeight||document.documentElement.clientHeight,ad_engine=0,keyOffset="https:"==top.location.protocol?5:0;
return{
checkNeedAds:checkNeedAds,
afterGetAdData:afterGetAdData
};
});define("rt/appmsg/getappmsgext.rt.js",[],function(){
"use strict";
return{
base_resp:{
ret:"number",
errmsg:"string",
wxtoken:"number"
},
advertisement_num:"number",
advertisement_info:[{
hint_txt_R:"string",
url_R:"string",
type_R:"string",
rl_R:"string",
apurl_R:"string",
traceid_R:"string",
group_id_R:"string",
ticket:"string",
aid:"string",
pt:"number",
image_url:"string",
ad_desc:"string",
biz_appid:"string",
pos_type:"number",
watermark_type:"number",
logo:"string",
app_info:{},
biz_info:{},
card_info:{}
}],
comment_enabled:"number",
appmsgticket:{
ticket:"string"
},
self_head_imgs:"string",
appmsgstat:{
ret:"number",
show:"boolean",
is_login:"boolean",
like_num:"number",
liked:"boolean",
read_num:"number",
real_read_num:"number"
},
timestamp:"number",
reward_total_count:"number",
reward_head_imgs:["string"]
};
});define("biz_wap/utils/storage.js",[],function(){
"use strict";
function t(t){
if(!t)throw"require function name.";
this.key=t,this.init();
}
var e="__WXLS__",n=window.localStorage||{
getItem:function(){},
setItem:function(){},
removeItem:function(){},
key:function(){},
length:0
};
return t.getItem=function(t){
return t=e+t,n.getItem(t);
},t.setItem=function(i,r){
i=e+i;
for(var a=3;a--;)try{
n.setItem(i,r);
break;
}catch(o){
t.clear();
}
},t.clear=function(){
var t,i;
for(t=n.length-1;t>=0;t--)i=n.key(t),0==i.indexOf(e)&&n.removeItem(i);
},t.prototype={
constructor:t,
init:function(){
this.check();
},
getData:function(){
var e=t.getItem(this.key)||"{}";
try{
e=JSON.parse(e);
}catch(n){
e={};
}
return e;
},
check:function(){
var e,n,i=this.getData(),r={},a=+new Date;
for(e in i)n=i[e],+n.exp>a&&(r[e]=n);
t.setItem(this.key,JSON.stringify(r));
},
set:function(e,n,i){
var r=this.getData();
r[e]={
val:n,
exp:i||+new Date
},t.setItem(this.key,JSON.stringify(r));
},
get:function(t){
var e=this.getData();
return e=e[t],e?e.val||null:null;
},
remove:function(e){
var n=this.getData();
n[e]&&delete n[e],t.setItem(this.key,JSON.stringify(n));
}
},t;
});define("biz_common/tmpl.js",[],function(){
"use strict";
var e=function(e,r,t){
var n="";
n=e.replace(/[\r\t\n]/g," ").split("<#").join("	").replace(/((^|#>)[^\t]*)'/g,"$1\r"),
n=t?n.replace(/\t==(.*?)#>/g,"',$1,'").replace(/\t=(.*?)#>/g,"', String($1).replace(/&/g,'&amp;').replace(/\"/g, '&quot;').replace(/'/g, '&#39;').replace(/</g, '&lt;').replace(/>/g, '&gt;') ,'"):n.replace(/\t=(.*?)#>/g,"',$1,'"),
n=n.split("	").join("');").split("#>").join("p.push('").split("\r").join("\\'");
var p=new Function("obj","var p=[],print=function(){p.push.apply(p,arguments);};with(obj){p.push('"+n+"');}return p.join('');");
return p(r);
},r=function(r,t,n){
var p=document.getElementById(r);
return p?e(p.innerHTML,t,n):"";
};
return{
render:r,
tmpl:e
};
});define("appmsg/share_tpl.html.js",[],function(){
return'<div class="rich_media_extra">\n    <a href="<#= url #>" class="share_appmsg_container appmsg_card_context flex_context">\n        <div class="flex_hd">\n            <i class="share_appmsg_icon"> </i>\n        </div>\n        <div class="flex_bd">\n            <div class="share_appmsg_title">分享给订阅用户</div>\n            <p class="share_appmsg_desc">可快速分享原创文章给你的公众号订阅用户</p>\n        </div>\n    </a>\n</div>\n';
});define("appmsg/img_copyright_tpl.html.js",[],function(){
return'<span class="original_img_wrp">            \n    <span class="tips_global">来自: <#=source_nickname#></span>\n</span>    ';
});