---
# An instance of the Blank widget.
# Documentation: https://wowchemy.com/docs/getting-started/page-builder/
widget: blank

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 50

design:
# Choose how many columns the section has. Valid values: 1 or 2.
  columns: "1"

# ... Put Your Section Options Here (title etc.) ...
title: Projects
---

{{% callout note %}}
This PROJECT section is **coming soon**.

Please bear with me, I am still learning to develop a website. :stuck_out_tongue:
{{% /callout %}}

Meanwhile, jump into my projects at [Github](https://github.com/jamwine).
<img src='https://avatars.githubusercontent.com/u/7883396?s=460&u=56eaac1fc8d368fa0e20a5358ebe36de17c6facd&v=4' alt='jamwine.png' width=400 height=400 class='center'>

 <!-- home section start -->
  <section class="home" id="home">
          <div class="max-width">
              <div class="home-content">
                  <div class="text-3">This PROJECT section is <span class="typing-2">.</span></div>
              </div>
          </div>
      </section>

<!-- services section start
   <section class="services" id="services">
          <div class="max-width">
              <h2 class="title">My services</h2>
              <div class="serv-content">
                  <div class="card">
                      <div class="box">
                          <i class="fas fa-paint-brush"></i>
                          <div class="text">Web Design</div>
                          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem quia sunt, quasi quo illo enim.</p>
                      </div>
                  </div>
                  <div class="card">
                      <div class="box">
                          <i class="fas fa-chart-line"></i>
                          <div class="text">Advertising</div>
                          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem quia sunt, quasi quo illo enim.</p>
                      </div>
                  </div>
                  <div class="card">
                      <div class="box">
                          <i class="fas fa-code"></i>
                          <div class="text">Apps Design</div>
                          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem quia sunt, quasi quo illo enim.</p>
                      </div>
                  </div>
                </div>
              </div>
          </div>
      </section> -->


<style>
  /*  import google fonts */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
}
html{
    scroll-behavior: smooth;
}

/* custom scroll bar */
::-webkit-scrollbar {
    width: 10px;
}
::-webkit-scrollbar-track {
    background: #f1f1f1;
}
::-webkit-scrollbar-thumb {
    background: #888;
}

::-webkit-scrollbar-thumb:hover {
    background: #555;
}

/* all similar content styling codes */
section{
    padding: 100px 0;
}
.max-width{
    max-width: 1300px;
    padding: 0 80px;
    margin: auto;
}
.about, .services, .skills, .teams, .contact, footer{
    font-family: 'Poppins', sans-serif;
}
.about .about-content, 
.services .serv-content,
.skills .skills-content,
.contact .contact-content{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
}
section .title{
    position: relative;
    text-align: center;
    font-size: 40px;
    font-weight: 500;
    margin-bottom: 60px;
    padding-bottom: 20px;
    font-family: 'Ubuntu', sans-serif;
}
section .title::before{
    content: "";
    position: absolute;
    bottom: 0px;
    left: 50%;
    width: 180px;
    height: 3px;
    background: #111;
    transform: translateX(-50%);
}
section .title::after{
    position: absolute;
    bottom: -8px;
    left: 50%;
    font-size: 20px;
    color: #31669b;
    padding: 0 5px;
    background: #fff;
    transform: translateX(-50%);
}


/* menu btn styling */
.menu-btn{
    color: #fff;
    font-size: 23px;
    cursor: pointer;
    display: none;
}
.scroll-up-btn{
    position: fixed;
    height: 45px;
    width: 42px;
    background: #31669b;
    right: 30px;
    bottom: 10px;
    text-align: center;
    line-height: 45px;
    color: #fff;
    z-index: 9999;
    font-size: 30px;
    border-radius: 6px;
    border-bottom-width: 2px;
    cursor: pointer;
    opacity: 0;
    pointer-events: none;
    transition: all 0.3s ease;
}
.scroll-up-btn.show{
    bottom: 30px;
    opacity: 1;
    pointer-events: auto;
}
.scroll-up-btn:hover{
    filter: brightness(90%);
}

  
/* home section styling */
.home{
    display: flex;
    background: url("images/banner.jpg") no-repeat center;
    height: 100vh;
    color: #fff;
    min-height: 500px;
    background-size: cover;
    background-attachment: fixed;
    font-family: 'Ubuntu', sans-serif;
}
.home .max-width{
    margin: auto 0 auto 30px;
}
.home .home-content .text-1{
    font-size: 27px;
}
.home .home-content .text-2{
    font-size: 75px;
    font-weight: 600;
    margin-left: -3px;
}
.home .home-content .text-3{
    font-size: 40px;
    margin: 2px 0;
    color: black;
}
.home .home-content .text-3 span{
    color: #31669b;
    font-weight: 400;
}
.home .home-content a{
    display: inline-block;
    background: #31669b;
    color: #fff;
    font-size: 15px;
    padding: 12px 36px;
    margin-top: 20px;
    font-weight: 400;
    border-radius: 6px;
    border: 2px solid #31669b;
    transition: all 0.3s ease;
}
.home .home-content a:hover{
    color: #31669b;
    background: none;
}

/* about section styling */
.about .title::after{
    content: "who i am";
}

.about .about-content{
    width: 95%;
}
.about .about-content .text{
    font-size: 27px;
    font-weight: 300;
    margin-bottom: 10px;
}
.about .about-content .text span{
    color: #31669b;
}
 .about .about-content p{
    text-align: justify;
} 

.about .about-content a{
    display: inline-block;
    background: #31669b;
    color: #fff;
    font-size: 15px;
    font-weight: 300;
    padding: 5px 10px;
    margin-top: 5px;
    border-radius: 3px;
    border: 1px solid #31669b;
    transition: all 0.3s ease;
}
.about .about-content a:hover{
    color: #31669b;
    background: none;
}

/* services section styling */
.services, .teams{
    color:#fff;
    /* background: #111; */
}
.services .title::before,
.teams .title::before{
    background: #fff;
}
.services .title::after,
.teams .title::after{
    content: "what i provide";
}
.services .serv-content .card{
    width: calc(33% - 20px);
    background: #31669b;
    text-align: center;
    border-radius: 6px;
    padding: 20px 25px;
    cursor: pointer;
    transition: all 0.3s ease;
}
.services .serv-content .card:hover{
    background: #1a4a7a;
}
.services .serv-content .card .box{
    transition: all 0.3s ease;
}
.services .serv-content .card:hover .box{
    transform: scale(1.05);
}
.services .serv-content .card i{
    font-size: 50px;
    color: #fff;
    transition: color 0.3s ease;
}
.services .serv-content .card:hover i{
    color: #fff;
}
.services .serv-content .card .text{
    font-size: 25px;
    font-weight: 500;
    margin: 10px 0 7px 0;
}

/* skills section styling */

.skills .title::after{
    content: "what i know";
}
.skills .skills-content .column{
    width: calc(50% - 30px);
}
.skills .skills-content .text{
    font-size: 20px;
    font-weight: 300;
    margin-bottom: 10px;
}
.skills .skills-content .left .bars,
.skills .skills-content .right .bars{
    margin-bottom: 15px;
}
.skills .skills-content .left .info,
.skills .skills-content .right .info{
    display: flex;
    margin-bottom: 5px;
    align-items: center;
    justify-content: space-between;
}
.skills .skills-content .left .span,
.skills .skills-content .right span{
    font-weight: 500;
    font-size: 18px;
}
.skills .skills-content .left .line,
.skills .skills-content .right .line{
    height: 5px;
    width: 100%;
    background: lightgrey;
    position: relative;
}
.skills .skills-content .left .line::before,
.skills .skills-content .right .line::before{
    content: "";
    position: absolute;
    height: 100%;
    left: 0;
    top: 0;
    background: #31669b;
}
.skills-content .left .ml::before,
.skills-content .right .sm::before{
    width: 90%;
}
.skills-content .left .trend::before,
.skills-content .right .iv::before{
    width: 95%;
}
.skills-content .left .ds::before,
.skills-content .right .dl::before{
    width: 85%;
}
.skills-content .left .cv::before,
.skills-content .right .ws::before{
    width: 80%;
}

</style>

 <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://kit.fontawesome.com/a076d05399.js"></script>
    <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/typed.js/2.0.11/typed.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/waypoints/4.0.1/jquery.waypoints.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css"/>
 </head>

   <div class="scroll-up-btn">
          <i class="fas fa-angle-up"></i>
    </div>






<script>  
  $(document).ready(function(){
      $(window).scroll(function(){
        // sticky navbar on scroll script
        if(this.scrollY > 20){
            $('.navbar').addClass("sticky");
        }else{
            $('.navbar').removeClass("sticky");
        }
        
        // scroll-up button show/hide script
        if(this.scrollY > 100){
            $('.scroll-up-btn').addClass("show");
        }else{
            $('.scroll-up-btn').removeClass("show");
        }
    });

    // slide-up script
    $('.scroll-up-btn').click(function(){
        $('html').animate({scrollTop: 0});
        // removing smooth scroll on slide-up button click
        $('html').css("scrollBehavior", "auto");
    });

    // typing text animation script
    var typed = new Typed(".typing", {
        strings: ["Software Engineer", "Python Developer", "Data Scientist"],
        typeSpeed: 100,
        backSpeed: 60,
        loop: true
    });

    var typed = new Typed(".typing-2", {
        strings: ["COMING SOON...","COMING SOON...","COMING SOON..."],
        typeSpeed: 100,
        backSpeed: 60,
        loop: true
    });
});
  </script>