<template>
    <button class="button" :style="{color: color, borderColor: color}" @click="handleClick" @dblclick="handleDblclick" :class="{rounded: rounded}"><slot></slot>!</button>
  </template>
  
  <script>
    export default {
      props: {
        rounded: Boolean,
        handleClick: {
          default: () => () => null
        },
        handleDblclick: {
          default: () => () => null
        },
        color: {
          default: '#42b983'
        }
      }
    }
  </script>
  
  <style>
    .rounded {
      border-radius: 5px;
    }
  
    .button {
      border: 3px solid;
      padding: 10px 20px;
      background-color: white;
      outline: none;
    }
    
  </style>