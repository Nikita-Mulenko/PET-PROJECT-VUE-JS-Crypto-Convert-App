<script>
  export default {
    props: {
        setCrypto: {
            type: Function,
            required: true
        },
        cryptoNow: {
            type: String,
            required: true
        }
    },
  }
</script>


<template>
    <ul>
        <li @click="setCrypto('BTC')" :className="cryptoNow == 'BTC' ? 'active' : ''">Bitcoin</li>
        <li @click="setCrypto('ETH')" :className="cryptoNow == 'ETH' ? 'active' : ''">ETH</li>
        <li @click="setCrypto('USDT')" :className="cryptoNow == 'USDT' ? 'active' : ''">USDT</li>
    </ul>
</template>


<style scoped>
ul{
    list-style: none;
    width: 200px;
    padding: 0;
    border-radius: 3px;
    border: 3px solid;
}
li{
    font-family: 'Calibri';
    display: block;
    background: #1A032D;
    padding: 20px;
    color: #fff;
}
li:hover, li.active{
    background: #3b0964;
    cursor: pointer;
}
</style>