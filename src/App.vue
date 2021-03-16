<template>
<div>
  <input type="text" v-model="text" >
  <button @click="getaddress()">住所自動入力</button>
  <p>Address:{{address}}</p>
  </div>
</template>

<script>
import axios from "axios";
export default{
data(){
  return{
    text:"",
    address:""
  };
},
methods:{
async getaddress(){
  const res = await axios.get('https://apis.postcode-jp.com/api/v4/postcodes/${this.test}?apiKey=bPRFvyBgjHxi0hvGJuY7O676Y9cNPnEVs8ejjmj');
  const allAddress=res.data;
  this.address=allAddress.address; 
}
}
};
</script>