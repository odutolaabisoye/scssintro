# Install Sass Compiler Plugin
# Configure from setting by chnaging "savePath": "/dist/css"

# Nesting
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


# Map
    font-weight: map-get($map: $font-weight, $key: medium);

# Partials
    Partial file name always starts from _ <br>
    You import a partials like this <br>

    @import './variables';


# Functions

Here is the Function<br>
@function weight($weight-name){
    @return $weight-name;
}

You can call it like this<br>

.main p {
  color: red;
  font-weight: bold; -->   Here
  }

# Mixin
@mixin flexCenter() {
    display: flex;
    justify-content: center;
    align-items: center;
}

//Call it Like  <br>

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


