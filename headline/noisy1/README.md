# html
```html
<div class="content">
  <div class="noisy1-wrapper">
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar-second-wrapper">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div>
    <div class="main-text">sample-text</div>
  </div>
</div>

```

# css

```css
.noisy1-wrapper {
  position: relative;
  overflow: hidden;
  height: 2em;

.noisy1-wrapper>.bar {
  position: relative;
  z-index: 2;
  width: 100%;
  height: 30%;

.noisy1-wrapper>.bar-second-wrapper {
  position: absolute;
  top: 0;
  height: 100%;
  width: 100%;

/*CHANGE BACKGROUND COLOR*/
.noisy1-wrapper .bar::after {
  position: absolute;
  content: '';
  height: 100%;
  background-color: black;
  animation-timing-function: ease;
  animation-iteration-count: 1;
  border-radius: 25px;

.bar:nth-child(1)::after {
  animation-duration: 0.8s;
  animation-delay: 0s;
  animation-name: shrink-right1;

.bar:nth-child(2)::after {
  animation-name: shrink-left1;
  animation-duration: 0.6s;
  animation-delay: 0.1s;

.bar:nth-child(3)::after {
  animation-name: shrink-right2;
  animation-duration: 0.4s;
  animation-delay: 0.2s;

.bar:nth-child(4)::after {
  animation-name: shrink-left2;
  animation-duration: 0.6s;
  animation-delay: 0.3s;

.bar-second-wrapper>.bar:nth-child(1)::after 
  animation-name: shrink-left1;
  animation-duration: 0.6s;
  animation-delay: 0.4s;

.bar-second-wrapper>.bar:nth-child(2)::after {
  animation-name: shrink-right2;
  animation-duration: 0.6s;
  animation-delay: 0.4s;

.bar-second-wrapper>.bar:nth-child(3)::after {
  animation-name: shrink-right2;
  animation-duration: 0.7s;
  animation-delay: 0.2s;

.bar-second-wrapper>.bar:nth-child(4)::after {
  animation-name: shrink-right1;
  animation-duration: 1s;
  animation-delay: 0.4s;

@keyframes shrink-right1 {
  0% {
    width: 100%;
    right: 90%;
  
  100% {
    width: 100%;
    right: -120%;
  }

@keyframes shrink-right2 {
  0% {
    width: 100%;
    right: 70%;
  
  100% {
    width: 100%;
    right: -160%;
  }

@keyframes shrink-left1 {
  0% {
    width: 100%;
    left: 80%;
  
  100% {
    width: 100%;
    left: -120%;
  }

@keyframes shrink-left2 {
  0% {
    width: 100%;
    left: 60%;
  
  100% {
    width: 100%;
    left: 100%;
  }

/*text style*/
/*CHANGE font indivisualy*/
.noisy1-wrapper>.main-text {
  z-index: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  animation: 1.2s ease 0s 1 fade-in;

@keyframes fade-in {
  0% {
    opacity: 0;
  
  40% {
    opacity: 0;
  
  100% {
    opacity: 1;
  }
}
```