<template>
  <div>
    <h1>{{ result }}</h1> <!-- 결과 -->
    <form @submit.prevent="onSubmitForm"> <!-- 제출하는 함수 -->
      <input type="text" ref="answer" minlength="4" maxlength="4" v-model="value" /> <!-- 양방향 바인딩  -->
      <button>입력</button>
    </form>
    <div>시도 : {{ tries.length }}</div> <!-- 시도 갯수 -->
    <ul>
      <li v-for="t in tries">
        <div>{{ t.try }}</div>
        <div>{{ t.result }}</div>
      </li> <!--  데이터의 각 요소를 순회하면서 HTML 요소를 생성 -->
    </ul>
  </div>
</template>

<script>
const getNumbers = () => {
  const candidates = [1, 2, 3, 4, 5, 6, 7, 8, 9];
  const array = [];
  for (let i = 0; i < 4; i++) { //  무작위로 선택된 4개의 고유 숫자 배열
    const chosen = candidates.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
    array.push(chosen);
  }
  return array;
}

export default {
  data() {
    return {
      answer: getNumbers(),
      tries: [],
      value: '',
      result: '',
    }
  },
  methods: {
    onSubmitForm(e) {
      if (this.value === this.answer.join('')) { // 정답 맞췃으면
        this.tries.push({
          try: this.value,
          result: `홈런`,
        });
        this.result = '홈런';
        alert("게임을 다시 실행합니다.");
        this.value = '';
        this.tries = [];
        this.$refs.answer.focus();
      } else {
        let strike = 0;
        let ball = 0;
        const answerArray = this.value.split('').map(v => parseInt(v));
      }
      this.value = ''; // 값은 빈 값으로
      this.$refs.answer.focus(); // 포커스 이동
    }
  }
}
</script>