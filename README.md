<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=div, initial-scale=1.0">
    <title>Document</title>
<style>
    body{
        background-color: #001f4f;
        font-family: "Raleway" , sans-serif;
    }
    .container{
        width: 350px;
        height: 500px;
        background-color: #fff;
        position: absolute;
        left: 50%;
        top:50%;
        transform: translateX(-50%) translateY(-50%);
        border-radius: 20px;;
    }
h1{
    position: absolute;
    left: 50%;
    top: -60px;
    width: 300px;
    transform: translateX(-50%);
    background-color: #ff851b;
    color: #fff;
    font-weight: 100;
    border-top-left-radius: 20px;
    border-top-right-radius:20px;
    font-size: 18px;
    text-align: center;
    padding: 10px;
}
.wrapper{
    padding: 20px;

}
input , select{
    width: 80%;
    border: none;
    border-bottom: 1px solid #0074d9;
    padding: 10px;

}
input :focus, select:focus{border: 1px solid #0074d9;
    outline: none;
    
}
select{

    width: 88% !important;
}
button{
    margin: 20px auto;
    width: 150px;
    height: 50px;
    background-color: #39cccc;
    color: #fff;
    font-size: 16px;
    border: none;
    border-radius: 5px;

}
.tip{
    text-align: center;
    font-size: 18px;
    display: none;
}
</style>
</head>
<body>
   <div class="container">
    <h1>TIP CALCULATOR</h1>
    <div class="wrapper">
        <p>Bill Amount</p>
        <input type="text"  name="Bill Amount" id="Amount" placeholder="Enter Your Amount">Rs
        <p>How was the service ?</p>
        <select id="services">
            <option selected disabled hidden> Select</option>
            <option value="0.25">25%</option>
            <option value="0.50">50%</option>
            
            <option value="0.75">75%</option>
            <option value="1.00">100% </option>
        </select>
    <p>Total number of persons</p>
    <input type="text" id="persons" placeholder="Number of people sharing the bill">
    <button id="colculate">Colculate</button>

    </div>
<div class="tip">
    <p>Tip Amount</p>
    <span id="total">0</span>Rs
    <span id="each">each</span>
</div>
   </div>
   <script>
    window.onload = () =>{
        document. querySelector('#calculate').onclick = calculateTip;
    }
    function calculateTip ( ) {
        let amount = document . querySelector ('#amount'). value;
        let persons = document . querySelector ('#persons'). value;
        let service = document . querySelector ('#services'). value;

        console.log(service);

        if (amount  === ' ' && service === 'Select') {
            alert ("Please Enter valid values");
            return;
        }
        if(persons === '1')
        document.querySelector(#each) .style.display = 'none';
        else
        document. querySelector(#each) .style.display= 'block';
        let total = (amount *service) / persons;
        total = total.toFixed(2);
        document.querySelector('.tip') .style.display = 'block';
        document.querySelector('#total') .innerHTML = total;
    }
   </script> 
</body>
</html>
