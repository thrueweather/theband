<template>
    <footer class="footer">
        <div class="container wrapp">
            <div class="footer-wrapp-title">
                <div class="footer-title">
                    <h1>contact</h1>
                    <h2>+48 202 - 555 - 0114</h2>
                </div>
                <div class="footer-form">
                    <form>
                        <button>subscribe</button>
                        <input type="text"/>
                    </form>
                    <div class="social">
                        <a href=""><img src="../assets/facebook.png" alt=""></a>
                        <a href=""><img src="../assets/youtube.png" alt=""></a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom-nav">
                <div class="copyright"><p>Copyright 2015 © by The Band</p></div>
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
        </div>
    </footer>
</template>

<script>
export default {
    
}
</script>


<style lang="sass" scoped>
$FONT_OSWALD: 'Oswald', sans-serif
$FONT_FAMILY_LORA: 'Lora', sans-serif
$DEFAULT_COLOR: #e4dddb
$TEXT_COLOR: #241c18

.footer 
    background: url('../assets/footer.png') no-repeat
    background-size: cover
    background-position: center
    .wrapp 
        display: flex
        flex-direction: column
        justify-content: space-between
        height: 100vh
        padding: 0 0 40px 0 
        .footer-wrapp-title
            text-align: center
            .footer-title
                margin: 0 170px 40px 170px
                line-height: 90px
                font-family: $FONT_OSWALD
                border-bottom: 3px dotted $DEFAULT_COLOR
                padding: 60px 60px 30px 60px
                h1 
                    margin: 0
                    font-size: 80px
                    letter-spacing: 5px
                    text-transform: uppercase
                    color: #241c18
                h2 
                    margin: 0
                    font-size: 72px
                    color: $DEFAULT_COLOR
            .footer-form
                display: flex
                margin: 0 220px
                form
                    display: flex
                    width: 526px
                    margin: auto
                    border: 5px solid #241c18
                    font-family: $FONT_OSWALD
                    button 
                        width: auto 
                        font-size: 36px
                        text-transform: uppercase
                        border: none
                        outline: none
                        background-color: #241c18
                        color: $DEFAULT_COLOR
                        padding: 0 20px
                        cursor: pointer
                    input
                        width: 100%
                        border: none
                        outline: none
                        background: none
                        padding-left: 20px
                .social 
                    a 
                        padding: 0 10px
        .footer-bottom-nav
            display: flex
            justify-content: space-between
            align-items: center
            .copyright
                p 
                    margin: 0
                    font-size: 18px
                    text-transform: uppercase
                    font-family: $FONT_FAMILY_LORA
                    font-weight: 600
                    color: $DEFAULT_COLOR
            nav 
                ul 
                    margin: 0
                    padding: 0
                    li
                        display: inline-block
                        padding: 0 10px
                        position: relative
                        a 
                            text-decoration: none
                            text-transform: uppercase
                            color: $DEFAULT_COLOR
                            font-family: $FONT_FAMILY_LORA
                            font-weight: 600
                            span 
                                margin-left: 5px
                                color: $DEFAULT_COLOR
                        &:hover::after
                            content: ""
                            position: absolute
                            top: 40px
                            left: 0
                            bottom: 0
                            right: 0
                            width: 50px
                            height: 17px
                            margin: auto
                            background: url("../assets/nav-hover.png") 0 0 no-repeat

@media only screen and (max-width : 991px)
    .footer 
        .wrapp 
            .footer-wrapp-title 
                .footer-title
                    margin: 0 0 40px 0
                    padding: 60px 0 30px 0
                .footer-form
                    margin: 0
            .footer-bottom-nav
                flex-direction: column
                text-align: center
                .copyright
                    margin-bottom: 20px

@media only screen and (max-width: 991px)
    .footer .wrapp 
        height: auto

@media only screen and (max-width : 767px)
    .footer 
        .wrapp 
            .footer-wrapp-title 
                .footer-title 
                    h1 
                        font-size: 60px
                    h2
                        font-size: 52px
                .footer-form 
                    form 
                        width: 326px
                        button
                            font-size: 20px

@media only screen and (max-width : 469px)
    .footer 
        .wrapp 
            .footer-wrapp-title 
                .footer-title 
                    h1
                        font-size: 50px
                    h2 
                        font-size: 32px
                .footer-form
                    flex-direction: column
                    form 
                        margin: 0 auto 40px auto
                        width: 300px
        .footer-bottom-nav
            padding-top: 20px

</style>
