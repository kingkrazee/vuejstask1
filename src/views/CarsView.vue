<template>
    <div>
      <CardComp v-for="car in cars" :key="car.id">
        <template #header>
          <h3>{{ car.name }}</h3>
        </template>
        <p>Make: {{ car.make }}</p>
        <p>Model: {{ car.model }}</p>
        <p>Year: {{ car.year }}</p>
        <p>Color: {{ car.color }}</p>
        <p>Price: {{ car.price}}</p>
      </CardComp>
    </div>
  </template>
  <script>
  import CardComp from '../components/CardComp.vue';
  export default {
    components: { CardComp },
    data() {
      return {
        cars: [
        {"make": "Toyota", "model": "Camry", "year": 2022, "color": "Silver", "price": 25000},
        {"make": "Honda", "model": "Civic", "year": 2023, "color": "Blue", "price": 22000},
        {"make": "Ford", "model": "Mustang", "year": 2021, "color": "Red", "price": 35000},
        {"make": "Chevrolet", "model": "Malibu", "year": 2022, "color": "Black", "price": 27000},
        {"make": "Nissan", "model": "Altima", "year": 2023, "color": "White", "price": 24000},
        {"make": "BMW", "model": "3 Series", "year": 2022, "color": "Gray", "price": 40000},
        {"make": "Mercedes-Benz", "model": "C-Class", "year": 2023, "color": "Silver", "price": 45000},
        {"make": "Audi", "model": "A4", "year": 2021, "color": "Black", "price": 38000},
        {"make": "Hyundai", "model": "Sonata", "year": 2022, "color": "Blue", "price": 26000},
        {"make": "Kia", "model": "Optima", "year": 2023, "color": "Red", "price": 23000}
        ]
      }
    }
  }
  </script>