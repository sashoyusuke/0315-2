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
    text:""
  };
},
methods:{
getaddress(){
  const res = await axios.get("https://apis.postcode-jp.com/api/v4/9cd5bef5b6fc8bf220049e41dcbd4290/param1/param2?cursor3=value1?cursor4=value2");
const allAddress= res.data;
this.address=allAddress;
}
}
};
</script>