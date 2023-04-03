<template>
  <html lang="en">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <title>BrziChesse</title>

    <link rel="stylesheet" href="/index.css">

    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootswatch@4.5.2/dist/sketchy/bootstrap.min.css" integrity="sha384-RxqHG2ilm4r6aFRpGmBbGTjsqwfqHOKy1ArsMhHusnRO47jcGqpIQqlQK/kmGy9R" crossorigin="anonymous">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>
<body>
  <div id="container" class="container">
        <table class="table table-hover"> 
            <thead> 
                <th scope="coll">Naziv </th>
                <th scope="coll">Cijena </th>
            </thead>
            <tbody> 
                <tr v-for="(item, index) in items" :key="index"> 
                    <td>{{item.name}}</td>
                    <td>{{item.price}} $</td>
                    <td> 
                        <div class="btn-group" role="group">
                            <button
                            type="button"
                            class="btn btn-info btn-sm"
                            @click="dodajItemUCart(item)"> Dodaj </button>
                        </div> 
                    </td>
                </tr> 
            </tbody>

        </table>

    </div>

</body>
</html>
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
     axios.get('http://127.0.0.1:5000/items')
      .then((response) => {
         this.items = response.data
      })
     }
    ,

  dodajItem(item) {
    axios.post('http://127.0.0.1:5000/app/cart/dodaj', item)
      .then((response) => {
      })
  },

  dodajItemUCart(item){
    this.dodajItem(item),
    this.dohvatiItem();
  },
  
},

    mounted(){
    this.dohvatiItem();
    }
}

</script>
