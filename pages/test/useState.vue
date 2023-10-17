<template>
    <div class="flex m-8 justify-between w-1/2">
        <UseStateCounter name="UseState First"></UseStateCounter>
        <UseStateCounter name="UseState Second"></UseStateCounter>
        <UseStateCounter name="UseState Third"></UseStateCounter>
    </div>

    <div>
        Message: {{ message }} <br>
        AppTheme: {{ appTheme }} <br>
        Hello: {{ hello }}
    </div>
    
</template>

<script setup lang="ts">
    import { ref } from 'vue'
    const message = ref("")

    import { useLocalStorage, useSessionStorage } from '@vueuse/core'
    const appTheme = useLocalStorage<string|null>('app-theme', null)
    const hello = useSessionStorage('hello',null)
    

    function onChangeUp(name:string, counter:number){
        message.value = `${name}: change counter up to ${counter}`
    }
</script>