# Sass

Sass - CSS + features + indentations
Scss - Sass with {} - like CSS instead of indentations

## Variables

    $primaryColor: #171717;
    header .btn{
        background: $primaryColor;
    }

## Nesting

    header{
        color: $textColor;
        .btn{
            background: $primaryColor
        }
    }
    button{
        background: $primaryColor;
        &:hover{
            background: #000;
        }
    }

## Organize code in separate files

    Styles (folder)
        _header.scss
        style.scss

        style.scss
            :
            @import "./header";
            :

        _header.scss
            header{
                :
            }

## Function (mixin)

    @mixin flexCenter{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    header{
        :
        @include flexCenter();
    }

    @mixin flexCenter($direction){      // took parameter
        :
        flex-direction: $direction
    }
    footer{
        :
        @include flexCenter(column);
    }

## Inherit (extend)

    footer{
        @extend header;     // inherits all properties of heeader
        :       // overwrite the unnessary/rest styles
    }

## Calculations

    section{
        width: 100% - 20%;
    }
