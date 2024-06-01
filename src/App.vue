
<template>
 <main>
  <h2>Teste sua frase</h2>
  <textarea v-model="frase" placeholder="Digite a frase aqui..."></textarea>
  <label> Selecione o tamanho da fonte:
    <select v-model="size">
      <option v-for="tamanho in sizes" :value="tamanho.value">{{ tamanho.label }}</option>
    </select>
  </label>
  <p :style="`font-size: ${size}px`">{{ frase }}</p>
 </main>
</template>

<script>
export default {
  data(){
    return{
      frase: '',
      sizes:[
        {value:'16',label:'16px'},
        {value:'24',label:'24px'},
        {value:'28',label:'28px'},
        {value:'36',label:'36px'},
        {value:'54',label:'54px'},
        {value:'96',label:'96px'},
        {value:'108',label:'108px'},
        {value:'124',label:'124px'},
      ],
      size: 16,
    }
  }
}
</script>


<style scoped>
 p{
  font-family: 'Alice';
 }
 textarea{
  width: 80vw;
  margin-bottom: 30px;
 }
</style>
