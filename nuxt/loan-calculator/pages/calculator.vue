<template>
  <section class="container">
    <img src="../assets/house.jpg">
    <form name="calculator">
      <div class="form-field">
        <label>Сума:</label>
        <input type="number" min="0" step="1000.00"></div>
      <div class="form-field">
        <label>Початковий внесок:</label>
        <input name="preliminary" type="number" min="0" step="1000.00">
        <div id="pre-warning"></div>
      </div>
      <div class="form-field">
        <label>Банк:</label>
        <select name="bank">
          <option v-for="(bank, key ) in banks" :value="key">{{bank.title}}</option>
        </select>
        <label>Программа:</label>
        <select name="plan">
          <option>Оберіть банк</option>
        </select></div>
      <div class="form-field">
        <label>Річний відсоток:</label>
        <input name="interest" type="number" min="0" max="100" step="0.5" value="25"></div>
      <div class="form-field">
        <button type="button" v-on:click="calc()">Розрахувати</button>
      </div>
    </form>
    -{{banks.privat}}-
  </section>
</template>

<script>
  export default {
    name: 'Calculator',
    data: () => {
      return {
        banks: {
          privat: {
            title: 'Приват Банк',
            plans: {
              plan1: {
                title: 'ПБ 1',
                interest: 20.0,
                min_initial_perc: 30
              },
              plan2: {
                title: 'ПБ 2',
                interest: 25.0,
                min_initial_perc: 20
              },
              plan3: {
                title: 'ПБ 3',
                interest: 20.0,
                min_initial_perc: 50
              }
            }
          },
          ostch: {
            title: 'Ощад Банк',
            plans: {
              plan1: {
                title: 'Ощ 1',
                interest: 25.0,
                min_initial_perc: 30
              },
              plan2: {
                title: 'Ощ 2',
                interest: 26.0,
                min_initial_perc: 20
              },
              plan3: {
                title: 'Ощ 3',
                interest: 21.0,
                min_initial_perc: 50
              }
            }
          }
        }
      }
    },
    methods: {
      calc: () => {
        console.log('CALC()', this)
      }
    }
  }
</script>

<style scoped>
  #pre-warning {
    display: none;
  }
</style>
