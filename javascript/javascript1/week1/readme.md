<!-- 
<!DOCTYPE html>
<html>
<button id="futureAge">FUTURE AGE CALCULATOR</button>
<button id="dogAge">DOG AGE CALCULATOR</button>
<button id="housePrice">HOUSE PRICE CALCULATOR</button>
<button id="ezNamey">STARTUP NAME GENERATOR</button>
<div id="result"></div>
-->
<script>
    var result;
    
    /********************
    ****** Age-ify ******
    ********************/
    document.getElementById("futureAge").onclick = function() {
        var yearOfBirth = prompt("Type inn your birthyear:");
        var yearFuture = prompt("Type inn future year:");
        var age = yearFuture - yearOfBirth;
        result = document.getElementById("result").innerHTML = "You will be "+age+" years old in "+yearFuture;
        console.log("You will be "+age+" years old in "+yearFuture);
    }
    
    /***************************
    ****** Goodboy-Oldboy ******
    ***************************/
    
    document.getElementById("dogAge").onclick = function() {
        var dogYearOfBirth = prompt("Type inn your dogs birthyear:");
        var dogYearFuture = prompt("Type inn future year:");
        var shouldShowResultInDogYears = prompt("Do you want your dogs age in: \n - Dogsyear \(press 1\) \n - Humanyears \(press 2\)");
        var dogYear = dogYearFuture-dogYearOfBirth;
        if(shouldShowResultInDogYears === "1"){
        result = document.getElementById("result").innerHTML = "Your dog will be "+(dogYear*7)+" dog years old in 2027";
        } 
        else if(shouldShowResultInDogYears === "2"){
        result = document.getElementById("result").innerHTML = "Your dog will be "+dogYear+" Human years old in "+dogYearFuture;
        }
        else{
        result = document.getElementById("result").innerHTML = "You didn't specify, SO: <br>Your dog will be "+dogYear+" Human years or "+dogYear*7+" dogyears old in "+dogYearFuture;
        }
        console.log(result);
    }
    /***************************
    ****** Housey Pricey ******
    ***************************/
    
    document.getElementById("housePrice").onclick = function() {
        
        var width = prompt("Type inn width of the house \(in m\):");
        var length = prompt("Type inn length of the house :");
        var height = prompt("Type inn height of the house :");
        
        var volumeInMeters = width*length*height;
        var gardenSizeInM2 = prompt("Type inn the garden size in M2:");
        var price = prompt("Type your price of the house :");
        var housePrice = volumeInMeters * 2.5 * 1000 + gardenSizeInM2 * 300;
        var fair = price - housePrice;
        if(price === 0 || price === "") { result = document.getElementById("result").innerHTML = "A house with messures: "+width+"m width, "+length+"m length, "+height+"m in height and a garden of "+gardenSizeInM2+"m2. Should cost: "+housePrice;}
        else{
            if(fair === 0){result = document.getElementById("result").innerHTML = "A house with messures: "+width+"m width, "+length+"m length, "+height+"m in height and a garden of "+gardenSizeInM2+"m2. Should cost: "+housePrice+"<br>The price of the house is fair";}
            else if (fair > 0){
                result = document.getElementById("result").innerHTML = "A house with messures: "+width+"m width, "+length+"m length, "+height+"m in height and a garden of "+gardenSizeInM2+"m2. Should cost: "+housePrice+"<br>The price of the house is not fair. You pay "+fair+" over market.";
            }else if (fair < 0){
                result =document.getElementById("result").innerHTML = "A house with messures: "+width+"m width, "+length+"m length, "+height+"m in height and a garden of "+gardenSizeInM2+"m2. Should cost: "+housePrice+"<br>The price of the house is in your favor. You pay "+fair+" under market.";
            }else {"Something went wrong!";}
            
            }
        console.log(result);
        }
        /* Peter will pay too much and Julia are paying less than market.*/
        
    /*********************
    ****** Ez Namey ******
    *********************/
    
    document.getElementById("ezNamey").onclick = function() {
    const Words = ["Crazy","Froggy","Amazing","Dazzling","Super","Corporate","Easy","Awsome","Sloppy","Dropout"];
    var startUpName = "";
    for(var i = 0; i<2; i++ ){
       startUpName = startUpName + Words[Math.floor(Math.random() * 10) + 0]+" ";
    }
    result = document.getElementById("result").innerHTML = "The startup: \""+startUpName+"\" contains "+(startUpName.length-1)+" characters";
    console.log(result);
    }
    
</script>
</html>
