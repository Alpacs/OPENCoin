<template>
  <TheHeader class="the-header"/>
  <SloganContent/>
  <InfoContent/>
  <SocialMedia/>
  <RoadMap/>
  <LinkToBuy/>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import SloganContent from './components/SloganContent.vue'
import InfoContent from './components/InfoContent.vue'
import SocialMedia from './components/SocialMedia.vue';
import RoadMap from './components/RoadMap.vue'
import LinkToBuy from './components/LinkToBuy.vue'

(function() {
    var link = document.querySelector("link[rel*='icon']") || document.createElement('link');
    link.type = 'image/x-icon';
    link.rel = 'shortcut icon';
    link.href = require('./assets/logo.svg');
    document.getElementsByTagName('head')[0].appendChild(link);
})();

export default {
  name: 'App',
  components: {
    TheHeader,
    SloganContent,
    InfoContent,
    SocialMedia,
    RoadMap,
    LinkToBuy
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700;800;900&display=swap');

html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;font-size:100%;font:inherit;vertical-align:baseline}
article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}
html{height:100%}
body{line-height:1}
ol,ul{list-style:none}
blockquote,q{quotes:none}
blockquote:before,blockquote:after,q:before,q:after{content:'';content:none}
table{border-collapse:collapse;border-spacing:0}
.the-header {
  z-index: 2;
}
* {
  -webkit-touch-callout: none; /* iOS Safari */
                -webkit-user-select: none; /* Safari */
                -khtml-user-select: none; /* Konqueror HTML */
                -moz-user-select: none; /* Old versions of Firefox */
                -ms-user-select: none; /* Internet Explorer/Edge */
                user-select: none; 
}
</style>
