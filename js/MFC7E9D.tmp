// JavaScript Document

$(document).ready(function(e) {
	var i = 0;
	function sum(delta){
		 i-=delta;
		 var leng = $("section").length-1;
		 if(i<0){i=0;}else if(i>leng){i=leng;}
		 console.log(i)
	}
	$(window).resize(function(){
		var st = $("section").eq(i).position().top;
		$(this).scrollTop(st);	
	});
		
	$("nav li").on("click", function(e){ 
			e.preventDefault; 
			var ht = $("section").height(); 
			var i = $(this).index(); 
			var nowTop = i*ht; 
			$("html,body").stop().animate({"scrollTop":nowTop},800);
	});
	$("section").on("mousewheel",function(event,delta){
		if($('body').is(":animated")){return false;}
		sum(delta);
		if(delta>0){ 
			var prev = $(this).prev().offset().top; 
			$("html,body").stop().animate({"scrollTop":prev},1000); 
		}
		if(delta<0){ 
			var next = $(this).next().offset().top; 
			$("html,body").stop().animate({"scrollTop":next},1000);
		}
		return false;
	});
	$(window).on("scroll",function(){
		var a = $(window).scrollTop();
		//console.log(a);	
		if(a>60){
			$("nav").css({"background-color":"rgba(255,255,255,0.5)"}); 
		}else{
			$("nav").css({"background-color":"rgba(255,255,255,1)"});
		}
	});

});