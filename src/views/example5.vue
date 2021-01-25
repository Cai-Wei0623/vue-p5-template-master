<template>
<div>
<el-calendar>
  <template #dateCell="{data}">
    <p :class="data.isSelected ? 'is-selected' : ''">
      {{ data.day.split('-').slice(1).join('-') }} {{ data.day.split('-').slice(1).join('-')==='01-25' ? '✔️' : '' }}
    </p>
  </template>
</el-calendar>
<div class="Datebackground"></div>
</div>
  
</template>

<script>
  export default {
    data() {
      return {
        value: new Date()
      }
    }
  }
</script>

<style>
.Datebackground {
  background-color: black;
  width:100vw;
  height:30vh;
}
.is-selected {
    color: #1989FA;
  }
</style>
