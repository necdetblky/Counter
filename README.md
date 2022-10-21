# counter
<html>
<head>
</head>
<body>
  <div class="container">
    <h1>Counter</h1>
      <p id="score">0</p>
        <div class="cont">
          <div class="inner"><button id="plus" style="color:green;">&plus;</button></div>
          <div class="inner"><button id="reset" style="color:yellow;">&#x21bb;</button></div>
          <div class="inner"><button id="minus" style="color:red;">&minus;</button></div>
    </div>
    </div>
</body>
</html>


body{
    font-family:system-ui;
    background:linear-gradient(to right, #282DC3, #FF1818);
    color:white;
  }
  .container{
    position:absolute;
    left:50%;
    top:50%;
    transform:translate(-50%, -50%);
    border:1px solid white;
    border-radius:50px;
    box-shadow:10px 10px 10px 10px black;
    padding:15px;
    margin:10px;
    text-align: center;
  }
  h1{
    font-size:50px;
  }
  #score{
    font-size:40px; 
    border:1px solid white;
    border-radius:70px;
    font-family:cursive;
    background-color:darkblue;
  }
  .inner{
    display: inline-block;
    padding:25px;
    font-size:10px;
  }
  button{
    color: white;
      border: none;
      font-size: 50px;
      background: none;
      cursor: pointer;
      display: inline-block;
  }
  
  
let plus = document.getElementById('plus');
let reset = document.getElementById('reset');
let minus = document.getElementById('minus');
let output = document.getElementById('score');
let score = 0;

plus.addEventListener('click', () => {
  score++;
  output.innerHTML = score;
  if(score >= 1 ){
    output.style.color = 'green';
  }else if(score == 0){output.style.color = 'white';}
});

minus.addEventListener('click', () => {
  score--;
  output.innerHTML = score;
  if(score < 0 ){
    output.style.color = 'red';
  }else if(score == 0){output.style.color = 'white';}
});

reset.addEventListener('click', () => {
  score = 0;
  output.innerHTML = score;
  output.style.color = 'white';
});
