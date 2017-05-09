(function(){if(window.jQuery)
var _jQuery=window.jQuery;var jQuery=window.jQuery=function(selector,context){return new jQuery.prototype.init(selector,context);};if(window.$)
var _$=window.$;window.$=jQuery;var quickExpr=/^[^<]*(<(.|\s)+>)[^>]*$|^#(\w+)$/;var isSimple=/^.[^:#\[\.]*$/;jQuery.fn=jQuery.prototype={init:function(selector,context){selector=selector||document;if(selector.nodeType){this[0]=selector;this.length=1;return this;}else if(typeof selector=="string"){var match=quickExpr.exec(selector);if(match&&(match[1]||!context)){if(match[1])
selector=jQuery.clean([match[1]],context);else{var elem=document.getElementById(match[3]);if(elem)
if(elem.id!=match[3])
return jQuery().find(selector);else{this[0]=elem;this.length=1;return this;}
else
selector=[];}}else
return new jQuery(context).find(selector);}else if(jQuery.isFunction(selector))
return new jQuery(document)[jQuery.fn.ready?"ready":"load"](selector);return this.setArray(selector.constructor==Array&&selector||(selector.jquery||selector.length&&selector!=window&&!selector.nodeType&&selector[0]!=undefined&&selector[0].nodeType)&&jQuery.makeArray(selector)||[selector]);},jquery:"1.2.3",size:function(){return this.length;},length:0,get:function(num){return num==undefined?jQuery.makeArray(this):this[num];},pushStack:function(elems){var ret=jQuery(elems);ret.prevObject=this;return ret;},setArray:function(elems){this.length=0;Array.prototype.push.apply(this,elems);return this;},each:function(callback,args){return jQuery.each(this,callback,args);},index:function(elem){var ret=-1;this.each(function(i){if(this==elem)
ret=i;});return ret;},attr:function(name,value,type){var options=name;if(name.constructor==String)
if(value==undefined)
return this.length&&jQuery[type||"attr"](this[0],name)||undefined;else{options={};options[name]=value;}
return this.each(function(i){for(name in options)
jQuery.attr(type?this.style:this,name,jQuery.prop(this,options[name],type,i,name));});},css:function(key,value){if((key=='width'||key=='height')&&parseFloat(value)<0)
value=undefined;return this.attr(key,value,"curCSS");},text:function(text){if(typeof text!="object"&&text!=null)
return this.empty().append((this[0]&&this[0].ownerDocument||document).createTextNode(text));var ret="";jQuery.each(text||this,function(){jQuery.each(this.childNodes,function(){if(this.nodeType!=8)
ret+=this.nodeType!=1?this.nodeValue:jQuery.fn.text([this]);});});return ret;},wrapAll:function(html){if(this[0])
jQuery(html,this[0].ownerDocument).clone().insertBefore(this[0]).map(function(){var elem=this;while(elem.firstChild)
elem=elem.firstChild;return elem;}).append(this);return this;},wrapInner:function(html){return this.each(function(){jQuery(this).contents().wrapAll(html);});},wrap:function(html){return this.each(function(){jQuery(this).wrapAll(html);});},append:function(){return this.domManip(arguments,true,false,function(elem){if(this.nodeType==1)
this.appendChild(elem);});},prepend:function(){return this.domManip(arguments,true,true,function(elem){if(this.nodeType==1)
this.insertBefore(elem,this.firstChild);});},before:function(){return this.domManip(arguments,false,false,function(elem){this.parentNode.insertBefore(elem,this);});},after:function(){return this.domManip(arguments,false,true,function(elem){this.parentNode.insertBefore(elem,this.nextSibling);});},end:function(){return this.prevObject||jQuery([]);},find:function(selector){var elems=jQuery.map(this,function(elem){return jQuery.find(selector,elem);});return this.pushStack(/[^+>] [^+>]/.test(selector)||selector.indexOf("..")>-1?jQuery.unique(elems):elems);},clone:function(events){var ret=this.map(function(){if(jQuery.browser.msie&&!jQuery.isXMLDoc(this)){var clone=this.cloneNode(true),container=document.createElement("div");container.appendChild(clone);return jQuery.clean([container.innerHTML])[0];}else
return this.cloneNode(true);});var clone=ret.find("*").andSelf().each(function(){if(this[expando]!=undefined)
this[expando]=null;});if(events===true)
this.find("*").andSelf().each(function(i){if(this.nodeType==3)
return;var events=jQuery.data(this,"events");for(var type in events)
for(var handler in events[type])
jQuery.event.add(clone[i],type,events[type][handler],events[type][handler].data);});return ret;},filter:function(selector){return this.pushStack(jQuery.isFunction(selector)&&jQuery.grep(this,function(elem,i){return selector.call(elem,i);})||jQuery.multiFilter(selector,this));},not:function(selector){if(selector.constructor==String)
if(isSimple.test(selector))
return this.pushStack(jQuery.multiFilter(selector,this,true));else
selector=jQuery.multiFilter(selector,this);var isArrayLike=selector.length&&selector[selector.length-1]!==undefined&&!selector.nodeType;return this.filter(function(){return isArrayLike?jQuery.inArray(this,selector)<0:this!=selector;});},add:function(selector){return!selector?this:this.pushStack(jQuery.merge(this.get(),selector.constructor==String?jQuery(selector).get():selector.length!=undefined&&(!selector.nodeName||jQuery.nodeName(selector,"form"))?selector:[selector]));},is:function(selector){return selector?jQuery.multiFilter(selector,this).length>0:false;},hasClass:function(selector){return this.is("."+selector);},val:function(value){if(value==undefined){if(this.length){var elem=this[0];if(jQuery.nodeName(elem,"select")){var index=elem.selectedIndex,values=[],options=elem.options,one=elem.type=="select-one";if(index<0)
return null;for(var i=one?index:0,max=one?index+1:options.length;i<max;i++){var option=options[i];if(option.selected){value=jQuery.browser.msie&&!option.attributes.value.specified?option.text:option.value;if(one)
return value;values.push(value);}}
return values;}else
return(this[0].value||"").replace(/\r/g,"");}
return undefined;}
return this.each(function(){if(this.nodeType!=1)
return;if(value.constructor==Array&&/radio|checkbox/.test(this.type))
this.checked=(jQuery.inArray(this.value,value)>=0||jQuery.inArray(this.name,value)>=0);else if(jQuery.nodeName(this,"select")){var values=value.constructor==Array?value:[value];jQuery("option",this).each(function(){this.selected=(jQuery.inArray(this.value,values)>=0||jQuery.inArray(this.text,values)>=0);});if(!values.length)
this.selectedIndex=-1;}else
this.value=value;});},html:function(value){return value==undefined?(this.length?this[0].innerHTML:null):this.empty().append(value);},replaceWith:function(value){return this.after(value).remove();},eq:function(i){return this.slice(i,i+1);},slice:function(){return this.pushStack(Array.prototype.slice.apply(this,arguments));},map:function(callback){return this.pushStack(jQuery.map(this,function(elem,i){return callback.call(elem,i,elem);}));},andSelf:function(){return this.add(this.prevObject);},data:function(key,value){var parts=key.split(".");parts[1]=parts[1]?"."+parts[1]:"";if(value==null){var data=this.triggerHandler("getData"+parts[1]+"!",[parts[0]]);if(data==undefined&&this.length)
data=jQuery.data(this[0],key);return data==null&&parts[1]?this.data(parts[0]):data;}else
return this.trigger("setData"+parts[1]+"!",[parts[0],value]).each(function(){jQuery.data(this,key,value);});},removeData:function(key){return this.each(function(){jQuery.removeData(this,key);});},domManip:function(args,table,reverse,callback){var clone=this.length>1,elems;return this.each(function(){if(!elems){elems=jQuery.clean(args,this.ownerDocument);if(reverse)
elems.reverse();}
var obj=this;if(table&&jQuery.nodeName(this,"table")&&jQuery.nodeName(elems[0],"tr"))
obj=this.getElementsByTagName("tbody")[0]||this.appendChild(this.ownerDocument.createElement("tbody"));var scripts=jQuery([]);jQuery.each(elems,function(){var elem=clone?jQuery(this).clone(true)[0]:this;if(jQuery.nodeName(elem,"script")){scripts=scripts.add(elem);}else{if(elem.nodeType==1)
scripts=scripts.add(jQuery("script",elem).remove());callback.call(obj,elem);}});scripts.each(evalScript);});}};jQuery.prototype.init.prototype=jQuery.prototype;function evalScript(i,elem){if(elem.src)
jQuery.ajax({url:elem.src,async:false,dataType:"script"});else
jQuery.globalEval(elem.text||elem.textContent||elem.innerHTML||"");if(elem.parentNode)
elem.parentNode.removeChild(elem);}
jQuery.extend=jQuery.fn.extend=function(){var target=arguments[0]||{},i=1,length=arguments.length,deep=false,options;if(target.constructor==Boolean){deep=target;target=arguments[1]||{};i=2;}
if(typeof target!="object"&&typeof target!="function")
target={};if(length==1){target=this;i=0;}
for(;i<length;i++)
if((options=arguments[i])!=null)
for(var name in options){if(target===options[name])
continue;if(deep&&options[name]&&typeof options[name]=="object"&&target[name]&&!options[name].nodeType)
target[name]=jQuery.extend(target[name],options[name]);else if(options[name]!=undefined)
target[name]=options[name];}
return target;};var expando="jQuery"+(new Date()).getTime(),uuid=0,windowData={};var exclude=/z-?index|font-?weight|opacity|zoom|line-?height/i;jQuery.extend({noConflict:function(deep){window.$=_$;if(deep)
window.jQuery=_jQuery;return jQuery;},isFunction:function(fn){return!!fn&&typeof fn!="string"&&!fn.nodeName&&fn.constructor!=Array&&/function/i.test(fn+"");},isXMLDoc:function(elem){return elem.documentElement&&!elem.body||elem.tagName&&elem.ownerDocument&&!elem.ownerDocument.body;},globalEval:function(data){data=jQuery.trim(data);if(data){var head=document.getElementsByTagName("head")[0]||document.documentElement,script=document.createElement("script");script.type="text/javascript";if(jQuery.browser.msie)
script.text=data;else
script.appendChild(document.createTextNode(data));head.appendChild(script);head.removeChild(script);}},nodeName:function(elem,name){return elem.nodeName&&elem.nodeName.toUpperCase()==name.toUpperCase();},cache:{},data:function(elem,name,data){elem=elem==window?windowData:elem;var id=elem[expando];if(!id)
id=elem[expando]=++uuid;if(name&&!jQuery.cache[id])
jQuery.cache[id]={};if(data!=undefined)
jQuery.cache[id][name]=data;return name?jQuery.cache[id][name]:id;},removeData:function(elem,name){elem=elem==window?windowData:elem;var id=elem[expando];if(name){if(jQuery.cache[id]){delete jQuery.cache[id][name];name="";for(name in jQuery.cache[id])
break;if(!name)
jQuery.removeData(elem);}}else{try{delete elem[expando];}catch(e){if(elem.removeAttribute)
elem.removeAttribute(expando);}
delete jQuery.cache[id];}},each:function(object,callback,args){if(args){if(object.length==undefined){for(var name in object)
if(callback.apply(object[name],args)===false)
break;}else
for(var i=0,length=object.length;i<length;i++)
if(callback.apply(object[i],args)===false)
break;}else{if(object.length==undefined){for(var name in object)
if(callback.call(object[name],name,object[name])===false)
break;}else
for(var i=0,length=object.length,value=object[0];i<length&&callback.call(value,i,value)!==false;value=object[++i]){}}
return object;},prop:function(elem,value,type,i,name){if(jQuery.isFunction(value))
value=value.call(elem,i);return value&&value.constructor==Number&&type=="curCSS"&&!exclude.test(name)?value+"px":value;},className:{add:function(elem,classNames){jQuery.each((classNames||"").split(/\s+/),function(i,className){if(elem.nodeType==1&&!jQuery.className.has(elem.className,className))
elem.className+=(elem.className?" ":"")+className;});},remove:function(elem,classNames){if(elem.nodeType==1)
elem.className=classNames!=undefined?jQuery.grep(elem.className.split(/\s+/),function(className){return!jQuery.className.has(classNames,className);}).join(" "):"";},has:function(elem,className){return jQuery.inArray(className,(elem.className||elem).toString().split(/\s+/))>-1;}},swap:function(elem,options,callback){var old={};for(var name in options){old[name]=elem.style[name];elem.style[name]=options[name];}
callback.call(elem);for(var name in options)
elem.style[name]=old[name];},css:function(elem,name,force){if(name=="width"||name=="height"){var val,props={position:"absolute",visibility:"hidden",display:"block"},which=name=="width"?["Left","Right"]:["Top","Bottom"];function getWH(){val=name=="width"?elem.offsetWidth:elem.offsetHeight;var padding=0,border=0;jQuery.each(which,function(){padding+=parseFloat(jQuery.curCSS(elem,"padding"+this,true))||0;border+=parseFloat(jQuery.curCSS(elem,"border"+this+"Width",true))||0;});val-=Math.round(padding+border);}
if(jQuery(elem).is(":visible"))
getWH();else
jQuery.swap(elem,props,getWH);return Math.max(0,val);}
return jQuery.curCSS(elem,name,force);},curCSS:function(elem,name,force){var ret;function color(elem){if(!jQuery.browser.safari)
return false;var ret=document.defaultView.getComputedStyle(elem,null);return!ret||ret.getPropertyValue("color")=="";}
if(name=="opacity"&&jQuery.browser.msie){ret=jQuery.attr(elem.style,"opacity");return ret==""?"1":ret;}
if(jQuery.browser.opera&&name=="display"){var save=elem.style.outline;elem.style.outline="0 solid black";elem.style.outline=save;}
if(name.match(/float/i))
name=styleFloat;if(!force&&elem.style&&elem.style[name])
ret=elem.style[name];else if(document.defaultView&&document.defaultView.getComputedStyle){if(name.match(/float/i))
name="float";name=name.replace(/([A-Z])/g,"-$1").toLowerCase();var getComputedStyle=document.defaultView.getComputedStyle(elem,null);if(getComputedStyle&&!color(elem))
ret=getComputedStyle.getPropertyValue(name);else{var swap=[],stack=[];for(var a=elem;a&&color(a);a=a.parentNode)
stack.unshift(a);for(var i=0;i<stack.length;i++)
if(color(stack[i])){swap[i]=stack[i].style.display;stack[i].style.display="block";}
ret=name=="display"&&swap[stack.length-1]!=null?"none":(getComputedStyle&&getComputedStyle.getPropertyValue(name))||"";for(var i=0;i<swap.length;i++)
if(swap[i]!=null)
stack[i].style.display=swap[i];}
if(name=="opacity"&&ret=="")
ret="1";}else if(elem.currentStyle){var camelCase=name.replace(/\-(\w)/g,function(all,letter){return letter.toUpperCase();});ret=elem.currentStyle[name]||elem.currentStyle[camelCase];if(!/^\d+(px)?$/i.test(ret)&&/^\d/.test(ret)){var style=elem.style.left,runtimeStyle=elem.runtimeStyle.left;elem.runtimeStyle.left=elem.currentStyle.left;elem.style.left=ret||0;ret=elem.style.pixelLeft+"px";elem.style.left=style;elem.runtimeStyle.left=runtimeStyle;}}
return ret;},clean:function(elems,context){var ret=[];context=context||document;if(typeof context.createElement=='undefined')
context=context.ownerDocument||context[0]&&context[0].ownerDocument||document;jQuery.each(elems,function(i,elem){if(!elem)
return;if(elem.constructor==Number)
elem=elem.toString();if(typeof elem=="string"){elem=elem.replace(/(<(\w+)[^>]*?)\/>/g,function(all,front,tag){return tag.match(/^(abbr|br|col|img|input|link|meta|param|hr|area|embed)$/i)?all:front+"></"+tag+">";});var tags=jQuery.trim(elem).toLowerCase(),div=context.createElement("div");var wrap=!tags.indexOf("<opt")&&[1,"<select multiple='multiple'>","</select>"]||!tags.indexOf("<leg")&&[1,"<fieldset>","</fieldset>"]||tags.match(/^<(thead|tbody|tfoot|colg|cap)/)&&[1,"<table>","</table>"]||!tags.indexOf("<tr")&&[2,"<table><tbody>","</tbody></table>"]||(!tags.indexOf("<td")||!tags.indexOf("<th"))&&[3,"<table><tbody><tr>","</tr></tbody></table>"]||!tags.indexOf("<col")&&[2,"<table><tbody></tbody><colgroup>","</colgroup></table>"]||jQuery.browser.msie&&[1,"div<div>","</div>"]||[0,"",""];div.innerHTML=wrap[1]+elem+wrap[2];while(wrap[0]--)
div=div.lastChild;if(jQuery.browser.msie){var tbody=!tags.indexOf("<table")&&tags.indexOf("<tbody")<0?div.firstChild&&div.firstChild.childNodes:wrap[1]=="<table>"&&tags.indexOf("<tbody")<0?div.childNodes:[];for(var j=tbody.length-1;j>=0;--j)
if(jQuery.nodeName(tbody[j],"tbody")&&!tbody[j].childNodes.length)
tbody[j].parentNode.removeChild(tbody[j]);if(/^\s/.test(elem))
div.insertBefore(context.createTextNode(elem.match(/^\s*/)[0]),div.firstChild);}
elem=jQuery.makeArray(div.childNodes);}
if(elem.length===0&&(!jQuery.nodeName(elem,"form")&&!jQuery.nodeName(elem,"select")))
return;if(elem[0]==undefined||jQuery.nodeName(elem,"form")||elem.options)
ret.push(elem);else
ret=jQuery.merge(ret,elem);});return ret;},attr:function(elem,name,value){if(!elem||elem.nodeType==3||elem.nodeType==8)
return undefined;var fix=jQuery.isXMLDoc(elem)?{}:jQuery.props;if(name=="selected"&&jQuery.browser.safari)
elem.parentNode.selectedIndex;if(fix[name]){if(value!=undefined)
elem[fix[name]]=value;return elem[fix[name]];}else if(jQuery.browser.msie&&name=="style")
return jQuery.attr(elem.style,"cssText",value);else if(value==undefined&&jQuery.browser.msie&&jQuery.nodeName(elem,"form")&&(name=="action"||name=="method"))
return elem.getAttributeNode(name).nodeValue;else if(elem.tagName){if(value!=undefined){if(name=="type"&&jQuery.nodeName(elem,"input")&&elem.parentNode)
throw"type property can't be changed";elem.setAttribute(name,""+value);}
if(jQuery.browser.msie&&/href|src/.test(name)&&!jQuery.isXMLDoc(elem))
return elem.getAttribute(name,2);return elem.getAttribute(name);}else{if(name=="opacity"&&jQuery.browser.msie){if(value!=undefined){elem.zoom=1;elem.filter=(elem.filter||"").replace(/alpha\([^)]*\)/,"")+
(parseFloat(value).toString()=="NaN"?"":"alpha(opacity="+value*100+")");}
return elem.filter&&elem.filter.indexOf("opacity=")>=0?(parseFloat(elem.filter.match(/opacity=([^)]*)/)[1])/100).toString():"";}
name=name.replace(/-([a-z])/ig,function(all,letter){return letter.toUpperCase();});if(value!=undefined)
elem[name]=value;return elem[name];}},trim:function(text){return(text||"").replace(/^\s+|\s+$/g,"");},makeArray:function(array){var ret=[];if(typeof array!="array")
for(var i=0,length=array.length;i<length;i++)
ret.push(array[i]);else
ret=array.slice(0);return ret;},inArray:function(elem,array){for(var i=0,length=array.length;i<length;i++)
if(array[i]==elem)
return i;return-1;},merge:function(first,second){if(jQuery.browser.msie){for(var i=0;second[i];i++)
if(second[i].nodeType!=8)
first.push(second[i]);}else
for(var i=0;second[i];i++)
first.push(second[i]);return first;},unique:function(array){var ret=[],done={};try{for(var i=0,length=array.length;i<length;i++){var id=jQuery.data(array[i]);if(!done[id]){done[id]=true;ret.push(array[i]);}}}catch(e){ret=array;}
return ret;},grep:function(elems,callback,inv){var ret=[];for(var i=0,length=elems.length;i<length;i++)
if(!inv&&callback(elems[i],i)||inv&&!callback(elems[i],i))
ret.push(elems[i]);return ret;},map:function(elems,callback){var ret=[];for(var i=0,length=elems.length;i<length;i++){var value=callback(elems[i],i);if(value!==null&&value!=undefined){if(value.constructor!=Array)
value=[value];ret=ret.concat(value);}}
return ret;}});var userAgent=navigator.userAgent.toLowerCase();jQuery.browser={version:(userAgent.match(/.+(?:rv|it|ra|ie)[\/: ]([\d.]+)/)||[])[1],safari:/webkit/.test(userAgent),opera:/opera/.test(userAgent),msie:/msie/.test(userAgent)&&!/opera/.test(userAgent),mozilla:/mozilla/.test(userAgent)&&!/(compatible|webkit)/.test(userAgent)};var styleFloat=jQuery.browser.msie?"styleFloat":"cssFloat";jQuery.extend({boxModel:!jQuery.browser.msie||document.compatMode=="CSS1Compat",props:{"for":"htmlFor","class":"className","float":styleFloat,cssFloat:styleFloat,styleFloat:styleFloat,innerHTML:"innerHTML",className:"className",value:"value",disabled:"disabled",checked:"checked",readonly:"readOnly",selected:"selected",maxlength:"maxLength",selectedIndex:"selectedIndex",defaultValue:"defaultValue",tagName:"tagName",nodeName:"nodeName"}});jQuery.each({parent:function(elem){return elem.parentNode;},parents:function(elem){return jQuery.dir(elem,"parentNode");},next:function(elem){return jQuery.nth(elem,2,"nextSibling");},prev:function(elem){return jQuery.nth(elem,2,"previousSibling");},nextAll:function(elem){return jQuery.dir(elem,"nextSibling");},prevAll:function(elem){return jQuery.dir(elem,"previousSibling");},siblings:function(elem){return jQuery.sibling(elem.parentNode.firstChild,elem);},children:function(elem){return jQuery.sibling(elem.firstChild);},contents:function(elem){return jQuery.nodeName(elem,"iframe")?elem.contentDocument||elem.contentWindow.document:jQuery.makeArray(elem.childNodes);}},function(name,fn){jQuery.fn[name]=function(selector){var ret=jQuery.map(this,fn);if(selector&&typeof selector=="string")
ret=jQuery.multiFilter(selector,ret);return this.pushStack(jQuery.unique(ret));};});jQuery.each({appendTo:"append",prependTo:"prepend",insertBefore:"before",insertAfter:"after",replaceAll:"replaceWith"},function(name,original){jQuery.fn[name]=function(){var args=arguments;return this.each(function(){for(var i=0,length=args.length;i<length;i++)
jQuery(args[i])[original](this);});};});jQuery.each({removeAttr:function(name){jQuery.attr(this,name,"");if(this.nodeType==1)
this.removeAttribute(name);},addClass:function(classNames){jQuery.className.add(this,classNames);},removeClass:function(classNames){jQuery.className.remove(this,classNames);},toggleClass:function(classNames){jQuery.className[jQuery.className.has(this,classNames)?"remove":"add"](this,classNames);},remove:function(selector){if(!selector||jQuery.filter(selector,[this]).r.length){jQuery("*",this).add(this).each(function(){jQuery.event.remove(this);jQuery.removeData(this);});if(this.parentNode)
this.parentNode.removeChild(this);}},empty:function(){jQuery(">*",this).remove();while(this.firstChild)
this.removeChild(this.firstChild);}},function(name,fn){jQuery.fn[name]=function(){return this.each(fn,arguments);};});jQuery.each(["Height","Width"],function(i,name){var type=name.toLowerCase();jQuery.fn[type]=function(size){return this[0]==window?jQuery.browser.opera&&document.body["client"+name]||jQuery.browser.safari&&window["inner"+name]||document.compatMode=="CSS1Compat"&&document.documentElement["client"+name]||document.body["client"+name]:this[0]==document?Math.max(Math.max(document.body["scroll"+name],document.documentElement["scroll"+name]),Math.max(document.body["offset"+name],document.documentElement["offset"+name])):size==undefined?(this.length?jQuery.css(this[0],type):null):this.css(type,size.constructor==String?size:size+"px");};});var chars=jQuery.browser.safari&&parseInt(jQuery.browser.version)<417?"(?:[\\w*_-]|\\\\.)":"(?:[\\w\u0128-\uFFFF*_-]|\\\\.)",quickChild=new RegExp("^>\\s*("+chars+"+)"),quickID=new RegExp("^("+chars+"+)(#)("+chars+"+)"),quickClass=new RegExp("^([#.]?)("+chars+"*)");jQuery.extend({expr:{"":function(a,i,m){return m[2]=="*"||jQuery.nodeName(a,m[2]);},"#":function(a,i,m){return a.getAttribute("id")==m[2];},":":{lt:function(a,i,m){return i<m[3]-0;},gt:function(a,i,m){return i>m[3]-0;},nth:function(a,i,m){return m[3]-0==i;},eq:function(a,i,m){return m[3]-0==i;},first:function(a,i){return i==0;},last:function(a,i,m,r){return i==r.length-1;},even:function(a,i){return i%2==0;},odd:function(a,i){return i%2;},"first-child":function(a){return a.parentNode.getElementsByTagName("*")[0]==a;},"last-child":function(a){return jQuery.nth(a.parentNode.lastChild,1,"previousSibling")==a;},"only-child":function(a){return!jQuery.nth(a.parentNode.lastChild,2,"previousSibling");},parent:function(a){return a.firstChild;},empty:function(a){return!a.firstChild;},contains:function(a,i,m){return(a.textContent||a.innerText||jQuery(a).text()||"").indexOf(m[3])>=0;},visible:function(a){return"hidden"!=a.type&&jQuery.css(a,"display")!="none"&&jQuery.css(a,"visibility")!="hidden";},hidden:function(a){return"hidden"==a.type||jQuery.css(a,"display")=="none"||jQuery.css(a,"visibility")=="hidden";},enabled:function(a){return!a.disabled;},disabled:function(a){return a.disabled;},checked:function(a){return a.checked;},selected:function(a){return a.selected||jQuery.attr(a,"selected");},text:function(a){return"text"==a.type;},radio:function(a){return"radio"==a.type;},checkbox:function(a){return"checkbox"==a.type;},file:function(a){return"file"==a.type;},password:function(a){return"password"==a.type;},submit:function(a){return"submit"==a.type;},image:function(a){return"image"==a.type;},reset:function(a){return"reset"==a.type;},button:function(a){return"button"==a.type||jQuery.nodeName(a,"button");},input:function(a){return/input|select|textarea|button/i.test(a.nodeName);},has:function(a,i,m){return jQuery.find(m[3],a).length;},header:function(a){return/h\d/i.test(a.nodeName);},animated:function(a){return jQuery.grep(jQuery.timers,function(fn){return a==fn.elem;}).length;}}},parse:[/^(\[) *@?([\w-]+) *([!*$^~=]*) *('?"?)(.*?)\4 *\]/,/^(:)([\w-]+)\("?'?(.*?(\(.*?\))?[^(]*?)"?'?\)/,new RegExp("^([:.#]*)("+chars+"+)")],multiFilter:function(expr,elems,not){var old,cur=[];while(expr&&expr!=old){old=expr;var f=jQuery.filter(expr,elems,not);expr=f.t.replace(/^\s*,\s*/,"");cur=not?elems=f.r:jQuery.merge(cur,f.r);}
return cur;},find:function(t,context){if(typeof t!="string")
return[t];if(context&&context.nodeType!=1&&context.nodeType!=9)
return[];context=context||document;var ret=[context],done=[],last,nodeName;while(t&&last!=t){var r=[];last=t;t=jQuery.trim(t);var foundToken=false;var re=quickChild;var m=re.exec(t);if(m){nodeName=m[1].toUpperCase();for(var i=0;ret[i];i++)
for(var c=ret[i].firstChild;c;c=c.nextSibling)
if(c.nodeType==1&&(nodeName=="*"||c.nodeName.toUpperCase()==nodeName))
r.push(c);ret=r;t=t.replace(re,"");if(t.indexOf(" ")==0)continue;foundToken=true;}else{re=/^([>+~])\s*(\w*)/i;if((m=re.exec(t))!=null){r=[];var merge={};nodeName=m[2].toUpperCase();m=m[1];for(var j=0,rl=ret.length;j<rl;j++){var n=m=="~"||m=="+"?ret[j].nextSibling:ret[j].firstChild;for(;n;n=n.nextSibling)
if(n.nodeType==1){var id=jQuery.data(n);if(m=="~"&&merge[id])break;if(!nodeName||n.nodeName.toUpperCase()==nodeName){if(m=="~")merge[id]=true;r.push(n);}
if(m=="+")break;}}
ret=r;t=jQuery.trim(t.replace(re,""));foundToken=true;}}
if(t&&!foundToken){if(!t.indexOf(",")){if(context==ret[0])ret.shift();done=jQuery.merge(done,ret);r=ret=[context];t=" "+t.substr(1,t.length);}else{var re2=quickID;var m=re2.exec(t);if(m){m=[0,m[2],m[3],m[1]];}else{re2=quickClass;m=re2.exec(t);}
m[2]=m[2].replace(/\\/g,"");var elem=ret[ret.length-1];if(m[1]=="#"&&elem&&elem.getElementById&&!jQuery.isXMLDoc(elem)){var oid=elem.getElementById(m[2]);if((jQuery.browser.msie||jQuery.browser.opera)&&oid&&typeof oid.id=="string"&&oid.id!=m[2])
oid=jQuery('[@id="'+m[2]+'"]',elem)[0];ret=r=oid&&(!m[3]||jQuery.nodeName(oid,m[3]))?[oid]:[];}else{for(var i=0;ret[i];i++){var tag=m[1]=="#"&&m[3]?m[3]:m[1]!=""||m[0]==""?"*":m[2];if(tag=="*"&&ret[i].nodeName.toLowerCase()=="object")
tag="param";r=jQuery.merge(r,ret[i].getElementsByTagName(tag));}
if(m[1]==".")
r=jQuery.classFilter(r,m[2]);if(m[1]=="#"){var tmp=[];for(var i=0;r[i];i++)
if(r[i].getAttribute("id")==m[2]){tmp=[r[i]];break;}
r=tmp;}
ret=r;}
t=t.replace(re2,"");}}
if(t){var val=jQuery.filter(t,r);ret=r=val.r;t=jQuery.trim(val.t);}}
if(t)
ret=[];if(ret&&context==ret[0])
ret.shift();done=jQuery.merge(done,ret);return done;},classFilter:function(r,m,not){m=" "+m+" ";var tmp=[];for(var i=0;r[i];i++){var pass=(" "+r[i].className+" ").indexOf(m)>=0;if(!not&&pass||not&&!pass)
tmp.push(r[i]);}
return tmp;},filter:function(t,r,not){var last;while(t&&t!=last){last=t;var p=jQuery.parse,m;for(var i=0;p[i];i++){m=p[i].exec(t);if(m){t=t.substring(m[0].length);m[2]=m[2].replace(/\\/g,"");break;}}
if(!m)
break;if(m[1]==":"&&m[2]=="not")
r=isSimple.test(m[3])?jQuery.filter(m[3],r,true).r:jQuery(r).not(m[3]);else if(m[1]==".")
r=jQuery.classFilter(r,m[2],not);else if(m[1]=="["){var tmp=[],type=m[3];for(var i=0,rl=r.length;i<rl;i++){var a=r[i],z=a[jQuery.props[m[2]]||m[2]];if(z==null||/href|src|selected/.test(m[2]))
z=jQuery.attr(a,m[2])||'';if((type==""&&!!z||type=="="&&z==m[5]||type=="!="&&z!=m[5]||type=="^="&&z&&!z.indexOf(m[5])||type=="$="&&z.substr(z.length-m[5].length)==m[5]||(type=="*="||type=="~=")&&z.indexOf(m[5])>=0)^not)
tmp.push(a);}
r=tmp;}else if(m[1]==":"&&m[2]=="nth-child"){var merge={},tmp=[],test=/(-?)(\d*)n((?:\+|-)?\d*)/.exec(m[3]=="even"&&"2n"||m[3]=="odd"&&"2n+1"||!/\D/.test(m[3])&&"0n+"+m[3]||m[3]),first=(test[1]+(test[2]||1))-0,last=test[3]-0;for(var i=0,rl=r.length;i<rl;i++){var node=r[i],parentNode=node.parentNode,id=jQuery.data(parentNode);if(!merge[id]){var c=1;for(var n=parentNode.firstChild;n;n=n.nextSibling)
if(n.nodeType==1)
n.nodeIndex=c++;merge[id]=true;}
var add=false;if(first==0){if(node.nodeIndex==last)
add=true;}else if((node.nodeIndex-last)%first==0&&(node.nodeIndex-last)/first>=0)
add=true;if(add^not)
tmp.push(node);}
r=tmp;}else{var fn=jQuery.expr[m[1]];if(typeof fn=="object")
fn=fn[m[2]];if(typeof fn=="string")
fn=eval("false||function(a,i){return "+fn+";}");r=jQuery.grep(r,function(elem,i){return fn(elem,i,m,r);},not);}}
return{r:r,t:t};},dir:function(elem,dir){var matched=[];var cur=elem[dir];while(cur&&cur!=document){if(cur.nodeType==1)
matched.push(cur);cur=cur[dir];}
return matched;},nth:function(cur,result,dir,elem){result=result||1;var num=0;for(;cur;cur=cur[dir])
if(cur.nodeType==1&&++num==result)
break;return cur;},sibling:function(n,elem){var r=[];for(;n;n=n.nextSibling){if(n.nodeType==1&&(!elem||n!=elem))
r.push(n);}
return r;}});jQuery.event={add:function(elem,types,handler,data){if(elem.nodeType==3||elem.nodeType==8)
return;if(jQuery.browser.msie&&elem.setInterval!=undefined)
elem=window;if(!handler.guid)
handler.guid=this.guid++;if(data!=undefined){var fn=handler;handler=function(){return fn.apply(this,arguments);};handler.data=data;handler.guid=fn.guid;}
var events=jQuery.data(elem,"events")||jQuery.data(elem,"events",{}),handle=jQuery.data(elem,"handle")||jQuery.data(elem,"handle",function(){var val;if(typeof jQuery=="undefined"||jQuery.event.triggered)
return val;val=jQuery.event.handle.apply(arguments.callee.elem,arguments);return val;});handle.elem=elem;jQuery.each(types.split(/\s+/),function(index,type){var parts=type.split(".");type=parts[0];handler.type=parts[1];var handlers=events[type];if(!handlers){handlers=events[type]={};if(!jQuery.event.special[type]||jQuery.event.special[type].setup.call(elem)===false){if(elem.addEventListener)
elem.addEventListener(type,handle,false);else if(elem.attachEvent)
elem.attachEvent("on"+type,handle);}}
handlers[handler.guid]=handler;jQuery.event.global[type]=true;});elem=null;},guid:1,global:{},remove:function(elem,types,handler){if(elem.nodeType==3||elem.nodeType==8)
return;var events=jQuery.data(elem,"events"),ret,index;if(events){if(types==undefined||(typeof types=="string"&&types.charAt(0)=="."))
for(var type in events)
this.remove(elem,type+(types||""));else{if(types.type){handler=types.handler;types=types.type;}
jQuery.each(types.split(/\s+/),function(index,type){var parts=type.split(".");type=parts[0];if(events[type]){if(handler)
delete events[type][handler.guid];else
for(handler in events[type])
if(!parts[1]||events[type][handler].type==parts[1])
delete events[type][handler];for(ret in events[type])break;if(!ret){if(!jQuery.event.special[type]||jQuery.event.special[type].teardown.call(elem)===false){if(elem.removeEventListener)
elem.removeEventListener(type,jQuery.data(elem,"handle"),false);else if(elem.detachEvent)
elem.detachEvent("on"+type,jQuery.data(elem,"handle"));}
ret=null;delete events[type];}}});}
for(ret in events)break;if(!ret){var handle=jQuery.data(elem,"handle");if(handle)handle.elem=null;jQuery.removeData(elem,"events");jQuery.removeData(elem,"handle");}}},trigger:function(type,data,elem,donative,extra){data=jQuery.makeArray(data||[]);if(type.indexOf("!")>=0){type=type.slice(0,-1);var exclusive=true;}
if(!elem){if(this.global[type])
jQuery("*").add([window,document]).trigger(type,data);}else{if(elem.nodeType==3||elem.nodeType==8)
return undefined;var val,ret,fn=jQuery.isFunction(elem[type]||null),event=!data[0]||!data[0].preventDefault;if(event)
data.unshift(this.fix({type:type,target:elem}));data[0].type=type;if(exclusive)
data[0].exclusive=true;if(jQuery.isFunction(jQuery.data(elem,"handle")))
val=jQuery.data(elem,"handle").apply(elem,data);if(!fn&&elem["on"+type]&&elem["on"+type].apply(elem,data)===false)
val=false;if(event)
data.shift();if(extra&&jQuery.isFunction(extra)){ret=extra.apply(elem,val==null?data:data.concat(val));if(ret!==undefined)
val=ret;}
if(fn&&donative!==false&&val!==false&&!(jQuery.nodeName(elem,'a')&&type=="click")){this.triggered=true;try{elem[type]();}catch(e){}}
this.triggered=false;}
return val;},handle:function(event){var val;event=jQuery.event.fix(event||window.event||{});var parts=event.type.split(".");event.type=parts[0];var handlers=jQuery.data(this,"events")&&jQuery.data(this,"events")[event.type],args=Array.prototype.slice.call(arguments,1);args.unshift(event);for(var j in handlers){var handler=handlers[j];args[0].handler=handler;args[0].data=handler.data;if(!parts[1]&&!event.exclusive||handler.type==parts[1]){var ret=handler.apply(this,args);if(val!==false)
val=ret;if(ret===false){event.preventDefault();event.stopPropagation();}}}
if(jQuery.browser.msie)
event.target=event.preventDefault=event.stopPropagation=event.handler=event.data=null;return val;},fix:function(event){var originalEvent=event;event=jQuery.extend({},originalEvent);event.preventDefault=function(){if(originalEvent.preventDefault)
originalEvent.preventDefault();originalEvent.returnValue=false;};event.stopPropagation=function(){if(originalEvent.stopPropagation)
originalEvent.stopPropagation();originalEvent.cancelBubble=true;};if(!event.target)
event.target=event.srcElement||document;if(event.target.nodeType==3)
event.target=originalEvent.target.parentNode;if(!event.relatedTarget&&event.fromElement)
event.relatedTarget=event.fromElement==event.target?event.toElement:event.fromElement;if(event.pageX==null&&event.clientX!=null){var doc=document.documentElement,body=document.body;event.pageX=event.clientX+(doc&&doc.scrollLeft||body&&body.scrollLeft||0)-(doc.clientLeft||0);event.pageY=event.clientY+(doc&&doc.scrollTop||body&&body.scrollTop||0)-(doc.clientTop||0);}
if(!event.which&&((event.charCode||event.charCode===0)?event.charCode:event.keyCode))
event.which=event.charCode||event.keyCode;if(!event.metaKey&&event.ctrlKey)
event.metaKey=event.ctrlKey;if(!event.which&&event.button)
event.which=(event.button&1?1:(event.button&2?3:(event.button&4?2:0)));return event;},special:{ready:{setup:function(){bindReady();return;},teardown:function(){return;}},mouseenter:{setup:function(){if(jQuery.browser.msie)return false;jQuery(this).bind("mouseover",jQuery.event.special.mouseenter.handler);return true;},teardown:function(){if(jQuery.browser.msie)return false;jQuery(this).unbind("mouseover",jQuery.event.special.mouseenter.handler);return true;},handler:function(event){if(withinElement(event,this))return true;arguments[0].type="mouseenter";return jQuery.event.handle.apply(this,arguments);}},mouseleave:{setup:function(){if(jQuery.browser.msie)return false;jQuery(this).bind("mouseout",jQuery.event.special.mouseleave.handler);return true;},teardown:function(){if(jQuery.browser.msie)return false;jQuery(this).unbind("mouseout",jQuery.event.special.mouseleave.handler);return true;},handler:function(event){if(withinElement(event,this))return true;arguments[0].type="mouseleave";return jQuery.event.handle.apply(this,arguments);}}}};jQuery.fn.extend({bind:function(type,data,fn){return type=="unload"?this.one(type,data,fn):this.each(function(){jQuery.event.add(this,type,fn||data,fn&&data);});},one:function(type,data,fn){return this.each(function(){jQuery.event.add(this,type,function(event){jQuery(this).unbind(event);return(fn||data).apply(this,arguments);},fn&&data);});},unbind:function(type,fn){return this.each(function(){jQuery.event.remove(this,type,fn);});},trigger:function(type,data,fn){return this.each(function(){jQuery.event.trigger(type,data,this,true,fn);});},triggerHandler:function(type,data,fn){if(this[0])
return jQuery.event.trigger(type,data,this[0],false,fn);return undefined;},toggle:function(){var args=arguments;return this.click(function(event){this.lastToggle=0==this.lastToggle?1:0;event.preventDefault();return args[this.lastToggle].apply(this,arguments)||false;});},hover:function(fnOver,fnOut){return this.bind('mouseenter',fnOver).bind('mouseleave',fnOut);},ready:function(fn){bindReady();if(jQuery.isReady)
fn.call(document,jQuery);else
jQuery.readyList.push(function(){return fn.call(this,jQuery);});return this;}});jQuery.extend({isReady:false,readyList:[],ready:function(){if(!jQuery.isReady){jQuery.isReady=true;if(jQuery.readyList){jQuery.each(jQuery.readyList,function(){this.apply(document);});jQuery.readyList=null;}
jQuery(document).triggerHandler("ready");}}});var readyBound=false;function bindReady(){if(readyBound)return;readyBound=true;if(document.addEventListener&&!jQuery.browser.opera)
document.addEventListener("DOMContentLoaded",jQuery.ready,false);if(jQuery.browser.msie&&window==top)(function(){if(jQuery.isReady)return;try{document.documentElement.doScroll("left");}catch(error){setTimeout(arguments.callee,0);return;}
jQuery.ready();})();if(jQuery.browser.opera)
document.addEventListener("DOMContentLoaded",function(){if(jQuery.isReady)return;for(var i=0;i<document.styleSheets.length;i++)
if(document.styleSheets[i].disabled){setTimeout(arguments.callee,0);return;}
jQuery.ready();},false);if(jQuery.browser.safari){var numStyles;(function(){if(jQuery.isReady)return;if(document.readyState!="loaded"&&document.readyState!="complete"){setTimeout(arguments.callee,0);return;}
if(numStyles===undefined)
numStyles=jQuery("style, link[rel=stylesheet]").length;if(document.styleSheets.length!=numStyles){setTimeout(arguments.callee,0);return;}
jQuery.ready();})();}
jQuery.event.add(window,"load",jQuery.ready);}
jQuery.each(("blur,focus,load,resize,scroll,unload,click,dblclick,"+"mousedown,mouseup,mousemove,mouseover,mouseout,change,select,"+"submit,keydown,keypress,keyup,error").split(","),function(i,name){jQuery.fn[name]=function(fn){return fn?this.bind(name,fn):this.trigger(name);};});var withinElement=function(event,elem){var parent=event.relatedTarget;while(parent&&parent!=elem)try{parent=parent.parentNode;}catch(error){parent=elem;}
return parent==elem;};jQuery(window).bind("unload",function(){jQuery("*").add(document).unbind();});jQuery.fn.extend({load:function(url,params,callback){if(jQuery.isFunction(url))
return this.bind("load",url);var off=url.indexOf(" ");if(off>=0){var selector=url.slice(off,url.length);url=url.slice(0,off);}
callback=callback||function(){};var type="GET";if(params)
if(jQuery.isFunction(params)){callback=params;params=null;}else{params=jQuery.param(params);type="POST";}
var self=this;jQuery.ajax({url:url,type:type,dataType:"html",data:params,complete:function(res,status){if(status=="success"||status=="notmodified")
self.html(selector?jQuery("<div/>").append(res.responseText.replace(/<script(.|\s)*?\/script>/g,"")).find(selector):res.responseText);self.each(callback,[res.responseText,status,res]);}});return this;},serialize:function(){return jQuery.param(this.serializeArray());},serializeArray:function(){return this.map(function(){return jQuery.nodeName(this,"form")?jQuery.makeArray(this.elements):this;}).filter(function(){return this.name&&!this.disabled&&(this.checked||/select|textarea/i.test(this.nodeName)||/text|hidden|password/i.test(this.type));}).map(function(i,elem){var val=jQuery(this).val();return val==null?null:val.constructor==Array?jQuery.map(val,function(val,i){return{name:elem.name,value:val};}):{name:elem.name,value:val};}).get();}});jQuery.each("ajaxStart,ajaxStop,ajaxComplete,ajaxError,ajaxSuccess,ajaxSend".split(","),function(i,o){jQuery.fn[o]=function(f){return this.bind(o,f);};});var jsc=(new Date).getTime();jQuery.extend({get:function(url,data,callback,type){if(jQuery.isFunction(data)){callback=data;data=null;}
return jQuery.ajax({type:"GET",url:url,data:data,success:callback,dataType:type});},getScript:function(url,callback){return jQuery.get(url,null,callback,"script");},getJSON:function(url,data,callback){return jQuery.get(url,data,callback,"json");},post:function(url,data,callback,type){if(jQuery.isFunction(data)){callback=data;data={};}
return jQuery.ajax({type:"POST",url:url,data:data,success:callback,dataType:type});},ajaxSetup:function(settings){jQuery.extend(jQuery.ajaxSettings,settings);},ajaxSettings:{global:true,type:"GET",timeout:0,contentType:"application/x-www-form-urlencoded",processData:true,async:true,data:null,username:null,password:null,accepts:{xml:"application/xml, text/xml",html:"text/html",script:"text/javascript, application/javascript",json:"application/json, text/javascript",text:"text/plain",_default:"*/*"}},lastModified:{},ajax:function(s){var jsonp,jsre=/=\?(&|$)/g,status,data;s=jQuery.extend(true,s,jQuery.extend(true,{},jQuery.ajaxSettings,s));if(s.data&&s.processData&&typeof s.data!="string")
s.data=jQuery.param(s.data);if(s.dataType=="jsonp"){if(s.type.toLowerCase()=="get"){if(!s.url.match(jsre))
s.url+=(s.url.match(/\?/)?"&":"?")+(s.jsonp||"callback")+"=?";}else if(!s.data||!s.data.match(jsre))
s.data=(s.data?s.data+"&":"")+(s.jsonp||"callback")+"=?";s.dataType="json";}
if(s.dataType=="json"&&(s.data&&s.data.match(jsre)||s.url.match(jsre))){jsonp="jsonp"+jsc++;if(s.data)
s.data=(s.data+"").replace(jsre,"="+jsonp+"$1");s.url=s.url.replace(jsre,"="+jsonp+"$1");s.dataType="script";window[jsonp]=function(tmp){data=tmp;success();complete();window[jsonp]=undefined;try{delete window[jsonp];}catch(e){}
if(head)
head.removeChild(script);};}
if(s.dataType=="script"&&s.cache==null)
s.cache=false;if(s.cache===false&&s.type.toLowerCase()=="get"){var ts=(new Date()).getTime();var ret=s.url.replace(/(\?|&)_=.*?(&|$)/,"$1_="+ts+"$2");s.url=ret+((ret==s.url)?(s.url.match(/\?/)?"&":"?")+"_="+ts:"");}
if(s.data&&s.type.toLowerCase()=="get"){s.url+=(s.url.match(/\?/)?"&":"?")+s.data;s.data=null;}
if(s.global&&!jQuery.active++)
jQuery.event.trigger("ajaxStart");if((!s.url.indexOf("http")||!s.url.indexOf("//"))&&s.dataType=="script"&&s.type.toLowerCase()=="get"){var head=document.getElementsByTagName("head")[0];var script=document.createElement("script");script.src=s.url;if(s.scriptCharset)
script.charset=s.scriptCharset;if(!jsonp){var done=false;script.onload=script.onreadystatechange=function(){if(!done&&(!this.readyState||this.readyState=="loaded"||this.readyState=="complete")){done=true;success();complete();head.removeChild(script);}};}
head.appendChild(script);return undefined;}
var requestDone=false;var xml=window.ActiveXObject?new ActiveXObject("Microsoft.XMLHTTP"):new XMLHttpRequest();xml.open(s.type,s.url,s.async,s.username,s.password);try{if(s.data)
xml.setRequestHeader("Content-Type",s.contentType);if(s.ifModified)
xml.setRequestHeader("If-Modified-Since",jQuery.lastModified[s.url]||"Thu, 01 Jan 1970 00:00:00 GMT");xml.setRequestHeader("X-Requested-With","XMLHttpRequest");xml.setRequestHeader("Accept",s.dataType&&s.accepts[s.dataType]?s.accepts[s.dataType]+", */*":s.accepts._default);}catch(e){}
if(s.beforeSend)
s.beforeSend(xml);if(s.global)
jQuery.event.trigger("ajaxSend",[xml,s]);var onreadystatechange=function(isTimeout){if(!requestDone&&xml&&(xml.readyState==4||isTimeout=="timeout")){requestDone=true;if(ival){clearInterval(ival);ival=null;}
status=isTimeout=="timeout"&&"timeout"||!jQuery.httpSuccess(xml)&&"error"||s.ifModified&&jQuery.httpNotModified(xml,s.url)&&"notmodified"||"success";if(status=="success"){try{data=jQuery.httpData(xml,s.dataType);}catch(e){status="parsererror";}}
if(status=="success"){var modRes;try{modRes=xml.getResponseHeader("Last-Modified");}catch(e){}
if(s.ifModified&&modRes)
jQuery.lastModified[s.url]=modRes;if(!jsonp)
success();}else
jQuery.handleError(s,xml,status);complete();if(s.async)
xml=null;}};if(s.async){var ival=setInterval(onreadystatechange,13);if(s.timeout>0)
setTimeout(function(){if(xml){xml.abort();if(!requestDone)
onreadystatechange("timeout");}},s.timeout);}
try{xml.send(s.data);}catch(e){jQuery.handleError(s,xml,null,e);}
if(!s.async)
onreadystatechange();function success(){if(s.success)
s.success(data,status);if(s.global)
jQuery.event.trigger("ajaxSuccess",[xml,s]);}
function complete(){if(s.complete)
s.complete(xml,status);if(s.global)
jQuery.event.trigger("ajaxComplete",[xml,s]);if(s.global&&!--jQuery.active)
jQuery.event.trigger("ajaxStop");}
return xml;},handleError:function(s,xml,status,e){if(s.error)s.error(xml,status,e);if(s.global)
jQuery.event.trigger("ajaxError",[xml,s,e]);},active:0,httpSuccess:function(r){try{return!r.status&&location.protocol=="file:"||(r.status>=200&&r.status<300)||r.status==304||r.status==1223||jQuery.browser.safari&&r.status==undefined;}catch(e){}
return false;},httpNotModified:function(xml,url){try{var xmlRes=xml.getResponseHeader("Last-Modified");return xml.status==304||xmlRes==jQuery.lastModified[url]||jQuery.browser.safari&&xml.status==undefined;}catch(e){}
return false;},httpData:function(r,type){var ct=r.getResponseHeader("content-type");var xml=type=="xml"||!type&&ct&&ct.indexOf("xml")>=0;var data=xml?r.responseXML:r.responseText;if(xml&&data.documentElement.tagName=="parsererror")
throw"parsererror";if(type=="script")
jQuery.globalEval(data);if(type=="json")
data=eval("("+data+")");return data;},param:function(a){var s=[];if(a.constructor==Array||a.jquery)
jQuery.each(a,function(){s.push(encodeURIComponent(this.name)+"="+encodeURIComponent(this.value));});else
for(var j in a)
if(a[j]&&a[j].constructor==Array)
jQuery.each(a[j],function(){s.push(encodeURIComponent(j)+"="+encodeURIComponent(this));});else
s.push(encodeURIComponent(j)+"="+encodeURIComponent(a[j]));return s.join("&").replace(/%20/g,"+");}});jQuery.fn.extend({show:function(speed,callback){return speed?this.animate({height:"show",width:"show",opacity:"show"},speed,callback):this.filter(":hidden").each(function(){this.style.display=this.oldblock||"";if(jQuery.css(this,"display")=="none"){var elem=jQuery("<"+this.tagName+" />").appendTo("body");this.style.display=elem.css("display");if(this.style.display=="none")
this.style.display="block";elem.remove();}}).end();},hide:function(speed,callback){return speed?this.animate({height:"hide",width:"hide",opacity:"hide"},speed,callback):this.filter(":visible").each(function(){this.oldblock=this.oldblock||jQuery.css(this,"display");this.style.display="none";}).end();},_toggle:jQuery.fn.toggle,toggle:function(fn,fn2){return jQuery.isFunction(fn)&&jQuery.isFunction(fn2)?this._toggle(fn,fn2):fn?this.animate({height:"toggle",width:"toggle",opacity:"toggle"},fn,fn2):this.each(function(){jQuery(this)[jQuery(this).is(":hidden")?"show":"hide"]();});},slideDown:function(speed,callback){return this.animate({height:"show"},speed,callback);},slideUp:function(speed,callback){return this.animate({height:"hide"},speed,callback);},slideToggle:function(speed,callback){return this.animate({height:"toggle"},speed,callback);},fadeIn:function(speed,callback){return this.animate({opacity:"show"},speed,callback);},fadeOut:function(speed,callback){return this.animate({opacity:"hide"},speed,callback);},fadeTo:function(speed,to,callback){return this.animate({opacity:to},speed,callback);},animate:function(prop,speed,easing,callback){var optall=jQuery.speed(speed,easing,callback);return this[optall.queue===false?"each":"queue"](function(){if(this.nodeType!=1)
return false;var opt=jQuery.extend({},optall);var hidden=jQuery(this).is(":hidden"),self=this;for(var p in prop){if(prop[p]=="hide"&&hidden||prop[p]=="show"&&!hidden)
return jQuery.isFunction(opt.complete)&&opt.complete.apply(this);if(p=="height"||p=="width"){opt.display=jQuery.css(this,"display");opt.overflow=this.style.overflow;}}
if(opt.overflow!=null)
this.style.overflow="hidden";opt.curAnim=jQuery.extend({},prop);jQuery.each(prop,function(name,val){var e=new jQuery.fx(self,opt,name);if(/toggle|show|hide/.test(val))
e[val=="toggle"?hidden?"show":"hide":val](prop);else{var parts=val.toString().match(/^([+-]=)?([\d+-.]+)(.*)$/),start=e.cur(true)||0;if(parts){var end=parseFloat(parts[2]),unit=parts[3]||"px";if(unit!="px"){self.style[name]=(end||1)+unit;start=((end||1)/e.cur(true))*start;self.style[name]=start+unit;}
if(parts[1])
end=((parts[1]=="-="?-1:1)*end)+start;e.custom(start,end,unit);}else
e.custom(start,val,"");}});return true;});},queue:function(type,fn){if(jQuery.isFunction(type)||(type&&type.constructor==Array)){fn=type;type="fx";}
if(!type||(typeof type=="string"&&!fn))
return queue(this[0],type);return this.each(function(){if(fn.constructor==Array)
queue(this,type,fn);else{queue(this,type).push(fn);if(queue(this,type).length==1)
fn.apply(this);}});},stop:function(clearQueue,gotoEnd){var timers=jQuery.timers;if(clearQueue)
this.queue([]);this.each(function(){for(var i=timers.length-1;i>=0;i--)
if(timers[i].elem==this){if(gotoEnd)
timers[i](true);timers.splice(i,1);}});if(!gotoEnd)
this.dequeue();return this;}});var queue=function(elem,type,array){if(!elem)
return undefined;type=type||"fx";var q=jQuery.data(elem,type+"queue");if(!q||array)
q=jQuery.data(elem,type+"queue",array?jQuery.makeArray(array):[]);return q;};jQuery.fn.dequeue=function(type){type=type||"fx";return this.each(function(){var q=queue(this,type);q.shift();if(q.length)
q[0].apply(this);});};jQuery.extend({speed:function(speed,easing,fn){var opt=speed&&speed.constructor==Object?speed:{complete:fn||!fn&&easing||jQuery.isFunction(speed)&&speed,duration:speed,easing:fn&&easing||easing&&easing.constructor!=Function&&easing};opt.duration=(opt.duration&&opt.duration.constructor==Number?opt.duration:{slow:600,fast:200}[opt.duration])||400;opt.old=opt.complete;opt.complete=function(){if(opt.queue!==false)
jQuery(this).dequeue();if(jQuery.isFunction(opt.old))
opt.old.apply(this);};return opt;},easing:{linear:function(p,n,firstNum,diff){return firstNum+diff*p;},swing:function(p,n,firstNum,diff){return((-Math.cos(p*Math.PI)/2)+0.5)*diff+firstNum;}},timers:[],timerId:null,fx:function(elem,options,prop){this.options=options;this.elem=elem;this.prop=prop;if(!options.orig)
options.orig={};}});jQuery.fx.prototype={update:function(){if(this.options.step)
this.options.step.apply(this.elem,[this.now,this]);(jQuery.fx.step[this.prop]||jQuery.fx.step._default)(this);if(this.prop=="height"||this.prop=="width")
this.elem.style.display="block";},cur:function(force){if(this.elem[this.prop]!=null&&this.elem.style[this.prop]==null)
return this.elem[this.prop];var r=parseFloat(jQuery.css(this.elem,this.prop,force));return r&&r>-10000?r:parseFloat(jQuery.curCSS(this.elem,this.prop))||0;},custom:function(from,to,unit){this.startTime=(new Date()).getTime();this.start=from;this.end=to;this.unit=unit||this.unit||"px";this.now=this.start;this.pos=this.state=0;this.update();var self=this;function t(gotoEnd){return self.step(gotoEnd);}
t.elem=this.elem;jQuery.timers.push(t);if(jQuery.timerId==null){jQuery.timerId=setInterval(function(){var timers=jQuery.timers;for(var i=0;i<timers.length;i++)
if(!timers[i]())
timers.splice(i--,1);if(!timers.length){clearInterval(jQuery.timerId);jQuery.timerId=null;}},13);}},show:function(){this.options.orig[this.prop]=jQuery.attr(this.elem.style,this.prop);this.options.show=true;this.custom(0,this.cur());if(this.prop=="width"||this.prop=="height")
this.elem.style[this.prop]="1px";jQuery(this.elem).show();},hide:function(){this.options.orig[this.prop]=jQuery.attr(this.elem.style,this.prop);this.options.hide=true;this.custom(this.cur(),0);},step:function(gotoEnd){var t=(new Date()).getTime();if(gotoEnd||t>this.options.duration+this.startTime){this.now=this.end;this.pos=this.state=1;this.update();this.options.curAnim[this.prop]=true;var done=true;for(var i in this.options.curAnim)
if(this.options.curAnim[i]!==true)
done=false;if(done){if(this.options.display!=null){this.elem.style.overflow=this.options.overflow;this.elem.style.display=this.options.display;if(jQuery.css(this.elem,"display")=="none")
this.elem.style.display="block";}
if(this.options.hide)
this.elem.style.display="none";if(this.options.hide||this.options.show)
for(var p in this.options.curAnim)
jQuery.attr(this.elem.style,p,this.options.orig[p]);}
if(done&&jQuery.isFunction(this.options.complete))
this.options.complete.apply(this.elem);return false;}else{var n=t-this.startTime;this.state=n/this.options.duration;this.pos=jQuery.easing[this.options.easing||(jQuery.easing.swing?"swing":"linear")](this.state,n,0,1,this.options.duration);this.now=this.start+((this.end-this.start)*this.pos);this.update();}
return true;}};jQuery.fx.step={scrollLeft:function(fx){fx.elem.scrollLeft=fx.now;},scrollTop:function(fx){fx.elem.scrollTop=fx.now;},opacity:function(fx){jQuery.attr(fx.elem.style,"opacity",fx.now);},_default:function(fx){fx.elem.style[fx.prop]=fx.now+fx.unit;}};jQuery.fn.offset=function(){var left=0,top=0,elem=this[0],results;if(elem)with(jQuery.browser){var parent=elem.parentNode,offsetChild=elem,offsetParent=elem.offsetParent,doc=elem.ownerDocument,safari2=safari&&parseInt(version)<522&&!/adobeair/i.test(userAgent),fixed=jQuery.css(elem,"position")=="fixed";if(elem.getBoundingClientRect){var box=elem.getBoundingClientRect();add(box.left+Math.max(doc.documentElement.scrollLeft,doc.body.scrollLeft),box.top+Math.max(doc.documentElement.scrollTop,doc.body.scrollTop));add(-doc.documentElement.clientLeft,-doc.documentElement.clientTop);}else{add(elem.offsetLeft,elem.offsetTop);while(offsetParent){add(offsetParent.offsetLeft,offsetParent.offsetTop);if(mozilla&&!/^t(able|d|h)$/i.test(offsetParent.tagName)||safari&&!safari2)
border(offsetParent);if(!fixed&&jQuery.css(offsetParent,"position")=="fixed")
fixed=true;offsetChild=/^body$/i.test(offsetParent.tagName)?offsetChild:offsetParent;offsetParent=offsetParent.offsetParent;}
while(parent&&parent.tagName&&!/^body|html$/i.test(parent.tagName)){if(!/^inline|table.*$/i.test(jQuery.css(parent,"display")))
add(-parent.scrollLeft,-parent.scrollTop);if(mozilla&&jQuery.css(parent,"overflow")!="visible")
border(parent);parent=parent.parentNode;}
if((safari2&&(fixed||jQuery.css(offsetChild,"position")=="absolute"))||(mozilla&&jQuery.css(offsetChild,"position")!="absolute"))
add(-doc.body.offsetLeft,-doc.body.offsetTop);if(fixed)
add(Math.max(doc.documentElement.scrollLeft,doc.body.scrollLeft),Math.max(doc.documentElement.scrollTop,doc.body.scrollTop));}
results={top:top,left:left};}
function border(elem){add(jQuery.curCSS(elem,"borderLeftWidth",true),jQuery.curCSS(elem,"borderTopWidth",true));}
function add(l,t){left+=parseInt(l)||0;top+=parseInt(t)||0;}
return results;};})();;if(typeof jQuery=='undefined'){throw'Unable to load Shadowbox, jQuery library not found.';}
var Shadowbox={};Shadowbox.lib={getStyle:function(el,style){return jQuery(el).css(style);},setStyle:function(el,style,value){if(typeof style!='object'){var temp={};temp[style]=value;style=temp;}
jQuery(el).css(style);},get:function(el){return(typeof el=='string')?document.getElementById(el):el;},remove:function(el){jQuery(el).remove();},getTarget:function(e){return e.target;},preventDefault:function(e){e=e.browserEvent||e;if(e.preventDefault){e.preventDefault();}else{e.returnValue=false;}},addEvent:function(el,name,handler){jQuery(el).bind(name,handler);},removeEvent:function(el,name,handler){jQuery(el).unbind(name,handler);},animate:function(el,obj,duration,callback){duration=Math.round(duration*1000);var o={};for(var p in obj){for(var p in obj){o[p]=String(obj[p].to);if(p!='opacity')o[p]+='px';}}
jQuery(el).animate(o,duration,null,callback);}};(function($){$.fn.shadowbox=function(options){return this.each(function(){var $this=$(this);var opts=$.extend({},options||{},$.metadata?$this.metadata():$.meta?$this.data():{});var cls=this.className||'';opts.width=parseInt((cls.match(/w:(\d+)/)||[])[1])||opts.width;opts.height=parseInt((cls.match(/h:(\d+)/)||[])[1])||opts.height;Shadowbox.setup($this,opts);});};})(jQuery);;if(typeof Shadowbox=='undefined'){throw'Unable to load Shadowbox, no base library adapter found.';}
(function(){var version='1.0';var options={assetURL:'',loadingImage:'images/loading.gif',animate:true,animSequence:'wh',flvPlayer:'flvplayer.swf',overlayColor:'#000',overlayOpacity:0.85,overlayBgImage:'images/overlay-85.png',listenOverlay:true,autoplayMovies:true,showMovieControls:true,resizeDuration:0.35,fadeDuration:0.35,displayNav:true,continuous:false,displayCounter:true,counterType:'default',viewportPadding:20,handleLgImages:'resize',initialHeight:160,initialWidth:320,enableKeys:true,keysClose:['c','q',27],keysNext:['n',39],keysPrev:['p',37],onOpen:null,onFinish:null,onChange:null,onClose:null,handleUnsupported:'link',skipSetup:false,text:{cancel:'Cancel',loading:'loading',close:'<span class="shortcut">C</span>lose',next:'<span class="shortcut">N</span>ext',prev:'<span class="shortcut">P</span>revious',errors:{single:'You must install the <a href="{0}">{1}</a> browser plugin to view this content.',shared:'You must install both the <a href="{0}">{1}</a> and <a href="{2}">{3}</a> browser plugins to view this content.',either:'You must install either the <a href="{0}">{1}</a> or the <a href="{2}">{3}</a> browser plugin to view this content.'}},errors:{fla:{name:'Flash',url:'http://www.adobe.com/products/flashplayer/'},qt:{name:'QuickTime',url:'http://www.apple.com/quicktime/download/'},wmp:{name:'Windows Media Player',url:'http://www.microsoft.com/windows/windowsmedia/'},f4m:{name:'Flip4Mac',url:'http://www.flip4mac.com/wmv_download.htm'}},skin:{main:'<div id="shadowbox_overlay"></div>'+'<div id="shadowbox_container">'+'<div id="shadowbox">'+'<div id="shadowbox_title">'+'<div id="shadowbox_title_inner"></div>'+'</div>'+'<div id="shadowbox_body">'+'<div id="shadowbox_body_inner"></div>'+'<div id="shadowbox_loading"></div>'+'</div>'+'<div id="shadowbox_toolbar">'+'<div id="shadowbox_toolbar_inner"></div>'+'</div>'+'</div>'+'</div>',loading:'<img src="{0}" alt="{1}" />'+'<span><a href="javascript:Shadowbox.close();">{2}</a></span>',counter:'<div id="shadowbox_counter">{0}</div>',close:'<div id="shadowbox_nav_close">'+'<a href="javascript:Shadowbox.close();">{0}</a>'+'</div>',next:'<div id="shadowbox_nav_next">'+'<a href="javascript:Shadowbox.next();">{0}</a>'+'</div>',prev:'<div id="shadowbox_nav_previous">'+'<a href="javascript:Shadowbox.previous();">{0}</a>'+'</div>'},ext:{img:['png','jpg','jpeg','gif','bmp'],qt:['dv','mov','moov','movie','mp4'],wmp:['asf','wm','wmv'],qtwmp:['avi','mpg','mpeg'],iframe:['asp','aspx','cgi','cfm','htm','html','pl','php','php3','php4','php5','phtml','rb','rhtml','shtml','txt','vbs']}};var default_options=null;var SL=Shadowbox.lib;var RE={resize:/(img|swf|flv)/,overlay:/(img|iframe|html|inline)/,swf:/\.swf\s*$/i,flv:/\.flv\s*$/i,domain:/:\/\/(.*?)[:\/]/,inline:/#(.+)$/,rel:/^(light|shadow)box/i,gallery:/^(light|shadow)box\[(.*?)\]/i,unsupported:/^unsupported-(\w+)/,param:/\s*([a-z_]*?)\s*=\s*(.+)\s*/,empty:/^(?:br|frame|hr|img|input|link|meta|range|spacer|wbr|area|param|col)$/i};var cache=[];var current_gallery;var current;var optimal_height=options.initialHeight;var optimal_width=options.initialWidth;var current_height=0;var current_width=0;var preloader;var initialized=false;var activated=false;var drag;var draggable;var overlay_img_needed;var ua=navigator.userAgent.toLowerCase();var isStrict=document.compatMode=='CSS1Compat',isOpera=ua.indexOf("opera")>-1,isIE=ua.indexOf('msie')>-1,isIE7=ua.indexOf('msie 7')>-1,isBorderBox=isIE&&!isStrict,isSafari=(/webkit|khtml/).test(ua),isSafari3=isSafari&&!!(document.evaluate),isGecko=!isSafari&&ua.indexOf('gecko')>-1,isWindows=(ua.indexOf('windows')!=-1||ua.indexOf('win32')!=-1),isMac=(ua.indexOf('macintosh')!=-1||ua.indexOf('mac os x')!=-1),isLinux=(ua.indexOf('linux')!=-1);var absolute_pos=isIE&&!isIE7;var plugins=null;if(navigator.plugins&&navigator.plugins.length){var detectPlugin=function(plugin_name){var detected=false;for(var i=0,len=navigator.plugins.length;i<len;++i){if(navigator.plugins[i].name.indexOf(plugin_name)>-1){detected=true;break;}}
return detected;};var f4m=detectPlugin('Flip4Mac');var plugins={fla:detectPlugin('Shockwave Flash'),qt:detectPlugin('QuickTime'),wmp:!f4m&&detectPlugin('Windows Media'),f4m:f4m};}else{var detectPlugin=function(plugin_name){var detected=false;try{var axo=new ActiveXObject(plugin_name);if(axo){detected=true;}}catch(e){}
return detected;};var plugins={fla:detectPlugin('ShockwaveFlash.ShockwaveFlash'),qt:detectPlugin('QuickTime.QuickTime'),wmp:detectPlugin('wmplayer.ocx'),f4m:false};}
var apply=function(o,e){for(var p in e)o[p]=e[p];return o;};var isLink=function(el){return typeof el.tagName=='string'&&(el.tagName.toUpperCase()=='A'||el.tagName.toUpperCase()=='AREA');};SL.getViewportHeight=function(){var height=window.innerHeight;var mode=document.compatMode;if((mode||isIE)&&!isOpera){height=isStrict?document.documentElement.clientHeight:document.body.clientHeight;}
return height;};SL.getViewportWidth=function(){var width=window.innerWidth;var mode=document.compatMode;if(mode||isIE){width=isStrict?document.documentElement.clientWidth:document.body.clientWidth;}
return width;};SL.getDocumentHeight=function(){var scrollHeight=isStrict?document.documentElement.scrollHeight:document.body.scrollHeight;return Math.max(scrollHeight,SL.getViewportHeight());};SL.getDocumentWidth=function(){var scrollWidth=isStrict?document.documentElement.scrollWidth:document.body.scrollWidth;return Math.max(scrollWidth,SL.getViewportWidth());};var clearOpacity=function(el){if(isIE){if(typeof el.style.filter=='string'&&(/alpha/i).test(el.style.filter)){el.style.filter='';}}else{el.style.opacity='';el.style['-moz-opacity']='';el.style['-khtml-opacity']='';}};var fadeIn=function(el,endingOpacity,duration,callback){if(options.animate){SL.setStyle(el,'opacity',0);el.style.visibility='visible';SL.animate(el,{opacity:{to:endingOpacity}},duration,function(){if(endingOpacity==1)clearOpacity(el);if(typeof callback=='function')callback();});}else{if(endingOpacity==1){clearOpacity(el);}else{SL.setStyle(el,'opacity',endingOpacity);}
el.style.visibility='visible';if(typeof callback=='function')callback();}};var fadeOut=function(el,duration,callback){var cb=function(){el.style.visibility='hidden';clearOpacity(el);if(typeof callback=='function')callback();};if(options.animate){SL.animate(el,{opacity:{to:0}},duration,cb);}else{cb();}};var appendHTML=function(el,html){el=SL.get(el);if(el.insertAdjacentHTML){el.insertAdjacentHTML('BeforeEnd',html);return el.lastChild;}
if(el.lastChild){var range=el.ownerDocument.createRange();range.setStartAfter(el.lastChild);var frag=range.createContextualFragment(html);el.appendChild(frag);return el.lastChild;}else{el.innerHTML=html;return el.lastChild;}};var overwriteHTML=function(el,html){el=SL.get(el);el.innerHTML=html;return el.firstChild;};var getComputedHeight=function(el){var h=Math.max(el.offsetHeight,el.clientHeight);if(!h){h=parseInt(SL.getStyle(el,'height'),10)||0;if(!isBorderBox){h+=parseInt(SL.getStyle(el,'padding-top'),10)
+parseInt(SL.getStyle(el,'padding-bottom'),10)
+parseInt(SL.getStyle(el,'border-top-width'),10)
+parseInt(SL.getStyle(el,'border-bottom-width'),10);}}
return h;};var getComputedWidth=function(el){var w=Math.max(el.offsetWidth,el.clientWidth);if(!w){w=parseInt(SL.getStyle(el,'width'),10)||0;if(!isBorderBox){w+=parseInt(SL.getStyle(el,'padding-left'),10)
+parseInt(SL.getStyle(el,'padding-right'),10)
+parseInt(SL.getStyle(el,'border-left-width'),10)
+parseInt(SL.getStyle(el,'border-right-width'),10);}}
return w;};var getPlayerType=function(url){if(RE.img.test(url))return'img';var match=url.match(RE.domain);var this_domain=match?document.domain==match[1]:false;if(url.indexOf('#')>-1&&this_domain)return'inline';var q_index=url.indexOf('?');if(q_index>-1)url=url.substring(0,q_index);if(RE.swf.test(url))return plugins.fla?'swf':'unsupported-swf';if(RE.flv.test(url))return plugins.fla?'flv':'unsupported-flv';if(RE.qt.test(url))return plugins.qt?'qt':'unsupported-qt';if(RE.wmp.test(url)){if(plugins.wmp){return'wmp';}else if(plugins.f4m){return'qt';}else{return isMac?(plugins.qt?'unsupported-f4m':'unsupported-qtf4m'):'unsupported-wmp';}}else if(RE.qtwmp.test(url)){if(plugins.qt){return'qt';}else if(plugins.wmp){return'wmp';}else{return isMac?'unsupported-qt':'unsupported-qtwmp';}}else if(!this_domain||RE.iframe.test(url)){return'iframe';}
return'unsupported';};var handleClick=function(ev){var link;if(isLink(this)){link=this;}else{link=SL.getTarget(ev);while(!isLink(link)&&link.parentNode){link=link.parentNode;}}
Shadowbox.open(link);if(current_gallery.length)SL.preventDefault(ev);};var setupGallery=function(obj){var copy=apply({},obj);if(!obj.gallery){current_gallery=[copy];current=0;}else{current_gallery=[];var index,ci;for(var i=0,len=cache.length;i<len;++i){ci=cache[i];if(ci.gallery){if(ci.content==obj.content&&ci.gallery==obj.gallery&&ci.title==obj.title){index=current_gallery.length;}
if(ci.gallery==obj.gallery){current_gallery.push(apply({},ci));}}}
if(index==null){current_gallery.unshift(copy);index=0;}
current=index;}
var match,r;for(var i=0,len=current_gallery.length;i<len;++i){r=false;if(current_gallery[i].type=='unsupported'){r=true;}else if(match=RE.unsupported.exec(current_gallery[i].type)){if(options.handleUnsupported=='link'){current_gallery[i].type='html';var m;switch(match[1]){case'qtwmp':m=String.format(options.text.errors.either,options.errors.qt.url,options.errors.qt.name,options.errors.wmp.url,options.errors.wmp.name);break;case'qtf4m':m=String.format(options.text.errors.shared,options.errors.qt.url,options.errors.qt.name,options.errors.f4m.url,options.errors.f4m.name);break;default:if(match[1]=='swf'||match[1]=='flv')match[1]='fla';m=String.format(options.text.errors.single,options.errors[match[1]].url,options.errors[match[1]].name);}
current_gallery[i]=apply(current_gallery[i],{height:160,width:320,content:'<div class="shadowbox_message">'+m+'</div>'});}else{r=true;}}else if(current_gallery[i].type=='inline'){var match=RE.inline.exec(current_gallery[i].content);if(match){var el;if(el=SL.get(match[1])){current_gallery[i].content=el.innerHTML;}else{throw'No element found with id '+match[1];}}else{throw'No element id found for inline content';}}
if(r){current_gallery.splice(i,1);if(i<current)--current;--i;}}};var buildBars=function(){var link=current_gallery[current];if(!link)return;var title_i=SL.get('shadowbox_title_inner');title_i.innerHTML=(link.title)?link.title:'';var tool_i=SL.get('shadowbox_toolbar_inner');tool_i.innerHTML='';if(options.displayNav){tool_i.innerHTML=String.format(options.skin.close,options.text.close);if(current_gallery.length>1){if(options.continuous){appendHTML(tool_i,String.format(options.skin.next,options.text.next));appendHTML(tool_i,String.format(options.skin.prev,options.text.prev));}else{if((current_gallery.length-1)>current){appendHTML(tool_i,String.format(options.skin.next,options.text.next));}
if(current>0){appendHTML(tool_i,String.format(options.skin.prev,options.text.prev));}}}}
if(current_gallery.length>1&&options.displayCounter){var counter='';if(options.counterType=='skip'){for(var i=0,len=current_gallery.length;i<len;++i){counter+='<a href="javascript:Shadowbox.change('+i+');"';if(i==current){counter+=' class="shadowbox_counter_current"';}
counter+='>'+(i+1)+'</a>';}}else{counter=(current+1)+' of '+current_gallery.length;}
appendHTML(tool_i,String.format(options.skin.counter,counter));}};var hideBars=function(callback){var title_m=getComputedHeight(SL.get('shadowbox_title'));var tool_m=0-getComputedHeight(SL.get('shadowbox_toolbar'));var title_i=SL.get('shadowbox_title_inner');var tool_i=SL.get('shadowbox_toolbar_inner');if(options.animate&&callback){SL.animate(title_i,{marginTop:{to:title_m}},0.2);SL.animate(tool_i,{marginTop:{to:tool_m}},0.2,callback);}else{SL.setStyle(title_i,'marginTop',title_m+'px');SL.setStyle(tool_i,'marginTop',tool_m+'px');}};var showBars=function(callback){var title_i=SL.get('shadowbox_title_inner');if(options.animate){if(title_i.innerHTML!=''){SL.animate(title_i,{marginTop:{to:0}},0.35);}
SL.animate(SL.get('shadowbox_toolbar_inner'),{marginTop:{to:0}},0.35,callback);}else{if(title_i.innerHTML!=''){SL.setStyle(title_i,'margin-top','0px');}
SL.setStyle(SL.get('shadowbox_toolbar_inner'),'margin-top','0px');callback();}};var resetDrag=function(){drag={x:0,y:0,start_x:null,start_y:null};};var toggleDrag=function(on){if(on){resetDrag();var styles=['position:absolute','cursor:'+(isGecko?'-moz-grab':'move')];styles.push(isIE?'background-color:#fff;filter:alpha(opacity=0)':'background-color:transparent');appendHTML('shadowbox_body_inner','<div id="shadowbox_drag_layer" style="'+styles.join(';')+'"></div>');SL.addEvent(SL.get('shadowbox_drag_layer'),'mousedown',listenDrag);}else{var d=SL.get('shadowbox_drag_layer');if(d){SL.removeEvent(d,'mousedown',listenDrag);SL.remove(d);}}};var listenDrag=function(ev){drag.start_x=ev.clientX;drag.start_y=ev.clientY;draggable=SL.get('shadowbox_content');SL.addEvent(document,'mousemove',positionDrag);SL.addEvent(document,'mouseup',unlistenDrag);if(isGecko)SL.setStyle(SL.get('shadowbox_drag_layer'),'cursor','-moz-grabbing');};var unlistenDrag=function(){SL.removeEvent(document,'mousemove',positionDrag);SL.removeEvent(document,'mouseup',unlistenDrag);if(isGecko)SL.setStyle(SL.get('shadowbox_drag_layer'),'cursor','-moz-grab');};var positionDrag=function(ev){var move_y=ev.clientY-drag.start_y;drag.start_y=drag.start_y+move_y;drag.y=Math.max(Math.min(0,drag.y+move_y),current_height-optimal_height);SL.setStyle(draggable,'top',drag.y+'px');var move_x=ev.clientX-drag.start_x;drag.start_x=drag.start_x+move_x;drag.x=Math.max(Math.min(0,drag.x+move_x),current_width-optimal_width);SL.setStyle(draggable,'left',drag.x+'px');};var loadContent=function(){var obj=current_gallery[current];if(!obj)return;buildBars();switch(obj.type){case'img':preloader=new Image();preloader.onload=function(){var h=obj.height?parseInt(obj.height,10):preloader.height;var w=obj.width?parseInt(obj.width,10):preloader.width;resizeContent(h,w,function(dims){showBars(function(){setContent({tag:'img',height:dims.i_height,width:dims.i_width,src:obj.content,style:'position:absolute'});if(dims.enableDrag&&options.handleLgImages=='drag'){toggleDrag(true);SL.setStyle(SL.get('shadowbox_drag_layer'),{height:dims.i_height+'px',width:dims.i_width+'px'});}
finishContent();});});preloader.onload=function(){};};preloader.src=obj.content;break;case'swf':case'flv':case'qt':case'wmp':var markup=Shadowbox.movieMarkup(obj);resizeContent(markup.height,markup.width,function(){showBars(function(){setContent(markup);finishContent();});});break;case'iframe':var h=obj.height?parseInt(obj.height,10):SL.getViewportHeight();var w=obj.width?parseInt(obj.width,10):SL.getViewportWidth();var content={tag:'iframe',name:'shadowbox_content',height:'100%',width:'100%',frameborder:'0',marginwidth:'0',marginheight:'0',scrolling:'auto'};resizeContent(h,w,function(dims){showBars(function(){setContent(content);var win=(isIE)?SL.get('shadowbox_content').contentWindow:window.frames['shadowbox_content'];win.location=obj.content;finishContent();});});break;case'html':case'inline':var h=obj.height?parseInt(obj.height,10):SL.getViewportHeight();var w=obj.width?parseInt(obj.width,10):SL.getViewportWidth();var content={tag:'div',cls:'html',html:obj.content};resizeContent(h,w,function(){showBars(function(){setContent(content);finishContent();});});break;default:throw'Shadowbox cannot open content of type '+obj.type;}
if(current_gallery.length>0){var next=current_gallery[current+1];if(!next){next=current_gallery[0];}
if(next.type=='img'){var preload_next=new Image();preload_next.src=next.href;}
var prev=current_gallery[current-1];if(!prev){prev=current_gallery[current_gallery.length-1];}
if(prev.type=='img'){var preload_prev=new Image();preload_prev.src=prev.href;}}};var setContent=function(obj){var id='shadowbox_content';var content=SL.get(id);if(content){switch(content.tagName.toUpperCase()){case'OBJECT':var link=current_gallery[(obj?current-1:current)];if(link.type=='wmp'&&isIE){try{shadowbox_content.controls.stop();shadowbox_content.URL='non-existent.wmv';window.shadowbox_content=function(){};}catch(e){}}else if(link.type=='qt'&&isSafari){try{document.shadowbox_content.Stop();}catch(e){}
content.innerHTML='';}
setTimeout(function(){SL.remove(content);},10);break;case'IFRAME':SL.remove(content);if(isGecko)delete window.frames[id];break;default:SL.remove(content);}}
if(obj){if(!obj.id)obj.id=id;return appendHTML('shadowbox_body_inner',Shadowbox.createHTML(obj));}
return null;};var finishContent=function(){var obj=current_gallery[current];if(!obj)return;hideLoading(function(){listenKeyboard(true);if(options.onFinish&&typeof options.onFinish=='function'){options.onFinish(obj);}});};var resizeContent=function(height,width,callback){optimal_height=height;optimal_width=width;var resizable=RE.resize.test(current_gallery[current].type);var dims=getDimensions(optimal_height,optimal_width,resizable);if(callback){var cb=function(){callback(dims);};switch(options.animSequence){case'hw':adjustHeight(dims.height,dims.top,true,function(){adjustWidth(dims.width,true,cb);});break;case'wh':adjustWidth(dims.width,true,function(){adjustHeight(dims.height,dims.top,true,cb);});break;default:adjustWidth(dims.width,true);adjustHeight(dims.height,dims.top,true,cb);}}else{adjustWidth(dims.width,false);adjustHeight(dims.height,dims.top,false);if(options.handleLgImages=='resize'&&resizable){var content=SL.get('shadowbox_content');if(content){content.height=dims.i_height;content.width=dims.i_width;}}}};var getDimensions=function(o_height,o_width,resizable){if(typeof resizable=='undefined')resizable=false;var height=o_height=parseInt(o_height);var width=o_width=parseInt(o_width);var shadowbox_b=SL.get('shadowbox_body');var view_height=SL.getViewportHeight();var extra_height=parseInt(SL.getStyle(shadowbox_b,'border-top-width'),10)
+parseInt(SL.getStyle(shadowbox_b,'border-bottom-width'),10)
+parseInt(SL.getStyle(shadowbox_b,'margin-top'),10)
+parseInt(SL.getStyle(shadowbox_b,'margin-bottom'),10)
+getComputedHeight(SL.get('shadowbox_title'))
+getComputedHeight(SL.get('shadowbox_toolbar'))
+(2*options.viewportPadding);if((height+extra_height)>=view_height){height=view_height-extra_height;}
var view_width=SL.getViewportWidth();var extra_body_width=parseInt(SL.getStyle(shadowbox_b,'border-left-width'),10)
+parseInt(SL.getStyle(shadowbox_b,'border-right-width'),10)
+parseInt(SL.getStyle(shadowbox_b,'margin-left'),10)
+parseInt(SL.getStyle(shadowbox_b,'margin-right'),10);var extra_width=extra_body_width+(2*options.viewportPadding);if((width+extra_width)>=view_width){width=view_width-extra_width;}
var enableDrag=false;var i_height=o_height;var i_width=o_width;var handle=options.handleLgImages;if(resizable&&(handle=='resize'||handle=='drag')){var change_h=(o_height-height)/o_height;var change_w=(o_width-width)/o_width;if(handle=='resize'){if(change_h>change_w){width=Math.round((o_width/o_height)*height);}else if(change_w>change_h){height=Math.round((o_height/o_width)*width);}
i_width=width;i_height=height;}else{var link=current_gallery[current];if(link)enableDrag=link.type=='img'&&(change_h>0||change_w>0);}}
return{height:height,width:width+extra_body_width,i_height:i_height,i_width:i_width,top:((view_height-(height+extra_height))/2)+options.viewportPadding,enableDrag:enableDrag};};var centerVertically=function(){var shadowbox=SL.get('shadowbox');var scroll=document.documentElement.scrollTop;var s_top=scroll+Math.round((SL.getViewportHeight()-(shadowbox.offsetHeight||0))/2);SL.setStyle(shadowbox,'top',s_top+'px');};var adjustHeight=function(height,top,animate,callback){height=parseInt(height);current_height=height;var sbi=SL.get('shadowbox_body_inner');if(animate&&options.animate){SL.animate(sbi,{height:{to:height}},options.resizeDuration,callback);}else{SL.setStyle(sbi,'height',height+'px');if(typeof callback=='function')callback();}
if(absolute_pos){centerVertically();SL.addEvent(window,'scroll',centerVertically);top+=document.documentElement.scrollTop;}
var shadowbox=SL.get('shadowbox');if(animate&&options.animate){SL.animate(shadowbox,{top:{to:top}},options.resizeDuration);}else{SL.setStyle(shadowbox,'top',top+'px');}};var adjustWidth=function(width,animate,callback){width=parseInt(width);current_width=width;var shadowbox=SL.get('shadowbox');if(animate&&options.animate){SL.animate(shadowbox,{width:{to:width}},options.resizeDuration,callback);}else{SL.setStyle(shadowbox,'width',width+'px');if(typeof callback=='function')callback();}};var listenKeyboard=function(on){if(!options.enableKeys)return;if(on){document.onkeydown=handleKey;}else{document.onkeydown='';}};var assertKey=function(valid,key,code){return(valid.indexOf(key)!=-1||valid.indexOf(code)!=-1);};var handleKey=function(e){var code=e?e.which:event.keyCode;var key=String.fromCharCode(code).toLowerCase();if(assertKey(options.keysClose,key,code)){Shadowbox.close();}else if(assertKey(options.keysPrev,key,code)){Shadowbox.previous();}else if(assertKey(options.keysNext,key,code)){Shadowbox.next();}};var toggleTroubleElements=function(on){var vis=(on?'visible':'hidden');var selects=document.getElementsByTagName('select');for(i=0,len=selects.length;i<len;++i){selects[i].style.visibility=vis;}
var objects=document.getElementsByTagName('object');for(i=0,len=objects.length;i<len;++i){objects[i].style.visibility=vis;}
var embeds=document.getElementsByTagName('embed');for(i=0,len=embeds.length;i<len;++i){embeds[i].style.visibility=vis;}};var showLoading=function(){var loading=SL.get('shadowbox_loading');overwriteHTML(loading,String.format(options.skin.loading,options.assetURL+options.loadingImage,options.text.loading,options.text.cancel));loading.style.visibility='visible';};var hideLoading=function(callback){var t=current_gallery[current].type;var anim=(t=='img'||t=='html');var loading=SL.get('shadowbox_loading');if(anim){fadeOut(loading,0.35,callback);}else{loading.style.visibility='hidden';callback();}};var resizeOverlay=function(){var overlay=SL.get('shadowbox_overlay');SL.setStyle(overlay,{height:'100%',width:'100%'});SL.setStyle(overlay,'height',SL.getDocumentHeight()+'px');if(!isSafari3){SL.setStyle(overlay,'width',SL.getDocumentWidth()+'px');}};var checkOverlayImgNeeded=function(){if(!(isGecko&&isMac))return false;for(var i=0,len=current_gallery.length;i<len;++i){if(!RE.overlay.exec(current_gallery[i].type))return true;}
return false;};var toggleOverlay=function(callback){var overlay=SL.get('shadowbox_overlay');if(overlay_img_needed==null){overlay_img_needed=checkOverlayImgNeeded();}
if(callback){resizeOverlay();if(overlay_img_needed){SL.setStyle(overlay,{visibility:'visible',backgroundColor:'transparent',backgroundImage:'url('+options.assetURL+options.overlayBgImage+')',backgroundRepeat:'repeat',opacity:1});callback();}else{SL.setStyle(overlay,{visibility:'visible',backgroundColor:options.overlayColor,backgroundImage:'none'});fadeIn(overlay,options.overlayOpacity,options.fadeDuration,callback);}}else{if(overlay_img_needed){SL.setStyle(overlay,'visibility','hidden');}else{fadeOut(overlay,options.fadeDuration);}
overlay_img_needed=null;}};Shadowbox.init=function(opts){if(initialized)return;options=apply(options,opts||{});appendHTML(document.body,options.skin.main);RE.img=new RegExp('\.('+options.ext.img.join('|')+')\s*$','i');RE.qt=new RegExp('\.('+options.ext.qt.join('|')+')\s*$','i');RE.wmp=new RegExp('\.('+options.ext.wmp.join('|')+')\s*$','i');RE.qtwmp=new RegExp('\.('+options.ext.qtwmp.join('|')+')\s*$','i');RE.iframe=new RegExp('\.('+options.ext.iframe.join('|')+')\s*$','i');var id=null;var resize=function(){clearInterval(id);id=null;resizeOverlay();resizeContent(optimal_height,optimal_width);};SL.addEvent(window,'resize',function(){if(activated){if(id){clearInterval(id);id=null;}
if(!id)id=setInterval(resize,50);}});if(options.listenOverlay){SL.addEvent(SL.get('shadowbox_overlay'),'click',Shadowbox.close);}
if(absolute_pos){SL.setStyle(SL.get('shadowbox_container'),'position','absolute');SL.setStyle('shadowbox_body','zoom',1);SL.addEvent(SL.get('shadowbox_container'),'click',function(e){var target=SL.getTarget(e);if(target.id&&target.id=='shadowbox_container')Shadowbox.close();});}
if(!options.skipSetup)Shadowbox.setup();initialized=true;};Shadowbox.setup=function(links,opts){if(!links){var links=[];var a=document.getElementsByTagName('a'),rel;for(var i=0,len=a.length;i<len;++i){rel=a[i].getAttribute('rel');if(rel&&RE.rel.test(rel))links[links.length]=a[i];}}else if(!links.length){links=[links];}
var link;for(var i=0,len=links.length;i<len;++i){link=links[i];if(typeof link.shadowboxCacheKey=='undefined'){link.shadowboxCacheKey=cache.length;SL.addEvent(link,'click',handleClick);}
cache[link.shadowboxCacheKey]=this.buildCacheObj(link,opts);}};Shadowbox.buildCacheObj=function(link,opts){var href=link.href;var o={el:link,title:link.getAttribute('title'),type:getPlayerType(href),options:apply({},opts||{}),content:href};var opt,l_opts=['title','type','height','width','gallery'];for(var i=0,len=l_opts.length;i<len;++i){opt=l_opts[i];if(typeof o.options[opt]!='undefined'){o[opt]=o.options[opt];delete o.options[opt];}}
var rel=link.getAttribute('rel');if(rel){var match=rel.match(RE.gallery);if(match)o.gallery=escape(match[2]);var params=rel.split(';');for(var i=0,len=params.length;i<len;++i){match=params[i].match(RE.param);if(match){if(match[1]=='options'){eval('o.options = apply(o.options, '+match[2]+')');}else{o[match[1]]=match[2];}}}}
return o;};Shadowbox.applyOptions=function(opts){if(opts){default_options=apply({},options);options=apply(options,opts);}};Shadowbox.revertOptions=function(){if(default_options){options=default_options;default_options=null;}};Shadowbox.open=function(obj,opts){if(activated)return;activated=true;if(isLink(obj)){if(typeof obj.shadowboxCacheKey=='undefined'||typeof cache[obj.shadowboxCacheKey]=='undefined'){obj=this.buildCacheObj(obj,opts);}else{obj=cache[obj.shadowboxCacheKey];}}
this.revertOptions();if(obj.options||opts){this.applyOptions(apply(apply({},obj.options||{}),opts||{}));}
setupGallery(obj);if(current_gallery.length){if(options.onOpen&&typeof options.onOpen=='function'){options.onOpen(obj);}
SL.setStyle(SL.get('shadowbox'),'display','block');toggleTroubleElements(false);var dims=getDimensions(options.initialHeight,options.initialWidth);adjustHeight(dims.height,dims.top);adjustWidth(dims.width);hideBars(false);toggleOverlay(function(){SL.setStyle(SL.get('shadowbox'),'visibility','visible');showLoading();loadContent();});}};Shadowbox.change=function(num){if(!current_gallery)return;if(!current_gallery[num]){if(!options.continuous){return;}else{num=(num<0)?(current_gallery.length-1):0;}}
current=num;toggleDrag(false);setContent(null);listenKeyboard(false);if(options.onChange&&typeof options.onChange=='function'){options.onChange(current_gallery[current]);}
showLoading();hideBars(loadContent);};Shadowbox.next=function(){return this.change(current+1);};Shadowbox.previous=function(){return this.change(current-1);};Shadowbox.close=function(){if(!activated)return;listenKeyboard(false);SL.setStyle(SL.get('shadowbox'),{display:'none',visibility:'hidden'});if(absolute_pos)SL.removeEvent(window,'scroll',centerVertically);toggleDrag(false);setContent(null);if(preloader){preloader.onload=function(){};preloader=null;}
toggleOverlay(false);toggleTroubleElements(true);if(options.onClose&&typeof options.onClose=='function'){options.onClose(current_gallery[current]);}
activated=false;};Shadowbox.clearCache=function(){for(var i=0,len=cache.length;i<len;++i){if(cache[i].el){SL.removeEvent(cache[i].el,'click',handleClick);delete cache[i].shadowboxCacheKey;}}
cache=[];};Shadowbox.movieMarkup=function(obj){var h=obj.height?parseInt(obj.height,10):300;var w=obj.width?parseInt(obj.width,10):300;var autoplay=options.autoplayMovies;var controls=options.showMovieControls;if(obj.options){if(obj.options.autoplayMovies!=null){autoplay=obj.options.autoplayMovies;}
if(obj.options.showMovieControls!=null){controls=obj.options.showMovieControls;}}
var markup={tag:'object',name:'shadowbox_content'};switch(obj.type){case'swf':var dims=getDimensions(h,w,true);h=dims.height;w=dims.width;markup.type='application/x-shockwave-flash';markup.data=obj.content;markup.children=[{tag:'param',name:'movie',value:obj.content}];break;case'flv':autoplay=autoplay?'true':'false';var showicons='false';var a=h/w;if(controls){showicons='true';h+=20;}
var dims=getDimensions(h,h/a,true);h=dims.height;w=(h-(controls?20:0))/a;var flashvars=['file='+obj.content,'height='+h,'width='+w,'autostart='+autoplay,'displayheight='+(h-(controls?20:0)),'showicons='+showicons,'backcolor=0x000000&amp;frontcolor=0xCCCCCC&amp;lightcolor=0x557722'];markup.type='application/x-shockwave-flash';markup.data=options.assetURL+options.flvPlayer;markup.children=[{tag:'param',name:'movie',value:options.assetURL+options.flvPlayer},{tag:'param',name:'flashvars',value:flashvars.join('&amp;')},{tag:'param',name:'allowfullscreen',value:'true'}];break;case'qt':autoplay=autoplay?'true':'false';if(controls){controls='true';h+=16;}else{controls='false';}
markup.children=[{tag:'param',name:'src',value:obj.content},{tag:'param',name:'scale',value:'aspect'},{tag:'param',name:'controller',value:controls},{tag:'param',name:'autoplay',value:autoplay}];if(isIE){markup.classid='clsid:02BF25D5-8C17-4B23-BC80-D3488ABDDC6B';markup.codebase='http://www.apple.com/qtactivex/qtplugin.cab#version=6,0,2,0';}else{markup.type='video/quicktime';markup.data=obj.content;}
break;case'wmp':autoplay=autoplay?1:0;markup.children=[{tag:'param',name:'autostart',value:autoplay}];if(isIE){if(controls){controls='full';h+=70;}else{controls='none';}
markup.classid='clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6';markup.children[markup.children.length]={tag:'param',name:'url',value:obj.content};markup.children[markup.children.length]={tag:'param',name:'uimode',value:controls};}else{if(controls){controls=1;h+=45;}else{controls=0;}
markup.type='video/x-ms-wmv';markup.data=obj.content;markup.children[markup.children.length]={tag:'param',name:'showcontrols',value:controls};}
break;}
markup.height=h;markup.width=w;return markup;};Shadowbox.createHTML=function(obj){var html='<'+obj.tag;for(var attr in obj){if(attr=='tag'||attr=='html'||attr=='children')continue;if(attr=='cls'){html+=' class="'+obj['cls']+'"';}else{html+=' '+attr+'="'+obj[attr]+'"';}}
if(RE.empty.test(obj.tag)){html+='/>\n';}else{html+='>\n';var cn=obj.children;if(cn){for(var i=0,len=cn.length;i<len;++i){html+=this.createHTML(cn[i]);}}
if(obj.html)html+=obj.html;html+='</'+obj.tag+'>\n';}
return html;};Shadowbox.getPlugins=function(){return plugins;};Shadowbox.getOptions=function(){return options;};Shadowbox.getCurrent=function(){return current_gallery[current];};Shadowbox.getVersion=function(){return version;};})();Array.prototype.indexOf=Array.prototype.indexOf||function(o){for(var i=0,len=this.length;i<len;++i){if(this[i]==o)return i;}
return-1;};String.format=String.format||function(format){var args=Array.prototype.slice.call(arguments,1);return format.replace(/\{(\d+)\}/g,function(m,i){return args[i];});};;