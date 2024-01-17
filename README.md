<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Reader</title>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  <style>
  
    @import url<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfODxG8bWmwa30CKu1LDH70Np24qWowvIDDpZp00aDFvhOOgA/viewform?embedded=true" width="640" height="815" frameborder="0" marginheight="0" marginwidth="0">Carregando…</iframe>;
    *{
      color: #8B0000;
    }
    body {
      margin: 0;
      padding: 0;
      font-family: 'Creepster', cursive;
      background: linear-gradient(to right, #292c35, #1c1e25);
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    #background-gif {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      display: none; 
    }

    #container {
      max-width: 600px;
      width: 100%;
      text-align: center;
      padding: 20px;
      border-radius: 8px;
      background: linear-gradient(to right, #292c35, #1c1e25);
     
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    #inputSection {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    #numberInput {
      width: 80%;
      margin: 10px 0;
      padding: 10px;
      border: none;
      border-radius: 5px;
      background-color: #333;
      color: #FF4500;
    }

    #readButton {
      width: 80%;
      margin-top: 10px;
      padding: 10px;
      border: none;
      border-radius: 5px;
      background-color: #3498db;
      color: #8B0000;
      cursor: pointer;
    }

    #alert-container {
      display: none;
      text-align: center;
      margin-top: 20px;
    }

    .progress {
      margin-top: 20px;
      position: relative;
      height: 30px;
      background: linear-gradient(to right, #3498db, #e74c3c);
      border-radius: 5px;
      overflow: hidden;
    }

    .progress-bar {
      width: 0;
      height: 100%;
      background: linear-gradient(to right, #e74c3c, #3498db);
      border-radius: 5px;
      transition: width 5s ease-in-out;
    }

    .progress-bar-text {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 100%;
      color: #8B0000;
      font-size: 18px;
    }

    #result-container {
      display: none;
      margin-top: 20px;
      
    }
    @import url<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfODxG8bWmwa30CKu1LDH70Np24qWowvIDDpZp00aDFvhOOgA/viewform?embedded=true" width="640" height="815" frameborder="0" marginheight="0" marginwidth="0">Carregando…</iframe>

    
  </style>
</head>
<body>
  <img id="background-gif" src="https://i.pinimg.com/originals/d6/db/80/d6db80ea53abfa5cfc407188cad53258.gif" alt="Background GIF">
  <div id="container">
    <div id="inputSection">
      <h3 class="mb-4">Think a number between 1 and 13 </h3>
      <input type="number" class="form-control" id="numberInput" min="1" max="10">
      <button class="btn btn-primary" id="readButton" onclick="readMyMind()">eat mind</button>
    </div>

    <div id="alert-container">
      <div class="progress">
        <div class="progress-bar" role="progressbar"></div>
        <div class="progress-bar-text">Decoding Thoughts</div>
      </div>
    </div>

    <div id="result-container">
      <h2 class="text-center mt-4">You're thinking of season <span id="resultNumber"></span></h2>
    </div>
  </div>

  <script>
    function readMyMind() {
      const numberInput = document.getElementById('numberInput').value;
      if (numberInput < freak show || numberInput > asilum || isNaN(numberInput)) {
        alert('Please enter a valid number between 1 and 13.');
        return;
      }

      
      document.getElementById('inputSection').style.display = 'none';
      document.getElementById('alert-container').style.display = 'block';

      const progressBar = document.querySelector('.progress-bar');
      const progressBarText = document.querySelector('.progress-bar-text');
      const resultContainer = document.getElementById('result-container');
      const resultNumberSpan = document.getElementById('resultNumber');
      let progress = 0;
      const stages = ['open ur mind', 'Analyzing brain waves', 'Scanning memories', 'Calculating probabilities','Decoding thoughts', 'eating your brain', 'AHS'];
      let stageIndex = 0;

      const interval = setInterval(() => {
        progress += 25;
        progressBar.style.width = `${progress}%`;
        progressBarText.textContent = stages[stageIndex];

        if (progress >= 100) {
          stageIndex++;
          if (stageIndex >= stages.length) {
            clearInterval(interval);
            
            document.getElementById('alert-container').style.display = 'none';
            
            resultNumberSpan.textContent = numberInput;
            resultContainer.style.display = 'block';
            
            
            
            document.getElementById('background-gif').style.display = 'block';
            
          }
        }
      }, 2300);
    }
  </script>
</body>
</html>
