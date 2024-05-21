<!DOCTYPE html>
<html lang="en">

<head>
     <title>MERAJ ABOUT </title>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <meta http-equiv="X-UA-Compatible" content="ie=edge">
     <!-- <link rel="stylesheet" href="css/style.css"> -->
     <link rel="shortcut icon" href="x.ico" type="image/x-icon">
<style>
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:ital@1&display=swap');
@import url('https://fonts.googleapis.com/icon?family=Material+Icons');
@import url('https://fonts.googleapis.com/css2?family=Space+Mono&display=swap');

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

:root {
    -webkit-tap-highlight-color: #0000;
    -webkit-user-select: none; 
    -ms-user-select: none; 
    user-select: none;
}

body {
    background-position: center;
    background-repeat: no-repeat;
    background-size: 100%;
    -webkit-background-size: 100%;
    -moz-background-size: 100%;
    -o-background-size: 100%;
    overflow: hidden;
}

h1:hover {
    cursor: pointer;
    background-color: #e8e1ef;
    color: #100b16;
    border-radius: .25em;
    padding: 1rem 2rem;
    transition: all 300ms linear;
}

#check {
    display: none;
}

#particles-js {
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: #100b16;
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: 50% 50%;
    transition: all .3s;
}

/* .loader {
    position: fixed;
    z-index: 99999;
    background-color: #100b16;
    width: 100vw;
    height: 100vh;
    color: #e8e1ef;
    display: flex;
    opacity: 1;
    justify-content: center;
    align-items: center;
    font-family: 'Space Mono', monospace;
    font-size: 1.25rem;
    transition: all 300ms linear;
} */

.modal{
    position: fixed;
    width: 100%;
    height: 100vh;
    background-color: #000000cc;
    z-index: -1;
    opacity: 0;
    transition: .5s;
    backdrop-filter: blur(5px);
}

.modal img{
    position: absolute;
    top: 25%;
    left: 50%;
    transform: translate(-50%, -50%) scale(.3);
    max-width: 100%;
    max-height: 100%;
    transition: .5s;
    border-radius: 5px;
}

.modal.show{
    opacity: 1;
    z-index: 99;
}

.modal.show img{
    top: 50%;
    transform: translate(-50%, -50%) scale(1);
}

.container {
    font-family: 'Poppins', sans-serif;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    transition: .3s;
}

.card {
    position: relative;
    width: 400px;
    border-radius: 10px;
    overflow: hidden;
    transition: .3s;
    --anim: none;
}

.card:before {
    content: '';
    position: absolute;
    width: 100%;
    height: 270px;
    top: 0;
    left: 0;
    clip-path: circle(400px at 50% -48.5%);
    transition: .3s;
    animation: var(--anim);
}

.header{
    position: relative;
    height: 265px;
    transition: .3s;
}

.mail {
    position: absolute;
    top: 1rem;
    right: 2rem;
    font-size: 1.5rem;
    opacity: .8;
    transition: .3s;
    z-index: 3;
    text-decoration: none;
}

.mail:hover {
    opacity: 1;
    transform: scale(1.07);
}

.hamburger-menu{
    position: relative;
    width: 21px;
    height: 16px;
    top: 1.4rem;
    left: 1.9rem;
    z-index: 3;
    cursor: pointer;
    transition: .3s;
    opacity: .8;
}

.hamburger-menu:hover{
    opacity: 1;
    position: relative;
    width: 25px;
}

.hamburger-menu .center{
    position: relative;
    height: 2px;
    width: 70%;
    top: 50%;
    transform: translateY(-50%);
    border-radius: 1px;
    transition: .3s;
}

.hamburger-menu:before, .hamburger-menu:after{
    content: '';
    position: absolute;
    width: 100%;
    height: 2px;
    border-radius: 1px;
    transition: .3s;
}

.hamburger-menu:before{
    top: 0;
}

.hamburger-menu:after{
    bottom: 0;
}

.main{
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: .3s;
}

.main .image{
    position: relative;
    width: 110px;
    height: 110px;
    border-radius: 50%;
    background: url('1.jpg') no-repeat center / cover;
    margin-bottom: 2px;
    overflow: hidden;
    cursor: pointer;
    transition: border .3s;
}

.image .hover{
    color: #fff;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: .5s;
    opacity: 0;
}

.image:hover .hover {
    opacity: 1;
}

.hover.active {
    opacity: 1;
}

.name {
    color: #fff;
    font-size: 1.2rem;
    font-weight: 500;
    line-height: 1;
    margin: 5px 0;
    transition: .3s;
}

.sub-name {
    color: #fff;
    font-family: 'Titillium Web', sans-serif;
    font-size: 1.2rem;
    opacity: .8;
    transition: .3s;
}

.content {
    display: flex;
    padding: 1.7rem 2.5rem 2.6rem 2.5rem;
    transition: .3s;
}

.right {
    padding-top: 1.5rem;
    display: flex;
    flex-direction: column;
    text-align: right;
    align-items: flex-end;
    justify-content: space-between;
    margin-left: 2.1rem;
    transition: .3s;
}

.number {
    color: #333;
    font-size: 2.1rem;
    font-weight: 200;
    line-height: 1.2;
    transition: .3s;
}

.number-title {
    color: #666;
    font-size: .55rem;
    font-weight: 400;
    line-height: 1;
    letter-spacing: 1px;
    text-transform: uppercase;
    transition: .3s;
}

.title {
    position: relative;
    font-weight: 500;
    font-size: 1.1rem;
    padding: 0 0 3px 0;
    margin-bottom: .9rem;
    display: inline-block;
    transition: .3s;
}

.title:after {
    content: '';
    position: absolute;
    height: 3px;
    width: 50%;
    border-radius: 1.5px;
    bottom: 0;
    left: 0;
}

.text {
    font-weight: 300;
    line-height: 1.7;
    transition: .3s;
}

.icons-container {
    padding: 1rem 0;
    transition: .3s;
}

.icon {
    font-size: 1.3rem;
    text-decoration: none;
    margin-right: 8px;
    transition: .3s;
}

.buttons-wrap {
    display: flex;
    margin-top: 5px;
    transition: .3s;
}

.follow-wrap, .share-wrap {
    flex: 4;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: .3s;
}

.follow-wrap:hover, .share-wrap:hover {
    flex: 5;
}

.follow {
    padding: 9.6px 0;
    width: 100%;
    text-align: center;
    text-decoration: none;
    font-size: .7rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    border-radius: 18.1px;
    margin-right: 3px;
    transition: .3s;
    animation: none;
}

.share {
    padding: 7.6px 0;
    width: 100%;
    text-decoration: none;
    text-align: center;
    font-size: .7rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-left: 3px;
    border-radius: 18.1px;
    transition: .3s;
}

.close {
    position: absolute;
    top: 1rem;
    right: 1rem;
    width: 30px;
    height: 30px;
    cursor: pointer;
    transition: .3s;
}

.close:before, .close:after {
    background-color: #fff;
    content: '';
    position: absolute;
    width: 100%;
    height: 3px;
    border-radius: 1.5px;
    top: 50%;
    left: 50%;
}

.close:before {
    transform: translate(-50%, -50%) rotate(45deg);
}

.close:after {
    transform: translate(-50%, -50%) rotate(135deg);
}

.close:hover {
    opacity: .5;
}

.sidebar {
    position: absolute;
    top: 50px;
    left: 15px;
    width: 45%;
    z-index: 1000;
    display: none;
    backdrop-filter: blur(12.5px);
    border-radius: 10px;
    border: 1px solid #00000025;
    transition: .3s;
}

.sidebar a {
    padding: 10px 15px;
    text-decoration: none;
    justify-content: center;
    display: flex;
    font-family: 'Poppins', sans-serif;
    transition: .3s;
}

.sidebar a:hover {
    transform: scale(1.2);
}

.dark .card {
    background-color: #00000060;
    box-shadow: 0 5px 15px 1px #0001;
    backdrop-filter: blur(10px);
}

.dark .card:before {
    background: #734f96;
}

.dark .mail {
    color: #1b262c;
}

.dark .hamburger-menu .center {
    background-color: #000;
}

.dark .hamburger-menu:before, .dark .hamburger-menu:after {
    background-color: #000;
}

.dark .main .image {
    border: 4px solid #24192f;
}

.dark .image .hover {
    background-color: #734f96a9;
}

.dark .title {
    color: #fff;
}

.dark .title:after {
    background-color: #fff;
}

.dark .text {
    color: #fff;
}

.dark .icon {
    color: #fff;
}

.dark .icon:hover {
    color: #734f96;
}

.dark .follow {
    background: #734f96;
    color: #000;
}

.dark .share {
    border: 2px solid #734f96;
    color: #734f96;
}

.dark .sidebar {
    background-color: #0005;
}

.dark .sidebar a {
    color: #fff;
}

.light .card{
    background-color: #ffffff60;
    box-shadow: 0 5px 15px 1px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(7.5px);
}

.light .card:before {
    background: linear-gradient(to top, #7F00FF, #E100FF);
}

.light .mail {
    color: #fff;
}

.light .hamburger-menu .center {
    background-color: #fff;
}

.light .hamburger-menu:before, .light .hamburger-menu:after {
    background-color: #fff;
}

.light .main .image {
    border: 4px solid #c300ff;
}

.light .image .hover {
    background: #9c00cc69;
}


.light .title {
    color: #555;
}

.light .title:after {
    background-color: #555;
}

.light .text {
    color: #666;
}

.light .icon {
    color: #c4c4c4;
}

.light .icon:hover {
    color: #9D4EDD;
}

.light .follow {
    background: linear-gradient(to right, #7F00FF, #E100FF);
    color: #fff;
}

.light .share {
    border: 2px solid #6200ffc0;
    color: #7F00FF;
}

.light .close:before, .light .close:after {
    background-color: #fff;
}

.light .sidebar a {
   color: #510080;
}

@media (max-width: 410px) {
    .content{
        flex-direction: column;
    }

    .right{
        flex-direction: row;
        text-align: center;
        justify-content: space-around;
        align-items: center;
        margin: 0;
    }
}

@media (max-width: 370px){
    .header{
        height: 230px;
    }

    .card:before{
        clip-path: circle(400px at 50% -74.5%);
        height: 230px;
    }

    .hamburger-menu{
        width: 16px;
        height: 12px;
        top: 1.1rem;
        left: 1.5rem;
    }

    .mail{
        font-size: 1.1rem;
        top: .75rem;
        right: 1.5rem;
    }

    .main .image{
        width: 90px;
        height: 90px;
        border-width: 3px;
    }

    .name, .sub-name{
        font-size: 1rem;
    }

    .content{
        padding: 1.2rem 1.8rem 1.8rem 1.8rem;
    }

    .number{
        font-size: 1.8rem;
    }

    .number-title{
        font-size: .4rem;
    }

    .right{
        padding-top: 1rem;
    }

    .title{
        font-size: .9rem;
        margin-bottom: .5rem;
    }

    .text{
        font-size: .8rem;
    }

    .icons-container{
        padding: .5rem 0;
    }

    .icon{
        font-size: 1.1rem;
    }

    .follow{
        padding: 7.6px 0;
        border-radius: 14.6px;
        font-size: .6rem;
    }

    .share{
        padding: 5.6px 0;
        border-radius: 14.6px;
        font-size: .6rem;
    }
}


.wrapper {
    position: absolute;
    left: 0;
    top: 20px;
    transform: scale(.8);
    margin-left: -75px;
}
.toggle {
    position: relative;
    display: inline-block;
    width: 100px;
    margin-left: 100px;
    padding: 5px;
    border-radius: 40px;
}
.toggle:before, .toggle:after {
    content: '';
    display: block;
}
.toggle:after {
    clear: both;
}
.toggle-bg {
    position: absolute;
    top: -5px;
    left: -5px;
    width: 100%;
    height: 100%;
    background-color: #e7bdffa1;
    border-radius: 40px;
    border: 5px solid #e0aaff;
    transition: all 300ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
    backdrop-filter: blur(2.5px);
    transition: .3s;
}
.toggle-input {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 1px solid red;
    border-radius: 40px;
    z-index: 2;
    opacity: 0;
    transition: .3s;
}
.toggle-switch {
    position: relative;
    width: 40px;
    height: 40px;
    margin-left: 50px;
    background-color: #f5eb42;
    border: 5px solid #e4c74d;
    border-radius: 50%;
    transition: all 300ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
    transform: translate(-4px,-4px);
}
.toggle-switch-figure {
    position: absolute;
    bottom: -15px;
    left: -50px;
    display: block;
    width: 80px;
    height: 30px;
    border: 8px solid #d4d4d2;
    border-radius: 20px;
    background-color: #fff;
    transform: scale(0.4);
    transition: all 300ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
.toggle-switch-figure:after {
    content: '';
    display: block;
    position: relative;
    top: -65px;
    right: -40px;
    width: 15px;
    height: 15px;
    border: 8px solid #d4d4d2;
    border-radius: 100%;
    border-right-color: transparent;
    border-bottom-color: transparent;
    transform: rotateZ(70deg);
    background-color: #fff;
}
.toggle-switch-figure:before {
    content: '';
    display: block;
    position: relative;
    top: -25px;
    right: -15px;
    width: 30px;
    height: 30px;
    border: 8px solid #d4d4d2;
    border-radius: 100%;
    border-right-color: transparent;
    border-bottom-color: transparent;
    transform: rotateZ(30deg);
    background-color: #fff;
}
.toggle-switch-figureAlt {
    content: '';
    position: absolute;
    top: 5px;
    left: 5px;
    width: 2px;
    height: 2px;
    background-color: #efeeda;
    border-radius: 100%;
    border: 4px solid #dee1c5;
    box-shadow: 42px -7px 0 -3px #fcfcfc, 65px -10px 0 -3px #fcfcfc, 54px 4px 0 -2px #fcfcfc, 70px 7px 0 -2px #fcfcfc, 55px 30px 0 -4px #fcfcfc, 44px 20px 0 -2px #fcfcfc, 65px 20px 0 -3px #fcfcfc;
    transition: all 0.12s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    transform: scale(0);
}
.toggle-switch-figureAlt:before {
    content: '';
    position: absolute;
    top: -5px;
    left: 5px;
    width: 10px;
    height: 10px;
    background-color: #efeeda;
    border-radius: 100%;
    border: 2.5px solid #dee1c5;
}
.toggle-switch-figureAlt:after {
    content: '';
    position: absolute;
    top: 10px;
    width: 1.5px;
    height: 1,5px;
    background-color: #efeeda;
    border-radius: 100%;
    border: 2.5px solid #dee1c5;
}
.toggle-input:checked ~ .toggle-switch {
    margin-left: 0;
    border-color: #dee1c5;
    background-color: #fffdf2;
}
.toggle-input:checked ~ .toggle-bg {
    background-color: #2d1f3da1;
    border-color: #231830;
}
.toggle-input:checked ~ .toggle-switch .toggle-switch-figure {
    margin-left: 40px;
    opacity: 0;
    transform: scale(0.1);
}
.toggle-input:checked ~ .toggle-switch .toggle-switch-figureAlt {
    transform: scale(1);
}

@keyframes fadeIn {
    0% {
        opacity: 0; 
        display: none;
    }
    100% {
        opacity: 1;
        display: block;
        z-index: 1000;
    }
  }

@keyframes fadeOut {
    0% { 
        opacity: 1; 
        display: block;
    }
    100% { 
        opacity: 0; 
        display: none;
        z-index: 0;
    }
  }

@keyframes cardDarkGradient {
    0% {
        background-image: linear-gradient(to top, #7F00FF, #E100FF);
    }
    100% {
        background: #734f96;
    }
}

@keyframes cardLightGradient {
    0% {
        background: #734f96;
    }
    100% {
        background-image: linear-gradient(to top, #7F00FF, #E100FF);
    }
}

@keyframes followDarkGradient {
    0% {
        background-image: linear-gradient(to right, #7F00FF, #E100FF);
    }
    100% {
        background: #734f96;
    }
}

@keyframes followLightGradient {
    0% {
        background: #734f96;
    }
    100% {
        background-image: linear-gradient(to right, #7F00FF, #E100FF);
    }
  }
</style>
</head>

<body id="body" class="dark" oncontextmenu="return false">
     <!-- <div class="loader" id="loader">
          <h1 data-value="OreO" id="loader-text">Created by OreO</h1>
     </div> -->
     <div id="particles-js"></div>
<script>
  function hexToRgb(e) {
  var a = /^#?([a-f\d])([a-f\d])([a-f\d])$/i;
  e = e.replace(a, function (e, a, t, i) {
    return a + a + t + t + i + i;
  });
  var t = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(e);
  return t
    ? { r: parseInt(t[1], 16), g: parseInt(t[2], 16), b: parseInt(t[3], 16) }
    : null;
}
function clamp(e, a, t) {
  return Math.min(Math.max(e, a), t);
}
function isInArray(e, a) {
  return a.indexOf(e) > -1;
}
var pJS = function (e, a) {
  var t = document.querySelector("#" + e + " > .particles-js-canvas-el");
  this.pJS = {
    canvas: { el: t, w: t.offsetWidth, h: t.offsetHeight },
    particles: {
      number: { value: 400, density: { enable: !0, value_area: 800 } },
      color: { value: "#fff" },
      shape: {
        type: "circle",
        stroke: { width: 0, color: "#ff0000" },
        polygon: { nb_sides: 5 },
        image: { src: "", width: 100, height: 100 }
      },
      opacity: {
        value: 1,
        random: !1,
        anim: { enable: !1, speed: 2, opacity_min: 0, sync: !1 }
      },
      size: {
        value: 20,
        random: !1,
        anim: { enable: !1, speed: 20, size_min: 0, sync: !1 }
      },
      line_linked: {
        enable: !0,
        distance: 100,
        color: "#fff",
        opacity: 1,
        width: 1
      },
      move: {
        enable: !0,
        speed: 2,
        direction: "none",
        random: !1,
        straight: !1,
        out_mode: "out",
        bounce: !1,
        attract: { enable: !1, rotateX: 3e3, rotateY: 3e3 }
      },
      array: []
    },
    interactivity: {
      detect_on: "canvas",
      events: {
        onhover: { enable: !0, mode: "grab" },
        onclick: { enable: !0, mode: "push" },
        resize: !0
      },
      modes: {
        grab: { distance: 100, line_linked: { opacity: 1 } },
        bubble: { distance: 200, size: 80, duration: 0.4 },
        repulse: { distance: 200, duration: 0.4 },
        push: { particles_nb: 4 },
        remove: { particles_nb: 2 }
      },
      mouse: {}
    },
    retina_detect: !1,
    fn: { interact: {}, modes: {}, vendors: {} },
    tmp: {}
  };
  var i = this.pJS;
  a && Object.deepExtend(i, a),
    (i.tmp.obj = {
      size_value: i.particles.size.value,
      size_anim_speed: i.particles.size.anim.speed,
      move_speed: i.particles.move.speed,
      line_linked_distance: i.particles.line_linked.distance,
      line_linked_width: i.particles.line_linked.width,
      mode_grab_distance: i.interactivity.modes.grab.distance,
      mode_bubble_distance: i.interactivity.modes.bubble.distance,
      mode_bubble_size: i.interactivity.modes.bubble.size,
      mode_repulse_distance: i.interactivity.modes.repulse.distance
    }),
    (i.fn.retinaInit = function () {
      i.retina_detect && window.devicePixelRatio > 1
        ? ((i.canvas.pxratio = window.devicePixelRatio), (i.tmp.retina = !0))
        : ((i.canvas.pxratio = 1), (i.tmp.retina = !1)),
        (i.canvas.w = i.canvas.el.offsetWidth * i.canvas.pxratio),
        (i.canvas.h = i.canvas.el.offsetHeight * i.canvas.pxratio),
        (i.particles.size.value = i.tmp.obj.size_value * i.canvas.pxratio),
        (i.particles.size.anim.speed =
          i.tmp.obj.size_anim_speed * i.canvas.pxratio),
        (i.particles.move.speed = i.tmp.obj.move_speed * i.canvas.pxratio),
        (i.particles.line_linked.distance =
          i.tmp.obj.line_linked_distance * i.canvas.pxratio),
        (i.interactivity.modes.grab.distance =
          i.tmp.obj.mode_grab_distance * i.canvas.pxratio),
        (i.interactivity.modes.bubble.distance =
          i.tmp.obj.mode_bubble_distance * i.canvas.pxratio),
        (i.particles.line_linked.width =
          i.tmp.obj.line_linked_width * i.canvas.pxratio),
        (i.interactivity.modes.bubble.size =
          i.tmp.obj.mode_bubble_size * i.canvas.pxratio),
        (i.interactivity.modes.repulse.distance =
          i.tmp.obj.mode_repulse_distance * i.canvas.pxratio);
    }),
    (i.fn.canvasInit = function () {
      i.canvas.ctx = i.canvas.el.getContext("2d");
    }),
    (i.fn.canvasSize = function () {
      (i.canvas.el.width = i.canvas.w),
        (i.canvas.el.height = i.canvas.h),
        i &&
          i.interactivity.events.resize &&
          window.addEventListener("resize", function () {
            (i.canvas.w = i.canvas.el.offsetWidth),
              (i.canvas.h = i.canvas.el.offsetHeight),
              i.tmp.retina &&
                ((i.canvas.w *= i.canvas.pxratio),
                (i.canvas.h *= i.canvas.pxratio)),
              (i.canvas.el.width = i.canvas.w),
              (i.canvas.el.height = i.canvas.h),
              i.particles.move.enable ||
                (i.fn.particlesEmpty(),
                i.fn.particlesCreate(),
                i.fn.particlesDraw(),
                i.fn.vendors.densityAutoParticles()),
              i.fn.vendors.densityAutoParticles();
          });
    }),
    (i.fn.canvasPaint = function () {
      i.canvas.ctx.fillRect(0, 0, i.canvas.w, i.canvas.h);
    }),
    (i.fn.canvasClear = function () {
      i.canvas.ctx.clearRect(0, 0, i.canvas.w, i.canvas.h);
    }),
    (i.fn.particle = function (e, a, t) {
      if (
        ((this.radius =
          (i.particles.size.random ? Math.random() : 1) *
          i.particles.size.value),
        i.particles.size.anim.enable &&
          ((this.size_status = !1),
          (this.vs = i.particles.size.anim.speed / 100),
          i.particles.size.anim.sync || (this.vs = this.vs * Math.random())),
        (this.x = t ? t.x : Math.random() * i.canvas.w),
        (this.y = t ? t.y : Math.random() * i.canvas.h),
        this.x > i.canvas.w - 2 * this.radius
          ? (this.x = this.x - this.radius)
          : this.x < 2 * this.radius && (this.x = this.x + this.radius),
        this.y > i.canvas.h - 2 * this.radius
          ? (this.y = this.y - this.radius)
          : this.y < 2 * this.radius && (this.y = this.y + this.radius),
        i.particles.move.bounce && i.fn.vendors.checkOverlap(this, t),
        (this.color = {}),
        "object" == typeof e.value)
      )
        if (e.value instanceof Array) {
          var s =
            e.value[Math.floor(Math.random() * i.particles.color.value.length)];
          this.color.rgb = hexToRgb(s);
        } else
          void 0 != e.value.r &&
            void 0 != e.value.g &&
            void 0 != e.value.b &&
            (this.color.rgb = { r: e.value.r, g: e.value.g, b: e.value.b }),
            void 0 != e.value.h &&
              void 0 != e.value.s &&
              void 0 != e.value.l &&
              (this.color.hsl = { h: e.value.h, s: e.value.s, l: e.value.l });
      else
        "random" == e.value
          ? (this.color.rgb = {
              r: Math.floor(256 * Math.random()) + 0,
              g: Math.floor(256 * Math.random()) + 0,
              b: Math.floor(256 * Math.random()) + 0
            })
          : "string" == typeof e.value &&
            ((this.color = e), (this.color.rgb = hexToRgb(this.color.value)));
      (this.opacity =
        (i.particles.opacity.random ? Math.random() : 1) *
        i.particles.opacity.value),
        i.particles.opacity.anim.enable &&
          ((this.opacity_status = !1),
          (this.vo = i.particles.opacity.anim.speed / 100),
          i.particles.opacity.anim.sync || (this.vo = this.vo * Math.random()));
      var n = {};
      switch (i.particles.move.direction) {
        case "top":
          n = { x: 0, y: -1 };
          break;
        case "top-right":
          n = { x: 0.5, y: -0.5 };
          break;
        case "right":
          n = { x: 1, y: -0 };
          break;
        case "bottom-right":
          n = { x: 0.5, y: 0.5 };
          break;
        case "bottom":
          n = { x: 0, y: 1 };
          break;
        case "bottom-left":
          n = { x: -0.5, y: 1 };
          break;
        case "left":
          n = { x: -1, y: 0 };
          break;
        case "top-left":
          n = { x: -0.5, y: -0.5 };
          break;
        default:
          n = { x: 0, y: 0 };
      }
      i.particles.move.straight
        ? ((this.vx = n.x),
          (this.vy = n.y),
          i.particles.move.random &&
            ((this.vx = this.vx * Math.random()),
            (this.vy = this.vy * Math.random())))
        : ((this.vx = n.x + Math.random() - 0.5),
          (this.vy = n.y + Math.random() - 0.5)),
        (this.vx_i = this.vx),
        (this.vy_i = this.vy);
      var r = i.particles.shape.type;
      if ("object" == typeof r) {
        if (r instanceof Array) {
          var c = r[Math.floor(Math.random() * r.length)];
          this.shape = c;
        }
      } else this.shape = r;
      if ("image" == this.shape) {
        var o = i.particles.shape;
        (this.img = {
          src: o.image.src,
          ratio: o.image.width / o.image.height
        }),
          this.img.ratio || (this.img.ratio = 1),
          "svg" == i.tmp.img_type &&
            void 0 != i.tmp.source_svg &&
            (i.fn.vendors.createSvgImg(this),
            i.tmp.pushing && (this.img.loaded = !1));
      }
    }),
    (i.fn.particle.prototype.draw = function () {
      function e() {
        i.canvas.ctx.drawImage(
          r,
          a.x - t,
          a.y - t,
          2 * t,
          (2 * t) / a.img.ratio
        );
      }
      var a = this;
      if (void 0 != a.radius_bubble) var t = a.radius_bubble;
      else var t = a.radius;
      if (void 0 != a.opacity_bubble) var s = a.opacity_bubble;
      else var s = a.opacity;
      if (a.color.rgb)
        var n =
          "rgba(" +
          a.color.rgb.r +
          "," +
          a.color.rgb.g +
          "," +
          a.color.rgb.b +
          "," +
          s +
          ")";
      else
        var n =
          "hsla(" +
          a.color.hsl.h +
          "," +
          a.color.hsl.s +
          "%," +
          a.color.hsl.l +
          "%," +
          s +
          ")";
      switch (
        ((i.canvas.ctx.fillStyle = n), i.canvas.ctx.beginPath(), a.shape)
      ) {
        case "circle":
          i.canvas.ctx.arc(a.x, a.y, t, 0, 2 * Math.PI, !1);
          break;
        case "edge":
          i.canvas.ctx.rect(a.x - t, a.y - t, 2 * t, 2 * t);
          break;
        case "triangle":
          i.fn.vendors.drawShape(
            i.canvas.ctx,
            a.x - t,
            a.y + t / 1.66,
            2 * t,
            3,
            2
          );
          break;
        case "polygon":
          i.fn.vendors.drawShape(
            i.canvas.ctx,
            a.x - t / (i.particles.shape.polygon.nb_sides / 3.5),
            a.y - t / 0.76,
            (2.66 * t) / (i.particles.shape.polygon.nb_sides / 3),
            i.particles.shape.polygon.nb_sides,
            1
          );
          break;
        case "star":
          i.fn.vendors.drawShape(
            i.canvas.ctx,
            a.x - (2 * t) / (i.particles.shape.polygon.nb_sides / 4),
            a.y - t / 1.52,
            (2 * t * 2.66) / (i.particles.shape.polygon.nb_sides / 3),
            i.particles.shape.polygon.nb_sides,
            2
          );
          break;
        case "image":
          if ("svg" == i.tmp.img_type) var r = a.img.obj;
          else var r = i.tmp.img_obj;
          r && e();
      }
      i.canvas.ctx.closePath(),
        i.particles.shape.stroke.width > 0 &&
          ((i.canvas.ctx.strokeStyle = i.particles.shape.stroke.color),
          (i.canvas.ctx.lineWidth = i.particles.shape.stroke.width),
          i.canvas.ctx.stroke()),
        i.canvas.ctx.fill();
    }),
    (i.fn.particlesCreate = function () {
      for (var e = 0; e < i.particles.number.value; e++)
        i.particles.array.push(
          new i.fn.particle(i.particles.color, i.particles.opacity.value)
        );
    }),
    (i.fn.particlesUpdate = function () {
      for (var e = 0; e < i.particles.array.length; e++) {
        var a = i.particles.array[e];
        if (i.particles.move.enable) {
          var t = i.particles.move.speed / 2;
          (a.x += a.vx * t), (a.y += a.vy * t);
        }
        if (
          (i.particles.opacity.anim.enable &&
            (1 == a.opacity_status
              ? (a.opacity >= i.particles.opacity.value &&
                  (a.opacity_status = !1),
                (a.opacity += a.vo))
              : (a.opacity <= i.particles.opacity.anim.opacity_min &&
                  (a.opacity_status = !0),
                (a.opacity -= a.vo)),
            a.opacity < 0 && (a.opacity = 0)),
          i.particles.size.anim.enable &&
            (1 == a.size_status
              ? (a.radius >= i.particles.size.value && (a.size_status = !1),
                (a.radius += a.vs))
              : (a.radius <= i.particles.size.anim.size_min &&
                  (a.size_status = !0),
                (a.radius -= a.vs)),
            a.radius < 0 && (a.radius = 0)),
          "bounce" == i.particles.move.out_mode)
        )
          var s = {
            x_left: a.radius,
            x_right: i.canvas.w,
            y_top: a.radius,
            y_bottom: i.canvas.h
          };
        else
          var s = {
            x_left: -a.radius,
            x_right: i.canvas.w + a.radius,
            y_top: -a.radius,
            y_bottom: i.canvas.h + a.radius
          };
        switch (
          (a.x - a.radius > i.canvas.w
            ? ((a.x = s.x_left), (a.y = Math.random() * i.canvas.h))
            : a.x + a.radius < 0 &&
              ((a.x = s.x_right), (a.y = Math.random() * i.canvas.h)),
          a.y - a.radius > i.canvas.h
            ? ((a.y = s.y_top), (a.x = Math.random() * i.canvas.w))
            : a.y + a.radius < 0 &&
              ((a.y = s.y_bottom), (a.x = Math.random() * i.canvas.w)),
          i.particles.move.out_mode)
        ) {
          case "bounce":
            a.x + a.radius > i.canvas.w
              ? (a.vx = -a.vx)
              : a.x - a.radius < 0 && (a.vx = -a.vx),
              a.y + a.radius > i.canvas.h
                ? (a.vy = -a.vy)
                : a.y - a.radius < 0 && (a.vy = -a.vy);
        }
        if (
          (isInArray("grab", i.interactivity.events.onhover.mode) &&
            i.fn.modes.grabParticle(a),
          (isInArray("bubble", i.interactivity.events.onhover.mode) ||
            isInArray("bubble", i.interactivity.events.onclick.mode)) &&
            i.fn.modes.bubbleParticle(a),
          (isInArray("repulse", i.interactivity.events.onhover.mode) ||
            isInArray("repulse", i.interactivity.events.onclick.mode)) &&
            i.fn.modes.repulseParticle(a),
          i.particles.line_linked.enable || i.particles.move.attract.enable)
        )
          for (var n = e + 1; n < i.particles.array.length; n++) {
            var r = i.particles.array[n];
            i.particles.line_linked.enable && i.fn.interact.linkParticles(a, r),
              i.particles.move.attract.enable &&
                i.fn.interact.attractParticles(a, r),
              i.particles.move.bounce && i.fn.interact.bounceParticles(a, r);
          }
      }
    }),
    (i.fn.particlesDraw = function () {
      i.canvas.ctx.clearRect(0, 0, i.canvas.w, i.canvas.h),
        i.fn.particlesUpdate();
      for (var e = 0; e < i.particles.array.length; e++) {
        var a = i.particles.array[e];
        a.draw();
      }
    }),
    (i.fn.particlesEmpty = function () {
      i.particles.array = [];
    }),
    (i.fn.particlesRefresh = function () {
      cancelRequestAnimFrame(i.fn.checkAnimFrame),
        cancelRequestAnimFrame(i.fn.drawAnimFrame),
        (i.tmp.source_svg = void 0),
        (i.tmp.img_obj = void 0),
        (i.tmp.count_svg = 0),
        i.fn.particlesEmpty(),
        i.fn.canvasClear(),
        i.fn.vendors.start();
    }),
    (i.fn.interact.linkParticles = function (e, a) {
      var t = e.x - a.x,
        s = e.y - a.y,
        n = Math.sqrt(t * t + s * s);
      if (n <= i.particles.line_linked.distance) {
        var r =
          i.particles.line_linked.opacity -
          n /
            (1 / i.particles.line_linked.opacity) /
            i.particles.line_linked.distance;
        if (r > 0) {
          var c = i.particles.line_linked.color_rgb_line;
          (i.canvas.ctx.strokeStyle =
            "rgba(" + c.r + "," + c.g + "," + c.b + "," + r + ")"),
            (i.canvas.ctx.lineWidth = i.particles.line_linked.width),
            i.canvas.ctx.beginPath(),
            i.canvas.ctx.moveTo(e.x, e.y),
            i.canvas.ctx.lineTo(a.x, a.y),
            i.canvas.ctx.stroke(),
            i.canvas.ctx.closePath();
        }
      }
    }),
    (i.fn.interact.attractParticles = function (e, a) {
      var t = e.x - a.x,
        s = e.y - a.y,
        n = Math.sqrt(t * t + s * s);
      if (n <= i.particles.line_linked.distance) {
        var r = t / (1e3 * i.particles.move.attract.rotateX),
          c = s / (1e3 * i.particles.move.attract.rotateY);
        (e.vx -= r), (e.vy -= c), (a.vx += r), (a.vy += c);
      }
    }),
    (i.fn.interact.bounceParticles = function (e, a) {
      var t = e.x - a.x,
        i = e.y - a.y,
        s = Math.sqrt(t * t + i * i),
        n = e.radius + a.radius;
      n >= s &&
        ((e.vx = -e.vx), (e.vy = -e.vy), (a.vx = -a.vx), (a.vy = -a.vy));
    }),
    (i.fn.modes.pushParticles = function (e, a) {
      i.tmp.pushing = !0;
      for (var t = 0; e > t; t++)
        i.particles.array.push(
          new i.fn.particle(i.particles.color, i.particles.opacity.value, {
            x: a ? a.pos_x : Math.random() * i.canvas.w,
            y: a ? a.pos_y : Math.random() * i.canvas.h
          })
        ),
          t == e - 1 &&
            (i.particles.move.enable || i.fn.particlesDraw(),
            (i.tmp.pushing = !1));
    }),
    (i.fn.modes.removeParticles = function (e) {
      i.particles.array.splice(0, e),
        i.particles.move.enable || i.fn.particlesDraw();
    }),
    (i.fn.modes.bubbleParticle = function (e) {
      function a() {
        (e.opacity_bubble = e.opacity), (e.radius_bubble = e.radius);
      }
      function t(a, t, s, n, c) {
        if (a != t)
          if (i.tmp.bubble_duration_end) {
            if (void 0 != s) {
              var o = n - (p * (n - a)) / i.interactivity.modes.bubble.duration,
                l = a - o;
              (d = a + l),
                "size" == c && (e.radius_bubble = d),
                "opacity" == c && (e.opacity_bubble = d);
            }
          } else if (r <= i.interactivity.modes.bubble.distance) {
            if (void 0 != s) var v = s;
            else var v = n;
            if (v != a) {
              var d = n - (p * (n - a)) / i.interactivity.modes.bubble.duration;
              "size" == c && (e.radius_bubble = d),
                "opacity" == c && (e.opacity_bubble = d);
            }
          } else
            "size" == c && (e.radius_bubble = void 0),
              "opacity" == c && (e.opacity_bubble = void 0);
      }
      if (
        i.interactivity.events.onhover.enable &&
        isInArray("bubble", i.interactivity.events.onhover.mode)
      ) {
        var s = e.x - i.interactivity.mouse.pos_x,
          n = e.y - i.interactivity.mouse.pos_y,
          r = Math.sqrt(s * s + n * n),
          c = 1 - r / i.interactivity.modes.bubble.distance;
        if (r <= i.interactivity.modes.bubble.distance) {
          if (c >= 0 && "mousemove" == i.interactivity.status) {
            if (i.interactivity.modes.bubble.size != i.particles.size.value)
              if (i.interactivity.modes.bubble.size > i.particles.size.value) {
                var o = e.radius + i.interactivity.modes.bubble.size * c;
                o >= 0 && (e.radius_bubble = o);
              } else {
                var l = e.radius - i.interactivity.modes.bubble.size,
                  o = e.radius - l * c;
                o > 0 ? (e.radius_bubble = o) : (e.radius_bubble = 0);
              }
            if (
              i.interactivity.modes.bubble.opacity != i.particles.opacity.value
            )
              if (
                i.interactivity.modes.bubble.opacity > i.particles.opacity.value
              ) {
                var v = i.interactivity.modes.bubble.opacity * c;
                v > e.opacity &&
                  v <= i.interactivity.modes.bubble.opacity &&
                  (e.opacity_bubble = v);
              } else {
                var v =
                  e.opacity -
                  (i.particles.opacity.value -
                    i.interactivity.modes.bubble.opacity) *
                    c;
                v < e.opacity &&
                  v >= i.interactivity.modes.bubble.opacity &&
                  (e.opacity_bubble = v);
              }
          }
        } else a();
        "mouseleave" == i.interactivity.status && a();
      } else if (
        i.interactivity.events.onclick.enable &&
        isInArray("bubble", i.interactivity.events.onclick.mode)
      ) {
        if (i.tmp.bubble_clicking) {
          var s = e.x - i.interactivity.mouse.click_pos_x,
            n = e.y - i.interactivity.mouse.click_pos_y,
            r = Math.sqrt(s * s + n * n),
            p = (new Date().getTime() - i.interactivity.mouse.click_time) / 1e3;
          p > i.interactivity.modes.bubble.duration &&
            (i.tmp.bubble_duration_end = !0),
            p > 2 * i.interactivity.modes.bubble.duration &&
              ((i.tmp.bubble_clicking = !1), (i.tmp.bubble_duration_end = !1));
        }
        i.tmp.bubble_clicking &&
          (t(
            i.interactivity.modes.bubble.size,
            i.particles.size.value,
            e.radius_bubble,
            e.radius,
            "size"
          ),
          t(
            i.interactivity.modes.bubble.opacity,
            i.particles.opacity.value,
            e.opacity_bubble,
            e.opacity,
            "opacity"
          ));
      }
    }),
    (i.fn.modes.repulseParticle = function (e) {
      function a() {
        var a = Math.atan2(d, p);
        if (
          ((e.vx = u * Math.cos(a)),
          (e.vy = u * Math.sin(a)),
          "bounce" == i.particles.move.out_mode)
        ) {
          var t = { x: e.x + e.vx, y: e.y + e.vy };
          t.x + e.radius > i.canvas.w
            ? (e.vx = -e.vx)
            : t.x - e.radius < 0 && (e.vx = -e.vx),
            t.y + e.radius > i.canvas.h
              ? (e.vy = -e.vy)
              : t.y - e.radius < 0 && (e.vy = -e.vy);
        }
      }
      if (
        i.interactivity.events.onhover.enable &&
        isInArray("repulse", i.interactivity.events.onhover.mode) &&
        "mousemove" == i.interactivity.status
      ) {
        var t = e.x - i.interactivity.mouse.pos_x,
          s = e.y - i.interactivity.mouse.pos_y,
          n = Math.sqrt(t * t + s * s),
          r = { x: t / n, y: s / n },
          c = i.interactivity.modes.repulse.distance,
          o = 100,
          l = clamp((1 / c) * (-1 * Math.pow(n / c, 2) + 1) * c * o, 0, 50),
          v = { x: e.x + r.x * l, y: e.y + r.y * l };
        "bounce" == i.particles.move.out_mode
          ? (v.x - e.radius > 0 && v.x + e.radius < i.canvas.w && (e.x = v.x),
            v.y - e.radius > 0 && v.y + e.radius < i.canvas.h && (e.y = v.y))
          : ((e.x = v.x), (e.y = v.y));
      } else if (
        i.interactivity.events.onclick.enable &&
        isInArray("repulse", i.interactivity.events.onclick.mode)
      )
        if (
          (i.tmp.repulse_finish ||
            (i.tmp.repulse_count++,
            i.tmp.repulse_count == i.particles.array.length &&
              (i.tmp.repulse_finish = !0)),
          i.tmp.repulse_clicking)
        ) {
          var c = Math.pow(i.interactivity.modes.repulse.distance / 6, 3),
            p = i.interactivity.mouse.click_pos_x - e.x,
            d = i.interactivity.mouse.click_pos_y - e.y,
            m = p * p + d * d,
            u = (-c / m) * 1;
          c >= m && a();
        } else
          0 == i.tmp.repulse_clicking && ((e.vx = e.vx_i), (e.vy = e.vy_i));
    }),
    (i.fn.modes.grabParticle = function (e) {
      if (
        i.interactivity.events.onhover.enable &&
        "mousemove" == i.interactivity.status
      ) {
        var a = e.x - i.interactivity.mouse.pos_x,
          t = e.y - i.interactivity.mouse.pos_y,
          s = Math.sqrt(a * a + t * t);
        if (s <= i.interactivity.modes.grab.distance) {
          var n =
            i.interactivity.modes.grab.line_linked.opacity -
            s /
              (1 / i.interactivity.modes.grab.line_linked.opacity) /
              i.interactivity.modes.grab.distance;
          if (n > 0) {
            var r = i.particles.line_linked.color_rgb_line;
            (i.canvas.ctx.strokeStyle =
              "rgba(" + r.r + "," + r.g + "," + r.b + "," + n + ")"),
              (i.canvas.ctx.lineWidth = i.particles.line_linked.width),
              i.canvas.ctx.beginPath(),
              i.canvas.ctx.moveTo(e.x, e.y),
              i.canvas.ctx.lineTo(
                i.interactivity.mouse.pos_x,
                i.interactivity.mouse.pos_y
              ),
              i.canvas.ctx.stroke(),
              i.canvas.ctx.closePath();
          }
        }
      }
    }),
    (i.fn.vendors.eventsListeners = function () {
      "window" == i.interactivity.detect_on
        ? (i.interactivity.el = window)
        : (i.interactivity.el = i.canvas.el),
        (i.interactivity.events.onhover.enable ||
          i.interactivity.events.onclick.enable) &&
          (i.interactivity.el.addEventListener("mousemove", function (e) {
            if (i.interactivity.el == window)
              var a = e.clientX,
                t = e.clientY;
            else
              var a = e.offsetX || e.clientX,
                t = e.offsetY || e.clientY;
            (i.interactivity.mouse.pos_x = a),
              (i.interactivity.mouse.pos_y = t),
              i.tmp.retina &&
                ((i.interactivity.mouse.pos_x *= i.canvas.pxratio),
                (i.interactivity.mouse.pos_y *= i.canvas.pxratio)),
              (i.interactivity.status = "mousemove");
          }),
          i.interactivity.el.addEventListener("mouseleave", function (e) {
            (i.interactivity.mouse.pos_x = null),
              (i.interactivity.mouse.pos_y = null),
              (i.interactivity.status = "mouseleave");
          })),
        i.interactivity.events.onclick.enable &&
          i.interactivity.el.addEventListener("click", function () {
            if (
              ((i.interactivity.mouse.click_pos_x =
                i.interactivity.mouse.pos_x),
              (i.interactivity.mouse.click_pos_y = i.interactivity.mouse.pos_y),
              (i.interactivity.mouse.click_time = new Date().getTime()),
              i.interactivity.events.onclick.enable)
            )
              switch (i.interactivity.events.onclick.mode) {
                case "push":
                  i.particles.move.enable
                    ? i.fn.modes.pushParticles(
                        i.interactivity.modes.push.particles_nb,
                        i.interactivity.mouse
                      )
                    : 1 == i.interactivity.modes.push.particles_nb
                    ? i.fn.modes.pushParticles(
                        i.interactivity.modes.push.particles_nb,
                        i.interactivity.mouse
                      )
                    : i.interactivity.modes.push.particles_nb > 1 &&
                      i.fn.modes.pushParticles(
                        i.interactivity.modes.push.particles_nb
                      );
                  break;
                case "remove":
                  i.fn.modes.removeParticles(
                    i.interactivity.modes.remove.particles_nb
                  );
                  break;
                case "bubble":
                  i.tmp.bubble_clicking = !0;
                  break;
                case "repulse":
                  (i.tmp.repulse_clicking = !0),
                    (i.tmp.repulse_count = 0),
                    (i.tmp.repulse_finish = !1),
                    setTimeout(function () {
                      i.tmp.repulse_clicking = !1;
                    }, 1e3 * i.interactivity.modes.repulse.duration);
              }
          });
    }),
    (i.fn.vendors.densityAutoParticles = function () {
      if (i.particles.number.density.enable) {
        var e = (i.canvas.el.width * i.canvas.el.height) / 1e3;
        i.tmp.retina && (e /= 2 * i.canvas.pxratio);
        var a =
            (e * i.particles.number.value) /
            i.particles.number.density.value_area,
          t = i.particles.array.length - a;
        0 > t
          ? i.fn.modes.pushParticles(Math.abs(t))
          : i.fn.modes.removeParticles(t);
      }
    }),
    (i.fn.vendors.checkOverlap = function (e, a) {
      for (var t = 0; t < i.particles.array.length; t++) {
        var s = i.particles.array[t],
          n = e.x - s.x,
          r = e.y - s.y,
          c = Math.sqrt(n * n + r * r);
        c <= e.radius + s.radius &&
          ((e.x = a ? a.x : Math.random() * i.canvas.w),
          (e.y = a ? a.y : Math.random() * i.canvas.h),
          i.fn.vendors.checkOverlap(e));
      }
    }),
    (i.fn.vendors.createSvgImg = function (e) {
      var a = i.tmp.source_svg,
        t = /#([0-9A-F]{3,6})/gi,
        s = a.replace(t, function (a, t, i, s) {
          if (e.color.rgb)
            var n =
              "rgba(" +
              e.color.rgb.r +
              "," +
              e.color.rgb.g +
              "," +
              e.color.rgb.b +
              "," +
              e.opacity +
              ")";
          else
            var n =
              "hsla(" +
              e.color.hsl.h +
              "," +
              e.color.hsl.s +
              "%," +
              e.color.hsl.l +
              "%," +
              e.opacity +
              ")";
          return n;
        }),
        n = new Blob([s], { type: "image/svg+xml;charset=utf-8" }),
        r = window.URL || window.webkitURL || window,
        c = r.createObjectURL(n),
        o = new Image();
      o.addEventListener("load", function () {
        (e.img.obj = o),
          (e.img.loaded = !0),
          r.revokeObjectURL(c),
          i.tmp.count_svg++;
      }),
        (o.src = c);
    }),
    (i.fn.vendors.destroypJS = function () {
      cancelAnimationFrame(i.fn.drawAnimFrame), t.remove(), (pJSDom = null);
    }),
    (i.fn.vendors.drawShape = function (e, a, t, i, s, n) {
      var r = s * n,
        c = s / n,
        o = (180 * (c - 2)) / c,
        l = Math.PI - (Math.PI * o) / 180;
      e.save(), e.beginPath(), e.translate(a, t), e.moveTo(0, 0);
      for (var v = 0; r > v; v++)
        e.lineTo(i, 0), e.translate(i, 0), e.rotate(l);
      e.fill(), e.restore();
    }),
    (i.fn.vendors.exportImg = function () {
      window.open(i.canvas.el.toDataURL("image/png"), "_blank");
    }),
    (i.fn.vendors.loadImg = function (e) {
      if (((i.tmp.img_error = void 0), "" != i.particles.shape.image.src))
        if ("svg" == e) {
          var a = new XMLHttpRequest();
          a.open("GET", i.particles.shape.image.src),
            (a.onreadystatechange = function (e) {
              4 == a.readyState &&
                (200 == a.status
                  ? ((i.tmp.source_svg = e.currentTarget.response),
                    i.fn.vendors.checkBeforeDraw())
                  : (console.log("Error pJS - Image not found"),
                    (i.tmp.img_error = !0)));
            }),
            a.send();
        } else {
          var t = new Image();
          t.addEventListener("load", function () {
            (i.tmp.img_obj = t), i.fn.vendors.checkBeforeDraw();
          }),
            (t.src = i.particles.shape.image.src);
        }
      else console.log("Error pJS - No image.src"), (i.tmp.img_error = !0);
    }),
    (i.fn.vendors.draw = function () {
      "image" == i.particles.shape.type
        ? "svg" == i.tmp.img_type
          ? i.tmp.count_svg >= i.particles.number.value
            ? (i.fn.particlesDraw(),
              i.particles.move.enable
                ? (i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw))
                : cancelRequestAnimFrame(i.fn.drawAnimFrame))
            : i.tmp.img_error ||
              (i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw))
          : void 0 != i.tmp.img_obj
          ? (i.fn.particlesDraw(),
            i.particles.move.enable
              ? (i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw))
              : cancelRequestAnimFrame(i.fn.drawAnimFrame))
          : i.tmp.img_error ||
            (i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw))
        : (i.fn.particlesDraw(),
          i.particles.move.enable
            ? (i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw))
            : cancelRequestAnimFrame(i.fn.drawAnimFrame));
    }),
    (i.fn.vendors.checkBeforeDraw = function () {
      "image" == i.particles.shape.type
        ? "svg" == i.tmp.img_type && void 0 == i.tmp.source_svg
          ? (i.tmp.checkAnimFrame = requestAnimFrame(check))
          : (cancelRequestAnimFrame(i.tmp.checkAnimFrame),
            i.tmp.img_error || (i.fn.vendors.init(), i.fn.vendors.draw()))
        : (i.fn.vendors.init(), i.fn.vendors.draw());
    }),
    (i.fn.vendors.init = function () {
      i.fn.retinaInit(),
        i.fn.canvasInit(),
        i.fn.canvasSize(),
        i.fn.canvasPaint(),
        i.fn.particlesCreate(),
        i.fn.vendors.densityAutoParticles(),
        (i.particles.line_linked.color_rgb_line = hexToRgb(
          i.particles.line_linked.color
        ));
    }),
    (i.fn.vendors.start = function () {
      isInArray("image", i.particles.shape.type)
        ? ((i.tmp.img_type = i.particles.shape.image.src.substr(
            i.particles.shape.image.src.length - 3
          )),
          i.fn.vendors.loadImg(i.tmp.img_type))
        : i.fn.vendors.checkBeforeDraw();
    }),
    i.fn.vendors.eventsListeners(),
    i.fn.vendors.start();
};
(Object.deepExtend = function (e, a) {
  for (var t in a)
    a[t] && a[t].constructor && a[t].constructor === Object
      ? ((e[t] = e[t] || {}), arguments.callee(e[t], a[t]))
      : (e[t] = a[t]);
  return e;
}),
  (window.requestAnimFrame = (function () {
    return (
      window.requestAnimationFrame ||
      window.webkitRequestAnimationFrame ||
      window.mozRequestAnimationFrame ||
      window.oRequestAnimationFrame ||
      window.msRequestAnimationFrame ||
      function (e) {
        window.setTimeout(e, 1e3 / 60);
      }
    );
  })()),
  (window.cancelRequestAnimFrame = (function () {
    return (
      window.cancelAnimationFrame ||
      window.webkitCancelRequestAnimationFrame ||
      window.mozCancelRequestAnimationFrame ||
      window.oCancelRequestAnimationFrame ||
      window.msCancelRequestAnimationFrame ||
      clearTimeout
    );
  })()),
  (window.pJSDom = []),
  (window.particlesJS = function (e, a) {
    "string" != typeof e && ((a = e), (e = "particles-js")),
      e || (e = "particles-js");
    var t = document.getElementById(e),
      i = "particles-js-canvas-el",
      s = t.getElementsByClassName(i);
    if (s.length) for (; s.length > 0; ) t.removeChild(s[0]);
    var n = document.createElement("canvas");
    (n.className = i), (n.style.width = "100%"), (n.style.height = "100%");
    var r = document.getElementById(e).appendChild(n);
    null != r && pJSDom.push(new pJS(e, a));
  }),
  (window.particlesJS.load = function (e, a, t) {
    var i = new XMLHttpRequest();
    i.open("GET", a),
      (i.onreadystatechange = function (a) {
        if (4 == i.readyState)
          if (200 == i.status) {
            var s = JSON.parse(a.currentTarget.response);
            window.particlesJS(e, s), t && t();
          } else
            console.log("Error pJS - XMLHttpRequest status: " + i.status),
              console.log("Error pJS - File config not found");
      }),
      i.send();
  });
</script>
     <div class="wrapper">
          <div class="toggle">
               <input class="toggle-input" type="checkbox">
               <div class="toggle-bg"></div>
               <div class="toggle-switch">
                    <div class="toggle-switch-figure"></div>
                    <div class="toggle-switch-figureAlt"></div>
               </div>
          </div>
     </div>

     <div class="modal">
          <img src="1.jpg" alt="Eren">
          <div class="close"></div>
     </div>

     <div id="container" class="container">
          <input type="checkbox" name="" id="check">
          <div class="card">
               <div class="sidebar" id="sidebar">
                    <a class="active" href="https://github.com/MERAJ29" target="_blank">Github</a>
                    <a class="active" href="https://https://www.instagram.com/official_meraj0.99?igsh=NWx5YnJ2amc3enVw==" target="_blank">Instagram</a>
                    <a class="active" href="#" target="_blank">YouTube</a>
                    <a class="active" href=["](https://www.instagram.com/official_meraj0.99?igsh=NWx5YnJ2amc3enVw)" target="_blank">Telegram</a>
               </div>
               <div class="header" onclick="toggle()">
                    <label for="check" class="checkbtn" id="chkbtn">
                         <div class="hamburger-menu">
                              <div class="center"></div>
                         </div>
                    </label>
                    <a href="mailto:carvefern.com@gmail.com" class="mail">
                         <i class="fa-regular fa-envelope"></i>
                    </a>
                    <div class="main">
                         <div class="image">
                              <div class="hover">
                                   <i class="fa-solid fa-user fa-2xl"></i>
                              </div>
                         </div>
                         <h3 class="name"></h3>
                         <h3 class="sub-name">• 【O】【m】【k】【a】【r】• </h3>
                    </div>
               </div>

               <div class="content">
                    <div class="left">
                         <div class="about-container">
                              <h3 class="title">About</h3>
                              <p class="text">✦ Cʟᴧss: 𝐂𝐈𝐕𝐈𝐋 𝐄𝐍𝐍𝐆 | Sᴄʜᴏᴏʟ: 𝐆𝐏𝐂 ✦</p>
                              <p class="text">~ Dᴇᴠ ~</p>
                              <p class="text">• 𝐇𝐀𝐂𝐊𝐈𝐍𝐆 |𝐕𝐈𝐃𝐄𝐎 𝐄𝐃𝐈𝐓𝐈𝐍𝐆|𝐇𝐓𝐌𝐋|•</p>
                         </div>
                         <div class="icons-container">
                              <a href="https://github.com/Omkarsharma30" class="icon">
                                   <i class="fa-brands fa-github"></i>
                              </a>
                              <a href="https://www.instagram.com/omkar.sharma_?igsh=MWs1cXF6OTJycGJ6ag==" class="icon">
                                   <i class="fa-brands fa-instagram"></i>
                              </a>
                              <a href="https://telegram.dog/Badhacker68" class="icon">
                                   <i class="fa-brands fa-telegram"></i>
                              </a>
                              <a href="#" class="icon">
                                   <i class="fa-brands fa-youtube"></i>
                              </a>
                         </div>
                         <div class="buttons-wrap">
                              <div class="follow-wrap">
                                   <a href="https://t.me/ethicalhackING34" class="follow">Follow</a>
                              </div>
                              <div class="share-wrap">
                                   <a href="https://telegram.dog/Badhacker68" class="share">Contact</a>
                              </div>
                         </div>
                    </div>
               </div>
          </div>
     </div>

     <script>
          document.onkeydown = function (e) {
               if (event.keyCode == 123) {
                    return false;
               }
               if (e.ctrlKey && e.shiftKey && e.keyCode == 'I'.charCodeAt(0)) {
                    return false;
               }
               if (e.ctrlKey && e.shiftKey && e.keyCode == 'C'.charCodeAt(0)) {
                    return false;
               }
               if (e.ctrlKey && e.shiftKey && e.keyCode == 'J'.charCodeAt(0)) {
                    return false;
               }
               if (e.ctrlKey && e.keyCode == 'U'.charCodeAt(0)) {
                    return false;
               }
          }
     </script>
<script>
const image = document.querySelector(".image"),
  hover = document.querySelector(".hover"),
  modal = document.querySelector(".modal"),
  close = document.querySelector(".close"),
  follow = document.querySelector(".follow"),
  card = document.querySelector(".card"),
  loader = document.getElementById("loader"),
  loaderText = document.getElementById("loader-text");
function load() {
  const e = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz1234567890";
  let t = null,
    a = 0;
  const o = loaderText.dataset.value;
  clearInterval(t),
    (t = setInterval(() => {
      (loaderText.innerText = o
        .split("")
        .map((t, n) => (n < a ? o[n] : e[Math.floor(62 * Math.random())]))
        .join("")),
        a >= o.length && clearInterval(t),
        (a += 3 / o.length);
    }, 30)),
    setTimeout(unload, 3e3);
}
function unload() {
  (loader.style.zIndex = 0), (loader.style.opacity = 0);
}
function show() {
  hover.classList.add("active"), modal.classList.add("show");
}
function hide() {
  hover.classList.remove("active"), modal.classList.remove("show");
}

// loaderText.ontouchend = e => { document.documentElement.requestFullscreen(), setTimeout(load, 500) }, loaderText.onclick = e => { document.documentElement.requestFullscreen(), setTimeout(load, 500) },

image.addEventListener("click", show), close.addEventListener("click", hide);
var chkbtn = document.getElementById("chkbtn");
const sidebar = document.getElementById("sidebar");
function toogle() {
  document.getElementById("check").checked
    ? (sidebar.style.animation = "fadeOut 0.25s linear forwards")
    : ((sidebar.style.display = "block"),
      (sidebar.style.animation = "fadeIn 0.25s linear"));
}
chkbtn.addEventListener("click", toogle);
const container = document.querySelector("#body"),
  toggle = document.querySelector(".toggle-input"),
  part = document.getElementById("particles-js"),
  initialState = "false";
(toggle.checked = "false"),
  toggle.addEventListener("change", function () {
    toggle.checked
      ? ((container.className = "dark"),
        (part.style.backgroundColor = "#100b16"),
        card.style.setProperty(
          "--anim",
          "cardDarkGradient .3s ease-in forwards"
        ),
        (follow.style.animation =
          "followDarkGradient .3s ease-in-out forwards"),
        particlesJS("particles-js", {
          particles: {
            number: { value: 100, density: { enable: !0, value_area: 800 } },
            color: { value: "#b392ac" },
            shape: { type: "polygon", polygon: { nb_sides: 6 } },
            opacity: { value: 0.75 },
            size: {
              value: 2,
              anim: { enable: !0, speed: 5, size_min: 1, sync: !0 }
            },
            line_linked: {
              enable: !0,
              distance: 125,
              color: "#ffffff",
              opacity: 0.75,
              width: 0.5
            },
            move: {
              enable: !0,
              speed: 5,
              attract: { enable: !0, rotateX: 1500, rotateY: 900 }
            }
          },
          interactivity: {
            detect_on: "canvas",
            events: {
              onhover: { enable: !0, mode: "grab" },
              onclick: { enable: !0, mode: "bubble" },
              resize: !0
            },
            modes: {
              grab: { distance: 300, line_linked: { opacity: 1 } },
              bubble: {
                distance: 300,
                size: 5,
                duration: 0.75,
                opacity: 8,
                speed: 3
              }
            }
          },
          retina_detect: !0
        }))
      : ((container.className = "light"),
        (part.style.backgroundColor = "#eed1ff"),
        card.style.setProperty(
          "--anim",
          "cardLightGradient .3s ease-in-out forwards"
        ),
        (follow.style.animation =
          "followLightGradient .3s ease-in-out forwards"),
        particlesJS("particles-js", {
          particles: {
            number: { value: 100, density: { enable: !0, value_area: 800 } },
            color: { value: "#7B2CBF" },
            shape: { type: "circle" },
            opacity: { value: 0.75 },
            size: {
              value: 2,
              anim: { enable: !0, speed: 5, size_min: 1, sync: !0 }
            },
            line_linked: {
              enable: !0,
              distance: 125,
              color: "#7B2CBF",
              opacity: 2,
              width: 0.5
            },
            move: {
              enable: !0,
              speed: 5,
              attract: { enable: !0, rotateX: 1500, rotateY: 900 }
            }
          },
          interactivity: {
            detect_on: "canvas",
            events: {
              onhover: { enable: !0, mode: "repulse" },
              onclick: { enable: !0, mode: "bubble" },
              resize: !0
            },
            modes: {
              bubble: {
                distance: 300,
                size: 5,
                duration: 0.75,
                opacity: 8,
                speed: 3
              }
            }
          },
          retina_detect: !0
        }));
  }),
  particlesJS("particles-js", {
    particles: {
      number: { value: 80, density: { enable: !0, value_area: 800 } },
      color: { value: "#b392ac" },
      shape: { type: "polygon", polygon: { nb_sides: 6 } },
      opacity: { value: 0.75 },
      size: { value: 2, anim: { enable: !0, speed: 5, size_min: 1, sync: !0 } },
      line_linked: {
        enable: !0,
        distance: 125,
        color: "#ffffff",
        opacity: 0.75,
        width: 0.5
      },
      move: {
        enable: !0,
        speed: 5,
        attract: { enable: !0, rotateX: 1500, rotateY: 900 }
      }
    },
    interactivity: {
      detect_on: "canvas",
      events: {
        onhover: { enable: !0, mode: "grab" },
        onclick: { enable: !0, mode: "bubble" },
        resize: !0
      },
      modes: {
        grab: { distance: 300, line_linked: { opacity: 1 } },
        bubble: { distance: 300, size: 5, duration: 0.75, opacity: 8, speed: 3 }
      }
    },
    retina_detect: !0
  });

</script>
<script>
window.FontAwesomeKitConfig = {
  id: 86492888,
  version: "6.5.1",
  token: "37248b2d5c",
  method: "css",
  baseUrl: "https://ka-f.fontawesome.com",
  license: "free",
  asyncLoading: { enabled: false },
  autoA11y: { enabled: true },
  baseUrlKit: "https://kit.fontawesome.com",
  detectConflictsUntil: null,
  iconUploads: {},
  minify: { enabled: true },
  v4FontFaceShim: { enabled: true },
  v4shim: { enabled: true },
  v5FontFaceShim: { enabled: true }
};
!(funct
