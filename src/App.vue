<script setup>
import { ProgressButtonComponent as EjsProgressbutton } from "@syncfusion/ej2-vue-splitbuttons";
const spinSettings = { position: 'Right', width: 30, template: '<div class="template"></div>' }
const animationSettings = { effect:'SlideUp', duration:500, easing:'linear' }
const iconCss = "e-btn-sb-icon e-download";
const beginHandler = function(args)
{
  this.content = "Downloading";
}
const endHandler = function(args)
{
  this.content = "Download";
}
</script>

<template>
 <ejs-progressbutton content="Download" :iconCss="iconCss" cssClass="e-hide-spinner"
                     :enableProgress="true" :begin="beginHandler" iconPosition="Right"
                     :end="endHandler"></ejs-progressbutton>
</template>

<style >
 @import '../node_modules/@syncfusion/ej2-base/styles/material.css';
 @import '../node_modules/@syncfusion/ej2-buttons/styles/material.css';
 @import '../node_modules/@syncfusion/ej2-popups/styles/material.css';
 @import '../node_modules/@syncfusion/ej2-splitbuttons/styles/material.css';
 .template {
    border: 2px solid green;
    border-style: dotted;
    border-radius: 50%;
    border-top-color: transparent;
    border-bottom-color: transparent;
    height: 16px;
    width: 16px;
  }
  .template {
    -webkit-animation: custom-rolling 1.3s linear infinite;
    animation: custom-rolling 1.3s linear infinite;
  }
  @keyframes custom-rolling {
    0% {
      -webkit-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      -webkit-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
 .e-download::before {
  content: '\e706';
  }
  @font-face {
    font-family: 'btn-icon';
    src:
    url(data:application/x-font-ttf;charset=utf-8;base64,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) format('truetype');
    font-weight: normal;
    font-style: normal;
  }
  .e-btn-sb-icon {
    font-family: 'btn-icon' !important;
    font-size: 55px;
  }

</style>
