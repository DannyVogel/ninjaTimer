<template>
    <div>
        <p>Your reaction time: {{ score }}ms</p>
        <p class="rank">Your rank: {{ rank }}</p>
    </div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Ninja';
        } else if (this.score < 400) {
            this.rank = 'Samurai';
        } else {
            this.rank = 'Slowpoke...'
        }
    },
}
</script>

<style>
.rank {
    font-size: 2em;
    color: #0faf87;
    font-weight: bold;
}
</style>