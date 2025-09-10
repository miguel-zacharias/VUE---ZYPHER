<template>
  <div class="products-page">
    <h1> CARTÕES PRESENTE </h1>
    <p>Presenteie quem você ama!</p>
    
    <div class="products-grid">
      <div 
        v-for="product in products" 
        :key="product.id"
        class="product-card"
        @click="viewProduct(product.id)"
      >
        <div class="product-emoji">{{ product.emoji }}</div>
        <h3>{{ product.name }}</h3>
        <p class="product-price">{{ product.price }}</p>
        <button class="view-btn">Ver Detalhes</button>
      </div>
    </div>

    <div v-if="selectedProduct" class="product-modal" @click="closeModal">
      <div class="modal-content" @click.stop>
        <h2>{{ selectedProduct.emoji }} {{ selectedProduct.name }}</h2>
        <p><strong>Preço:</strong> {{ selectedProduct.price }}</p>
        <p><strong>Descrição:</strong> {{ selectedProduct.description }}</p>
        <button @click="closeModal" class="close-btn">Fechar</button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()

const products = ref([
  {
    id: 1,
    name: 'GIFTCARD',
    price: 'R$ 100.00',
    emoji: '💻',
  },
  {
    id: 2,
    name: 'GIFTCARD',
    price: 'R$ 199,00',
    emoji: '🖱️',
  },
  {
    id: 3,
    name: 'GIFTCARD',
    price: 'R$ 349,00',
    emoji: '⌨️',
  },
  {
    id: 4,
    name: 'GIFTCARD',
    price: 'R$ 1.299,00',
    emoji: '🖥️',
  }
])

const selectedProductId = ref(null)

const selectedProduct = computed(() => {
  return products.value.find(p => p.id === selectedProductId.value)
})

const viewProduct = (productId) => {
  selectedProductId.value = productId
}

const closeModal = () => {
  selectedProductId.value = null
}
</script>

<style scoped>
.products-page {
  text-align: center;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.product-card {
  background-color: white;
  border: 2px solid #dee2e6;
  border-radius: 8px;
  padding: 20px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.product-card:hover {
  border-color: #007bff;
  transform: translateY(-5px);
  box-shadow: 0 4px 12px rgba(0, 123, 255, 0.15);
}

.product-emoji {
  font-size: 3rem;
  margin-bottom: 15px;
}

.product-card h3 {
  color: #495057;
  margin-bottom: 10px;
}

.product-price {
  font-size: 1.2rem;
  font-weight: bold;
  color: #28a745;
  margin-bottom: 15px;
}

.view-btn {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.view-btn:hover {
  background-color: #0056b3;
}

.product-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  background-color: white;
  padding: 30px;
  border-radius: 8px;
  max-width: 400px;
  width: 90%;
  text-align: center;
}

.close-btn {
  background-color: #6c757d;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 15px;
}

.close-btn:hover {
  background-color: #545b62;
}
</style>
