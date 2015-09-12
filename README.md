这里记录学习javascript的点点滴滴
====

example
//单独写一个函数方法
``` bash
function fnName(){}
var fnName = function(){}

()()
```
//
(function(){
  //do something...
})()

function function_name1 (function_name1) {
	// body...
	alert(function_name1)
}

function function_name2(function_name2){
	alert(function_name2)
}


var module1 = new Object({

	_count : 0,

	m1 : function(module1_fn_name){
		alert(module1_fn_name)
	},
	m2 : function(module1_fn_name2){
		alert(module1_fn_name2)
	}
});


module1.m1('m1m1m1m1m1')

module1.m2('m2m2m2m2m2')

module1._count = 5;

//这样的写法会暴露所有模块成员，内部状态可以被外部改写。比如，外部代码可以直接改变内部计数器的值。

```bash
var module2 = (function(){

	var _count = 0;

	var m1 = function(){
		//do something...
	}

	var m2 = function(){
		//do something...
	}


	return {

		m1 : m1,
		m2 : m2
	};

})()
```

//使用上面的写法，外部代码无法读取内部的_count变量。


var module1 = (function(mod){

	mod.m3 = function(){

		//.....
	};

	return mod;

})(module1)


var module1 = (function(mod){

	//

	return mod;


})(window.module1 || {})
