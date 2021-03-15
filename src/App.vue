<template>
<div>
  <input type="text" v-model="text" >
  <button @click="getaddress()">住所自動入力</button>
  <p>Address:{{address}}</p>
  </div>
</template>

<script>

export default{
data(){
  return{
    text:""
  };
},
methods:{

}
}