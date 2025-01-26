# HTML CODE
# login-and-register-webpage
<!DOCTYPE html>
<html lang="en">

    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width,
        initial-scale=1.0">
        <title>website with Login & Registration</title>
        <link rel="stylesheet" href="sample2.css">
    </head>

    <body>
        <header>
            <h2 class="satya">Satya</h2>
            <nav class="navigation">
                <a href="#">Home</a>
                <a href="#">About </a>
                <a href="#">Contact Us</a>
                <button class="btnlogin-popup">Login</button>
            </nav>
        </header>

        <div class="wrapper">
            <span class="icon-close"><ion-icon name="close"></ion-icon></span>

            <div class="form-box login">
                <h2>Login</h2>
                <form action="#">
                    <div class="input-box">
                        <span class="icon"><ion-icon name="mail"></ion-icon></span>
                        <input type="email" required>
                        <label>Email</label>
                        </label>
                    </div>
                    <div class="input-box">
                        <span class="icon"><ion-icon name="lock-closed"></ion-icon></span>
                        <input type="password" required>
                        <label>Password</label>
                    </div>
                    <div class="remember-forgot">
                        <label><input type="checkbox">
                        Remember me </label>
                        <a href="#">Forgot Password</a>
                    </div>
                    <button type="submit" class="btn">Login</button>
                    <div class="login-register">
                        <p>Don't have an account?
                            <a href="#" 
                            class="register-link">Register</a>
                        </p>
                    </div>
                </form>
            </div>
        <div class="form-box register">
                <h2>Registration</h2>
                <form action="#">
                    <div class="input-box">
                        <span class="icon">
                        <ion-icon name="person"></ion-icon></span>
                        <input type="text" required>
                        <label>Username</label>
                        </label>
                    </div>
                    <div class="input-box">
                        <span class="icon"><ion-icon name="mail"></ion-icon></span>
                        <input type="email" required>
                        <label>Email</label>
                        </label>
                    </div>
                    <div class="input-box">
                        <span class="icon"><ion-icon name="lock-closed"></ion-icon></span>
                        <input type="password" required>
                        <label>Password</label>
                    </div>
                    <div class="remember-forgot">
                        <label><input type="checkbox">
                       I agree to the terms & conditions</label>
                       
                    
                    </div>
                    <button type="submit" class="btn">Register</button>
                    <div class="login-register">
                        <p>Already have an account
                        <a href="#" class="login-link">Login</a>
                        </p>
                    </div>
                </form>
        </div>

        <script src="sample3.js"></script>
        <script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
        <script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
        
     </body>
</html>

# CSS CODE
  @import url("https://fonts.google.com/specimen/Poppins");
* {
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'popins',sans-serif;
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-image: url("cute.jpg");
    height: 500px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
   
}
/*body {
    background-image: url("img.jpg");
    height: 500px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
  }*/
header {
    position:fixed;
    top:0;
    left:0;
    width:100%;
    padding:20px 100px;
    display:flex;
    justify-content: space-between;
    align-items:center;
    z-index: 99;
}
.satya {
    font-size: 2em;
    color:#fff;
    user-select: none;
}
.navigation a {
    position: relative;
    font-size: 1.1em;
    color:#fff;
    text-decoration: none;
    font-weight: 500;
    margin-left: 40px;
}
.navigation a::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -6px;
    width: 100%;
    height: 3px;
    background: #fff;
    border-radius: 5px;
    transform-origin: right;
    transform: scaleX(0);
    transition: transform .5s;
}
.navigation a:hover::after {
    transform-origin: left;
    transform: scaleX(1);
}

.navigation .btnlogin-popup{
    width: 130px;
    height: 50px;
    background: transparent;
    border: 2px solid #fff;
    outline: none;
    border-radius: 6px;
    cursor: pointer;
    font-size: 1.1em;
    color:#fff;
    font-weight: 500;
    margin-left: 40px;
    transition:.5s;
}
.navigation.btnLogin-popup:hover{
    background: #fff;
    color: #162938;
}


.wrapper{
    position: relative;
    width: 400px;
    height: 440px;
    background: transparent;
    border: 2px solid rgba(225, 225, 225,5);
    border-radius:20px ;
    backdrop-filter: blur(20px);
    box-shadow: 0 0 30px rgba(0,0,0,.5);
    display:flex;
    justify-content: center;
    align-items: center;
   overflow:hidden ;
   transform:scale(0);
   transition: transform .5s ease,height .2s ease;
}
.wrapper.active-popup{
    transform:scale(1);}

.wrapper.active{
    height:520px;
}
.wrapper.form-box {
    width: 100px;
    padding:40px;   
}
.wrapper .form-box.login{
    transition: transform .18s ease;
    transform: translateX(0);
    /*display:none;*/
}
.wrapper.active .form-box.login{
    transition: none;
    transform: translateX(-400px);

}
.wrapper .form-box.register{
    position:absolute;
    transition: none;
    transform: translateX(400px);
}
.wrapper.active .form-box.register{
    transition: transform .18s ease;
    transform: translateX(0);
}
.wrapper .icon-close{
    position: absolute;
    top:0;
    right:0;
    width: 45px;
    height:45px;
    background:#162938;
    font-size: 2em;
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    border-bottom-left-radius: 20px ;
    cursor: pointer;
    z-index:1;

}
.from-box h2{
    font-size:2em ;
    color:#162938;
    text-align: center;
}
.input-box{
    position:relative; 
    width : 100%;
    height: 50px;
    border-bottom: 2px solid #162938;
    margin: 30px 0;
}
.input-box label{
    position: absolute;
    top: 50%;
    left:5px;
    transform: translateY(-50);
    font-size:1em;
    color: #162938;
    font-weight: 500;
    pointer-events: none;
    transition: .5s;
}
.input-box input:focus~label,
.input-box input:valid~label{
    top:-5px;
}
.input-box input{
    width: 100%;
    height:100%;
    background:transparent;
    border: none;
    outline: none;
    font-size: 1em;
    color: #162938;
    font-weight: 600;
    padding:0 35px 0  5px ;

}
.input-box .icon{
    position: absolute;
    right: 8px;
    font: size 1.2em; 
    color: #162938;
    
}
.remember-forgot{
    font-size:.9em;
    color: #162938;
    font-weight: 500;
    margin: -15px 0 15px;
    display: flex;
    justify-content: space-between;

}
.remember-forgot label input{
    accent-color: #162938;
    margin-right: 3px;
}
.remember-forgot a{
    color:#162938;
}
.remember-forgot a:hover{
    text-decoration: underline;
}
.btn{
    width:100%;
    height: 45px;
    background: #162938;
    border: none;
    outline:none;
    border-radius:6px;
    cursor:pointer;
    font-size: 1em;
    color: #fff;
    font-weight: 500;
}
.login-regiter{
    font-size:.9em;
    color:#162938;
    text-align:center;
    margin:25px 0 10px;

}
.login-regiter p a{
    color: #162938;
    text-decoration: none;
    font-weight: 600;
}
.login-regiter p a:hover{
    text-decoration: underline;
}

# JAVASCRIPT CODE
const wrapper=document.querySelector('.wrapper');
const loginLink=document.querySelector('.login-link');
const registerLink=document.querySelector('.register-link');
const btnPopup = document.querySelector('.btnlogin-popup');
const iconClose=document.querySelector('.icon-close');

registerLink.addEventListener('click',() => {
    wrapper.classList.add('active');
});
loginLink.addEventListener('click',() => {
    wrapper.classList.remove('active');
});
btnPopup.addEventListener('click',() => {
    wrapper.classList.add('active-popup');
});
iconClose.addEventListener('click',() => {
    wrapper.classList.remove('active-popup');
});

