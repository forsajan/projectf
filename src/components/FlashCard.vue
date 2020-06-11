<template>
  <div>
      <div v-for="l in thelist" :key="l.id">
          <div>
            <div v-if="!showAnswer(l.id)" v-on:click="toggleQuestionAnswer(l.id)" class="card">{{ l.question }}</div>
            <div v-if="showAnswer(l.id)" v-on:click="toggleQuestionAnswer(l.id)" class="card">{{ l.answer }}</div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'FlashCard',
  data(){
      return {
        thelist: [{
            id: 1,
            question: "Question 1",
            answer: "Answer 1"
        },{
            id: 2,
            question: "Question 2",
            answer: "Answer 2"
        }, ],
        currentCard: {
            id: -1,
            showAnswer: false,
        }
    }
  },
  methods: {
          setCurrentCard(id) {
              this.currentCard.id = id
              this.currentCard.showAnswer = true
          },
          showAnswer(id) {
              return (id === this.currentCard.id && this.currentCard.showAnswer)
          },
          toggleQuestionAnswer(id){
              this.currentCard.id = id
              this.currentCard.showAnswer = !this.currentCard.showAnswer
          }
      },
//   mounted() {
//       const listCount = this.thelist.length
//       for()
//   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
    border: 1px solid #efefef;
    border-radius: 8px;
    padding: 10px;
    text-align: left;
}
</style>
