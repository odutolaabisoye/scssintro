# Install Sass Compiler Plugin
# Configure from setting by chnaging "savePath": "/dist/css"

# Nesting
``` css
    .main{
        width: 80%;
        margin: 0 auto;
        p{
            color: $text-color;
            font-weight: map-get($map: $font-weight, $key: medium);
        }
        #{&}_paragraph {
            color: $accent-color;
            font-weight: map-get($map: $font-weight, $key: bold);
            &:hover {
                color: purple;
            }
        }
    }
```

# Map
```css
    font-weight: map-get($map: $font-weight, $key: medium);
```
# Partials
    <!-- Partial file name always starts from _ <br>
    You import a partials like this <br> -->
```css
    @import './variables';
```

# Functions

<!-- Here is the Function<br> -->
```css
@function weight($weight-name){
    @return $weight-name;
}
```

<!-- You can call it like this<br> -->
```css
.main p {
  color: red;
  font-weight: bold; -->   Here
  }
```
# Mixin
```css
@mixin flexCenter() {
    display: flex;
    justify-content: center;
    align-items: center;
}

```
<!-- Call it Like  <br> -->
```css
.main{
    @include flexCenter; --> here
    width: 80%;
    margin: 0 auto;
    p{
        color: $text-color;
        font-weight: weight(regular);
    }
    #{&}_paragraph {
        color: $accent-color;
        font-weight: map-get($map: $font-weight, $key: bold);
        &:hover {
            color: purple;
        }
    }
}
```
<!-- Another waay to use mixen with if statement -->
```css
@mixin theme($light-theme: true) {
    @if $light-theme {
        background: $primary-color;
        color: $text-color;
    }
}
```

<!--You can call it out like this -->

```css
.light {
    @include theme ($light-theme: true);
}
```