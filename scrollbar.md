###  自定义scroll bar 对不同浏览器

#### IE

- 基本设置

```
div{
    -ms-overflow-style: -ms-autohiding-scrollbar;
  scrollbar-base-color: #262627;
  scrollbar-3dlight-color: #262627;
  scrollbar-highlight-color: #262627;
  scrollbar-track-color: #262627;
  scrollbar-arrow-color: #262627;
  scrollbar-shadow-color: #262627;
}
```

- if need remove the scrollbar

```
div{
   -ms-overflow-style:none; 
}
```

#### Chrome

- 基本设置

```
div::-webkit-scrollbar {
    display: block;
    width: 10px;
}
div::-webkit-scrollbar-thumb:vertical {
    background-color: #262627;
  }
```

- if need remove the scrollbar

```
div::-webkit-scrollbar {
    display: none;
}
```
