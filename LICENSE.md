<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    
</body><style>
    .nav{
        width:100px;
        height:200px;
        cursor: pointer;
    }
    .nav p{
        width:50px;
        height:50px;
        color:red;
    }
    .color{
        width:100px;
        height:100px;
        list-style: none;
    }
    .color .color-1{
        width:100px;
        height:100px;
        background-color: #DC85CD;
    }
    .color .color-2{
        width:100px;
        height:100px;
        background-color: #33CCFF;
        display: none;
    }
    .color .color-3{
        width:100px;
        height:100px;
        background-color: #4AA52B;
        display: none;
    }
</style>
</head>
<body>
<div class="nav">
    <p>第一个</p>
    <p>第二个</p>
    <p>第三个</p>
</div>
<ul class="color">
    <li class="color-1"></li>
    <li class="color-2"></li>
    <li class="color-3"></li>
</ul>
<script>
    var theNav=document.querySelectorAll(".nav p");
    var theColor=document.querySelectorAll(".color li");
    for(var i=0;i<theNav.length;i++){
        (function(i){
            theNav[i].onmousedown=function(){
                for(var j=0;j<theNav.length;j++){
                    theColor[j].style.display="none";

                }
                theColor[i].style.display="block";

            }
        })(i);
    }
</script>
</html>
