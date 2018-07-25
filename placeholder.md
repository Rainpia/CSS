### 对于IE来说，顺序很重要，要先 input 后 placeholder

```
input{
    color: red;
}
::-webkit-input-placeholder { /* WebKit, Blink, Edge */
  color:    #979797;
}
:-moz-placeholder { /* Mozilla Firefox 4 to 18 */
  color:   #979797;
  opacity:  1;
}
::-moz-placeholder { /* Mozilla Firefox 19+ */
  color:    #979797;
  opacity:  1;
}
:-ms-input-placeholder { /* Internet Explorer 10-11 */
  color:   #979797;
}
```