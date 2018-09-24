<template>
    <div class="Music">
        <div class="container">
            <div class="Music-wrapp">
                <div class="Music-discography-wrapp">
                    <img src="../assets/cover.png" alt="">  
                    <div class="discography">
                        <h3>Discography</h3>
                        <div class="albums">
                            <div class="albums-item">
                                <h3>Surprise Without Flaws</h3>
                                <span>&#9679;</span>
                                <p>2015</p>
                                <button class="usten">usten</button>
                                <button class="buy">buy</button>
                            </div>
                            <div class="albums-item">
                                <h3>Mists Of A Shadow</h3>
                                <span>&#9679;</span>
                                <p>2014</p>
                                <button class="usten">usten</button>
                                <button class="buy">buy</button>
                            </div>
                            <div class="albums-item">
                                <h3>Heroes Of The Sun</h3>
                                <span>&#9679;</span>
                                <p>2013</p>
                                <button class="usten">usten</button>
                                <button class="buy">buy</button>
                            </div>
                            <div class="albums-item">
                                <h3>Picure Of The Past</h3>
                                <span>&#9679;</span>
                                <p>2012</p>
                                <button class="usten">usten</button>
                                <button class="buy">buy</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="Music-paying-wrapp">
                    <div class="playing">
                        <h2>Now playing</h2>
                        <p>01. Clouds In The Forest</p>
                    </div>
                    <div class="controls">
                        <button class="rewind"><img src="../assets/Rewind.png" alt=""></button>
                        <button class="pause"><img v-bind:style="{width: '31px'}" src="../assets/Pause.png" alt=""></button>
                        <button class="forward"><img src="../assets/Forward.png" alt=""></button>
                        <input type="range" min="0" max="100" value="40">
                    </div>
                    <div class="songs">
                        <h3>Surprise Without Flaws</h3>
                        <div class="list" v-for="(item, index) in songs" :key="index"
                            v-bind:style="{opacity: item.active ? 1 : 0.5}">
                            <h3>&#9658; {{item.title}}</h3>
                            <p><span>. . . . . . . . . . . . . . . . . . . . . .</span> {{item.time}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        songs: [{
            id: 1,
            title: '01. Clouds In The Forest',
            time: '3:20',
            active: true
        }, {
            id: 2,
            title: '02. Rat In The River',
            time: '2:48',
            active: false
        }, {
            id: 3,
            title: '03. Giants And Companions',
            time: '2:27',
            active: false
        }, {
            id: 4,
            title: '04. Ashamed Of Light',
            time: '3:32',
            active: false
        }, {
            id: 5,
            title: '05. Doubting The Forest',
            time: '2:40',
            active: false
        }, {
            id: 6,
            title: '06. Criminals Of The Lake',
            time: '2:55',
            active: false
        }, {
            id: 7,
            title: '07. Curse Of Eternity',
            time: '1:33'
        }, {
            id: 8,
            title: '08. Fog In My Town',
            time: '1:33',
            active: false
        }, {
            id: 9,
            title: '09. Serpent In The Mountains',
            time: '3:24',
            active: false
        }]
    })
}
</script>


<style lang="sass">
    .Music
        padding: 80px 0
        background-color: #f8f8f8
        .Music-wrapp
            display: flex
            flex-direction: row
            .Music-discography-wrapp
                font-family: "Oswald", sans-serif
                .discography
                    margin-left: 60px
                    h3 
                        font-size: 36px
                        font-weight: 400
                    .albums
                        display: flex
                        flex-direction: column
                        .albums-item
                            display: flex
                            align-items: center
                            margin: 7px 0
                            h3 
                                width: 284px
                                margin: 0
                                font-size: 36px
                                font-weight: 100
                            span 
                                color: #e4dddb
                                margin: 0 10px
                            p 
                                margin: 0 10px
                                font-weight: 100
                            button 
                                margin: 0 10px
                                padding: 8px 10px
                                border: none 
                                color: white
                                cursor: pointer
                                text-transform: uppercase
                                font-weight: 600
                            .usten
                                background-color: #e4dddb
                            .buy 
                                background-color: #826b60
            .Music-paying-wrapp
                width: 100%
                padding-left: 100px
                font-family: "Oswald", sans-serif 
                .playing
                    h2 
                        margin: 0 0 60px 0
                        font-size: 36px 
                        font-weight: 400
                    p 
                        margin: 10px 0 30px 0
                        font-size: 18px
                        font-family: "Lora", sans-serif
                        font-style: italic
                        color: #826b60
                .controls
                    width: 100%
                    margin: 0 0 80px 0
                    text-align: center
                    button 
                        margin: 0 30px 20px 30px
                        border: none
                        background: none
                        cursor: pointer
                        img 
                            width: 52px
                            height: 31px
                .songs
                    font-family: "Oswald", sans-serif 
                    h3 
                        font-size: 30px
                        font-weight: 300
                    .list 
                        display: flex
                        justify-content: space-between
                        align-items: center
                        margin: 5px 0
                        font-family: "Lora", sans-serif
                        color: #826b60
                        h3 
                            margin: 0
                            font-size: 18px
                            font-style: italic
                            img
                                cursor: pointer
                        p
                            margin: 0
                            span 
                                margin: 0 0 0 20px
                                font-size: 10px

    @media only screen and (max-width : 991px) 
        .Music .Music-wrapp
            flex-direction: column
            .Music-discography-wrapp
                text-align: center
                img
                    width: 100%
                .discography
                    margin: 0
                    .albums
                        justify-content: center
                        align-items: center
            .Music-paying-wrapp
                padding: 0
                text-align: center
                .playing
                    h2 
                        margin: 40px 0 0 0
    
    @media only screen and (max-width : 520px) 
        .Music .Music-wrapp .Music-discography-wrapp .discography .albums .albums-item h3
            width: auto
            font-size: 26px
    
    @media only screen and (max-width : 468px) 
        .Music .Music-wrapp .Music-discography-wrapp .discography .albums .albums-item
            flex-direction: column
            margin: 0
            padding: 10px 0
            border-bottom: 1px solid black
            .buy
                width: 66px
            &:last-child
                border: none
        .Music .Music-wrapp .Music-paying-wrapp .controls button
            margin: 0 10px 20px 10px
        .Music .Music-wrapp .Music-paying-wrapp .songs .list 
            h3 
                font-size: 16px
            span
                display: none
</style>  