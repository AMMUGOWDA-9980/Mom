<!DOCTYPE html>
<html>
<head>
    <title>Form Validation</title>
</head>
<body>

<h2>Registration Form</h2>

<form onsubmit="return validateForm()">

    Name:
    <input type="text" id="name"><br><br>

    Email:
    <input type="text" id="email"><br><br>

    Password:
    <input type="password" id="password"><br><br>

    Age:
    <input type="number" id="age"><br><br>

    <input type="submit" value="Register">

</form>

<script>
function validateForm() {

    let name = document.getElementById("name").value;
    let email = document.getElementById("email").value;
    let password = document.getElementById("password").value;
    let age = document.getElementById("age").value;

    if (name == "") {
        alert("Please enter your name");
        return false;
    }

    if (email == "") {
        alert("Please enter your email");
        return false;
    }

    if (password.length < 6) {
        alert("Password must have 6 characters");
        return false;
    }

    if (age < 18 || age > 60) {
        alert("Age must be between 18 and 60");
        return false;
    }

    alert("Registration successful!");
    return true;
}
</script>

</body>
</html>
