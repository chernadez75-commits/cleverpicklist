<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Clever Foods - Ingredient Pick & Check List</title>

<style>
body{
    margin:0;
    font-family:Arial,Helvetica,sans-serif;
    background:#f4f6f8;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.container{
    background:white;
    width:340px;
    padding:35px;
    border-radius:12px;
    box-shadow:0 10px 25px rgba(0,0,0,.15);
    text-align:center;
}

h2{
    color:#2c3e50;
    margin-bottom:10px;
}

p{
    color:#666;
    margin-bottom:25px;
}

input{
    width:100%;
    padding:14px;
    font-size:18px;
    border-radius:8px;
    border:1px solid #ccc;
    text-align:center;
    box-sizing:border-box;
}

button{
    margin-top:15px;
    width:100%;
    padding:14px;
    background:#00843D;
    color:white;
    border:none;
    border-radius:8px;
    font-size:18px;
    cursor:pointer;
}

button:hover{
    background:#006d32;
}

#error{
    color:red;
    margin-top:15px;
    display:none;
}
</style>

</head>
<body>

<div class="container">

<h2>Clever Foods</h2>

<p>Ingredient Pick & Check List</p>

<input
type="password"
id="pin"
placeholder="Enter PIN"
maxlength="4">

<button onclick="checkPin()">
Continue
</button>

<p id="error">
Invalid PIN. Please try again.
</p>

</div>

<script>

const validPins = [
"2020",
"2021",
"2022",
"2023"
];

const pdfLink = "https://gocleverfoods-my.sharepoint.com/personal/sergio_sepulveda_gocleverfoods_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fsergio%5Fsepulveda%5Fgocleverfoods%5Fcom%2FDocuments%2FIngredient%20Pick%20%26%20Check%20List%2FClever%20Ingredient%20Pick%20%26%20Check%20List%2Epdf&parent=%2Fpersonal%2Fsergio%5Fsepulveda%5Fgocleverfoods%5Fcom%2FDocuments%2FIngredient%20Pick%20%26%20Check%20List&ga=1";

function checkPin(){

const pin=document.getElementById("pin").value;

if(validPins.includes(pin)){

window.location.href=pdfLink;

}else{

document.getElementById("error").style.display="block";

}

}

document.getElementById("pin").addEventListener("keypress",function(e){

if(e.key==="Enter"){
checkPin();
}

});

</script>

</body>
</html>
