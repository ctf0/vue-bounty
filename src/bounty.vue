<template>
    <span/>
</template>

<script>
import bounty from 'bounty'

export default {
    props: {
        initialValue: {
            type: Number,
            default: 0,
            required: false
        },
        value: {
            type: Number,
            default: 0,
            required: true
        },
        animationDelay: {
            type: Number,
            default: 100,
            required: false
        },
        letterAnimationDelay: {
            type: Number,
            default: 100,
            required: false
        }
    },
    mounted() {
        this.init(this.value, this.initialValue)
    },
    methods: {
        init(val, old) {
            return bounty({
                el: this.$el,
                value: val,
                initialValue: old,
                lineHeight: 1,
                letterSpacing: 1,
                animationDelay: this.animationDelay,
                letterAnimationDelay: this.letterAnimationDelay
            })
        }
    },
    watch: {
        value(val, oldVal) {
            this.init(val, oldVal || 0)
        }
    },
    render() {}
}
</script>