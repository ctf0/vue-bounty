<template>
    <span/>
</template>

<script>
import bounty from 'bounty'

export default {
    props: ['value'],
    mounted() {
        this.init(this.value, 0)
    },
    methods: {
        init(val, old) {
            return bounty({
                el: this.$el,
                value: val,
                initialValue: old,
                lineHeight: 1,
                letterSpacing: 1,
                animationDelay: 100,
                letterAnimationDelay: 100
            })
        }
    },
    watch: {
        value(val, oldVal) {
            setTimeout(() => {
                this.init(val, oldVal || 0)
            }, 100)
        }
    }
}
</script>
