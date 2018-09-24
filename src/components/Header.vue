<template>
    <header>
        <div class="container">
           <div class="top-nav">
                <nav>
                    <ul>
                        <li><a href="">home</a></li>
                        <li><a href="">about</a></li>
                        <li><a href="">music</a></li>
                        <li><a href="">tours</a></li>
                        <li><a href="">contact</a></li>
                    </ul>
                </nav>
            </div>
            <div class="header-title">
                <div class="header-title-wrapp">
                    <h1>We are</h1>
                    <h2>The Band</h2>
                </div>
            </div>
        </div>
        
    </header>
</template>

<style lang="sass">
$BACKGROUND_HEADER: url('../assets/Guitar Photo.png')
$TEXT_COLOR: #241c18
$DEFAULT_COLOR: #826b60
$NAV_HOVER: url('../assets/nav-hover.png') 100% round round;
$BACKGROUND_WORDS: url('../assets/Background words.png')
$FONT_FAMILY_OSWALD: 'Oswald', sans-serif
$FONT_FAMILY_LORA: 'Lora', sans-serif

header
    height: 100vh
    background-image: $BACKGROUND_HEADER
    background-size: cover
    background-position: center
    position: relative
    .top-nav 
        padding-top: 40px
        nav 
            ul 
                margin: 0
                padding: 0
                li
                    display: inline-block
                    padding: 0 10px
                    a 
                        text-decoration: none
                        text-transform: uppercase
                        color: $TEXT_COLOR
                        font-family: $FONT_FAMILY_LORA
                        font-weight: 600
                        span 
                            margin-left: 5px
                            color: $DEFAULT_COLOR
                    &:hover::after
                        content: ""
                        display: block
                        width: 50px
                        height: 17px
                        margin: auto
                        background: url("../assets/nav-hover.png") 0 0 no-repeat
    .header-title
        position: absolute
        top: 0
        bottom: 0
        right: 8%
        width: 400px
        height: 440px
        margin: auto
        display: flex
        align-items: center
        text-align: center
        background-image: $BACKGROUND_WORDS
        background-size: cover
        .header-title-wrapp
            text-align: center
            text-transform: uppercase
            line-height: 15px
            h1 
                font-size: 90px
                color: #e4dddb
                font-family: $FONT_FAMILY_OSWALD
            h2 
                font-size: 80px
                color: #241c18
                font-family: $FONT_FAMILY_OSWALD

@media only screen and (max-width : 991px) 
    header .top-nav nav ul
        text-align: center
    header .header-title
        top: 0
        left: 0
        right: 0
        bottom: 0
        width: 100%
        height: 100%
        justify-content: center
        background-image: none

@media only screen and (max-width : 480px)
    header .header-title .header-title-wrapp h2
        font-size: 70px
</style>
