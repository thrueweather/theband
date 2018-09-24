<template>
    <div class="Tours">
        <div class="container">
            <div class="Tours-title">
                <h1>Tour dates</h1>
            </div>
            <div class="Tours-wrapp">
                <div class="concerts">
                    <ul>
                        <li v-for="(concert, index) in concerts" :key="index">
                            <div class="concert-wrapp">
                                <div class="text" v-bind:style="{color: concert.color}">
                                    {{concert.title}}
                                    <br/>
                                    {{concert.city}}
                                </div>
                                <div class="dot" v-bind:style="{color: concert.color}">&#11044;</div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="Tickets">
                <div class="Tickets-wrapp" v-for="(ticket, index) in tickets" :key="index">
                    <div class="left">
                        <div class="date">
                            <h1>{{ticket.day}}</h1>
                            <h3><span>{{ticket.month}}</span> <br/> {{ticket.year}}</h3>
                        </div>
                        <div class="title">
                            <h2>{{ticket.title}}</h2>
                        </div> 
                    </div>
                    <div class="right">
                        <button>buy tickets</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        concerts: [
            {id: 1, title: 'ALEXANDRA PALACE, 10/03/2015', city: 'LONDON, UNITED KINGDOM', color: '#e4dddb'},
            {id: 2, title: 'FIELD DAY, 14/04/2015', city: 'SYDNEY, AUSTRALIA', color: '#e4dddb'},
            {id: 3, title: 'SYDNEY OPERA HOUSE, 18/04/2015', city: 'SYDNEY, AUSTRALIA', color: '#e4dddb'},
            {id: 4, title: 'HEINEKEN MUSIC HALL, 02/05/2015', city: 'AMSTERDAM, HOLLAND', color: '#e4dddb'},
            {id: 5, title: 'FOREST NATIONAL, 07/06/2015', city: 'BRUSSELS, BELGIUM', color: '#e4dddb'},
            {id: 6, title: 'SPORTHALLE, 07/10/2015', city: 'HAMBURG, GERMANY', color: '#e4dddb'},
            {id: 7, title: 'TAP 1, today', city: 'COPENHAGEN, DENMARK', color: '#241c18'},
            {id: 8, title: 'COLUMBIANHALLE, 16/12/2015', city: 'BERLIN, GERMANY', color: '#826b60'},
            {id: 9, title: 'Torwar, 19/12/2015', city: 'WARSAW, POLAND', color: '#826b60'},
            {id: 10, title: 'MEDIOLANUM FORUM, 16/01/2016', city: 'MILAN, ITALY', color: '#826b60'},
            {id: 11, title: 'ZENITH, 23/02/2016', city: 'PARIS, FRANCE', color: '#826b60'},
            {id: 12, title: 'ALEXANDRA PALACE, 14/03/2016', city: 'LONDON, UK', color: '#826b60'},
        ].reverse(),
        tickets: [
            {id: 1, day: 12, month: 'dec', year: '2015', title: 'Tap 1 // Copenhagen, Denmark'},
            {id: 2, day: 16, month: 'dec', year: '2015', title: 'Columbianhalle  // Berlin, Germany'},
            {id: 3, day: 19, month: 'dec', year: '2015', title: 'Torwar  // Warsaw, Poland'},
            {id: 4, day: 12, month: 'dec', year: '2015', title: 'Tap 1 // Copenhagen, Denmark'},
            {id: 5, day: 16, month: 'dec', year: '2015', title: 'Columbianhalle  // Berlin, Germany'},
            {id: 6, day: 19, month: 'dec', year: '2015', title: 'Torwar  // Warsaw, Poland'},
        ]
    })
}
</script>


<style lang="sass" scoped>
$FONT_OSWALD: 'Oswald', sans-serif

.Tours
    background-color: #f1eeed
    padding: 60px 0
    .Tours-title
        text-align: center
        font-family: $FONT_OSWALD
        h1
            font-size: 36px
            margin: 0
    .Tours-wrapp
        height: 400px
        .concerts
            width: 50%
            margin: auto
            transform: rotate(-270deg)
            text-align: right
            ul
                margin: 0
                padding: 0
                border-left: 3px solid #e4dddb
                li 
                    display: flex;
                    justify-content: flex-end
                    margin: 0
                    list-style: none
                    transform: rotate(180deg)
                    padding: 10px 0
                    font-size: 16px
                    .concert-wrapp
                        display: flex
                        justify-content: right
                        align-items: center
                        position: relative
                        .text 
                            padding-right: 20px
                        .dot
                            position: absolute
                            right: -10px
    .Tickets
        max-height: 300px
        overflow: auto
        .Tickets-wrapp
            display: flex
            justify-content: space-between
            align-items: center
            border-bottom: 3px dotted #826b60
            margin: 0 40px
            padding: 0 40px
            .left
                display: flex
                align-items: center
                font-family: $FONT_OSWALD
                .date 
                    height: 50px
                    display: flex
                    align-items: center
                    padding-right: 20px
                    border-right: 5px solid #e4dddb
                    h1 
                        margin: 0
                        font-size: 50px
                        font-weight: bold
                    h3
                        margin: 0
                        font-size: 23px
                        font-weight: bold
                        text-transform: uppercase
                        line-height: 26px
                        span 
                            position: relative
                            top: 3.5px
                .title
                    margin-left: 20px
                    h2
                        font-size: 30px
                        font-weight: 300
            .right
                button 
                    background-color: #826b60
                    margin: 0 10px
                    padding: 8px 10px
                    border: none
                    color: white
                    cursor: pointer
                    text-transform: uppercase
                    font-size: 14px
                    font-weight: 600

@media only screen and (max-width : 991px)
    .Tours .Tours-wrapp .concerts
        width: 80%

@media only screen and (max-width : 767px)
    .Tours 
        .Tickets
            max-height: 100px
            .Tickets-wrapp
                padding: 0
                .concerts
                    width: 100%
    .Tours .Tickets .Tickets-wrapp .left .title h2
        font-size: 18px
    .Tours .Tickets .Tickets-wrapp
        margin: 0
        .right
            button 
                margin: 0
                font-size: 12px
@media only screen and (max-width : 675px)
    .Tours 
        .Tours-wrapp
            height: 100%
            .concerts
                text-align: left
                transform: rotate(0deg)
                padding: 40px 0
                ul 
                    li
                        justify-content: flex-start
                        transform: rotate(0deg);
                        .concert-wrapp
                            .dot 
                                right: 0
                                left: -10px
                            .text 
                                padding-right: 0
                                padding-left: 30px
@media only screen and (max-width : 480px)
    .Tours 
        .Tickets
            max-height: 200px
            .Tickets-wrapp
                flex-direction: column
                padding: 10px 0


</style>   
