

<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Landing Page</title>

    <!--<link rel="stylesheet" href="style.css">-->
    <style>
       

.light {

    --mainColor: #45B65C;

    --hovercolor: #00776C;

    --backgroundcolor: #f2fff5;

    --darkone: #042009;

    --darktwo: #13521e;

    --lightone: #b9b8b8;

    --lightTwo: #929292;

}



.dark{

    --mainColor: #45B65C;

    --hovercolor: #00776C;

    --backgroundcolor: #00221f;

    --darkone: #eaffee;

    --darktwo: #fff;

    --lightone: #ccc;

    --lightTwo: #eaffee;

}



*, *::before, *::after{

    padding: 0;

    margin: 0;

    box-sizing: border-box;

}

body{

    font-family: Arial, Helvetica, sans-serif;

}



.stop-scrolling{

    height: 100%;

    overflow: hidden;

}



img{

    width: 100%;

}

a{

    text-decoration: none;

}

.big-wrapper{

    position: relative;

    padding: 1.7rem 0 2rem;

    width: 100%;

    min-height: 100vh;

    overflow: hidden;

    background-color: var(--backgroundcolor);

    display: flex;

    flex-direction: column;

    justify-content: space-between;

}



.container{

    position: relative;

    max-width: 81rem;

    width: 100%;

    margin: 0 auto;

    padding: 0 3rem;

    z-index: 10;

}



header{

    position: relative;

    z-index: 70;



}



header .container{

    display: flex;

    justify-content: space-between;

    align-items: center;

}



.overlay {

    display: none;

}



.logo{

    display: flex;

    align-items: center;

    cursor: pointer;

}



.logo img{

    width: 40px;

    margin-right: 0.6rem;

    margin-top: -0.6rem;

} 



h3, h1{

    color: var(--darktwo);

}

/*.links{

    display: none;

}*/



.hamburger-menu{

    position: relative;

    z-index: 99;

    width: 2rem;

    height: 2rem;

    display: flex;

    align-items: center;

    justify-content: center;

    cursor: pointer;

    display: none;

}



.hamburger-menu .bar{

    position: relative;

    width: 100%;

    height: 3px;

    background-color: var(--darktwo);

    border-radius: 3px;

    transition: .5s;

}



.bar::before, 

.bar::after{

    content: "";

    position: absolute;

    width: 100%;

    height: 100%;

    background-color: var(--darktwo);

    border-radius: 3px;

    transition: 0.5s;

}



.bar::before{

    transform: translateY(-8px);

}



.bar::after{

    transform: translateY(8px);

}



.big-wrapper.active  .hamburger-menu .bar{

    background-color: transparent;

}



.big-wrapper.active .bar::before{

    transform: translate(0) rotate(-45deg);

}



.big-wrapper.active .bar::after{

    transform: translate(0) rotate(45deg);

}



.logo .word{

    color: #CA8F1C;

    /*color: var(--darkone);*/

}

.links ul{

  display: flex;

  list-style: none;

  align-items: center;

}



.links a{

    color: var(--lightTwo);

    margin-left: 4.5rem;

    display: inline-block;

    transition: 0.3s;

}



.links a:hover{

    color: var(--hovercolor);

    transform: scale(1.05);

}



.logo h3{

    color: var(--darkTwo);

    font-size: 1.55rem;

    line-height: 1.2;

    font-weight: 700;

}



.btn{

    display: inline-block;

    padding: 0.9rem 1.9rem;

    color: #ffffff !important;

    background-color: var(--mainColor);

    border-radius: 16px;

    text-transform: capitalize;

    transition: 0.3s;

}



.btn:hover{

    background-color: var(--hovercolor);

    transform: scale(1) !important;

}



.showcase-area .container{

    display: grid;

    grid-template-columns: repeat(2, 1fr);

    align-items: center;

    justify-content: center;

}



.big-tittle{

    font-size: 1.4rem;

    color: var(--darkone);

    text-transform: capitalize;

    line-height: 1.4;

}



.text{

    color: var(--lightone);

    font-size: 1.1rem;

    margin: 1.9rem 0 2.5rem;

    max-width: 600px;

    line-height: 2.3;

}



.showcase-area .btn{

    box-shadow: 0 0 40px 2px rgba(0, 0, 0, 0.05);

}



.person{

    width: 123%;

    transform: translate(15%, 25px);

}



.toggle-btn{

    display: flex;

    justify-content: center;

    align-items: center;

    border: none;

    border: var(--darkTwo);

    color: var(--backgroundcolor);

    outline: none;

    cursor: pointer;

    height: 39px;

    width: 39px;

    border-radius: 50%;

    font-size: 1.1rem;

    transition: 0.3s;

}



.toggle-btn img{

    height: 20px;

    width: 20px;

    line-height: 39px;

}



.toggle-btn:hover{

    background: var(--hovercolor);

}



.big-wrapper.light .toggle-btn img:last-child{

    display: none;

}



.big-wrapper.light .toggle-btn img:first-child{

    display: block;

}



.big-wrapper.dark .toggle-btn img:last-child{

    display: block;

}



.big-wrapper.dark .toggle-btn img:first-child{

    display: none;

}



.toggle-btn{

    background-color: var(--darkone);

}



.shape{

    position: absolute;

    z-index: 0;

    width: 500px;

    bottom: -180px;

    left: -15px;

    opacity: 0.1;

}



.copy{

    position: absolute;

    top: 0;

    left: 0;

    z-index: 100;

    animation: appear 1s 1 both;

}



@keyframes appear {

    0%{

        clip-path: circle(30% at -25% -25%);

    }

    100%{

        clip-path: circle(150% at 0 0);

    }

}



@media screen and (max-width: 870px) {

    .showcase-area .container{

        grid-template-columns: 1fr;

    }



    .person{

        width: 100%;

        transform: none;

    }



    .hamburger-menu {

        display: flex;

    }



    .links{

        position: fixed;

        top: 0;

        right: 0;

        max-width: 450px;

        width: 70%;

        height: 100%;

        background-color: var(--mainColor);

        z-index: 95;

        display: flex;

        align-items: center;

        justify-content: center;

        transform: translateX(100%);

        transition: 0.5s;

    }



    .links ul{

        flex-direction: column;

    }



    .links a{

        color: #fff;

        margin-left: 0;

        padding: 2rem 0;

    }



    .links .btn{

        background-color: none;

    }



    .overlay{

        display: block;

        position: fixed;

        top: 0;

        left: 0;

        right: 0;

        bottom: 0;

        background-color: rgba(0, 0, 0, 0.7);

        opacity: 0;

        pointer-events: none;

        transition: 0.5s;

    }



    .big-wrapper.active .links{

        transform: translateX(0);



        box-shadow: 0 0 50px 2px rgba(0, 0, 0, 0.4);

    }



    .big-wrapper.active  .overlay {

        pointer-events: all;

        opacity: 1;

    }



    .showcase-area{

        padding: 2.5rem 0;

        max-width: 700px;

        margin: 0 auto;

    }



    .showcase-area .container{

        grid-template-columns: 1fr;

        justify-content: center;

        grid-gap: 2rem;

    }



    .big-tittle{

        font-size: 1.1rem;

    }



    .text{

        font-size: .95rem;

        margin: 1.4rem 0 1.5rem;

    }



    .person{

        width: 100%;

        transform: none;

    }



    .logo h3{

        font-size: 1.25rem;

    }



    .shape{

        bottom: -180px;

        left: -150px;

    }



}



@media screen and (max-width: 470px){

    .container{

        padding: 0 1.5rem;

    }



    .big-tittle{

        font-size: 0.9rem;

    }



    .text{

        margin: 1.1rem 0 1.5rem;

    }



    .showcase-area .btn{

        font-size: 0.8rem;

    }

}






    </style>

</head>

<body>

   <main>

       <div class="big-wrapper light">

          <img src="https://api1.ngd.africa/media/uploads/images/shape.png" alt="" class="shape">



          <header>

            <div class="container">

                <div class="logo">

                    <img src="https://api1.ngd.africa/media/uploads/images/logo_Kf773A2.png" alt="logo">

                    <h3 class="word">Artivision</h3>

                </div>



                <div class="links">

                    <ul>

                        <li><a href="#">Features</a></li>

                        <li><a href="#">Projects</a></li>

                        <li><a href="#">About me</a></li>

                        <li><a href="#" class="btn">Contact me</a></li>

                    </ul>

                </div>



                <div class="overlay"></div>



                <div class="hamburger-menu">

                    <div class="bar"></div>

                </div>

            </div>

          </header>



          <div class="showcase-area">

             <div class="container">

                <div class="left">

                    <div class="big-tille">

                        <h1 class="word">Welcome !</h1>

                        <h1 class="word">Meet Mmenim Mathias.</h1>

                    </div>

                    <p class="text">

                       Mmenim Mathias brings the ultimate web experience closest to you.

                       Achievable through studying and incoporating the best practices of user experience design.

                       This is his first prototype, which would serve as his portfolio.

                    </p>

                    <div class="cta">

                        <a href="#" class="btn">View projects</a>

                    </div>

                </div>

  

                <div class="right">

              <img src="https://api1.ngd.africa/media/uploads/images/person.png"/>


                </div>

             </div>

          </div>



          <div class="bottom-area">

              <div class="container">

                  <button class="toggle-btn">

                      <!--<i class="far fa-mooon"><img src="images/moon.svg" class="botton" alt="moon"></i>

                      <i class="far fa-sun"><img src="images/sun.svg" class="button" alt="sun"></i>-->
                      
                      <img src="https://img.icons8.com/emoji/48/000000/white-circle-emoji.png"/>
                      
                      <img src="https://img.icons8.com/material-outlined/24/000000/sun--v1.png" class="button" alt="sun"/>
                  
                      <!--<img src="images/moon.svg" class="botton" alt="moon">

                      <img src="sun.svg" class="button" alt="sun">-->

                     

                  </button>

              </div>

          </div>

       </div>

   </main> 







   <!--<script src="https://kit.fontawesome.com/a81368914c.js"></script>-->

   <!--<script src="script.js"></script>-->
   
   <script>
      // select the elements

var toggle_btn;

var big_wrapper;

var hamburger_menu;



function declare(){

    toggle_btn = document.querySelector(".toggle-btn");

    big_wrapper = document.querySelector(".big-wrapper");

    hamburger_menu = document.querySelector(".hamburger-menu");

}



const main = document.querySelector("main");



declare();



let dark = false;

function toggleAnimation(){

    //clone the wrapper

    dark = !dark;

    let clone = big_wrapper .cloneNode(true);

    if(dark){

        clone.classList.remove("light");

        clone.classList.add("dark");

    }

    else{

        clone.classList.remove("dark");

        clone.classList.add("light")

    }

    clone.classList.add("copy");

    main.appendChild(clone);



    document.body.classList.add("stop-scrolling");



    clone.addEventListener("animationend", () => {

        document.body.classList.remove("stop-scrolling");

        big_wrapper.remove();

        clone.classList.remove("copy");

        //Reset variables

        declare();

        events();

    })

}



function events(){

    toggle_btn.addEventListener("click", toggleAnimation);

    hamburger_menu.addEventListener("click", () => {

        big_wrapper.classList.toggle("active");

    })

}



events();






   </script>

</body>

</html>
