<template>
    <div id="app" class="app">
        <Header/> 
        <About/>
        <Music/>
        <Tours/>
        <Footer/>
    </div>
</template>

<script>

import Header from './components/Header'
import About from './components/About'
import Music from './components/Music'
import Tours from './components/Tours'
import Footer from './components/Footer'

export default {
    name: 'app',
    components: { 
        Header, 
        About, 
        Music,
        Tours,
        Footer
    }
}
</script>


<style lang="sass">
@import url('https://fonts.googleapis.com/css?family=Lora:400,700|Oswald:300,400,500,700');
html, body
    width: 100%
    height: 100%
    margin: 0
.container
    margin-right: auto
    margin-left: auto
    padding-right: 15px
    padding-left: 15px


input[type=range]
    -webkit-appearance: none
    width: 100%

input[type=range]::-webkit-slider-runnable-track     
    height: 5px
    background: #e4dddb
    border: none
    border-radius: 4px

input[type=range]::-webkit-slider-thumb     
    -webkit-appearance: none
    border: none
    height: 20px
    width: 20px
    border-radius: 50%
    background: #826b60
    margin-top: -7px

input[type=range]:focus 
    outline: none

input[type=range]:focus::-webkit-slider-runnable-track 
    background: #ccc

::-webkit-scrollbar-button 
    background-image:url('')
    background-repeat:no-repeat
    width: 0px
    height: 0px
    opacity: 0
::-webkit-scrollbar-track 
    background-color: #eeeeee86
::-webkit-scrollbar-thumb 
    -webkit-border-radius: 0px
    background-color: #cbc2bd
    &:hover
        background-color: #826b60
::-webkit-resizer
    background-image:url('')
    background-repeat: no-repeat
    width: 0px 
    height: 0px
::-webkit-scrollbar 
    width: 15px

@media (min-width: 576px)
  .container
    max-width: 540px
@media (min-width: 768px)
  .container
    max-width: 720px
@media (min-width: 992px)
  .container
    max-width: 960px
@media (min-width: 1200px)
  .container
    max-width: 1170px
</style>