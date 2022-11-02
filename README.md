<!DOCTYPE html>
<html>
<head> 

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">


<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>


<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>


<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script> 

<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.10.0/css/all.css" integrity="sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p" crossorigin="anonymous"/> 



<title></title> 

<style type="text/css"> 

/*Calculator Start*/ 

.calculat{
margin:0 auto;
height:460px;
width:280px;
background-color:silver;
border:2px solid cyan;
padding:10px;
margin-top:50px;
}
.main-bar{
margin-bottom:20px;
text-align:right; 

}
.line{ 

margin-bottom:10px;
}
.last{ 

width:100%;
}
#btn{
box-shadow:1px 1px 1px 1px black;
font-size:20px;
cursor:pointer;
width:61px;
border-top:1.5px solid lime;
border-left:1.5px solid blue;
}
#btnl{
width:100px;
height:40px;
margin:0 auto; 

}
#display{
height:50px;
font-size:30px;
}
/*Calculator End */
.clea{
clear:both;
}
hr{
border:7px solid silver;
}
hr{
border:4px solid silver;
}
i{
float:right;
} 

/* Scrolling */


.items{
display:flex;
overflow-x:auto;
}
.items .item{
min-width:150px;
height:200px;
background:red;
margin:10px;
}
img{
width:150px;
height:200px;
} 

.mrhu{
text-align:center;
border:30px solid white;
border-radius:50%;
border-top:30px solid lime;
width:150px;
height:150px;
animation:ruhu 2s linear infinite;
}
@keyframes ruhu{
0%{transform:rotate(0deg);}
100%{transform:rotate(360deg);}
}

#goo{
font-size:40px;
}
#clock{
font-size:50px;
color:aqua;
background:gray;
}
#range{
width:300px;
}
</style>






</head>
<body> 

<button onclick="window.print()">print this page</button>


<div id="goo" ></div>
<!-- Calculator Start --> 

<i class="fa-solid fa-dryer"></i>




<i class="fas fa-calculator fa-2x"></i>


<div class="calculat">
<form action="" name="form"> 

<input type="text" class="form-control main-bar" id="display" name="display" placeholder="0"> 

<div class="line">
<input type="button" value="7" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="8" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="9" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="+" id="btn" class="alert alert-danger" onclick="calci(this.value)">
</div> 

<div class="line">
<input type="button" value="4" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="5" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="6" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="-" id="btn" class="alert alert-danger" onclick="calci(this.value)">
</div> 

<div class="line"> 

<input type="button" value="1" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="2" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="3" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="/" id="btn" class="alert alert-danger" onclick="calci(this.value)">
</div> 

<div class="line">
<input type="button" value="0" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="00" id="btn" class="alert alert-success" onclick="calci(this.value)"> 

<input type="button" value="." id="btn" class="alert alert-primary" onclick="calci(this.value)"> 

<input type="button" value="*" id="btn" class="alert alert-danger" onclick="calci(this.value)">
</div> 

<div class="last"> 

<input type="button" value="C" id="btnl" class="btn btn-warning" onclick="display.value = null"> 

<input type="button" value="=" id="btnl" class="btn btn-success" onclick="display.value = eval(display.value)"> 

</div>
</div>
</form>
<!-- Calculator End -->
<hr>
<center><div id="clock" ></div></center>
<hr>
<div class="clea"></div>


<div class="items"> 

<div class="item"><img src="scol1.jpg"></div>
<div class="item"><img src="scol2.jpg"></div>
<div class="item"><img src="scol3.jpg"></div>
<div class="item"><img src="scol4.jpg"></div>
<div class="item"><img src="scol5.jpg"></div>
<div class="item"><img src="scol6.jpg"></div>
<div class="item"><img src="scol7.jpg"></div>
<div class="item"><img src="scol8.jpg"></div>
<div class="item"><img src="scol9.jpg"></div>
<div class="item"><img src="scol10.jpg"></div>
<div class="item"><img src="scol11.jpg"></div>
<div class="item"><img src="scol12.jpg"></div> 

</div>
<div class="clea"></div>
<hr>


<div class="mrhu"><i><center>Ruhul</center></i></div>

<br>
<p>Volume</p>
<input type="range" id="range" value="50" >


<script type="text/javascript"> 

function calci(x){ 

form.display.value = form.display.value +x; 

};

function showTime(){
var d = new Date();
var h =d.getHours();
var m =d.getMinutes();
var s =d.getSeconds();
var session = "AM";

if(h==0){
	h = 12;
}
if(h>12){
h=h-12;
session="PM";
}




if(h<10){
h="0"+h;
}
if(m<10){
m="0"+m;
}

if(s<10){
s="0"+s;
}

document.getElementById("clock").innerHTML=h + ":" + m + ":" + s + ":" + session ;

setTimeout(showTime,1000);
};
showTime();

var ti = new Date().getHours();
var greet;

if(ti < 12){
greet="{Morning}";
}
else if(ti<13){
greet="{Afternoon}"
}
else{
greet="{Evening}";
}
document.getElementById("goo").innerHTML="Good -" + greet;







</script>


</body>
</html>
