<!--&lt;!&ndash;Result Component&ndash;&gt;-->
<!--<template>-->
<!--  <div class="result">-->
<!--    &lt;!&ndash;Rendering data dynamically &ndash;&gt;-->
<!--    <div class="title">{{results[resultIndex].title}}</div>-->
<!--    <div class="desc">-->
<!--      {{results[resultIndex].desc}}-->
<!--    </div>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  name: "ResultComponent",-->
<!--  props:["results", "totalCorrect"],-->
<!--  computed:{-->
<!--    resultIndex(){-->
<!--      let index = 0;-->

<!--      this.results.forEach((e,i)=>{-->
<!--        if (e.min <= this.totalCorrect && e.max >= this.totalCorrect){-->
<!--          index = i;-->
<!--        }-->
<!--      })-->

<!--      return index;-->
<!--    }-->
<!--  }-->
<!--};-->
<!--</script>-->

<!--<style scoped>-->

<!--</style>-->