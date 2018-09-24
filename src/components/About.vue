<template>
    <div class="About">
        <div class="container">
            <div class="Band-wrapp">
                <div class="Band-opacity">
                    <p>Lawrie Alton <span>&#9679;</span> vocalist</p>
                    <p>Charles Timmy <span>&#9679;</span> guitar</p>
                    <p>curt sheard <span>&#9679;</span> bass</p>
                    <p>Cade Ryker <span>&#9679;</span> drums</p>
                    <p>Tommie Brendan <span>&#9679;</span> electronics</p>
                </div>
                <div class="Band-members">
                    <p v-bind:style="{ opacity: 0.3}">Lawrie Alton <span>&#9679;</span> vocalist</p>
                    <p v-bind:style="{ opacity: 0.3}">Charles Timmy <span>&#9679;</span> guitar</p>
                    <p v-bind:style="{ opacity: 1}">curt sheard <span>&#9679;</span> bass</p>
                    <p v-bind:style="{ opacity: 0.3}">Cade Ryker <span>&#9679;</span> drums</p>
                    <p v-bind:style="{ opacity: 0.3}">Tommie Brendan <span>&#9679;</span> electronics</p>
                </div>
            </div>
            <div class="About-wrapp">
                <div class="Artist-name">
                    <h1>Curt</h1>
                    <h2>Sheard</h2>
                </div>
                <div class="About-text">
                    <h3>Meet our band</h3>
                    <p>
                        Court Sheard, swag iPhone neutra williamsburg, 
                        sriracha you probably haven't heard of them PBR&B marfa seitan. 
                        Four dollar toast wayfarers helvetica etsy, affogato pinterest schlitz. 
                        Squid yr mlkshk, pinterest pour-over polaroid photo booth. Yr fixie plaid kogi.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="sass">
$DEFAULT_COLOR: #826b60
$FONT_FAMILY_OSWALD: 'Oswald', sans-serif
$FONT_FAMILY_LORA: 'Lora', sans-serif

.About
    background-image: url('../assets/curt.png')
    background-size: cover
    background-position: center
    padding: 80px
    .Band-wrapp
        display: flex
        justify-content: center
        align-items: center
        margin-bottom: 100px
        .Band-opacity
            opacity: 0
            width: 69%
        .Band-members
            width: auto
            transform: rotate(-90deg)
            text-transform: uppercase
            text-align: center
            color: $DEFAULT_COLOR
            p
                letter-spacing: 3px
                font-family: $FONT_FAMILY_OSWALD
                font-size: 10px
                font-weight: 500
                span 
                    font-size: 17px
    .About-wrapp
        display: flex
        align-items: center
        .Artist-name
            width: 70%
            text-transform: uppercase
            text-align: center
            line-height: 15px
            h1 
                font-size: 90px
                color: #826b60
                font-family: $FONT_FAMILY_OSWALD
            h2 
                font-size: 80px
                color: #241c18
                font-family: $FONT_FAMILY_OSWALD
        .About-text
            width: 30%
            text-align: center
            h3 
                margin: 0 0 20px 0
                font-family: $FONT_FAMILY_OSWALD
                font-size: 36px
                font-weight: 400
                color: #241c18
            p 
                margin: 0
                font-family: $FONT_FAMILY_LORA
                text-align: left
                font-size: 14px
                line-height: 35px

@media only screen and (max-width : 991px) 
        .About .Band-wrapp .Band-opacity
            display: none
        .About .Band-wrapp 
            margin: 0
            .Band-members
                transform: rotate(0deg)
        .About .About-wrapp
            flex-direction: column
            .Artist-name 
                width: 100%
            .About-text
                width: 100%
                p
                    text-align: center
@media only screen and (max-width : 767px)
    .About
        padding: 60px 0
</style>
