# html

```html
  <div class="blockout">
    <div class="text-box">sample text</div>
  </div>
```

# css
```css

.blockout{
  position:relative;
  display: inline-block;
  padding:2em;/*free change*/
  overflow: hidden;
  box-sizing: content-box;
}

.blockout::after{
  content:"";
  position:absolute;
  top:0;
  left:0;
  height:100%;
  background-color:#2e2e2e;
  animation: 1.5s ease-in 0s blockout-right 1;
}

.blockout > .text-box{
  opacity:auto;
}

@keyframes blockout-right{
  0%{
    left:0;
    width:100%;
  }
  30%{
    left:0;
    width:100%;
  }
  60%{
    left:100%;
    width:0%;
  }
}
```