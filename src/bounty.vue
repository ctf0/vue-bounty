<template>
    <span class="js-bounty" />
</template>

<script>
import bounty from 'bounty'

export default {
    props: {
        initialValue: {
            type: [String, Number],
            default: 0,
            required: false
        },
        value: {
            type: [String, Number],
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
        },
        lineHeight: {
            type: Number,
            default: 1,
            required: false
        },
        letterSpacing: {
            type: Number,
            default: 1,
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
                lineHeight: this.lineHeight,
                letterSpacing: this.letterSpacing,
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
