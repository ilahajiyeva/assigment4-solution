<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Forms</title>
    <link rel="stylesheet" href="js.css">
    <link rel="stylesheet" href="assets/css/all.css">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
</head>
<body>
<div class = "container">
    <h3 class = "head">Sign Up</h3>
    <form action="#" id="frmgrp" method="post" name="frmgrp" autocomplete="on">
        <p><label for="firstname">First Name</label></p>
        <div class="tooltip">
            <input type="text"  name="firstname" id="firstname" placeholder="First Name" required autofocus>
            <label class="firstName">What is your name?</label>
        </div>
        <p id="result"></p>
        <p><label for="lastname">Last Name</label></p>
        <div class="tooltip">
            <input type="text"  name="lastname" id="lastname" placeholder="Last Name" required>
            <label class="lastName">What is your name?</label>
        </div>
        <p id="result1"></p>
        <p>Gender</p>
        <label for="man"></label>
        <div>
            <input type="radio" id="man" name="gender">Male
            <label for="woman"></label>
            <input type="radio" id="woman" name="gender">Female
        </div>
        <p>Birthday</p>
        <div>
            <select class="year">
                <option>Jan</option>
                <option>Feb</option>
                <option>Mar</option>
                <option>Apr</option>
                <option>May</option>
                <option>Jun</option>
                <option>Jul</option>
                <option>Aug</option>
                <option>Sep</option>
                <option>Oct</option>
                <option>Nov</option>
                <option>Dec</option>
            </select>
            <select class="year">
                <option>01</option>
                <option>02</option>
                <option>03</option>
                <option>04</option>
                <option>05</option>
                <option>06</option>
                <option>07</option>
                <option>08</option>
                <option>09</option>
                <option>10</option>
                <option>11</option>
                <option>12</option>
            </select>
            <input type="number" max="2005" min="1930" value="1992" class="year1">
        </div>
        <p><label for="email">Email</label></p>
        <div class="tooltip">
            <input type="email" name="email" id="email" placeholder="Email address">
            <label class="email">Enter your E-mail address</label>
            <p id="result3"></p>
        </div>
        <p><label for="password">Password</label></p>
        <div class="tooltip">
            <input type="password" name="password" id="password" placeholder="Password(6 or more charachters)" minlength="6">
            <label class="password">Enter Password(6 or more charachters)</label>
        </div>

        <div>
            <input type="checkbox" id="checkBox" name="checkBox">
        </div>
        <label class="checkbox" for="checkBox">I read and agree</label>
        <div>
            <input type="button" name="button" id="btn1" value="Sign Up" onclick="signUp();">
        </div>
        <div class="sign">
            Already have an account?<a href="login.html" target="_blank">Sign In</a>
        </div>
    </form>
</div>
<script>
    function signUp() {
        var firstname, lastname, result, result1, message, Email, result3;
        result = document.getElementById("result");
        result1 = document.getElementById("result1");
        result3 = document.getElementById("result3");
        firstname = document.getElementById("firstname");
        Email = document.getElementById("email");
        lastname = document.getElementById("lastname");

        if (firstname.checkValidity() === false) {
            firstname.style.border = "1px solid red";
            message = firstname.validationMessage;
        } else {
            message = "";
        }
        result.innerHTML = message;

        if (lastname.checkValidity() === false) {
            lastname.style.border = "1px solid red";
            message = lastname.validationMessage;
        } else {
            message = "";
        }
        result1.innerHTML = message;

        if (document.frmgrp.checkBox.checked) {
            message = ""
        } else {
            alert("Please read & check it!");
        }

        if (Email.checkValidity() === false) {
            Email.style.border = "1px solid red";
            message = Email.validationMessage;
        }
        result3.innerHTML=message;
    }


</script>
</body>
</html>
