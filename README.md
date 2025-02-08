# Traffic-Ligths
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Traffic Lights</title>
    <link rel="stylesheet" href="style.css">
<style>
    *{
        box-sizing: border-box;
    }
    body{
        background-color: #329ed6;
        display: flex;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        margin: 0;
    }
    .container{
        display:flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: column;
        width: 85px;
        height: 250px;
        padding: 15px;
        background-color: #2d3e55;
        border-radius: 50px;
    }
    .circle{
        position: relative;
        background-color: rgba(0,0,0,0.3);
        border-radius: 50%;
        height: 50px;
        width: 50px;
    }
    .circle:after{
        border-right: 4px solid rgba(255,255,255,0.6);
        position: absolute;
        content: '';
        width: 40px;
        height: 40px;
        border-radius: 50%;
        top: 5px;
        left: 4px;
    }
    .circle.red{
        background-color: #c0392b;
        box-shadow: 0 0 20px 5px #c0392b;
    }
    .circle.yellow{
        background-color: #f1c40f;
        box-shadow: 0 0 20px 5px #f1c40f;
    }
    .circle,green{
        background-color: #2ecc71;
        box-shadow: 0 0 20px 5px #2ecc71;
    }
</style>
</head>
<body>
    <div class="container">
        <div class="circle red" color="red"></div>
        <div class="circle yellow" color="yellow"></div>
        <div class="circle green" color="green"></div>
    </div>
    <script>
        const circles=document.querySelectorAll('.circle');
        let active light=0;
        setInterval(changelight,1000);
        function changelight(){
            circles[activelight].className='circle';
            activeLight++;
            if(activeLight>2){
                activeLight=0;
            }
            const currentlight=circles[
                activeLight];
            currentLight.classList.add(currentLight.getAttribute('color'));
        }
    </script>
</body>
</html>
