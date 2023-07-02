<!DOCTYPE html>
<html>
<head>
    <title>EXTREME LOOT</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }

        h1 {
            font-size: 2rem;
        }

        #user-login {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-top: 2rem;
        }

        input[type="email"],
        input[type="text"] {
            width: 300px;
            height: 40px;
            font-size: 1.2rem;
            margin-bottom: 1rem;
            text-align: center;
        }

        .start-button {
            width: 200px;
            height: 60px;
            font-size: 1.5rem;
            background-color: #ff4500;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .start-button:hover {
            background-color: #ff6633;
        }
    </style>
</head>
<body>
    <h1>EXTREME LOOT</h1>

    <div id="user-login">
        <h2>User Login</h2>
        <input type="email" id="email" placeholder="Email ID">
        <input type="text" id="paytm-number" placeholder="Paytm Number">
        <button class="start-button" onclick="loginUser()">Start</button>
    </div>

    <script>
        var users = {};

        function loginUser() {
            var email = document.getElementById("email").value;
            var paytmNumber = document.getElementById("paytm-number").value;

            if (email && paytmNumber) {
                if (!users[email]) {
                    users[email] = paytmNumber;
                    console.log("User " + email + " logged in with Paytm number " + paytmNumber + ".");
                    window.location.href = "https://cooe.in/promote/#/register?c=6YK15RP1";
                } else {
                    console.log("User already logged in with this email ID.");
                }
            } else {
                alert("Please fill in both the Email ID and Paytm Number.");
            }
        }
    </script>
</body>
</html>
