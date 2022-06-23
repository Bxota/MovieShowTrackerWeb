<template>
    <div id="header">
        <ul>
            <p @click="emitClickEvent('Download')">Download</p>
            <h1 @click="emitClickEvent('Accueil')">Movie & Show Tracker</h1>
            <p @click="emitClickEvent('Information')">Information</p>
        </ul>
    </div>
</template>

<script>
    export default {
        methods : {
            emitClickEvent(data) {
                this.emitter.emit("event", data)
            }
        }
    }
</script>

<style lang="stylus">
  @import '@/assets/header.styl'
</style>