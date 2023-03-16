# JSON-FORMATER
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MyTheme</title>
</head>
<script>
    function json(){
    
        var data=document.getElementById("data").value;
        var json=document.getElementById("json");
         var modData;
        if(data.charAt(0) == "\""){
            // console.log(true)
            modData = data.slice(1,-1);
        }
        else {
            // console.log(false)
            modData = data;
        }
        
       console.log(modData);
        var temp = JSON.parse(modData);
        console.log(temp);
        var result = JSON.stringify(temp, undefined,2);
    
        json.innerHTML = result;
    
    }
    </script>
<style>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    body{
        background: greenyellow;
    }
    .header{
  
        padding: 20px;
        
        background: linear-gradient(greenyellow, green);
        box-shadow: 0px 0px 5px black;
    }

    li{
       
        list-style: none;
    }
    a{
         margin: 0 20px;
        text-decoration: none;
       color: Black;

        font-size: 20px;
    }
    a:hover{
        color: white;
    }
    .twophase{
        display: flex;
    }
    textarea{
        background: black;
        overflow-y: auto;
        padding: 20px;
        color: greenyellow;
      
        font-size: 15px;
        margin: auto;
        border: 2px solid green;
        height:500px;
        width: 100%;
    }
    button{
        cursor: pointer;
        border: none;
        border-radius: 5px;
        text-align: center;
        margin: 10px 40%;
        height: 50px;
        width: 250px;
        font-size: 30px;
        background-color: rgb(132, 234, 132);
    }
    button:hover{
        background-color: white;
        box-shadow: 0px 0 5px black;
    }

</style>
<body>
<!-- header  -->
<div class="header">
<ul>
    <li>
        <a href="https://www.miningwebs.in/">Home</a>
  
    </li>
</ul>
</div>
<div class="twophase">
<textarea name="" id="data" cols="30" rows="10" placeholder="paste here"></textarea>

<textarea name="" id="json" cols="30" rows="10"></textarea>
</div>
<button id="Convert" onclick="json()">Convert JSON</button>
<p style="color:black;">Made by miningwebs.in</p>
</body>
</html>
