<template>
  <div class="questions-ctr">
<!--    <div class="progress">-->
<!--&lt;!&ndash;      Binding Dynamic progress bar Styling&ndash;&gt;-->
<!--      <div class="bar" :style="{width:`${(questionsAnswered/questions.length) * 100}%`}"></div>-->
<!--      <div class="status">{{questionsAnswered}} out of {{questions.length}} questions answered</div>-->
<!--    </div>-->
    <transition-group name="fade">
      <div
        class="single-question"
        v-for="(question, qi) in questions"
        :key="question.q"
        v-show="questionsAnswered === qi">
        <div class="question">{{question.q}}</div>
        <div class="answers">
          <div
            class="answer"
            v-for="answer in question.answers"
            :key="answer.text"
            @click.prevent="selectAnswer(answer.is_correct)"
          >
            {{answer.text}}
          </div>
        </div>
      </div>
    </transition-group>

  </div>
</template>

<script>
export default {
  name: "QuestionsComponent",
  props:["questions", "questionsAnswered"],
  emits:['question-answered'],
  methods:{
    //Selecting answer emitter function
    selectAnswer(is_correct){
      this.$emit('question-answered', is_correct)
    }
  }
};
</script>

<style scoped>

</style>