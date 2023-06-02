<!DOCTYPE html>
<html lang="en">
<style>

button {
    background:transparent;
    border:none;
    outline:none;
    display:block;
    height:200px;
    width:200px;
    cursor:pointer;
}
.container {
  width: 1000px;
  height: 1000px;
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: -300px;
  margin-left: -600px;
}
.trim {
     max-height:128px;
     max-width: 340px;
     overflow: hidden;
 }

body {
background-image: url("backdrop.jpg");
no-repeat;
background-size: 2000px;
width: 1000px;
height: 1000px;
}

.text-block {
  position: absolute;
  bottom: 570px;
  right: 530px;
  background-color: gray;
  color: white;
  height: 350px;
  width: 400px;
  padding-left: 20px;
  padding-right: 20px;
}

</style>
<header>
  <meta charset="UTF-8">
  <title>Gavin's Calculator</title>    <h1>Hello, my name is gavin, this is my calculator.</h1>





    <p>The product of your inputs are:

    <span id = 'result'></span></p>

    <script>

    function myFunction() {

    var x = parseFloat(document.getElementById("firstdiget").value);

    var y = parseFloat(document.getElementById("lastdiget").value);


    var result = x * y;

    var gstring = result.toString();

    if (gstring == 'NaN'){

    document.getElementById('result').textContent = '';
    }
    else {
    document.getElementById('result').textContent = gstring;
    }
    }


    </script>


</header>

<body>


<div class="container">

  <img src="tab.png" alt="tab" style="width:50%;">
  <div class="trim"><div class="container"> <input type="button"></div> <img src="button.jpg"/></div>

  <div class="text-block">
  <input type="button" onclick="myFunction()" style="background: url(button.jpg) no-repeat; width:100px; height:100px;">


  <form>
  <label for="firstdiget">First number:</label><br>
  <input type="text" id = firstdiget name="firstdiget"><br>
  <label for="lastdiget">Last number:</label><br>
  <input type="text" id = lastdiget name="lastdiget">
  </form>
  </div>
  </div>








</body>
</html>
