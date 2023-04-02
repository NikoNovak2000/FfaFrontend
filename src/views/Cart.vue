
<template>
<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootswatch@4.5.2/dist/sketchy/bootstrap.min.css" integrity="sha384-RxqHG2ilm4r6aFRpGmBbGTjsqwfqHOKy1ArsMhHusnRO47jcGqpIQqlQK/kmGy9R" crossorigin="anonymous">
 <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>
  <div class="Cart">
    <table class="table table-hover"> 
            <thead> 
                <th scope="coll">Naziv </th>
                <th scope="coll">Cijena </th>
                <th scope="coll">Slika </th>
                <th scope="coll">Kolicina </th>

            </thead>

            <tbody> 
                <tr v-for="(item, index) in items" :key="index"> 
                    <td>{{item.name}}</td>
                    <td>{{item.price}} $</td>
                    <td><img :src="item.img" :height = "50"></td>
                    <td>{{item.quantity}} </td>
                </tr> 
            </tbody>

        </table>
       
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios'



export default{
  el: '#app',
  data() {
    return {
      items: []
    }
    },
  components: {
    
  },

  methods:{
      dohvatiItem(){
     axios.get('http://127.0.0.1:5000/app/cart')
      .then((response) => {
         console.log('Ovo su podaci koji se dohvacaju' + response.data.data)
         this.items = response.data
         console.log(this.items)
         for (let i = 0; i < this.items.length; i++) {
          console.log(this.items[i])
         }
      })
      
    },


},
mounted(){
    this.dohvatiItem();
  }
  
}


</script>
