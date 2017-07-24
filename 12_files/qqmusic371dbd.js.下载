define("pages/video_ctrl.js",[],function(){
"use strict";
function o(o){
return o=o||window,o.cgiData&&2==o.cgiData.ori_status?!0:!1;
}
function t(o){
return o=o||window,!1;
}
function i(){
return-1!=r.indexOf("&vl=1")?!1:"54"==top.window.appmsg_type?!1:!0;
}
function n(){
return-1!=r.indexOf("&dd=1")?!1:"54"==top.window.appmsg_type?!1:!0;
}
function e(){
var o=top.window.__videoDefaultRatio||16/9;
return"54"==top.window.appmsg_type?o:o;
}
document.domain="qq.com";
var r=window.location.href;
return{
showPauseTips:n,
showVideoLike:i,
showVideoDetail:t,
showH5Profile:o,
getRatio:e
};
});define("biz_common/ui/imgonepx.js",[],function(){
"use strict";
return"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAIAAACQd1PeAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyBpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMC1jMDYwIDYxLjEzNDc3NywgMjAxMC8wMi8xMi0xNzozMjowMCAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNSBXaW5kb3dzIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOkJDQzA1MTVGNkE2MjExRTRBRjEzODVCM0Q0NEVFMjFBIiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOkJDQzA1MTYwNkE2MjExRTRBRjEzODVCM0Q0NEVFMjFBIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6QkNDMDUxNUQ2QTYyMTFFNEFGMTM4NUIzRDQ0RUUyMUEiIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6QkNDMDUxNUU2QTYyMTFFNEFGMTM4NUIzRDQ0RUUyMUEiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz6p+a6fAAAAD0lEQVR42mJ89/Y1QIABAAWXAsgVS/hWAAAAAElFTkSuQmCC";
});define("biz_common/utils/respTypes.js",[],function(require,exports,module,alert){
"use strict";
var logList=[],log=function(r){
logList.push(r);
},printLog=function(){
for(var r=0,e=logList.length;e>r;++r)console.log("[RespType]"+logList[r]);
},isArray=function(r){
return"[object Array]"==Object.prototype.toString.call(r);
},getValueType=function(r){
return isArray(r)?"array":typeof r;
},parseRtDesc=function(r,e){
var t="mix",o=!1,c=e;
if(e){
var n="_R",s=e.indexOf(n),i=e.length-n.length;
o=-1!=s&&s==i,c=o?e.substring(0,i):e;
}
return"string"==typeof r?t=r:isArray(r)?t="array":"object"==typeof r&&(t="object"),
{
key:c,
type:t,
isRequired:o
};
},checkForArrayRtDesc=function(r,e){
if(!isArray(r))return!1;
for(var t=0,o=r.length;o>t;++t){
for(var c,n=r[t],s=0,i=0===e.length;c=e[s++];)if(checkForRtDesc(n,c)){
i=!0;
break;
}
if(!i)return!1;
}
return!0;
},checkForStringRtDesc=function(r,e){
var t=getValueType(r),o=parseRtDesc(e),c=o.type==t;
return c||log("miss match type : "+t+" !== "+o.type),c;
},checkForObjectRtDesc=function(r,e){
if("object"!=typeof r||isArray(r))return log("must be object"),!1;
var t=r,o=r;
for(var c in e)if(e.hasOwnProperty(c)){
var n=e[c],s=parseRtDesc(n,c),i=s.key;
o=t[i];
var u=getValueType(o);
if(s.isRequired&&void 0===o)return log("is required @key="+i),!1;
if(void 0!==o){
if(u!=s.type&&"mix"!=s.type)return log("miss match type : "+u+" !== "+s.type+" @key="+i),
!1;
if(("array"==u||"object"==u)&&"mix"!=s.type&&!checkForRtDesc(o,n))return!1;
}
}
return!0;
},checkForRtDesc=function(r,e){
return isArray(e)?checkForArrayRtDesc(r,e):"object"==typeof e?checkForObjectRtDesc(r,e):"string"==typeof e?checkForStringRtDesc(r,e):!1;
},check=function(json,rtDescs){
if("string"==typeof json)try{
json=eval("("+json+")");
}catch(e){
return log("parse json error"),!1;
}
if("object"!=typeof json)return log("must be object"),!1;
isArray(rtDesc)||(rtDescs=[rtDescs]);
for(var rtDesc,i=0;rtDesc=rtDescs[i++];)if(checkForRtDesc(json,rtDesc))return!0;
return!1;
};
return{
check:function(r,e){
logList=[];
try{
var t=check(r,e);
return t||printLog(),t;
}catch(o){
return logList.push("[rtException]"+o.toString()),printLog(),!1;
}
},
getMsg:function(){
return logList.join(";");
}
};
});define("biz_wap/utils/log.js",["biz_wap/utils/mmversion.js","biz_wap/jsapi/core.js"],function(i){
"use strict";
var s=i("biz_wap/utils/mmversion.js"),e=i("biz_wap/jsapi/core.js");
return function(i,n,o){
"string"!=typeof i&&(i=JSON.stringify(i)),n=n||"info",o=o||function(){};
var t;
s.isIOS?t="writeLog":s.isAndroid&&(t="log"),t&&e.invoke(t,{
level:n,
msg:"[WechatFe]"+i
},o);
};
});define("sougou/index.js",["appmsg/emotion/emotion.js","biz_common/tmpl.js","biz_wap/utils/ajax.js","biz_common/dom/event.js","biz_common/utils/string/html.js","sougou/a_tpl.html.js","appmsg/cmt_tpl.html.js","appmsg/my_comment_tpl.html.js"],function(t){
"use strict";
function e(t){
var e=document.getElementById("js_cover"),n=[];
e&&n.push(e);
var o=document.getElementById("js_content");
if(o)for(var m=o.getElementsByTagName("img")||[],s=0,r=m.length;r>s;s++)n.push(m.item(s));
for(var a=[],s=0,r=n.length;r>s;s++){
var p=n[s],l=p.getAttribute("data-src")||p.getAttribute("src");
l&&(a.push(l),function(e){
i.on(p,"click",function(){
return"ios"==t?window.JSInvoker&&window.JSInvoker.openImageList&&window.JSInvoker.openImageList(JSON.stringify({
index:e,
array:a
})):window.JSInvoker&&JSInvoker.weixin_openImageList&&window.JSInvoker.weixin_openImageList(JSON.stringify({
index:e,
array:a
})),!1;
});
}(s));
}
}
var n=t("appmsg/emotion/emotion.js"),o=t("biz_common/tmpl.js"),i=(t("biz_wap/utils/ajax.js"),
t("biz_common/tmpl.js"),t("biz_common/dom/event.js"));
t("biz_common/utils/string/html.js");
t("sougou/a_tpl.html.js"),t("appmsg/cmt_tpl.html.js");
if(document.getElementById("js_report_article3").style.display="none",document.getElementById("js_toobar3").style.display="none",
function(){
var e=t("appmsg/my_comment_tpl.html.js"),n=document.createElement("div");
n.innerHTML=o.tmpl(e,{}),document.body.appendChild(n);
}(),n.init(),navigator.userAgent.toLowerCase().match(/ios/)){
var m=navigator.userAgent.toLowerCase().match(/(?:sogousearch\/ios\/)(.*)/);
if(m&&m[1]){
var s=m[1].replace(/\./g,"");
parseInt(s)>422&&e("ios");
}
}else e("android");
window.onerror=function(t){
var e=new Image;
e.src="/mp/jsreport?key=86&content="+t+"&r="+Math.random();
};
});define("biz_wap/safe/mutation_observer_report.js",[],function(){
"use strict";
window.addEventListener&&window.addEventListener("load",function(){
window.__moonsafe_mutation_report_keys||(window.__moonsafe_mutation_report_keys={});
var e=window.moon&&moon.moonsafe_id||29715,o=window.moon&&moon.moonsafe_key||0,t=[],n={},r=function(e){
return"[object Array]"==Object.prototype.toString.call(e);
},s=function(e,o,s){
s=s||1,n[e]||(n[e]=0),n[e]+=s,o&&(r(o)?t=t.concat(o):t.push(o)),setTimeout(function(){
a();
},1500);
},a=function(){
var r=[],s=t.length,i=["r="+Math.random()];
for(var c in n)n.hasOwnProperty(c)&&r.push(e+"_"+(1*c+1*o)+"_"+n[c]);
for(var c=0;s>c&&!(c>=10);++c)i.push("log"+c+"="+encodeURIComponent(t[c]));
if(!(0==r.length&&i.length<=1)){
var _,d="idkey="+r.join(";")+"&lc="+(i.length-1)+"&"+i.join("&");
if(window.ActiveXObject)try{
_=new ActiveXObject("Msxml2.XMLHTTP");
}catch(w){
try{
_=new ActiveXObject("Microsoft.XMLHTTP");
}catch(f){
_=!1;
}
}else window.XMLHttpRequest&&(_=new XMLHttpRequest);
_&&(_.open("POST",location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?",!0),_.setRequestHeader("cache-control","no-cache"),
_.setRequestHeader("Content-Type","application/x-www-form-urlencoded; charset=UTF-8"),
_.setRequestHeader("X-Requested-With","XMLHttpRequest"),_.onreadystatechange=function(){
4===_.readyState&&(t.length>10?(t=t.slice(10),a()):(t=[],n={}));
},t=[],n={},_.send(d));
}
};
try{
if(!window.__observer)return;
var i=window.__observer_data;
if(window.__observer.takeRecords){
var c=window.__observer.takeRecords();
if(c&&c.length){
i.count++;
var _=new Date;
c.forEach(function(e){
for(var o=e.addedNodes,t=0;t<o.length;t++){
var n=o[t];
if("SCRIPT"===n.tagName){
var r=n.src;
!r||/qq\.com/.test(r)||/weishi\.com/.test(r)||i.list.push(r);
}
}
}),i.exec_time+=new Date-_;
}
}
window.__observer.disconnect();
for(var d=window.__moonsafe_mutation_report_keys.observer||2,w=window.__moonsafe_mutation_report_keys.script_src||8,f=window.__moonsafe_mutation_report_keys.setattribute||9,u=window.__moonsafe_mutation_report_keys.ajax||10,m=25,v=0;v<i.list.length;v++){
var l=i.list[v],h=["[moonsafe][observer][url]:"+location.href,"[moonsafe][observer][src]:"+l,"[moonsafe][observer][ua]:"+navigator.userAgent];
i.list.length==v+1&&(h.push("[moonsafe][observer][count]:"+i.count),h.push("[moonsafe][observer][exec_time]:"+i.exec_time+"ms")),
s(d,h),"inlinescript_without_nonce"==l&&s(m,h);
}
var p=window.__danger_src;
if(p)for(var y=[{
key:"xmlhttprequest",
idkey:u
},{
key:"script_src",
idkey:w
},{
key:"script_setAttribute",
idkey:f
}],v=0;v<y.length;v++){
var b=y[v].key,g=p[b];
if(g&&g.length)for(var k=0;k<g.length;k++){
var h=["[moonsafe]["+b+"][url]:"+location.href,"[moonsafe]["+b+"][src]:"+g[k],"[moonsafe]["+b+"][ua]:"+navigator.userAgent];
s(y[v].idkey,h);
}
}
}catch(q){
var R=3,h=["[moonsafe][observer][exception]:"+q];
s(R,h);
}
},!1);
});define("appmsg/fereport.js",["biz_wap/utils/wapsdk.js","biz_common/utils/http.js","appmsg/log.js"],function(e){
"use strict";
function i(){
var e=window.performance||window.msPerformance||window.webkitPerformance;
if(e&&e.timing){
var i=e.timing,s=0,m=0,a=window.location.protocol,d=Math.random(),p=1>2*d,l=1>10*d,r=1>25*d,_=1>100*d,u=1>250*d,w=1>500*d,c=!0;
"https:"==a?(s=18,window.__mooninline&&(s=156),m=27,c=!1):"http:"==a&&(s=9,window.__mooninline&&(s=155),
m=19);
var g=window.__wxgspeeds||{};
if(g&&g.moonloadtime&&g.moonloadedtime){
var v,S=g.moonloadedtime-g.moonloadtime;
v=localStorage&&JSON.parse(localStorage.getItem("__WXLS__moonarg"))&&"fromls"==JSON.parse(localStorage.getItem("__WXLS__moonarg")).method?21:22,
o.saveSpeeds({
sample:21==v||22==v&&_?1:0,
uin:uin,
pid:s,
speeds:{
sid:v,
time:S
}
});
}
g&&g.mod_downloadtime&&o.saveSpeeds({
uin:uin,
pid:s,
speeds:{
sid:24,
time:g.mod_downloadtime
}
});
var f=i.domContentLoadedEventStart-i.navigationStart;
if(f>3e3&&(o.setBasicTime({
sample:l&&c||r&&!c?1:0,
uin:uin,
pid:m
}),(new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_28_1&lc=1&log0="+encodeURIComponent(location.href)),
o.setBasicTime({
sample:u&&c||_&&!c?1:0,
uin:uin,
pid:s
}),n.htmlSize){
var h=n.htmlSize/(i.responseEnd-i.connectStart);
o.saveSpeeds({
sample:w,
uin:uin,
pid:s,
speeds:{
sid:25,
time:Math.round(h)
}
});
}
if(g&&g.combo_times)for(var j=1;j<g.combo_times.length;j++)o.saveSpeeds({
sample:u,
uin:uin,
pid:s,
speeds:{
sid:26,
time:g.combo_times[j]-g.combo_times[j-1]
}
});
if(g&&g.mod_num){
var b=g.hit_num/g.mod_num;
o.saveSpeeds({
sample:u,
uin:uin,
pid:s,
speeds:[{
sid:27,
time:Math.round(100*b)
},{
sid:28,
time:Math.round(1e3*b)
}]
});
}
var z=window.logs.pagetime.jsapi_ready_time-i.navigationStart;
o.saveSpeeds(156==s||155==s?{
sample:p,
uin:uin,
pid:s,
speeds:{
sid:31,
time:z
}
}:{
sample:w,
uin:uin,
pid:s,
speeds:{
sid:31,
time:z
}
}),o.send(),window.setTimeout(function(){
window.__moonclientlog&&t("[moon] "+window.__moonclientlog.join(" ^^^ "));
},250);
}
}
var o=e("biz_wap/utils/wapsdk.js"),n=e("biz_common/utils/http.js"),t=e("appmsg/log.js");
i();
});define("appmsg/report.js",["biz_common/dom/event.js","biz_wap/utils/ajax.js","appmsg/cdn_img_lib.js","biz_wap/utils/mmversion.js","biz_common/utils/report.js","biz_common/utils/monitor.js"],function(e){
"use strict";
function t(){
var t=(e("biz_wap/utils/mmversion.js"),e("biz_common/utils/report.js"),e("biz_common/utils/monitor.js")),a=!1,r=window.performance||window.msPerformance||window.webkitPerformance;
return function(){
return;
}(),r&&r.timing&&r.timing.navigationStart?(a=r.timing.navigationStart,function(){
return;
}(),function(){
function e(){
if(-1==n.indexOf("NetType/"))return!1;
for(var e=["2G","cmwap","cmnet","uninet","uniwap","ctwap","ctnet"],t=0,i=e.length;i>t;++t)if(-1!=n.indexOf(e[t]))return!0;
return!1;
}
var i=window.performance&&window.performance.timing,r=write_sceen_time-a,s=first_sceen__time-a,d=page_endtime-a,m=(window.onload_endtime||+new Date)-a;
-1!=navigator.userAgent.indexOf("MicroMessenger")&&(r=real_show_page_time-a,s=real_show_page_time-a);
var g=window.logs.jsapi_ready_time?window.logs.jsapi_ready_time-a:void 0,w=window.logs.a8key_ready_time?window.logs.a8key_ready_time-a:void 0,p=i&&i.connectEnd-i.connectStart,c=i&&i.secureConnectionStart&&i.connectEnd-i.secureConnectionStart,u=i&&i.domainLookupEnd&&i.domainLookupStart&&i.domainLookupEnd-i.domainLookupStart;
if(window.logs.pagetime.wtime=r,window.logs.pagetime.ftime=s,window.logs.pagetime.ptime=d,
window.logs.pagetime.onload_time=m,window.logs.pagetime.jsapi_ready_time=g,window.logs.pagetime.a8key_ready_time=w,
need_report_cost?o({
url:"/mp/report_cost",
type:"post",
data:{
id_key_list:["1|1|"+d,"1|2|"+s,"1|3|"+m,"1|4|"+g,"1|5|"+w,"1|6|"+p,"1|7|"+c,"1|8|"+u].join(";")
}
}):Math.random()<.01&&o({
url:"/mp/report_cost",
type:"post",
data:{
id_key_list:["#1|1|"+d,"1|2|"+s,"1|3|"+m,"1|4|"+g,"1|5|"+w,"1|6|"+p,"1|7|"+c,"1|8|"+u].join(";")
}
}),need_report_cost&&s>3e3){
var l=new Image,f=(new Date).getTime();
l.onload=function(){
var e=(new Date).getTime()-f,t=(new Date).getTime(),i=new Image;
i.onload=function(){
var i=(new Date).getTime()-t;
o({
url:"/mp/report_cost",
type:"post",
data:{
id_key_list:["^2|1|"+e,"2|2|"+i].join(";")
}
});
},i.src="http://ugc.qpic.cn/adapt/0/7d8963bb-aace-df23-0569-f8a4e388eacb/100?r="+Math.random();
},l.src="http://ugc.qpic.cn/adapt/0/7d8963bb-aace-df23-0569-f8a4e388eacb/100?r="+Math.random();
}
if(!(Math.random()>.2||0>m||0>r||0>s||0>d)){
if(g&&t.setAvg(27822,15,g),w&&t.setAvg(27822,17,w),d>=15e3)return t.setAvg(27822,29,d),
void t.send();
t.setAvg(27822,1,d).setAvg(27822,3,m).setAvg(27822,5,s),window.isWeixinCached&&t.setAvg(27822,19,d),
e()?(t.setAvg(27822,9,d),window.isWeixinCached&&t.setAvg(27822,23,d)):"wifi"==networkType?(t.setAvg(27822,7,d),
window.isWeixinCached&&t.setAvg(27822,21,d)):"2g/3g"==networkType?(t.setAvg(27822,11,d),
window.isWeixinCached&&t.setAvg(27822,25,d)):(t.setAvg(27822,13,d),window.isWeixinCached&&t.setAvg(27822,28,d)),
window.moon&&moon.clearSample&&(t.setAvg(27822,71,d),e()?t.setAvg(27822,73,d):"wifi"==networkType?t.setAvg(27822,75,d):"2g/3g"==networkType?t.setAvg(27822,77,d):t.setAvg(27822,79,d)),
p&&t.setAvg(27822,65,p),c&&t.setAvg(27822,67,c),u&&t.setAvg(27822,69,u),t.send();
}
}(),function(){
window.logs.jsapi_ready_fail&&(t.setSum(24729,55,window.logs.jsapi_ready_fail),t.send());
}(),function(){
var e=document.getElementById("js_toobar3"),t=document.getElementById("page-content"),n=window.innerHeight||document.documentElement.clientHeight;
if(t&&!(Math.random()>.1)){
var o=function(){
var a=window.pageYOffset||document.documentElement.scrollTop,s=e.offsetTop;
if(a+n>=s){
for(var d,m,g=t.getElementsByTagName("img"),w={},p=[],c=0,u=0,l=0,f=0,_=g.length;_>f;++f){
var v=g[f];
d=v.getAttribute("data-src")||v.getAttribute("src"),m=v.getAttribute("src"),d&&(d.isCDN()?u++:l++,
c++,w[m]={});
}
if(p.push("1="+1e3*c),p.push("2="+1e3*u),p.push("3="+1e3*l),r.getEntries){
var h=r.getEntries(),y=window.logs.img.download,A=[0,0,0],j=[0,0,0];
c=u=0;
for(var f=0,k=h.length;k>f;++f){
var T=h[f],b=T.name;
b&&"img"==T.initiatorType&&w[b]&&(b.isCDN()&&(j[0]+=T.duration,u++),A[0]+=T.duration,
c++,w[b]={
startTime:T.startTime,
responseEnd:T.responseEnd
});
}
A[0]>0&&c>0&&(A[2]=A[0]/c),j[0]>0&&u>0&&(j[2]=j[0]/u);
for(var f in y)if(y.hasOwnProperty(f)){
for(var M=y[f],E=0,x=0,C=0,z=0,S=0,_=M.length;_>S;++S){
var d=M[S];
if(w[d]&&w[d].startTime&&w[d].responseEnd){
var D=w[d].startTime,I=w[d].responseEnd;
E=Math.max(E,I),x=x?Math.min(x,D):D,d.isCDN()&&(C=Math.max(E,I),z=x?Math.min(x,D):D);
}
}
A[1]+=Math.round(E-x),j[1]+=Math.round(C-z);
}
for(var N=4,W=7,f=0;3>f;f++)A[f]=Math.round(A[f]),j[f]=Math.round(j[f]),A[f]>0&&(p.push(N+f+"="+A[f]),
"wifi"==networkType?p.push(N+f+6+"="+A[f]):"2g/3g"==networkType&&p.push(N+f+12+"="+A[f])),
j[f]>0&&(p.push(W+f+"="+j[f]),"wifi"==networkType?p.push(W+f+6+"="+j[f]):"2g/3g"==networkType&&p.push(W+f+12+"="+j[f]));
}
i.off(window,"scroll",o,!1);
}
};
i.on(window,"scroll",o,!1);
}
}(),void function(){
if(!(Math.random()>.001)){
var e=document.createElement("iframe"),t=[600,800,1e3,1200,1500,2e3,3e3,5e3,1e4,18e3],i=Math.ceil(10*Math.random())-1,n=uin+mid+idx+Math.ceil(1e3*Math.random())+(new Date).getTime();
e.style.display="none",e.id="js_ajax",e.setAttribute("data-time",i),e.src="/mp/iframetest?action=page&traceid="+n+"&devicetype="+devicetype+"&timeout="+t[i];
var o=document.getElementById("js_article");
o.appendChild(e);
}
}()):!1;
}
var i=e("biz_common/dom/event.js"),n=navigator.userAgent,o=e("biz_wap/utils/ajax.js");
e("appmsg/cdn_img_lib.js"),i.on(window,"load",function(){
if(""==networkType&&window.isInWeixinApp()){
var e={
"network_type:fail":"fail",
"network_type:edge":"2g/3g",
"network_type:wwan":"2g/3g",
"network_type:wifi":"wifi"
};
JSAPI.invoke("getNetworkType",{},function(i){
networkType=e[i.err_msg],t();
});
}else t();
},!1);
});define("appmsg/report_and_source.js",["biz_common/utils/string/html.js","biz_common/dom/event.js","biz_common/utils/url/parse.js","biz_wap/utils/ajax.js","appmsg/open_url_with_webview.js","biz_wap/jsapi/core.js"],function(e,t,o,i){
"use strict";
function n(){
var e=p.indexOf("://")<0?"http://"+p:p;
if(-1!=e.indexOf("mp.weixin.qq.com/s")||-1!=e.indexOf("mp.weixin.qq.com/mp/appmsg/show")){
var t=e.split("#");
e=m.addParam(t[0],"scene",25,!0)+(t[1]?"#"+t[1]:""),e=e.replace(/#rd$/g,"#wechat_redirect");
}else e="http://mp.weixinbridge.com/mp/wapredirect?url="+encodeURIComponent(p);
try{
if("mp.weixin.qq.com"!=top.window.location.host)return window.top.open(e,"_blank"),
!1;
}catch(o){}
var i=location.search.replace("wx_header","del_wx_header"),n={
url:"/mp/advertisement_report"+i+"&report_type=3&action_type=0&url="+encodeURIComponent(p)+"&__biz="+biz+"&r="+Math.random(),
type:"GET",
mayAbort:!0,
async:!1
};
return n.timeout=2e3,n.complete=function(){
_(e,{
sample:0,
reject:function(){
location.href=e;
}
});
},c(n),!1;
}
e("biz_common/utils/string/html.js");
var r=e("biz_common/dom/event.js"),m=e("biz_common/utils/url/parse.js"),c=e("biz_wap/utils/ajax.js"),a=msg_title.htmlDecode(),p=msg_source_url.htmlDecode(),s=document.getElementById("js_report_article3"),_=e("appmsg/open_url_with_webview.js"),l=e("biz_wap/jsapi/core.js");
r.tap(s,function(){
var e=["/mp/infringement?url=",encodeURIComponent(window.msg_link),"&title=",encodeURIComponent(a),"&__biz=",biz].join("");
return location.href=e+"#wechat_redirect",!1;
});
var d=document.getElementById("js_view_source");
r.on(d,"click",function(){
return n(),!1;
});
});define("appmsg/page_pos.js",["biz_common/utils/string/html.js","biz_common/dom/event.js","biz_wap/utils/ajax.js","biz_common/utils/cookie.js","biz_common/utils/http.js","appmsg/cdn_img_lib.js","biz_wap/utils/storage.js"],function(e){
"use strict";
function t(e,t){
if(e&&!(e.length<=0))for(var o,n,i,a=/http(s)?\:\/\/([^\/\?]*)(\?|\/)?/,d=0,r=e.length;r>d;++d)o=e[d],
o&&(n=o.getAttribute(t),n&&(i=n.match(a),i&&i[2]&&(h[i[2]]=!0)));
}
function o(e){
for(var t=0,o=v.length;o>t;++t)if(v[t]==e)return!0;
return!1;
}
function n(){
h={},t(document.getElementsByTagName("a"),"href"),t(document.getElementsByTagName("link"),"href"),
t(document.getElementsByTagName("iframe"),"src"),t(document.getElementsByTagName("script"),"src"),
t(document.getElementsByTagName("img"),"src");
var e=[];
for(var n in h)h.hasOwnProperty(n)&&(window.networkType&&"wifi"==window.networkType&&!y&&o(n)&&(y=!0),
e.push(n));
return h={},e.join(",");
}
function i(){
var e,t=window.pageYOffset||document.documentElement.scrollTop,o=b.js_content,i=b.screen_height,a=b.screen_width,d=b.scroll_height,r=Math.ceil(d/i),m=Math.ceil((o.scrollHeight||o.offsetHeight)/i),s=(window.logs.read_height||t)+i,_=b.pageEndTop,l=b.imgs,c=Math.ceil(s/i)||1,g=b.media,p=50,u=0,h=0,v=0,j=0,T=s+p>_?1:0;
c>r&&(c=r);
var z=function(t){
if(t)for(var o=0,n=t.length;n>o;++o){
var i=t[o];
if(i){
u++;
var a=i.getAttribute("src"),d=i.getAttribute("data-type");
a&&0==a.indexOf("http")&&(h++,a.isCDN()&&(v++,-1!=a.indexOf("tp=webp")&&j++),d&&(e["img_"+d+"_cnt"]=e["img_"+d+"_cnt"]||0,
e["img_"+d+"_cnt"]++));
}
}
e.download_cdn_webp_img_cnt=j||0,e.download_img_cnt=h||0,e.download_cdn_img_cnt=v||0,
e.img_cnt=u||0;
},O=window.appmsgstat||{},E=window.logs.img||{},x=window.logs.pagetime||{},k=E.load||{},D=E.read||{},I=[],S=[],B=0,N=0,M=0;
for(var H in D)H&&0==H.indexOf("http")&&D.hasOwnProperty(H)&&S.push(H);
for(var H in k)H&&0==H.indexOf("http")&&k.hasOwnProperty(H)&&I.push(H);
for(var P=0,q=I.length;q>P;++P){
var A=I[P];
A&&A.isCDN()&&(-1!=A.indexOf("/0")&&B++,-1!=A.indexOf("/640")&&N++,-1!=A.indexOf("/300")&&M++);
}
var e={
__biz:biz,
title:msg_title.htmlDecode(),
mid:mid,
idx:idx,
subscene:window.subscene||0,
read_cnt:O.read_num||0,
like_cnt:O.like_num||0,
screen_width:a,
screen_height:i,
screen_num:m,
idkey:"",
copyright_stat:"",
ori_article_type:"",
video_cnt:window.logs.video_cnt||0,
read_screen_num:c||0,
is_finished_read:T,
scene:source,
content_len:f.content_length||0,
start_time:page_begintime,
end_time:(new Date).getTime(),
img_640_cnt:N,
img_0_cnt:B,
img_300_cnt:M,
wtime:x.onload_time||0,
ftime:x.ftime||0,
ptime:x.ptime||0,
onload_time:x.onload_time||0,
reward_heads_total:window.logs.reward_heads_total||0,
reward_heads_fail:window.logs.reward_heads_fail||0,
outer_pic:window.logs.outer_pic||0,
publish_time:ct
};
if(window.networkType&&"wifi"==window.networkType&&(e.wifi_all_imgs_cnt=I.length,
e.wifi_read_imgs_cnt=S.length),window.logs.webplog&&4==window.logs.webplog.total){
var R=window.logs.webplog;
e.webp_total=1,e.webp_lossy=R.lossy,e.webp_lossless=R.lossless,e.webp_alpha=R.alpha,
e.webp_animation=R.animation;
}
if(e.copyright_stat=window._copyright_stat||"",e.ori_article_type=window._ori_article_type||"",
window.__addIdKeyReport&&window.moon&&(moon.hit_num>0&&moon.hit_num<1e3&&window.__addIdKeyReport(27613,30,moon.hit_num),
moon.mod_num>0&&moon.mod_num<1e3&&window.__addIdKeyReport(27613,31,moon.mod_num)),
window.logs.idkeys){
var Y=window.logs.idkeys,J=[];
for(var K in Y)if(Y.hasOwnProperty(K)){
var C=Y[K];
C.val>0&&J.push(K+"_"+C.val);
}
e.idkey=J.join(";");
}
z(!!g&&g.getElementsByTagName("img")),z(l);
var W=(new Date).getDay(),L=n();
return(y||0!==user_uin&&Math.floor(user_uin/100)%7==W)&&(e.domain_list=L),y&&(e.html_content=w),
window.isSg&&(e.from="sougou"),e.source=window.friend_read_source||"",e.req_id=window.req_id||"",
e.recommend_version=window.friend_read_version||"",e.class_id=window.friend_read_class_id||"",
e;
}
function a(e){
j||(j=!0,p.remove("page_time"),e.report_time=parseInt(+new Date/1e3),_({
url:"/mp/appmsgreport?action=page_time",
type:"POST",
mayAbort:!0,
data:e,
async:!1,
timeout:2e3
}));
}
function d(){
if(window._adRenderData&&"undefined"!=typeof JSON&&JSON.stringify){
var e=JSON.stringify(window._adRenderData),t=+new Date,o=[biz,sn,mid,idx].join("_"),n=new c("ad");
n.set(o,{
info:e,
time:t
},+new Date+24e4);
}
g.set(o,z,+new Date+72e5);
}
function r(){
return window.__video_report_data;
}
function m(e){
e&&e.play_type&&(u.remove("spad"),e.report_type=1,_({
url:"/mp/ad_video_report?action=video_play_report",
type:"POST",
mayAbort:!0,
data:e,
async:!1,
timeout:2e3
}));
}
e("biz_common/utils/string/html.js");
var s=e("biz_common/dom/event.js"),_=e("biz_wap/utils/ajax.js"),l=(e("biz_common/utils/cookie.js"),
e("biz_common/utils/http.js"));
e("appmsg/cdn_img_lib.js");
var w,c=e("biz_wap/utils/storage.js"),g=new c("page_pos"),p=new c("time_on_page"),u=new c("spad"),f={};
!function(){
w=document.getElementsByTagName("html"),w&&1==!!w.length&&l&&(w=w[0].innerHTML,f.content_length=l.htmlSize),
window.logs.pageinfo=f;
}();
var h={},y=!1,v=["wap.zjtoolbar.10086.cn","125.88.113.247","115.239.136.61","134.224.117.240","hm.baidu.com","c.cnzz.com","w.cnzz.com","124.232.136.164","img.100msh.net","10.233.12.76","wifi.witown.com","211.137.132.89","qiao.baidu.com","baike.baidu.com"],b={
js_content:document.getElementById("js_content"),
screen_height:document.documentElement.clientHeight||window.innerHeight,
screen_width:document.documentElement.clientWidth||window.innerWidth,
scroll_height:document.body.scrollHeight||document.body.offsetHeight,
pageEndTop:document.getElementById("js_toobar3").offsetTop,
imgs:document.getElementById("js_content").getElementsByTagName("img")||[],
media:document.getElementById("media")
},j=!1,T=null,z=0,O=(msg_link.split("?").pop(),[biz,sn,mid,idx].join("_"));
!function(){
if(window.localStorage&&!localStorage.getItem("clear_page_pos")){
for(var e=localStorage.length-1;e>=0;){
var t=localStorage.key(e);
t.match(/^\d+$/)?localStorage.removeItem(t):t.match(/^adinfo_/)&&localStorage.removeItem(t),
e--;
}
localStorage.setItem("clear_page_pos","true");
}
}(),window.localStorage&&(s.on(window,"load",function(){
z=1*g.get(O);
var e=location.href.indexOf("scrolltodown")>-1?!0:!1,t=(document.getElementById("img-content"),
document.getElementById("js_cmt_area"));
if(e&&t&&t.offsetTop){
var o=t.offsetTop;
window.scrollTo(0,o-25);
}else window.scrollTo(0,z);
if(window.__wxjs_is_wkwebview){
var n=p.getData("page_time");
n.page_time&&(a(n.page_time.val),(new Image).src=location.protocol+"//mp.weixin.qq.com/mp/jsmonitor?idkey=28307_59_1&r="+Math.random());
var s=u.getData("spad");
s.spad&&m(s.spad.val),window.setInterval(function(){
var e=i();
p.set("page_time",e,+new Date+864e7),d(),e=r(),u.set("spad",e,+new Date+864e7);
},1e3);
}
}),s.on(window,"unload",function(){
d(),window.__ajaxtest="2";
var e=i();
a(e);
}),window.logs.read_height=0,s.on(window,"scroll",function(){
var e=window.pageYOffset||document.documentElement.scrollTop;
window.logs.read_height=Math.max(window.logs.read_height,e),clearTimeout(T),T=setTimeout(function(){
z=window.pageYOffset,g.set(O,z,+new Date+72e5);
},500);
}),s.on(document,"touchmove",function(){
var e=window.pageYOffset||document.documentElement.scrollTop;
window.logs.read_height=Math.max(window.logs.read_height,e),clearTimeout(T),T=setTimeout(function(){
z=window.pageYOffset,g.set(O,z,+new Date+72e5);
},500);
}));
});define("appmsg/cdn_speed_report.js",["biz_common/dom/event.js","biz_wap/jsapi/core.js","biz_wap/utils/ajax.js"],function(e){
"use strict";
function i(){
function e(e){
var i=[];
for(var n in e)i.push(n+"="+encodeURIComponent(e[n]||""));
return i.join("&");
}
if(networkType){
var i=window.performance||window.msPerformance||window.webkitPerformance;
if(i&&"undefined"!=typeof i.getEntries){
var n,t,a=100,o=document.getElementsByTagName("img"),s=o.length,p=navigator.userAgent,m=!1;
/micromessenger\/(\d+\.\d+)/i.test(p),t=RegExp.$1;
for(var g=0,w=o.length;w>g;g++)if(n=parseInt(100*Math.random()),!(n>a)){
var d=o[g].getAttribute("src");
if(d&&!(d.indexOf("mp.weixin.qq.com")>=0)){
for(var f,u=i.getEntries(),c=0;c<u.length;c++)if(f=u[c],f.name==d){
var _=o[g].getAttribute("data-fail");
r({
type:"POST",
url:"/mp/appmsgpicreport?__biz="+biz+"#wechat_redirect",
data:e({
rnd:Math.random(),
uin:uin,
version:version,
client_version:t,
device:navigator.userAgent,
time_stamp:parseInt(+new Date/1e3),
url:d,
img_size:o[g].fileSize||0,
user_agent:navigator.userAgent,
net_type:networkType,
appmsg_id:window.appmsgid||"",
sample:s>100?100:s,
delay_time:parseInt(f.duration),
from:window.isSg?"sougou":"",
fail:_
})
}),m=!0;
break;
}
if(m)break;
}
}
}
}
}
var n=e("biz_common/dom/event.js"),t=e("biz_wap/jsapi/core.js"),r=e("biz_wap/utils/ajax.js"),a={
"network_type:fail":"fail",
"network_type:edge":"2g/3g",
"network_type:wwan":"2g/3g",
"network_type:wifi":"wifi"
};
t.invoke("getNetworkType",{},function(e){
networkType=a[e.err_msg],i();
}),n.on(window,"load",i,!1);
});define("appmsg/wxtopic.js",["biz_wap/utils/ajax.js","biz_wap/jsapi/core.js","biz_common/dom/event.js","appmsg/topic_tpl.html.js"],function(t){
"use strict";
function e(t){
t.parentNode.removeChild(t);
}
function i(t,e){
var i=c;
e.img_url||(e.img_url=topic_default_img);
for(var o in e){
var a=new RegExp("{"+o+"}","g");
i=i.replace(a,e[o]);
}
var p=document.createElement("span");
p.className="db topic_area",p.innerHTML=i,t.parentNode.insertBefore(p,t),t.parentNode.removeChild(t),
r.tap(p,function(){
var e=location.protocol+"//mp.weixin.qq.com/mp/topic?action=topic_detail_page&topic_id="+t.getAttribute("data-topic-id")+"&topic_type="+t.getAttribute("data-topic-type")+"&sn="+t.getAttribute("data-topic-sn")+"&scene=101#wechat_redirect";
n.invoke("openUrlWithExtraWebview",{
url:e,
openType:1
},function(t){
t&&-1!==t.err_msg.indexOf(":ok")||(location.href=e);
});
});
}
function o(t){
var o={
topic_id:t.getAttribute("data-topic-id"),
topic_type:t.getAttribute("data-topic-type"),
sn:t.getAttribute("data-topic-sn"),
biz:biz
};
p({
url:"/mp/topic?action=get_topic_info",
type:"post",
data:o,
success:function(o){
if(console.log(o),o=JSON.parse(o),0!=o.base_resp.ret)return void e(t);
var a={
title:o.title,
author:o.author||(o.leading_actor?o.leading_actor.replace(/\$\$/g," / "):"-"),
img_url:o.img_url,
msg_num:o.msg_num
};
i(t,a);
},
error:function(){
e(t);
}
});
}
function a(){
var t=document.getElementsByTagName("wxtopic");
t[0]&&o(t[0]);
}
var p=t("biz_wap/utils/ajax.js"),n=t("biz_wap/jsapi/core.js"),r=t("biz_common/dom/event.js"),c=t("appmsg/topic_tpl.html.js");
a();
});define("appmsg/new_index.js",["biz_common/dom/event.js","biz_wap/jsapi/core.js"],function(e){
"use strict";
var n=e("biz_common/dom/event.js"),s=e("biz_wap/jsapi/core.js"),t=document.getElementById("js_new_appmsg_addcontact");
n.tap(t,function(){
return s.invoke("addContact",{
webtype:"1",
username:user_name_new||user_name
},function(e){
(-1!=e.err_msg.indexOf("ok")||-1!=e.err_msg.indexOf("added"))&&(t.style.display="none");
}),!1;
});
});define("appmsg/weapp.js",["biz_common/utils/string/html.js","pages/weapp_tpl.html.js","biz_wap/utils/ajax.js","biz_common/dom/event.js","biz_common/tmpl.js","biz_wap/jsapi/core.js","biz_common/dom/class.js"],function(e,t,n,i){
"use strict";
function a(e,t,n){
var i=new Image;
i.src=("http://mp.weixin.qq.com/mp/jsreport?1=1&key=106&content="+n+",biz:"+biz+",mid:"+mid+",uin:"+uin+"[key1]"+encodeURIComponent(t.toString())+"&r="+Math.random()).substr(0,1024),
console&&t&&console.error(t);
}
function p(e,t,n,i,a,p,r){
u({
url:"/mp/appmsgreport?action=appmsg_weapp_report",
data:{
__biz:window.biz||"",
mid:window.mid||"",
idx:window.idx||"",
weapp_appid:e||"",
weapp_pos:t||0,
weapp_title:i||0,
weapp_nickname:n||0,
type:a||0,
scene:window.source||-1,
weapp_type:p,
is_confirm:r||0
},
type:"POST",
dataType:"json",
async:!0,
success:function(){}
});
}
function r(){
var e=c("js_content");
if(!e)return!1;
y=e.getElementsByTagName("mp-weapp")||[],v=e.getElementsByTagName("mp-miniprogram")||[],
b=[];
for(var t=e.getElementsByTagName("a"),n=0,i=t.length;i>n;n++){
var a=t[n],p=a.getAttribute("data-miniprogram-appid");
p&&b.push(a);
}
if(y.length<=0&&v.length<=0&&0==b.length)return!1;
try{
I=JSON.parse(weapp_sn_arr_json).weapp_card_list;
}catch(r){
return!1;
}
return!0;
}
function o(e){
return e=e||"",e.replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;").replace(/"/g,"&quot;");
}
function d(e,t,n,i,a){
return p(e,t,n,i,4,a),window.__addIdKeyReport&&window.__addIdKeyReport("28307",103),
location.href="https://mp.weixin.qq.com/mp/waerrpage?type=upgrade&appid="+encodeURIComponent(e)+"#wechat_redirect",
!1;
}
function m(e,t,n,a,r){
return p(e,t,n,a,5,r),i("请在微信内打开小程序"),!1;
}
function s(){
var e={
__biz:biz,
mid:mid,
idx:idx,
uin:uin,
key:key,
pass_ticket:pass_ticket,
weapp_num:I.length
};
window.reportWeappid=[];
for(var t=0;t<I.length;t++)e["weapp_appid_"+t]=I[t].appid,e["weapp_sn_"+t]=I[t].sn,
window.reportWeappid.push(I[t].appid);
var n="/mp/appmsg_weapp?action=batch_get_weapp";
for(var i in e)n+="&"+i+"="+encodeURIComponent(e[i]);
var r=function(){};
g.on(document.getElementById("js_minipro_dialog_ok"),"click",function(){
r&&r(),document.getElementById("js_minipro_dialog").style.display="none";
}),g.on(document.getElementById("js_minipro_dialog_cancel"),"click",function(){
var e=document.getElementById("js_minipro_dialog");
e.style.display="none",p(e._appid,e._i,e._nickname,e._title,3,1,1),window.__addIdKeyReport&&window.__addIdKeyReport("28307",116);
}),u({
url:n,
type:"GET",
dataType:"json",
async:!0,
success:function(e){
try{
if(e.base_resp.ret)throw new Error("Fetch weapp info but get ret="+e.base_resp.ret);
var t=!1,n=!1,i=navigator.userAgent.match(/MicroMessenger\/(\d+)\.(\d+)\.(\d+)/);
if(i){
var s=Number(i[1]),l=Number(i[2]),c=Number(i[3]);
s>6?t=!0:6===s&&l>5?t=!0:6===s&&5===l&&c>=3&&(t=!0);
}else navigator.userAgent.match(/MicroMessenger\//)||(n=!0);
for(var u=e.weapp_info,y={},v="appid="+encodeURIComponent(e.appid)+(e.appmsg_compact_url?"&appmsg_compact_url="+encodeURIComponent(e.appmsg_compact_url):""),b=0;b<u.length;b++)y[u[b].weapp_appid]=u[b];
for(b=0;b<k.length;b++)(function(e){
var i=k[e].appid,s=k[e].path,l=k[e].imageUrl,c=k[e].title,u=k[e].elem,b=y[i];
if(b){
var j=u.tagName.toLowerCase(),I=u.firstChild&&1==u.firstChild.nodeType;
if("a"!=j)u.innerHTML=w.tmpl(_,{
imageUrl:o(l),
title:o(c),
nickname:o(b.nickname),
avatar:o(b.logo_url)
});else{
if(I){
var R=u.firstChild;
R&&h.addClass(u,"weapp_image_link");
}else h.addClass(u,"weapp_text_link");
u.href="javascript:void(0);";
}
var z=s.indexOf("?");
s.indexOf("?")>=0?s=s.slice(0,z)+".html"+s.slice(z)+"&"+v:s+=".html?"+v,g.on(u,"a"==j?"click":"tap",function(){
if(r=function(){
var r=I?1:"a"==j?2:0,o={
userName:b.weapp_username,
scene:1058,
sceneNote:encodeURIComponent(location.href),
relativeURL:s
};
return void 0!==b.app_version&&(o.appVersion=b.app_version),t?(f.invoke("openWeApp",o,function(t){
return"openWeApp:ok"===t.err_msg?window.__addIdKeyReport&&window.__addIdKeyReport("28307",102):"system:function_not_exist"===t.err_msg?n?m(i,e,b.nickname,c,r):d(i,e,b.nickname,c,r):void a(107,new Error(t.err_msg),"");
}),window.__addIdKeyReport&&window.__addIdKeyReport("28307",100),p(i,e,b.nickname,c,3,r,I?2:0),
I&&window.__addIdKeyReport&&window.__addIdKeyReport("28307",115),!1):n?m(i,e,b.nickname,c,r):d(i,e,b.nickname,c,r);
},I){
document.getElementById("js_minipro_dialog_name").innerText=b.nickname;
var o=document.getElementById("js_minipro_dialog");
return o.style.display="block",o._appid=i,o._i=e,o._nickname=b.nickname,o._title=c,
p(i,e,b.nickname,c,3,1,0),t&&window.__addIdKeyReport&&window.__addIdKeyReport("28307",114),
!1;
}
return r();
},"a"==j);
}
})(b);
var j=null,I=function(){
j=null;
for(var e=window.innerHeight||document.documentElement.clientHeight,t=0;t<R.length;t++){
var n=R[t].elem,i=n.tagName.toLowerCase(),a=n.firstChild&&1==n.firstChild.nodeType,r=a?1:"a"==i?2:0,o=R[t].elem.getBoundingClientRect();
o.top<e&&o.bottom>0&&(setTimeout(function(){
window.__addIdKeyReport&&window.__addIdKeyReport("28307",101);
},0),p(R[t].appid,t,y[R[t].appid].nickname,R[t].title,2,r),R.splice(t--,1));
}
};
I(),g.on(window,"scroll",function(){
j||(j=setTimeout(I,100));
});
}catch(z){
a(106,z,"parsing weapp info error");
}
},
error:function(){}
});
}
function l(){
for(var e=0;e<v.length+y.length;e++){
var t=e<v.length,n=t?v[e]:y[e-v.length],i=n.getAttribute(t?"data-miniprogram-appid":"data-weapp-appid")||"",a=n.getAttribute(t?"data-miniprogram-path":"data-weapp-path")||"",p=n.getAttribute(t?"data-miniprogram-imageUrl":"data-weapp-imageUrl")||"",r=n.getAttribute(t?"data-miniprogram-title":"data-weapp-title")||"",o=document.createElement("span");
n.setAttribute("class",""),o.setAttribute("class","weapp_display_element js_weapp_display_element"),
k.push({
appid:i,
path:a,
imageUrl:p,
title:r,
elem:o
}),R.push({
appid:i,
elem:o,
title:r
}),n.parentNode.insertBefore(o,n.nextSibling);
}
for(var e=0;e<b.length;e++){
var d=b[e];
k.push({
appid:d.getAttribute("data-miniprogram-appid"),
path:d.getAttribute("data-miniprogram-path"),
elem:d
}),R.push({
appid:d.getAttribute("data-miniprogram-appid"),
elem:d,
title:""
});
}
}
function c(e){
return document.getElementById(e);
}
e("biz_common/utils/string/html.js");
var _=e("pages/weapp_tpl.html.js"),u=e("biz_wap/utils/ajax.js"),g=e("biz_common/dom/event.js"),w=e("biz_common/tmpl.js"),f=e("biz_wap/jsapi/core.js"),h=e("biz_common/dom/class.js"),y=null,v=null,b=null,j={},k=[],I=[],R=[];
return r()?(l(),s(),j):void 0;
});define("appmsg/voice.js",["biz_common/utils/string/html.js","pages/voice_tpl.html.js","pages/voice_component.js"],function(e){
"use strict";
function i(){
var e=d("js_content");
return e?(r._oElements=e.getElementsByTagName("mpvoice")||[],r._oElements.length<=0?!1:!0):!1;
}
function o(){
r.musicLen=r._oElements.length;
}
function n(){
for(var e=0,i=0;i<r.musicLen;i++){
var o=r._oElements[i],n={},c=o.getAttribute("voice_encode_fileid")||"";
try{
c=decodeURIComponent(c);
}catch(d){}
n.voiceid=s.encodeStr(c),n.voiceid=n.voiceid.replace(/&#61;/g,"=").replace(/^\s/,"").replace(/\s$/,""),
n.src=r.srcRoot.replace("#meidaid#",n.voiceid),n.voiceid&&"undefined"!=n.voiceid&&(t(o,n,e),
e++);
}
}
function t(e,i,o){
i.duration=parseInt((1*e.getAttribute("play_length")||0)/1e3,10),i.duration_str=s.formatTime(i.duration),
i.posIndex=o;
var n=e.getAttribute("name")||"";
try{
n=decodeURIComponent(n);
}catch(t){}
i.title=s.encodeStr(n).replace(/^\s/,"").replace(/\s$/,""),i.fileSize=1*e.getAttribute("high_size")||0,
i.nickname=window.nickname,s.renderPlayer(a,i,e),c(i),r.musicList[i.voiceid+"_"+i.posIndex]=i;
}
function c(e){
var i=e.voiceid+"_"+e.posIndex,o="";
if(window.voice_in_appmsg&&window.voice_in_appmsg[e.voiceid]){
var n=window.voice_in_appmsg[e.voiceid],t=window.biz||"",c=window.mid||"",a=window.idx||"";
n.bizuin&&n.appmsgid&&n.idx&&(t=n.bizuin,c=n.appmsgid,a=n.idx);
var r=window.location.protocol||"https:";
o=r+"//mp.weixin.qq.com/mp/audio?_wxindex_=#_wxindex_#&scene=104&__biz=#biz#&mid=#mid#&idx=#idx#&voice_id=#voice_id#&sn=#sn##wechat_redirect".replace("#_wxindex_#",e.posIndex).replace("#biz#",t).replace("#mid#",c).replace("#idx#",a).replace("#voice_id#",e.voiceid).replace("#sn#",n.sn||"");
}
var m=s.decodeStr(e.title);
e.player=s.init({
wxIndex:e.posIndex,
type:2,
songId:e.voiceid,
comment_id:"",
src:e.src,
allowPause:!0,
duration:e.duration,
title:m,
singer:window.nickname?window.nickname+"的语音":"公众号语音",
epname:"来自文章",
coverImgUrl:window.__appmsgCgiData.hd_head_img,
playingCss:"share_audio_playing",
playCssDom:d("voice_main_"+i),
playArea:d("voice_play_"+i),
progress:d("voice_progress_"+i),
fileSize:e.fileSize,
playtimeDom:d("voice_playtime_"+i),
bufferDom:d("voice_buffer_"+i),
playdotDom:d("voice_playdot_"+i),
seekRange:d("voice_seekRange_"+i),
seekContainer:d("voice_main_"+i),
loadingDom:d("voice_loading_"+i),
detailArea:o?d("voice_detail_"+i):"",
detailUrl:o,
webUrl:o
});
}
function d(e){
return document.getElementById(e);
}
e("biz_common/utils/string/html.js");
var a=e("pages/voice_tpl.html.js"),s=e("pages/voice_component.js"),r={
musicList:{},
musicLen:0,
srcRoot:location.protocol+"//res.wx.qq.com/voice/getvoice?mediaid=#meidaid#"
};
return i()?(o(),n(),r.musicList):void 0;
});define("appmsg/qqmusic.js",["biz_common/utils/string/html.js","pages/qqmusic_tpl.html.js","pages/voice_component.js"],function(e){
"use strict";
function i(){
var e=c("js_content");
return e?(u._oElements=e.getElementsByTagName("qqmusic")||[],u._oElements.length<=0?!1:!0):!1;
}
function t(){
u.musicLen=u._oElements.length;
}
function s(){
for(var e=0,i=0;i<u.musicLen;i++){
var t=u._oElements[i],s={};
s.musicid=o.encodeStr(t.getAttribute("musicid")||"").replace(/^\s/,"").replace(/\s$/,""),
s.musicid&&"undefined"!=s.musicid&&(m(t,s,e),e++);
}
}
function m(e,i,t){
i.media_id=o.encodeStr(e.getAttribute("mid")||"").replace(/^\s/,"").replace(/\s$/,""),
i.duration=parseInt((e.getAttribute("play_length")||0)/1e3,10),i.posIndex=t,i.musicImgPart=o.encodeStr(e.getAttribute("albumurl")||"").replace(/^\s/,"").replace(/\s$/,"");
var s="";
s=i.musicImgPart.split("/");
try{
s=s[s.length-1],s=s.split(".")[0];
}catch(m){
s="";
}
i.music_img=s?u.imgroot2.replace("#mid#",s):u.imgroot+i.musicImgPart,i.audiourl=o.encodeStr(e.getAttribute("audiourl")||"").replace(/^\s/,"").replace(/\s$/,""),
i.singer=o.encodeStr(e.getAttribute("singer")||"").replace(/^\s/,"").replace(/\s$/,""),
i.music_name=o.encodeStr(e.getAttribute("music_name")||"").replace(/^\s/,"").replace(/\s$/,""),
o.renderPlayer(r,i,e),n(i),u.musicList[i.musicid+"_"+i.posIndex]=i;
}
function n(e){
var i=e.musicid+"_"+e.posIndex,t=["http://i.y.qq.com/v8/playsong.html?referFrom=music.qq.com&songid=",e.musicid,"&songmid=",e.media_id,,"&ADTAG=weixin_gzh#wechat_redirect"].join(""),s=o.decodeStr(e.music_name);
e.player=o.init({
wxIndex:e.posIndex,
type:0,
comment_id:"",
mid:e.media_id,
songId:e.musicid,
duration:e.duration,
title:s,
singer:window.nickname?window.nickname+"推荐的歌":"公众号推荐的歌",
epname:"QQ音乐",
coverImgUrl:e.music_img,
playingCss:"qqmusic_playing",
playCssDom:c("qqmusic_main_"+i),
playArea:c("qqmusic_play_"+i),
detailUrl:t,
webUrl:t,
detailArea:c("qqmusic_home_"+i)
});
}
function c(e){
return document.getElementById(e);
}
e("biz_common/utils/string/html.js");
var r=e("pages/qqmusic_tpl.html.js"),o=e("pages/voice_component.js"),u={
imgroot:"https://imgcache.qq.com/music/photo/mid_album_68",
imgroot2:"https://y.gtimg.cn/music/photo_new/T002R68x68M000#mid#.jpg",
musicList:{},
musicLen:0
};
return i()?(t(),s(),u.musicList):void 0;
});