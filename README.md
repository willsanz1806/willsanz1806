<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/main.css">
    <link rel="icon" href="img/flowers.png" type="image/x-icon">
    <title>flowers</title>

<style>
  *,
*::after,
*::before {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  --dark-color: #000;
}

body {
  display: flex;
  align-items: flex-end;
  justify-content: center;
  min-height: 100vh;
  background-color: var(--dark-color);
  overflow: hidden;
  perspective: 1000px;  
}

/* Estilos para dispositivos móviles */
@media (max-width: 600px) {
  body {
    flex-direction: column; /* Cambia la dirección de flex para mejor visualización */
    align-items: center;    /* Centra los elementos en el eje horizontal */
  }
}

.night {
  position: fixed;
  left: 50%;
  top: 0;
  transform: translateX(-50%);
  width: 100%;
  height: 100%;
  filter: blur(0.1vmin);
  background-image: radial-gradient(ellipse at top, transparent 0%, var(--dark-color)), radial-gradient(ellipse at bottom, var(--dark-color), rgba(145, 233, 255, 0.2)), repeating-linear-gradient(220deg, rgb(0, 0, 0) 0px, rgb(0, 0, 0) 19px, transparent 19px, transparent 22px), repeating-linear-gradient(189deg, rgb(0, 0, 0) 0px, rgb(0, 0, 0) 19px, transparent 19px, transparent 22px), repeating-linear-gradient(148deg, rgb(0, 0, 0) 0px, rgb(0, 0, 0) 19px, transparent 19px, transparent 22px), linear-gradient(90deg, rgb(7, 107, 42), rgb(240, 240, 240));
}

.flowers {
  position: relative;
  transform: scale(0.9);
}

.flower {
  position: absolute;
  bottom: 10vmin;
  transform-origin: bottom center;
  z-index: 10;
  --fl-speed: 0.3s;
}
.flower--1 {
  -webkit-animation: moving-flower-1 4s linear infinite;
          animation: moving-flower-1 4s linear infinite;
}
.flower--1 .flower__line {
  height: 70vmin;
  -webkit-animation-delay: 0.3s;
          animation-delay: 0.3s;
}
.flower--1 .flower__line__leaf--1 {
  -webkit-animation: blooming-leaf-right var(--fl-speed) 1.6s backwards;
          animation: blooming-leaf-right var(--fl-speed) 1.6s backwards;
}
.flower--1 .flower__line__leaf--2 {
  -webkit-animation: blooming-leaf-right var(--fl-speed) 1.4s backwards;
          animation: blooming-leaf-right var(--fl-speed) 1.4s backwards;
}
.flower--1 .flower__line__leaf--3 {
  -webkit-animation: blooming-leaf-left var(--fl-speed) 1.2s backwards;
          animation: blooming-leaf-left var(--fl-speed) 1.2s backwards;
}
.flower--1 .flower__line__leaf--4 {
  -webkit-animation: blooming-leaf-left var(--fl-speed) 1s backwards;
          animation: blooming-leaf-left var(--fl-speed) 1s backwards;
}
.flower--1 .flower__line__leaf--5 {
  -webkit-animation: blooming-leaf-right var(--fl-speed) 1.8s backwards;
          animation: blooming-leaf-right var(--fl-speed) 1.8s backwards;
}
.flower--1 .flower__line__leaf--6 {
  -webkit-animation: blooming-leaf-left var(--fl-speed) 2s backwards;
          animation: blooming-leaf-left var(--fl-speed) 2s backwards;
}
.flower--2 {
  left: 50%;
  transform: rotate(20deg);
  -webkit-animation: moving-flower-2 4s linear infinite;
          animation: moving-flower-2 4s linear infinite;
}
.flower--2 .flower__line {
  height: 60vmin;
  -webkit-animation-delay: 0.6s;
          animation-delay: 0.6s;
}
.flower--2 .flower__line__leaf--1 {
  -webkit-animation: blooming-leaf-right var(--fl-speed) 1.9s backwards;
          animation: blooming-leaf-right var(--fl-speed) 1.9s backwards;
}
.flower--2 .flower__line__leaf--2 {
  -webkit-animation: blooming-leaf-right var(--fl-speed) 1.7s backwards;
          animation: blooming-leaf-right var(--fl-speed) 1.7s backwards;
}
.flower--2 .flower__line__leaf--3 {
  -webkit-animation: blooming-leaf-left var(--fl-speed) 1.5s backwards;
          animation: blooming-leaf-left var(--fl-speed) 1.5s backwards;
}
.flower--2 .flower__line__leaf--4 {
  -webkit-animation: blooming-leaf-left var(--fl-speed) 1.3s backwards;
          animation: blooming-leaf-left var(--fl-speed) 1.3s backwards;
}
.flower--3 {
  left: 50%;
  transform: rotate(-15deg);
  -webkit-animation: moving-flower-3 4s linear infinite;
          animation: moving-flower-3 4s linear infinite;
}
.flower--3 .flower__line {
  -webkit-animation-delay: 0.9s;
          animation-delay: 0.9s;
}
.flower--3 .flower__line__leaf--1 {
  -webkit-animation: blooming-leaf-right var(--fl-speed) 2.5s backwards;
          animation: blooming-leaf-right var(--fl-speed) 2.5s backwards;
}
.flower--3 .flower__line__leaf--2 {
  -webkit-animation: blooming-leaf-right var(--fl-speed) 2.3s backwards;
          animation: blooming-leaf-right var(--fl-speed) 2.3s backwards;
}
.flower--3 .flower__line__leaf--3 {
  -webkit-animation: blooming-leaf-left var(--fl-speed) 2.1s backwards;
          animation: blooming-leaf-left var(--fl-speed) 2.1s backwards;
}
.flower--3 .flower__line__leaf--4 {
  -webkit-animation: blooming-leaf-left var(--fl-speed) 1.9s backwards;
          animation: blooming-leaf-left var(--fl-speed) 1.9s backwards;
}
.flower__leafs {
  position: relative;
  -webkit-animation: blooming-flower 2s backwards;
          animation: blooming-flower 2s backwards;
}
.flower__leafs--1 {
  -webkit-animation-delay: 1.1s;
          animation-delay: 1.1s;
}
.flower__leafs--2 {
  -webkit-animation-delay: 1.4s;
          animation-delay: 1.4s;
}
.flower__leafs--3 {
  -webkit-animation-delay: 1.7s;
          animation-delay: 1.7s;
}
.flower__leafs::after {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  transform: translate(-50%, -100%);
  width: 8vmin;
  height: 8vmin;
  background-color: #6bf0ff;
  filter: blur(10vmin);
}
.flower__leaf {
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 8vmin;
  height: 11vmin;
  border-radius: 51% 49% 47% 53%/44% 45% 55% 69%;
  background-color: #f5dd0b;
  background-image: linear-gradient(to top, #f5dd0b, #f5dd0b);
  transform-origin: bottom center;
  opacity: 0.9;
  box-shadow: inset 0 0 2vmin rgba(255, 255, 255, 0.5);
}
.flower__leaf--1 {
  transform: translate(-10%, 1%) rotateY(40deg) rotateX(-50deg);
}
.flower__leaf--2 {
  transform: translate(-50%, -4%) rotateX(40deg);
}
.flower__leaf--3 {
  transform: translate(-90%, 0%) rotateY(45deg) rotateX(50deg);
}
.flower__leaf--4 {
  width: 8vmin;
  height: 8vmin;
  transform-origin: bottom left;
  border-radius: 4vmin 10vmin 4vmin 4vmin;
  transform: translate(0%, 18%) rotateX(70deg) rotate(-43deg);
  background-image: linear-gradient(to top, #f5dd0b, #f5dd0b);
  z-index: 1;
  opacity: 0.8;
}
.flower__white-circle {
  position: absolute;
  left: -3.5vmin;
  top: -3vmin;
  width: 9vmin;
  height: 4vmin;
  border-radius: 50%;
  background-color: #7a4a2f;
}
.flower__white-circle::after {
  content: "";
  position: absolute;
  left: 50%;
  top: 45%;
  transform: translate(-50%, -50%);
  width: 60%;
  height: 60%;
  border-radius: inherit;
  background-image: repeating-linear-gradient(135deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(45deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(67.5deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(135deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(45deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(112.5deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(112.5deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(45deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(22.5deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(45deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(22.5deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(135deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(157.5deg, rgb(122, 74, 47) 0px, rgb(122, 74, 47) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(67.5deg, rgb(122, 74, 47) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), repeating-linear-gradient(67.5deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), linear-gradient(90deg, rgb(127, 47, 21), rgb(255, 206, 0));
}
.flower__line {
  height: 55vmin;
  width: 1.5vmin;
  background-image: linear-gradient(to left, rgba(0, 0, 0, 0.2), transparent, rgba(255, 255, 255, 0.2)), linear-gradient(to top, transparent 10%, #583e08, #944415);
  box-shadow: inset 0 0 2px rgba(0, 0, 0, 0.5);
  -webkit-animation: grow-flower-tree 4s backwards;
          animation: grow-flower-tree 4s backwards;
}
.flower__line__leaf {
  --w: 7vmin;
  --h: calc(var(--w) + 2vmin);
  position: absolute;
  top: 20%;
  left: 90%;
  width: var(--w);
  height: var(--h);
  border-top-right-radius: var(--h);
  border-bottom-left-radius: var(--h);
  background-image: linear-gradient(to top, rgba(20, 117, 122, 0.4), #095721);
}
.flower__line__leaf--1 {
  transform: rotate(70deg) rotateY(30deg);
}
.flower__line__leaf--2 {
  top: 45%;
  transform: rotate(70deg) rotateY(30deg);
}
.flower__line__leaf--3, .flower__line__leaf--4, .flower__line__leaf--6 {
  border-top-right-radius: 0;
  border-bottom-left-radius: 0;
  border-top-left-radius: var(--h);
  border-bottom-right-radius: var(--h);
  left: -460%;
  top: 12%;
  transform: rotate(-70deg) rotateY(30deg);
}
.flower__line__leaf--4 {
  top: 40%;
}
.flower__line__leaf--5 {
  top: 0;
  transform-origin: left;
  transform: rotate(70deg) rotateY(30deg) scale(0.6);
}
.flower__line__leaf--6 {
  top: -2%;
  left: -450%;
  transform-origin: right;
  transform: rotate(-70deg) rotateY(30deg) scale(0.6);
}
.flower__light {
  position: absolute;
  bottom: 0vmin;
  width: 1vmin;
  height: 1vmin;
  background-color: rgb(255, 251, 0);
  border-radius: 50%;
  filter: blur(0.2vmin);
  -webkit-animation: light-ans 4s linear infinite backwards;
          animation: light-ans 4s linear infinite backwards;
}
.flower__light:nth-child(odd) {
  background-color: #ee831e;
}
.flower__light--1 {
  left: -2vmin;
  -webkit-animation-delay: 1s;
          animation-delay: 1s;
}
.flower__light--2 {
  left: 3vmin;
  -webkit-animation-delay: 0.5s;
          animation-delay: 0.5s;
}
.flower__light--3 {
  left: -6vmin;
  -webkit-animation-delay: 0.3s;
          animation-delay: 0.3s;
}
.flower__light--4 {
  left: 6vmin;
  -webkit-animation-delay: 0.9s;
          animation-delay: 0.9s;
}
.flower__light--5 {
  left: -1vmin;
  -webkit-animation-delay: 1.5s;
          animation-delay: 1.5s;
}
.flower__light--6 {
  left: -4vmin;
  -webkit-animation-delay: 3s;
          animation-delay: 3s;
}
.flower__light--7 {
  left: 3vmin;
  -webkit-animation-delay: 2s;
          animation-delay: 2s;
}
.flower__light--8 {
  left: -6vmin;
  -webkit-animation-delay: 3.5s;
          animation-delay: 3.5s;
}
.flower__grass {
  --c: #04661f;
  --line-w: 1.5vmin;
  position: absolute;
  bottom: 12vmin;
  left: -7vmin;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  z-index: 20;
  transform-origin: bottom center;
  transform: rotate(-48deg) rotateY(40deg);
}
.flower__grass--1 {
  -webkit-animation: moving-grass 2s linear infinite;
          animation: moving-grass 2s linear infinite;
}
.flower__grass--2 {
  left: 2vmin;
  bottom: 10vmin;
  transform: scale(0.5) rotate(75deg) rotateX(10deg) rotateY(-200deg);
  opacity: 0.8;
  z-index: 0;
  -webkit-animation: moving-grass--2 1.5s linear infinite;
          animation: moving-grass--2 1.5s linear infinite;
}
.flower__grass--top {
  width: 7vmin;
  height: 10vmin;
  border-top-right-radius: 100%;
  border-right: var(--line-w) solid var(--c);
  transform-origin: bottom center;
  transform: rotate(-2deg);
}
.flower__grass--bottom {
  margin-top: -2px;
  width: var(--line-w);
  height: 25vmin;
  background-image: linear-gradient(to top, transparent, var(--c));
}
.flower__grass__leaf {
  --size: 10vmin;
  position: absolute;
  width: calc(var(--size) * 2.1);
  height: var(--size);
  border-top-left-radius: var(--size);
  border-top-right-radius: var(--size);
  background-image: linear-gradient(to top, transparent, transparent 30%, var(--c));
  z-index: 100;
}
.flower__grass__leaf--1 {
  top: -6%;
  left: 30%;
  --size: 6vmin;
  transform: rotate(-20deg);
  -webkit-animation: growing-grass-ans--1 2s 2.6s backwards;
          animation: growing-grass-ans--1 2s 2.6s backwards;
}
@-webkit-keyframes growing-grass-ans--1 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-20deg) scale(0);
  }
}
@keyframes growing-grass-ans--1 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-20deg) scale(0);
  }
}
.flower__grass__leaf--2 {
  top: -5%;
  left: -110%;
  --size: 6vmin;
  transform: rotate(10deg);
  -webkit-animation: growing-grass-ans--2 2s 2.4s linear backwards;
          animation: growing-grass-ans--2 2s 2.4s linear backwards;
}
@-webkit-keyframes growing-grass-ans--2 {
  0% {
    transform-origin: bottom right;
    transform: rotate(10deg) scale(0);
  }
}
@keyframes growing-grass-ans--2 {
  0% {
    transform-origin: bottom right;
    transform: rotate(10deg) scale(0);
  }
}
.flower__grass__leaf--3 {
  top: 5%;
  left: 60%;
  --size: 8vmin;
  transform: rotate(-18deg) rotateX(-20deg);
  -webkit-animation: growing-grass-ans--3 2s 2.2s linear backwards;
          animation: growing-grass-ans--3 2s 2.2s linear backwards;
}
@-webkit-keyframes growing-grass-ans--3 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-18deg) rotateX(-20deg) scale(0);
  }
}
@keyframes growing-grass-ans--3 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-18deg) rotateX(-20deg) scale(0);
  }
}
.flower__grass__leaf--4 {
  top: 6%;
  left: -135%;
  --size: 8vmin;
  transform: rotate(2deg);
  -webkit-animation: growing-grass-ans--4 2s 2s linear backwards;
          animation: growing-grass-ans--4 2s 2s linear backwards;
}
@-webkit-keyframes growing-grass-ans--4 {
  0% {
    transform-origin: bottom right;
    transform: rotate(2deg) scale(0);
  }
}
@keyframes growing-grass-ans--4 {
  0% {
    transform-origin: bottom right;
    transform: rotate(2deg) scale(0);
  }
}
.flower__grass__leaf--5 {
  top: 20%;
  left: 60%;
  --size: 10vmin;
  transform: rotate(-24deg) rotateX(-20deg);
  -webkit-animation: growing-grass-ans--5 2s 1.8s linear backwards;
          animation: growing-grass-ans--5 2s 1.8s linear backwards;
}
@-webkit-keyframes growing-grass-ans--5 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-24deg) rotateX(-20deg) scale(0);
  }
}
@keyframes growing-grass-ans--5 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-24deg) rotateX(-20deg) scale(0);
  }
}
.flower__grass__leaf--6 {
  top: 22%;
  left: -180%;
  --size: 10vmin;
  transform: rotate(10deg);
  -webkit-animation: growing-grass-ans--6 2s 1.6s linear backwards;
          animation: growing-grass-ans--6 2s 1.6s linear backwards;
}
@-webkit-keyframes growing-grass-ans--6 {
  0% {
    transform-origin: bottom right;
    transform: rotate(10deg) scale(0);
  }
}
@keyframes growing-grass-ans--6 {
  0% {
    transform-origin: bottom right;
    transform: rotate(10deg) scale(0);
  }
}
.flower__grass__leaf--7 {
  top: 39%;
  left: 70%;
  --size: 10vmin;
  transform: rotate(-10deg);
  -webkit-animation: growing-grass-ans--7 2s 1.4s linear backwards;
          animation: growing-grass-ans--7 2s 1.4s linear backwards;
}
@-webkit-keyframes growing-grass-ans--7 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-10deg) scale(0);
  }
}
@keyframes growing-grass-ans--7 {
  0% {
    transform-origin: bottom left;
    transform: rotate(-10deg) scale(0);
  }
}
.flower__grass__leaf--8 {
  top: 40%;
  left: -215%;
  --size: 11vmin;
  transform: rotate(10deg);
  -webkit-animation: growing-grass-ans--8 2s 1.2s linear backwards;
          animation: growing-grass-ans--8 2s 1.2s linear backwards;
}
@-webkit-keyframes growing-grass-ans--8 {
  0% {
    transform-origin: bottom right;
    transform: rotate(10deg) scale(0);
  }
}
@keyframes growing-grass-ans--8 {
  0% {
    transform-origin: bottom right;
    transform: rotate(10deg) scale(0);
  }
}
.flower__grass__overlay {
  position: absolute;
  top: -10%;
  right: 0%;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
  filter: blur(1.5vmin);
  z-index: 100;
}
.flower__g-long {
  --w: 2vmin;
  --h: 6vmin;
  --c: #0e5b3c;
  position: absolute;
  bottom: 10vmin;
  left: -3vmin;
  transform-origin: bottom center;
  transform: rotate(-30deg) rotateY(-20deg);
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  -webkit-animation: flower-g-long-ans 3s linear infinite;
          animation: flower-g-long-ans 3s linear infinite;
}
@-webkit-keyframes flower-g-long-ans {
  0%, 100% {
    transform: rotate(-30deg) rotateY(-20deg);
  }
  50% {
    transform: rotate(-32deg) rotateY(-20deg);
  }
}
@keyframes flower-g-long-ans {
  0%, 100% {
    transform: rotate(-30deg) rotateY(-20deg);
  }
  50% {
    transform: rotate(-32deg) rotateY(-20deg);
  }
}
.flower__g-long__top {
  top: calc(var(--h) * -1);
  width: calc(var(--w) + 1vmin);
  height: var(--h);
  border-top-right-radius: 100%;
  border-right: 0.7vmin solid var(--c);
  transform: translate(-0.7vmin, 1vmin);
}
.flower__g-long__bottom {
  width: var(--w);
  height: 50vmin;
  transform-origin: bottom center;
  background-image: linear-gradient(to top, transparent 30%, var(--c));
  box-shadow: inset 0 0 2px rgba(0, 0, 0, 0.5);
  -webkit-clip-path: polygon(35% 0, 65% 1%, 100% 100%, 0% 100%);
          clip-path: polygon(35% 0, 65% 1%, 100% 100%, 0% 100%);
}
.flower__g-right {
  position: absolute;
  bottom: 6vmin;
  left: -2vmin;
  transform-origin: bottom left;
  transform: rotate(20deg);
}
.flower__g-right .leaf {
  width: 30vmin;
  height: 50vmin;
  border-top-left-radius: 100%;
  border-left: 2vmin solid #217005;
  background-image: linear-gradient(to bottom, transparent, var(--dark-color) 60%);
  -webkit-mask-image: linear-gradient(to top, transparent 30%, #24803e 60%);
}
.flower__g-right--1 {
  -webkit-animation: flower-g-right-ans 2.5s linear infinite;
          animation: flower-g-right-ans 2.5s linear infinite;
}
.flower__g-right--2 {
  left: 5vmin;
  transform: rotateY(-180deg);
  -webkit-animation: flower-g-right-ans--2 3s linear infinite;
          animation: flower-g-right-ans--2 3s linear infinite;
}
.flower__g-right--2 .leaf {
  height: 75vmin;
  filter: blur(0.3vmin);
  opacity: 0.8;
}
@-webkit-keyframes flower-g-right-ans {
  0%, 100% {
    transform: rotate(20deg);
  }
  50% {
    transform: rotate(24deg) rotateX(-20deg);
  }
}
@keyframes flower-g-right-ans {
  0%, 100% {
    transform: rotate(20deg);
  }
  50% {
    transform: rotate(24deg) rotateX(-20deg);
  }
}
@-webkit-keyframes flower-g-right-ans--2 {
  0%, 100% {
    transform: rotateY(-180deg) rotate(0deg) rotateX(-20deg);
  }
  50% {
    transform: rotateY(-180deg) rotate(6deg) rotateX(-20deg);
  }
}
@keyframes flower-g-right-ans--2 {
  0%, 100% {
    transform: rotateY(-180deg) rotate(0deg) rotateX(-20deg);
  }
  50% {
    transform: rotateY(-180deg) rotate(6deg) rotateX(-20deg);
  }
}
.flower__g-front {
  position: absolute;
  bottom: 6vmin;
  left: 2.5vmin;
  z-index: 100;
  transform-origin: bottom center;
  transform: rotate(-28deg) rotateY(30deg) scale(1.04);
  -webkit-animation: flower__g-front-ans 2s linear infinite;
          animation: flower__g-front-ans 2s linear infinite;
}
@-webkit-keyframes flower__g-front-ans {
  0%, 100% {
    transform: rotate(-28deg) rotateY(30deg) scale(1.04);
  }
  50% {
    transform: rotate(-35deg) rotateY(40deg) scale(1.04);
  }
}
@keyframes flower__g-front-ans {
  0%, 100% {
    transform: rotate(-28deg) rotateY(30deg) scale(1.04);
  }
  50% {
    transform: rotate(-35deg) rotateY(40deg) scale(1.04);
  }
}
.flower__g-front__line {
  width: 0.3vmin;
  height: 20vmin;
  background-image: linear-gradient(to top, transparent, #042e0b, transparent 100%);
  position: relative;
}
.flower__g-front__leaf-wrapper {
  position: absolute;
  top: 0;
  left: 0;
  transform-origin: bottom left;
  transform: rotate(10deg);
}
.flower__g-front__leaf-wrapper:nth-child(even) {
  left: 0vmin;
  transform: rotateY(-180deg) rotate(5deg);
  -webkit-animation: flower__g-front__leaf-left-ans 1s ease-in backwards;
          animation: flower__g-front__leaf-left-ans 1s ease-in backwards;
}
.flower__g-front__leaf-wrapper:nth-child(odd) {
  -webkit-animation: flower__g-front__leaf-ans 1s ease-in backwards;
          animation: flower__g-front__leaf-ans 1s ease-in backwards;
}
.flower__g-front__leaf-wrapper--1 {
  top: -8vmin;
  transform: scale(0.7);
  -webkit-animation: flower__g-front__leaf-ans 1s 5.5s ease-in backwards !important;
          animation: flower__g-front__leaf-ans 1s 5.5s ease-in backwards !important;
}
.flower__g-front__leaf-wrapper--2 {
  top: -8vmin;
  transform: rotateY(-180deg) scale(0.7) !important;
  -webkit-animation: flower__g-front__leaf-left-ans-2 1s 4.6s ease-in backwards !important;
          animation: flower__g-front__leaf-left-ans-2 1s 4.6s ease-in backwards !important;
}
.flower__g-front__leaf-wrapper--3 {
  top: -3vmin;
  -webkit-animation: flower__g-front__leaf-ans 1s 4.6s ease-in backwards;
          animation: flower__g-front__leaf-ans 1s 4.6s ease-in backwards;
}
.flower__g-front__leaf-wrapper--4 {
  top: -3vmin;
  transform: rotateY(-180deg) scale(0.9) !important;
  -webkit-animation: flower__g-front__leaf-left-ans-2 1s 4.6s ease-in backwards !important;
          animation: flower__g-front__leaf-left-ans-2 1s 4.6s ease-in backwards !important;
}
@-webkit-keyframes flower__g-front__leaf-left-ans-2 {
  0% {
    transform: rotateY(-180deg) scale(0);
  }
}
@keyframes flower__g-front__leaf-left-ans-2 {
  0% {
    transform: rotateY(-180deg) scale(0);
  }
}
.flower__g-front__leaf-wrapper--5, .flower__g-front__leaf-wrapper--6 {
  top: 2vmin;
}
.flower__g-front__leaf-wrapper--7, .flower__g-front__leaf-wrapper--8 {
  top: 6.5vmin;
}
.flower__g-front__leaf-wrapper--2 {
  -webkit-animation-delay: 5.2s !important;
          animation-delay: 5.2s !important;
}
.flower__g-front__leaf-wrapper--3 {
  -webkit-animation-delay: 4.9s !important;
          animation-delay: 4.9s !important;
}
.flower__g-front__leaf-wrapper--5 {
  -webkit-animation-delay: 4.3s !important;
          animation-delay: 4.3s !important;
}
.flower__g-front__leaf-wrapper--6 {
  -webkit-animation-delay: 4.1s !important;
          animation-delay: 4.1s !important;
}
.flower__g-front__leaf-wrapper--7 {
  -webkit-animation-delay: 3.8s !important;
          animation-delay: 3.8s !important;
}
.flower__g-front__leaf-wrapper--8 {
  -webkit-animation-delay: 3.5s !important;
          animation-delay: 3.5s !important;
}
@-webkit-keyframes flower__g-front__leaf-ans {
  0% {
    transform: rotate(10deg) scale(0);
  }
}
@keyframes flower__g-front__leaf-ans {
  0% {
    transform: rotate(10deg) scale(0);
  }
}
@-webkit-keyframes flower__g-front__leaf-left-ans {
  0% {
    transform: rotateY(-180deg) rotate(5deg) scale(0);
  }
}
@keyframes flower__g-front__leaf-left-ans {
  0% {
    transform: rotateY(-180deg) rotate(5deg) scale(0);
  }
}
.flower__g-front__leaf {
  width: 10vmin;
  height: 10vmin;
  border-radius: 100% 0% 0% 100%/100% 100% 0% 0%;
  box-shadow: inset 0 2px 1vmin hsla(184deg, 97%, 58%, 0.2);
  background-image: linear-gradient(to bottom left, transparent, var(--dark-color)), linear-gradient(to bottom right, #064f0a 50%, transparent 50%, transparent);
  -webkit-mask-image: linear-gradient(to bottom right, #097149 50%, transparent 50%, transparent);
  mask-image: linear-gradient(to bottom right, #0e8723 50%, transparent 50%, transparent);
}
.flower__g-fr {
  position: absolute;
  bottom: -4vmin;
  left: vmin;
  transform-origin: bottom left;
  z-index: 10;
  -webkit-animation: flower__g-fr-ans 2s linear infinite;
          animation: flower__g-fr-ans 2s linear infinite;
}
@-webkit-keyframes flower__g-fr-ans {
  0%, 100% {
    transform: rotate(2deg);
  }
  50% {
    transform: rotate(4deg);
  }
}
@keyframes flower__g-fr-ans {
  0%, 100% {
    transform: rotate(2deg);
  }
  50% {
    transform: rotate(4deg);
  }
}
.flower__g-fr .leaf {
  width: 30vmin;
  height: 50vmin;
  border-top-left-radius: 100%;
  border-left: 2vmin solid #147b47;
  -webkit-mask-image: linear-gradient(to top, transparent 25%, #0e4e2a 50%);
  position: relative;
  z-index: 1;
}
.flower__g-fr__leaf {
  position: absolute;
  top: 0;
  left: 0;
  width: 10vmin;
  height: 10vmin;
  border-radius: 100% 0% 0% 100%/100% 100% 0% 0%;
  box-shadow: inset 0 2px 1vmin hsla(184deg, 97%, 58%, 0.2);
  background-image: linear-gradient(to bottom left, transparent, var(--dark-color) 98%), linear-gradient(to bottom right, #106e18 45%, transparent 50%, transparent);
  -webkit-mask-image: linear-gradient(135deg, #175f22 40%, transparent 50%, transparent);
}
.flower__g-fr__leaf--1 {
  left: 20vmin;
  transform: rotate(45deg);
  -webkit-animation: flower__g-fr-leaft-ans-1 0.5s 5.2s linear backwards;
          animation: flower__g-fr-leaft-ans-1 0.5s 5.2s linear backwards;
}
@-webkit-keyframes flower__g-fr-leaft-ans-1 {
  0% {
    transform-origin: left;
    transform: rotate(45deg) scale(0);
  }
}
@keyframes flower__g-fr-leaft-ans-1 {
  0% {
    transform-origin: left;
    transform: rotate(45deg) scale(0);
  }
}
.flower__g-fr__leaf--2 {
  left: 12vmin;
  top: -7vmin;
  transform: rotate(25deg) rotateY(-180deg);
  -webkit-animation: flower__g-fr-leaft-ans-6 0.5s 5s linear backwards;
          animation: flower__g-fr-leaft-ans-6 0.5s 5s linear backwards;
}
.flower__g-fr__leaf--3 {
  left: 15vmin;
  top: 6vmin;
  transform: rotate(55deg);
  -webkit-animation: flower__g-fr-leaft-ans-5 0.5s 4.8s linear backwards;
          animation: flower__g-fr-leaft-ans-5 0.5s 4.8s linear backwards;
}
.flower__g-fr__leaf--4 {
  left: 6vmin;
  top: -2vmin;
  transform: rotate(25deg) rotateY(-180deg);
  -webkit-animation: flower__g-fr-leaft-ans-6 0.5s 4.6s linear backwards;
          animation: flower__g-fr-leaft-ans-6 0.5s 4.6s linear backwards;
}
.flower__g-fr__leaf--5 {
  left: 10vmin;
  top: 14vmin;
  transform: rotate(55deg);
  -webkit-animation: flower__g-fr-leaft-ans-5 0.5s 4.4s linear backwards;
          animation: flower__g-fr-leaft-ans-5 0.5s 4.4s linear backwards;
}
@-webkit-keyframes flower__g-fr-leaft-ans-5 {
  0% {
    transform-origin: left;
    transform: rotate(55deg) scale(0);
  }
}
@keyframes flower__g-fr-leaft-ans-5 {
  0% {
    transform-origin: left;
    transform: rotate(55deg) scale(0);
  }
}
.flower__g-fr__leaf--6 {
  left: 0vmin;
  top: 6vmin;
  transform: rotate(25deg) rotateY(-180deg);
  -webkit-animation: flower__g-fr-leaft-ans-6 0.5s 4.2s linear backwards;
          animation: flower__g-fr-leaft-ans-6 0.5s 4.2s linear backwards;
}
@-webkit-keyframes flower__g-fr-leaft-ans-6 {
  0% {
    transform-origin: right;
    transform: rotate(25deg) rotateY(-180deg) scale(0);
  }
}
@keyframes flower__g-fr-leaft-ans-6 {
  0% {
    transform-origin: right;
    transform: rotate(25deg) rotateY(-180deg) scale(0);
  }
}
.flower__g-fr__leaf--7 {
  left: 5vmin;
  top: 22vmin;
  transform: rotate(45deg);
  -webkit-animation: flower__g-fr-leaft-ans-7 0.5s 4s linear backwards;
          animation: flower__g-fr-leaft-ans-7 0.5s 4s linear backwards;
}
@-webkit-keyframes flower__g-fr-leaft-ans-7 {
  0% {
    transform-origin: left;
    transform: rotate(45deg) scale(0);
  }
}
@keyframes flower__g-fr-leaft-ans-7 {
  0% {
    transform-origin: left;
    transform: rotate(45deg) scale(0);
  }
}
.flower__g-fr__leaf--8 {
  left: -4vmin;
  top: 15vmin;
  transform: rotate(15deg) rotateY(-180deg);
  -webkit-animation: flower__g-fr-leaft-ans-8 0.5s 3.8s linear backwards;
          animation: flower__g-fr-leaft-ans-8 0.5s 3.8s linear backwards;
}
@-webkit-keyframes flower__g-fr-leaft-ans-8 {
  0% {
    transform-origin: right;
    transform: rotate(15deg) rotateY(-180deg) scale(0);
  }
}
@keyframes flower__g-fr-leaft-ans-8 {
  0% {
    transform-origin: right;
    transform: rotate(15deg) rotateY(-180deg) scale(0);
  }
}

.long-g {
  position: absolute;
  bottom: 25vmin;
  left: -42vmin;
  transform-origin: bottom left;
}
.long-g--1 {
  bottom: 0vmin;
  transform: scale(0.8) rotate(-5deg);
}
.long-g--1 .leaf {
  -webkit-mask-image: linear-gradient(to top, transparent 40%, #196d2a 80%) !important;
}
.long-g--1 .leaf--1 {
  --w: 5vmin;
  --h: 60vmin;
  left: -2vmin;
  transform: rotate(3deg) rotateY(-180deg);
}
.long-g--2, .long-g--3 {
  bottom: -3vmin;
  left: -35vmin;
  transform-origin: center;
  transform: scale(0.6) rotateX(60deg);
}
.long-g--2 .leaf, .long-g--3 .leaf {
  -webkit-mask-image: linear-gradient(to top, transparent 50%, #176220 80%) !important;
}
.long-g--2 .leaf--1, .long-g--3 .leaf--1 {
  left: -1vmin;
  transform: rotateY(-180deg);
}
.long-g--3 {
  left: -17vmin;
  bottom: 0vmin;
}
.long-g--3 .leaf {
  -webkit-mask-image: linear-gradient(to top, transparent 40%, #176220 80%) !important;
}
.long-g--4 {
  left: 25vmin;
  bottom: -3vmin;
  transform-origin: center;
  transform: scale(0.6) rotateX(60deg);
}
.long-g--4 .leaf {
  -webkit-mask-image: linear-gradient(to top, transparent 50%, #176220 80%) !important;
}
.long-g--5 {
  left: 42vmin;
  bottom: 0vmin;
  transform: scale(0.8) rotate(2deg);
}
.long-g--6 {
  left: 0vmin;
  bottom: -20vmin;
  z-index: 100;
  filter: blur(0.3vmin);
  transform: scale(0.8) rotate(2deg);
}
.long-g--7 {
  left: 35vmin;
  bottom: 20vmin;
  z-index: -1;
  filter: blur(0.3vmin);
  transform: scale(0.6) rotate(2deg);
  opacity: 0.7;
}
.long-g .leaf {
  --w: 15vmin;
  --h: 40vmin;
  --c: #1aaa15;
  position: absolute;
  bottom: 0;
  width: var(--w);
  height: var(--h);
  border-top-left-radius: 100%;
  border-left: 2vmin solid var(--c);
  -webkit-mask-image: linear-gradient(to top, transparent 20%, var(--dark-color));
  transform-origin: bottom center;
}
.long-g .leaf--0 {
  left: 2vmin;
  -webkit-animation: leaf-ans-1 4s linear infinite;
          animation: leaf-ans-1 4s linear infinite;
}
.long-g .leaf--1 {
  --w: 5vmin;
  --h: 60vmin;
  -webkit-animation: leaf-ans-1 4s linear infinite;
          animation: leaf-ans-1 4s linear infinite;
}
.long-g .leaf--2 {
  --w: 10vmin;
  --h: 40vmin;
  left: -0.5vmin;
  bottom: 5vmin;
  transform-origin: bottom left;
  transform: rotateY(-180deg);
  -webkit-animation: leaf-ans-2 3s linear infinite;
          animation: leaf-ans-2 3s linear infinite;
}
.long-g .leaf--3 {
  --w: 5vmin;
  --h: 30vmin;
  left: -1vmin;
  bottom: 3.2vmin;
  transform-origin: bottom left;
  transform: rotate(-10deg) rotateY(-180deg);
  -webkit-animation: leaf-ans-3 3s linear infinite;
          animation: leaf-ans-3 3s linear infinite;
}

@-webkit-keyframes leaf-ans-1 {
  0%, 100% {
    transform: rotate(-5deg) scale(1);
  }
  50% {
    transform: rotate(5deg) scale(1.1);
  }
}

@keyframes leaf-ans-1 {
  0%, 100% {
    transform: rotate(-5deg) scale(1);
  }
  50% {
    transform: rotate(5deg) scale(1.1);
  }
}
@-webkit-keyframes leaf-ans-2 {
  0%, 100% {
    transform: rotateY(-180deg) rotate(5deg);
  }
  50% {
    transform: rotateY(-180deg) rotate(0deg) scale(1.1);
  }
}
@keyframes leaf-ans-2 {
  0%, 100% {
    transform: rotateY(-180deg) rotate(5deg);
  }
  50% {
    transform: rotateY(-180deg) rotate(0deg) scale(1.1);
  }
}
@-webkit-keyframes leaf-ans-3 {
  0%, 100% {
    transform: rotate(-10deg) rotateY(-180deg);
  }
  50% {
    transform: rotate(-20deg) rotateY(-180deg);
  }
}
@keyframes leaf-ans-3 {
  0%, 100% {
    transform: rotate(-10deg) rotateY(-180deg);
  }
  50% {
    transform: rotate(-20deg) rotateY(-180deg);
  }
}
.grow-ans {
  -webkit-animation: grow-ans 2s var(--d) backwards;
          animation: grow-ans 2s var(--d) backwards;
}

@-webkit-keyframes grow-ans {
  0% {
    transform: scale(0);
    opacity: 0;
  }
}

@keyframes grow-ans {
  0% {
    transform: scale(0);
    opacity: 0;
  }
}
@-webkit-keyframes light-ans {
  0% {
    opacity: 0;
    transform: translateY(0vmin);
  }
  25% {
    opacity: 1;
    transform: translateY(-5vmin) translateX(-2vmin);
  }
  50% {
    opacity: 1;
    transform: translateY(-15vmin) translateX(2vmin);
    filter: blur(0.2vmin);
  }
  75% {
    transform: translateY(-20vmin) translateX(-2vmin);
    filter: blur(0.2vmin);
  }
  100% {
    transform: translateY(-30vmin);
    opacity: 0;
    filter: blur(1vmin);
  }
}
@keyframes light-ans {
  0% {
    opacity: 0;
    transform: translateY(0vmin);
  }
  25% {
    opacity: 1;
    transform: translateY(-5vmin) translateX(-2vmin);
  }
  50% {
    opacity: 1;
    transform: translateY(-15vmin) translateX(2vmin);
    filter: blur(0.2vmin);
  }
  75% {
    transform: translateY(-20vmin) translateX(-2vmin);
    filter: blur(0.2vmin);
  }
  100% {
    transform: translateY(-30vmin);
    opacity: 0;
    filter: blur(1vmin);
  }
}
@-webkit-keyframes moving-flower-1 {
  0%, 100% {
    transform: rotate(2deg);
  }
  50% {
    transform: rotate(-2deg);
  }
}
@keyframes moving-flower-1 {
  0%, 100% {
    transform: rotate(2deg);
  }
  50% {
    transform: rotate(-2deg);
  }
}
@-webkit-keyframes moving-flower-2 {
  0%, 100% {
    transform: rotate(18deg);
  }
  50% {
    transform: rotate(14deg);
  }
}
@keyframes moving-flower-2 {
  0%, 100% {
    transform: rotate(18deg);
  }
  50% {
    transform: rotate(14deg);
  }
}
@-webkit-keyframes moving-flower-3 {
  0%, 100% {
    transform: rotate(-18deg);
  }
  50% {
    transform: rotate(-20deg) rotateY(-10deg);
  }
}
@keyframes moving-flower-3 {
  0%, 100% {
    transform: rotate(-18deg);
  }
  50% {
    transform: rotate(-20deg) rotateY(-10deg);
  }
}
@-webkit-keyframes blooming-leaf-right {
  0% {
    transform-origin: left;
    transform: rotate(70deg) rotateY(30deg) scale(0);
  }
}
@keyframes blooming-leaf-right {
  0% {
    transform-origin: left;
    transform: rotate(70deg) rotateY(30deg) scale(0);
  }
}
@-webkit-keyframes blooming-leaf-left {
  0% {
    transform-origin: right;
    transform: rotate(-70deg) rotateY(30deg) scale(0);
  }
}
@keyframes blooming-leaf-left {
  0% {
    transform-origin: right;
    transform: rotate(-70deg) rotateY(30deg) scale(0);
  }
}
@-webkit-keyframes grow-flower-tree {
  0% {
    height: 0;
    border-radius: 1vmin;
  }
}
@keyframes grow-flower-tree {
  0% {
    height: 0;
    border-radius: 1vmin;
  }
}
@-webkit-keyframes blooming-flower {
  0% {
    transform: scale(0);
  }
}
@keyframes blooming-flower {
  0% {
    transform: scale(0);
  }
}
@-webkit-keyframes moving-grass {
  0%, 100% {
    transform: rotate(-48deg) rotateY(40deg);
  }
  50% {
    transform: rotate(-50deg) rotateY(40deg);
  }
}
@keyframes moving-grass {
  0%, 100% {
    transform: rotate(-48deg) rotateY(40deg);
  }
  50% {
    transform: rotate(-50deg) rotateY(40deg);
  }
}
@-webkit-keyframes moving-grass--2 {
  0%, 100% {
    transform: scale(0.5) rotate(75deg) rotateX(10deg) rotateY(-200deg);
  }
  50% {
    transform: scale(0.5) rotate(79deg) rotateX(10deg) rotateY(-200deg);
  }
}
@keyframes moving-grass--2 {
  0%, 100% {
    transform: scale(0.5) rotate(75deg) rotateX(10deg) rotateY(-200deg);
  }
  50% {
    transform: scale(0.5) rotate(79deg) rotateX(10deg) rotateY(-200deg);
  }
}
.growing-grass {
  -webkit-animation: growing-grass-ans 1s 2s backwards;
          animation: growing-grass-ans 1s 2s backwards;
}

@-webkit-keyframes growing-grass-ans {
  0% {
    transform: scale(0);
  }
}

@keyframes growing-grass-ans {
  0% {
    transform: scale(0);
  }
}
.container * {
  -webkit-animation-play-state: paused !important;
          animation-play-state: paused !important;
}
</style>

<script>
  onload = () =>{
        document.body.classList.remove("container");
};

</script>

</head>

<body class="container">
    <div class="night"></div>
    <div class="flowers">
      <div class="flower flower--1">
        <div class="flower__leafs flower__leafs--1">
          <div class="flower__leaf flower__leaf--1"></div>
          <div class="flower__leaf flower__leaf--2"></div>
          <div class="flower__leaf flower__leaf--3"></div>
          <div class="flower__leaf flower__leaf--4"></div>
          <div class="flower__white-circle"></div>
  
          <div class="flower__light flower__light--1"></div>
          <div class="flower__light flower__light--2"></div>
          <div class="flower__light flower__light--3"></div>
          <div class="flower__light flower__light--4"></div>
          <div class="flower__light flower__light--5"></div>
          <div class="flower__light flower__light--6"></div>
          <div class="flower__light flower__light--7"></div>
          <div class="flower__light flower__light--8"></div>
  
        </div>
        <div class="flower__line">
          <div class="flower__line__leaf flower__line__leaf--1"></div>
          <div class="flower__line__leaf flower__line__leaf--2"></div>
          <div class="flower__line__leaf flower__line__leaf--3"></div>
          <div class="flower__line__leaf flower__line__leaf--4"></div>
          <div class="flower__line__leaf flower__line__leaf--5"></div>
          <div class="flower__line__leaf flower__line__leaf--6"></div>
        </div>
      </div>
  
      <div class="flower flower--2">
        <div class="flower__leafs flower__leafs--2">
          <div class="flower__leaf flower__leaf--1"></div>
          <div class="flower__leaf flower__leaf--2"></div>
          <div class="flower__leaf flower__leaf--3"></div>
          <div class="flower__leaf flower__leaf--4"></div>
          <div class="flower__white-circle"></div>
  
          <div class="flower__light flower__light--1"></div>
          <div class="flower__light flower__light--2"></div>
          <div class="flower__light flower__light--3"></div>
          <div class="flower__light flower__light--4"></div>
          <div class="flower__light flower__light--5"></div>
          <div class="flower__light flower__light--6"></div>
          <div class="flower__light flower__light--7"></div>
          <div class="flower__light flower__light--8"></div>
  
        </div>
        <div class="flower__line">
          <div class="flower__line__leaf flower__line__leaf--1"></div>
          <div class="flower__line__leaf flower__line__leaf--2"></div>
          <div class="flower__line__leaf flower__line__leaf--3"></div>
          <div class="flower__line__leaf flower__line__leaf--4"></div>
        </div>
      </div>
  
      <div class="flower flower--3">
        <div class="flower__leafs flower__leafs--3">
          <div class="flower__leaf flower__leaf--1"></div>
          <div class="flower__leaf flower__leaf--2"></div>
          <div class="flower__leaf flower__leaf--3"></div>
          <div class="flower__leaf flower__leaf--4"></div>
          <div class="flower__white-circle"></div>
  
          <div class="flower__light flower__light--1"></div>
          <div class="flower__light flower__light--2"></div>
          <div class="flower__light flower__light--3"></div>
          <div class="flower__light flower__light--4"></div>
          <div class="flower__light flower__light--5"></div>
          <div class="flower__light flower__light--6"></div>
          <div class="flower__light flower__light--7"></div>
          <div class="flower__light flower__light--8"></div>
  
        </div>
        <div class="flower__line">
          <div class="flower__line__leaf flower__line__leaf--1"></div>
          <div class="flower__line__leaf flower__line__leaf--2"></div>
          <div class="flower__line__leaf flower__line__leaf--3"></div>
          <div class="flower__line__leaf flower__line__leaf--4"></div>
        </div>
      </div>
  
      <div class="grow-ans" style="--d:1.2s">
        <div class="flower__g-long">
          <div class="flower__g-long__top"></div>
          <div class="flower__g-long__bottom"></div>
        </div>
      </div>
  
      <div class="growing-grass">
        <div class="flower__grass flower__grass--1">
          <div class="flower__grass--top"></div>
          <div class="flower__grass--bottom"></div>
          <div class="flower__grass__leaf flower__grass__leaf--1"></div>
          <div class="flower__grass__leaf flower__grass__leaf--2"></div>
          <div class="flower__grass__leaf flower__grass__leaf--3"></div>
          <div class="flower__grass__leaf flower__grass__leaf--4"></div>
          <div class="flower__grass__leaf flower__grass__leaf--5"></div>
          <div class="flower__grass__leaf flower__grass__leaf--6"></div>
          <div class="flower__grass__leaf flower__grass__leaf--7"></div>
          <div class="flower__grass__leaf flower__grass__leaf--8"></div>
          <div class="flower__grass__overlay"></div>
        </div>
      </div>
  
      <div class="growing-grass">
        <div class="flower__grass flower__grass--2">
          <div class="flower__grass--top"></div>
          <div class="flower__grass--bottom"></div>
          <div class="flower__grass__leaf flower__grass__leaf--1"></div>
          <div class="flower__grass__leaf flower__grass__leaf--2"></div>
          <div class="flower__grass__leaf flower__grass__leaf--3"></div>
          <div class="flower__grass__leaf flower__grass__leaf--4"></div>
          <div class="flower__grass__leaf flower__grass__leaf--5"></div>
          <div class="flower__grass__leaf flower__grass__leaf--6"></div>
          <div class="flower__grass__leaf flower__grass__leaf--7"></div>
          <div class="flower__grass__leaf flower__grass__leaf--8"></div>
          <div class="flower__grass__overlay"></div>
        </div>
      </div>
  
      <div class="grow-ans" style="--d:2.4s">
        <div class="flower__g-right flower__g-right--1">
          <div class="leaf"></div>
        </div>
      </div>
  
      <div class="grow-ans" style="--d:2.8s">
        <div class="flower__g-right flower__g-right--2">
          <div class="leaf"></div>
        </div>
      </div>
  
      <div class="grow-ans" style="--d:2.8s">
        <div class="flower__g-front">
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--1">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--2">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--3">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--4">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--5">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--6">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--7">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__leaf-wrapper flower__g-front__leaf-wrapper--8">
            <div class="flower__g-front__leaf"></div>
          </div>
          <div class="flower__g-front__line"></div>
        </div>
      </div>
  
      <div class="grow-ans" style="--d:3.2s">
        <div class="flower__g-fr">
          <div class="leaf"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--1"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--2"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--3"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--4"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--5"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--6"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--7"></div>
          <div class="flower__g-fr__leaf flower__g-fr__leaf--8"></div>
        </div>
      </div>
  
      <div class="long-g long-g--0">
        <div class="grow-ans" style="--d:3s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:2.2s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:3.4s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:3.6s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
  
      <div class="long-g long-g--1">
        <div class="grow-ans" style="--d:3.6s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:3.8s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:4s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:4.2s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
  
      <div class="long-g long-g--2">
        <div class="grow-ans" style="--d:4s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:4.2s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:4.4s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:4.6s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
  
      <div class="long-g long-g--3">
        <div class="grow-ans" style="--d:4s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:4.2s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:3s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:3.6s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
  
      <div class="long-g long-g--4">
        <div class="grow-ans" style="--d:4s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:4.2s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:3s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:3.6s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
  
      <div class="long-g long-g--5">
        <div class="grow-ans" style="--d:4s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:4.2s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:3s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:3.6s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
  
      <div class="long-g long-g--6">
        <div class="grow-ans" style="--d:4.2s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:4.4s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:4.6s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:4.8s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
  
      <div class="long-g long-g--7">
        <div class="grow-ans" style="--d:3s">
          <div class="leaf leaf--0"></div>
        </div>
        <div class="grow-ans" style="--d:3.2s">
          <div class="leaf leaf--1"></div>
        </div>
        <div class="grow-ans" style="--d:3.5s">
          <div class="leaf leaf--2"></div>
        </div>
        <div class="grow-ans" style="--d:3.6s">
          <div class="leaf leaf--3"></div>
        </div>
      </div>
    </div>
    
    <script src="main.js"></script>
  </body>
</html>
