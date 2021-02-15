---
# An instance of the Blank widget.
# Documentation: https://wowchemy.com/docs/getting-started/page-builder/
widget: blank

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 52

design:
# Choose how many columns the section has. Valid values: 1 or 2.
  columns: "1"

# ... Put Your Section Options Here (title etc.) ...
title: Testing
---

<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,500,600,700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/2.1.2/TweenMax.min.js"></script>
  <!-- <link rel="stylesheet" href="style.css"> -->

  <style>

    * {
    margin: 0;
    padding: 0
  }

  body {
    width: 100%;
    height: 100vh;
    font-family: 'agency fb';
    background: url('reindeer.png') no-repeat;
    background-position: 50%;
    background-size: cover;
    overflow: hidden;
  }

  ul {
    list-style: none;
  }

  .nav {
    width: 200px;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .logo {
    flex: 0 0 50%;
    background: #FFEB00;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .logo h1 {
    font-weight: 300;
    text-transform: uppercase;
    font-size: 16px;
    line-height: 2;
  }

  .logo span {
    font-size: 60px;
    line-height: 1;
  }

  .menu-links {
    flex: 1;
    display: flex;
    justify-content: flex-end;
    text-align: right;
    padding-top: 50px;
  }

  .menu-links ul {
    width: 100%;
  }

  .menu-links ul li {
    padding: 10px;
    color: #494949;
    font-size: 20px;
    font-weight: 600;
    text-transform: uppercase;
    cursor: pointer;
  }

  .menu-links ul li:hover {
    background: #494949;
    color: #fff;
  }

  .scrolldown {
    flex: 1;
    display: flex;
    justify-content: center;
    transform: rotate(-90deg);
  }

  .scrolldown::before {
    display: inline-block;
    content: "";
    border-top: 1px solid #000;
    width: 65px;
    margin: 0 10px 0 0;
    transform: translateY(10px);
  }

  .text {
    position: absolute;
    top: 25%;
    right: 180px;
    transform: translateY(-50%);
    text-align: right;
    color: #494949;
  }

  .text .title {
    font-size: 150px;
  }

  .watchnow {
    position: absolute;
    top: 60%;
    right: 0;
    transform: translateY(-50%);
    background: #FFEB00;
    padding: 30px 180px 30px 30px;
  }

  .watchnow a {
    text-decoration: none;
    color: #000;
    font-size: 20px;
    font-weight: 600;
    text-transform: uppercase;
    border-bottom: 3px solid #000;
    padding-bottom: 5px;
  }

  .fa-play {
    color: #fff;
    font-size: 30px;
    margin-right: 20px;
    cursor: pointer;
  }

  .media {
    position: absolute;
    bottom: 0;
    right: 0;
    padding: 20px;
  }

  .media ul li {
    display: inline-block;
    padding: 20px;
    font-size: 20px;
    color: #494949;
    cursor: pointer;
    border-radius: 50%;
  }

  .media ul li:hover {
    background: #FFEB00;
  }

  .ellipse-container {
    width: 608px;
    height: 608px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 50%;
    margin: 0 auto;
    z-index: -1;
  }

  .ellipse {
    position: absolute;
    top: 0;
    border-radius: 50%;
    border-style: solid;
  }

  .ellipse.thin {
    width: 100%;
    height: 100%;
    border-width: 1px;
    border-color: #494949;
    opacity: .5;
  }

  .ellipse.thick {
    width: 93%;
    height: 93%;
    border-width: 10px;
    border-color: #fff;
    transform: rotate(-45deg);
    top: 12px;
    left: 12px;
  }

  .ellipse.yellow {
    width: 93%;
    height: 93%;
    border-width: 10px;
    border-color: #FFEB00 transparent;
    transform: rotate(-45deg);
    top: 12px;
    left: 12px;
    animation: ellipseRotate 15s ease-in-out infinite;
  }

  @keyframes ellipseRotate {
    0% {
      transform: rotate(-45deg);
    }
    100% {
      transform: rotate(-405deg);
    }
  }

  .circle1,
  .circle2 {
    border-style: solid;
    width: 64px;
    height: 64px;
    border-width: 1px;
    border-color: rgba(0,0,0,.5);
    border-radius: 50%;
    position: absolute;
  }

  .circle1 {
    top: 150px;
    left: 150px;
  }

  .circle2 {
    bottom: 150px;
    right: 130px;
  }

  .circle1::before,
  .circle1::after,
  .circle2::before,
  .circle2::after {
    content: '';
    border-radius: 50%;
    display: inline-block;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .circle1::before,
  .circle2::before {
    width: 12px;
    height: 12px;
    background: #fff;
    z-index: 1;
  }

  .circle1::after,
  .circle2::after {
    width: 40px;
    height: 40px;
    background: #FFEB00;
  }

  .circle1 span,
  .circle2 span {
    position: absolute;
    top: 25px;
    width: 100px;
    font-size: 14px;
  }

  .circle1 span {
    left: 75px;
  }

  .circle2 span {
    left: -90px;
  }

  .overlay {
    position: absolute;
    width: 100%;
    height: 100vh;
    background: #FFEB00;
    top: 0%;
    z-index: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .overlay h1 {
    font-size: 100px;
    letter-spacing: 20px;
  }

  .overlay span {
    font-size: 30px;
    letter-spacing: 3px;
  }

</style>



  <title>Reindeer</title>
</head>

<body>

  <div class="overlay">
    <h1>Reindeer</h1>
    <span>snow life</span>
  </div>

  <div class="wrapper">

    <div class="nav">
      <div class="logo">
        <h1>
          <span>rein <br> deer</span>
          <br>
          snow life
        </h1>
      </div>

      <div class="menu-links">
        <ul>
          <li>home.</li>
          <li>snow life.</li>
          <li>contact.</li>
        </ul>
      </div>

      <div class="scrolldown">scroll</div>
    </div>

    <div class="text">
      <div class="title">reindeer</div>
      <p>Mauris elementum, dui ac sagittis <br> cursus, libero elit sodales odio</p>
    </div>

    <div class="watchnow">
      <i class="fa fa-play"></i>
      <a href="#">watch now!</a>
    </div>

    <div class="media">
      <ul>
        <li><i class="fa fa-facebook"></i></li>
        <li><i class="fa fa-twitter"></i></li>
        <li><i class="fa fa-instagram"></i></li>
      </ul>
    </div>

    <div class="ellipse-container">
      <div class="ellipse thin"></div>
      <div class="ellipse thick"></div>
      <div class="ellipse yellow"></div>
      <div class="circle1"><span>Maecenas purus at</span></div>
      <div class="circle2"><span>Fringilla Maecenas</span></div>
    </div>

  </div>

  <script>

    TweenMax.to(".overlay h1", 2, {
      opacity: 0,
      y: -60,
      ease: Expo.easeInOut
    })

    TweenMax.to(".overlay span", 2, {
      delay: .3,
      opacity: 0,
      y: -60,
      ease: Expo.easeInOut
    })

    TweenMax.to(".overlay", 2, {
      delay: 1,
      top: "-100%",
      ease: Expo.easeInOut
    })

    TweenMax.from(".ellipse-container", 1, {
      delay: 2,
      opacity: 0,
      ease: Expo.easeInOut
    })

    TweenMax.from(".yellow", 1, {
      delay: 3.5,
      opacity: 0,
      ease: Expo.easeInOut
    })

    TweenMax.from(".circle1", 1, {
      delay: 2.4,
      opacity: 0,
      ease: Expo.easeInOut
    })

    TweenMax.from(".circle2", 1, {
      delay: 2.6,
      opacity: 0,
      ease: Expo.easeInOut
    })

    TweenMax.from(".logo", 1, {
      delay: 3,
      opacity: 0,
      y: -100,
      ease: Expo.easeInOut
    })

    TweenMax.staggerFrom(".menu-links ul li", 1, {
      delay: 3.2,
      opacity: 0,
      x: -100,
      ease: Expo.easeInOut
    }, 0.08)

    TweenMax.from(".scrolldown", 1, {
      delay: 3.4,
      opacity: 0,
      y: 100,
      ease: Expo.easeInOut
    })

    TweenMax.from(".text .title", 1, {
      delay: 3,
      opacity: 0,
      x: 200,
      ease: Expo.easeInOut
    })

    TweenMax.from(".text p", 1, {
      delay: 3.2,
      opacity: 0,
      x: 200,
      ease: Expo.easeInOut
    })

    TweenMax.from(".watchnow", 1, {
      delay: 3.4,
      opacity: 0,
      x: 200,
      ease: Expo.easeInOut
    })

    TweenMax.staggerFrom(".media ul li", 1, {
      delay: 3,
      opacity: 0,
      y: 100,
      ease: Expo.easeInOut
    }, 0.08)

  </script>
</body>

</html>