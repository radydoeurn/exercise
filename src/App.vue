<template>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
  <div class="home">
    <!-- Welcome section -->
    <div class="welcome-section text-center">
      <h1>List of fruit</h1>
      <p class="lead">
       Hope you enjoy to see the picture of the fruit and appreciate that you cannot eat it.
      </p>
      <thead>
        <tr>
          <th>Name</th>
          <th>Price</th>
          <th>Description</th>
          <th>Image</th>
        </tr>
      </thead>

    </div>

    <!-- Fruits list -->
    
    <div class="row justify-content-center fruits-list">
      <div class="col-md-4" v-for="fruit in fruits" :key="fruit.id">
        <div class="card mb-3">
          <img :src="fruit.imageUrl" :alt="fruit.name" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{{ fruit.name }}</h5>
            <p class="card-text">Price: {{ fruit.price }}</p>
            <p class="card-text">{{ fruit.description }}</p>
            <button class="btn btn-primary">Buy now</button>
          </div>
        </div>
      </div>
    </div>    
  </div>
</template>

<script>
export default {
  data() {
    return {
      fruits: [
        {
          id: 1,
          name: "Avocado",
          price: "$30",
          description: "Fresh and crunchy Avocado",
          imageUrl:
            "https://images.pexels.com/photos/142890/pexels-photo-142890.jpeg?auto=compress&cs=tinysrgb&w=600"
        },
        {
          id: 2,
          name: "Grape",
          price: "$25",
          description: "Sweet and ripe grape",
          imageUrl:
            "https://images.pexels.com/photos/60021/grapes-wine-fruit-vines-60021.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
        },
        {
          id: 3,
          name: "Kiwi",
          price: "$35",
          description: "eat to be a queen",
          imageUrl:
            "https://images.pexels.com/photos/3904800/pexels-photo-3904800.jpeg?auto=compress&cs=tinysrgb&w=600",
          
        },
          {
          id: 4,
          name: "Strawbery",
          price: "$20",
          description:"Sweet and fresh",
          imageUrl:
            "https://images.pexels.com/photos/4038803/pexels-photo-4038803.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
        },
          {
          id: 4,
          name: "Strawbery",
          price: "$20",
          description:"Sweet and fresh",
          imageUrl:
            "https://images.pexels.com/photos/20030797/pexels-photo-20030797/free-photo-of-heap-of-peaches.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
        },
          {
          id: 4,
          name: "Strawbery",
          price: "$20",
          description:"Sweet and fresh",
          imageUrl:
            "https://images.pexels.com/photos/672101/pexels-photo-672101.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
        },
        // Add more fruits as needed
      ],
    };
  },
};
</script>

<style scoped>
/* Styles for the Home component */
.home {
  padding: 20px;
}

.fruits-list .fruit {
  margin-bottom: 20px;
 
}
th{
  
  text-align: center;
  font-size: 10;
  padding: 15px;
  border: 1px solid rgba(0, 0, 0, 0.211);
}
</style>