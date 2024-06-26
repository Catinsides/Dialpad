<script setup>
import { defineEmits } from 'vue';

const emit = defineEmits(['key']);

const handleClick = (e) => {
    let isKey = e.target.classList.contains("key");
    if (!isKey) return

    let rel = e.target.getAttribute("rel");

    emit("key", rel);
}
</script>

<template>
    <div id="phone">
        <div id="wrapper" @click="handleClick">
            <div class="key" rel="1">1</div>
            <div class="key" rel="2">2<span>abc</span></div>
            <div class="key" rel="3">3<span>def</span></div>
            <div class="clear"></div>
            <div class="key" rel="4">4<span>ghi</span></div>
            <div class="key" rel="5">5<span>jkl</span></div>
            <div class="key" rel="6">6<span>mno</span></div>
            <div class="clear"></div>
            <div class="key" rel="7">7<span>pqrs</span></div>
            <div class="key" rel="8">8<span>tuv</span></div>
            <div class="key" rel="9">9<span>wxyz</span></div>
            <div class="clear"></div>
            <div class="key special" rel="*">*</div>
            <div class="key" rel="1">0<span>oper</span></div>
            <div class="key special" rel="#">#</div>
            <div class="clear"></div>
            <div class="key nb"></div>
            <div class="key phone" rel="Make Call"><i class="fa fa-phone"></i></div>
            <div class="key nb"></div>
            <div class="clear"></div>
        </div>
    </div>
</template>

<style scoped>
@import url(//fonts.googleapis.com/css?family=Lato:100,300);
@import url(//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css);

#phone {
    font-family: 'Lato', sans-serif;
    font-weight: 300;

    background: url(https://blogs.which.co.uk/technology/files/2013/03/iphone_5_hero.jpg) no-repeat 50.4% top;
    background-size: contain;
    height: 655px;
}

#wrapper {
    width: 252px;
    height: 410px;
    margin: 0 auto 0 auto;
    position: relative;
    top: 116px;
    padding: 24px 0 0 0;
    background: #fff;
}

.key {
    border-radius: 50px 50px 50px 50px;
    color: #444;
    width: 70px;
    height: 70px;
    text-align: center;
    font-size: 30px;
    float: left;
    box-sizing: border-box;
    padding: 5px 0 0 0;
    margin: 0 7px 10px 7px;
    border: 1px solid #444;
    cursor: pointer;
}

.key span {
    display: block;
    color: #444;
    text-align: center;
    font-size: 12px;
    text-transform: uppercase;
}

.key.special {
    line-height: 60px;
}

.key.nb {
    border: none;
}

.key.phone {
    background: #5CDB74;
    border: none;
    color: #FFF;
    line-height: 60px;
    font-size: 40px;
}

.key:hover {
    background-color: rgba(0, 0, 0, 0.05);
    transition: background-color 0.3s ease-in-out;
}

.key.phone:hover {
    background-color: rgba(92, 219, 116, 0.75);
    transition: background-color 0.3s ease-in-out;
}

.clear {
    clear: both;
}
</style>
