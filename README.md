# OOPJSByPrototype
it is same code to support OOP in JS. work by prototype
Author: Eric Meng
	作者：孟详毅
	above code implement oop. following is demo. it is little different to java oop. every thing is override by sub-class. in Java, only method override.
	以上实现面向对象，以下是例子。
	please follow LGPL protocol
	请遵守 LGPL 协议
	my wechat is: treeiv email:cat555666@126.com, if you have question, my pleasure to discuss.
	我的微信是treeiv. 电邮 cat555666@126.com. 如果有问题欢迎讨论。
var Animal=function(){
	alert("Animal name is "+this.name);
}.body({
	name:"generic animal",
	sing:function(){
		alert(this.name+" sing");
	}
});
var Chiken=function(){
	Chiken.super.constructor.apply(this);
	alert("Chiken name is "+this.name);
}.body({
	name:"chiken",
	sing:function(sth){
		alert(this.name+" sing ji ji gou " + sth);
	}
}).extend(Animal);
var Duck=function(){
	Duck.super.constructor.apply(this);
	alert("Duck name is "+this.name);
}.body({
	name:"duck",
	sing:function(){
		Duck.super.sing.apply(this,arguments)
		alert(this.name+" sing gua gua");
	}
}).extend(Animal);
var TomDuck=function(){
	TomDuck.super.constructor.apply(this);
	alert("TomDuck name is "+this.name);
}.body({
	name:"Tom duck",
	sing:function(){
		alert(this.name+" what's fuck sing");
	}
}).extend(Duck);
var tomDuck=new TomDuck();
tomDuck.sing();
var duck=new Duck();
duck.sing("....");
