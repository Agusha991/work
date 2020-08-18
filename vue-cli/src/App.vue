<template>
  <div id="app">
    <h1>{{ hello }}</h1>
    <p>{{ info }}</p>
    <div class="bpm">
      <p>hello</p>
      <p>{{ BPM.BPM_forWhat }}</p>
      <div>
        <h1> Выполняет задачи</h1>
        <p v-for="problem in BPM.BPM_problem" :key="problem.problem" class="info">
          {{ problem.problem }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'me',
  data() {
    return {
      hello: 'Привет меня зовут Никита!',
      info: 'Мне 21 год, я учусь в АфСПБГУП на программиста, так же заканчиваю учебу  на курсах в AttractorSchool fullstack developer. Знаю react, redux-react, mongodb, mysql.' +
        ' Опыта в react у меня около полугода, работал в компании два месяца и ушел,  отношения к сотрудникам  было не очень хорошим, люблю учиться, развиваться, решать задачи, дружелюбный,' +
        ' быстро нахожу общий язык с людьми',
      BPM: {
        BPM_Info: 'BPM это  управление и оптимизация  бизнес процесса. Бизнес процесс подразумевает собой  постановку работы  предприятия так , чтобы  оно отвечало заказчикам и покупателям.',
        BPM_forWhat: 'BPM  нужен для автоматизации бизнес-процессов, основная цель это  автоматизировать концептуальную схему процесса, сделав из нее исполняемую схему. Есть Creatio оно служить для' +
          'управления взаимоотношениями с клиентами и системы управления бизнес-процессами.',
        BPM_problem: [
          {problem: "Создание бизнес-процессов"},
          {problem: 'Автоматизация бизнес-процессов'},
          {problem: 'Выполнение бизнес-процессов'},
          {problem: 'Мониторинг и оптимизация процессов'},
          {problem: 'Готовые инструменты для решения бизнес-задач'},
          {problem: 'Интеграции с другими системами'},
          {problem: 'Управление данными и документами'},
          {problem: 'Управление организационной структурой предприятия'},
        ]
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

p {
  width: 800px;
  text-align: center;
  border: 2px solid grey;
  border-radius: 5px;
  padding: 15px;
  line-height: 35px;
  font-weight: bold;
  margin: 0 auto 10px;

}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
