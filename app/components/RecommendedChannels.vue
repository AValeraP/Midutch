<script setup>
import infoChannels from "~/data/channels.json"
</script>
<template>
    <div class=" m-5 p-5 border-2-white rounded p-5 flex">
        <h1 class="font-bold text-white">RECOMMENDED CHANNELS</h1>
        
        <button class="hover:bg-gray-700 rounded-full p-2">
        <svg width="16" height="12" viewBox="0 0 16 12" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M13.999 12V0H15.999V12H13.999ZM3.999 5L6.5 2.5L5 1L0 6L5 11L6.5 9.5L4 7H12V5H3.999Z" fill="#EFEFF1"/>
        </svg>
        </button>


        <!--Aqui un v-for para recorrer canales-->
        <div class="">
            <label v-for="(item, key) in infoChannels.infoChannels"
            :key="key"
            class="mx-1 my-0.5 text-white font-bold text-xs">
            {{ item.name }}<br>
            {{ item.category }}<br>
        </label>
        </div>
    </div>
</template>