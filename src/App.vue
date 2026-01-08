<script setup>
import { ref, reactive } from 'vue'

/* ===================== CATEGORIES ===================== */
const categories = [
  { id: 'bakery', label: 'Випічка', icon: '🥖' },
  
  { id: 'fruits', label: 'Фрукти', icon: '🍎' },
  { id: 'vegetables', label: 'Овочі', icon: '🥦' },
  
  { id: 'meat', label: 'М’ясо та м’ясні продукти', icon: '🥩' },
  { id: 'fish', label: 'Риба та морепродукти', icon: '🐟' },
  
  { id: 'eggs', label: 'Яйця', icon: '🥚' },
  
  { id: 'dairy', label: 'Молочні продукти', icon: '🥛' },
  { id: 'fats', label: 'Жири', icon: '🧈' },
  
  { id: 'grains', label: 'Крупи та бобові', icon: '🌾' },
  { id: 'pasta', label: 'Макаронні вироби', icon: '🍝' },
  
  { id: 'spices', label: 'Спеції та трави', icon: '🌿' },
  { id: 'sauces', label: 'Соуси', icon: '🥫' },
  
  { id: 'sweets', label: 'Солодощі', icon: '🍫' },
  { id: 'drinks', label: 'Напої', icon: '🥤' },
]

/* ===================== INVENTORY ===================== */
const inventory = reactive({
  meat: [
    { name: 'Куриця ціла обрізана', icon: '🍗', amount: 720, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Ребра свинні', icon: '🥩', amount: 250, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Сало не солене', icon: '🥓', amount: 600, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Сало солене', icon: '🥓', amount: 350, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Свинні стейки', icon: '🥩', amount: 400, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Фарш свинячий', icon: '🥩', amount: 144, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Філе свинина', icon: '🥩', amount: 1000, unit: 'g', units: ['g','kg'], tags: ['свіже'] }
  ],
  fish: [
    { name: 'Лосось засолений', icon: '🐟', amount: 130, unit: 'g', units: ['g','kg'], tags: ['свіже'] }
  ],
  eggs: [
    { name: 'Яйця курячі', icon: '🥚', amount: 16, unit: 'шт', units: ['шт'], tags: ['свіже'] }
  ],
  dairy: [
    { name: 'Творог грудковий', icon: '🧀', amount: 230, unit: 'g', units: ['g','kg'], tags: ['заморожено'] },
    { name: 'Творог jemny', icon: '🧀', amount: 130, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Молоко', icon: '🥛', amount: 700, unit: 'ml', units: ['ml','l'], tags: ['свіже'] }
  ],
  grains: [
    { name: 'Булгур', icon: '🌾', amount: 96, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Гречка', icon: '🌾', amount: 496, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Кускус', icon: '🌾', amount: 196, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Пшоно', icon: '🌾', amount: 320, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Рис Basmati', icon: '🌾', amount: 36, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Рис Jasmine', icon: '🌾', amount: 0, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Чечевиця', icon: '🌾', amount: 195, unit: 'g', units: ['g','kg'], tags: ['сухе'] }
  ],
  pasta: [
    { name: 'Вермішель', icon: '🍝', amount: 172, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Макарони бабочка', icon: '🍝', amount: 300, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Макарони різнокольорові', icon: '🍝', amount: 118, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Макарони трубочка', icon: '🍝', amount: 63, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Спагетті', icon: '🍝', amount: 52, unit: 'g', units: ['g','kg'], tags: ['сухе'] }
  ],
  bakery: [
    { name: 'Борошно гладке', icon: '🥖', amount: 1119, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Ванільний цукор', icon: '🧂', amount: 20, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Дріжджі сушені', icon: '🥖', amount: 8, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Манка', icon: '🌾', amount: 299, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Розпушувач тіста до печива', icon: '🥖', amount: 48, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Розпушувач тіста до пряників/бісквіту', icon: '🥖', amount: 12, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Сода', icon: '🧂', amount: 228, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Сіль', icon: '🧂', amount: 362, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Цукор', icon: '🧂', amount: 674, unit: 'g', units: ['g','kg'], tags: ['сухе'] }
  ],
  vegetables: [
    { name: 'Картопля', icon: '🥔', amount: 2000, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Морква', icon: '🥕', amount: 0, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Огірок', icon: '🥒', amount: 2, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Петрушка', icon: '🌿', amount: 30, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Помідор', icon: '🍅', amount: 3, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Цибуля ріпчаста', icon: '🧅', amount: 0, unit: 'шт', units: ['шт'], tags: ['свіже'] }
  ],
  fruits: [
    { name: 'Клубніка', icon: '🍓', amount: 450, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Яблука', icon: '🍎', amount: 500, unit: 'g', units: ['g','kg'], tags: ['свіже'] }
  ],
  spices: [
    { name: 'Кріп', icon: '🌿', amount: 10, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Лавровий лист', icon: '🌿', amount: 5, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Орегано', icon: '🌿', amount: 4, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Паприка копчена мелена', icon: '🌶️', amount: 8, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Перець духмяний', icon: '🌶️', amount: 4, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Перець чорний', icon: '🌶️', amount: 7, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Перець чорний цілий', icon: '🌶️', amount: 5, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Петрушка', icon: '🌿', amount: 2, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа для картоплі по-американськи', icon: '🌶️', amount: 3, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа для картоплі по-американськи #2', icon: '🌶️', amount: 15, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа для куриці', icon: '🌶️', amount: 3, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа для м\'яса', icon: '🌶️', amount: 1, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа для плову', icon: '🌶️', amount: 10, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа до шашлику', icon: '🌶️', amount: 28, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа до шашлику #2', icon: '🌶️', amount: 75, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Приправа сипка', icon: '🌶️', amount: 111, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Розмарин', icon: '🌿', amount: 18, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Суміш зелені', icon: '🌿', amount: 10, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Хмелі сунелі', icon: '🌿', amount: 23, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Хмелі сунелі #2', icon: '🌿', amount: 30, unit: 'g', units: ['g','kg'], tags: ['сухе'] }
  ],
  drinks: [
    { name: 'Кофе мелена', icon: '☕', amount: 85, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Чай ромашковий', icon: '🍵', amount: 2, unit: 'шт', units: ['шт'], tags: ['сухе'] },
    { name: 'Чай чорний', icon: '🍵', amount: 3, unit: 'шт', units: ['шт'], tags: ['сухе'] },
    { name: 'Кофе таблетки Тасімо Мілка', icon: '☕', amount: 4, unit: 'шт', units: ['шт'], tags: ['сухе'] }
  ],
  sweets: [
    { name: 'Варення клубніки', icon: '🍯', amount: 650, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Варення малинове', icon: '🍯', amount: 1000, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Варення смородини', icon: '🍯', amount: 400, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Вафельні вафельні листи', icon: '🍪', amount: 18, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Какао несквік', icon: '🍫', amount: 110, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Какао пудра', icon: '🍫', amount: 80, unit: 'g', units: ['g','kg'], tags: ['сухе'] },
    { name: 'Медові кільця', icon: '🍯', amount: 174, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Родзинки', icon: '🍇', amount: 57, unit: 'g', units: ['g','kg'], tags: ['сухе'] }
  ],
  fats: [
    { name: 'Масло сливочне', icon: '🧈', amount: 395, unit: 'g', units: ['g','kg'], tags: ['свіже'] },
    { name: 'Олія соняшникова', icon: '🫒', amount: 500, unit: 'ml', units: ['ml','l'], tags: ['свіже'] },
  ],
  sauces: [
    { name: 'Кетчуп до шашлику', icon: '🥫', amount: 1, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Соус аджика', icon: '🥫', amount: 1, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Соус гірчиця міцна', icon: '🥫', amount: 1, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Соус солодкий чилі', icon: '🥫', amount: 1, unit: 'шт', units: ['шт'], tags: ['свіже'] },
    { name: 'Цитроніка', icon: '🍋', amount: 60, unit: 'ml', units: ['ml','l'], tags: ['свіже'] }
  ]
})

/* ===================== UI STATE ===================== */
const activeCategory = ref(null)
const activeItem = ref(null)
const inputValue = ref('')
const displayUnit = ref('')
const editingMode = ref('edit') // 'edit' | 'add'

/* ===================== ICONS ===================== */
const iconList = [
  '🥩','🍗','🥓','🍖','🐟','🧀','🥛','🥦','🍎','🍓','🌾','🍝','🍬','🧂','🌶️',
  '🍅','🧈','🫒','🆕','🥖','🍯','🍪','🍋','🍇','🥕','🥔','🥒','🧅','☕','🍵','🥚','🌿','🥫','🥬','🫙'
]

/* ===================== HELPERS ===================== */
const pretty = item => {
  switch(item.unit){
    case 'kg': return `${(item.amount/1000).toFixed(2)} кг`
    case 'g': return `${item.amount} г`
    case 'l': return `${(item.amount/1000).toFixed(2)} л`
    case 'ml': return `${item.amount} мл`
    default: return `${item.amount} шт`
  }
}

const formatForDisplay = (amount, unit) => ['kg','l'].includes(unit) ? (amount/1000).toString() : amount.toString()
const toBase = (value, unit) => {
  const v = parseFloat(value || 0)
  return ['kg','l'].includes(unit) ? Math.round(v*1000) : Math.round(v)
}

/* ===================== MODAL ===================== */
function openItem(item){
  activeItem.value = { ...item, original: item }
  displayUnit.value = item.unit
  inputValue.value = formatForDisplay(item.amount, item.unit)
  editingMode.value = 'edit'
  activeItem.value.units = ['g','kg','ml','l'].includes(item.unit) ? [item.unit === 'g'||item.unit==='kg'? 'g':'ml','kg' || 'l'] : [item.unit]
}

function openAddModal(){
  if(!activeCategory.value) return alert('Оберіть категорію!')
  activeItem.value = { name:'', icon:'🆕', amount:0, unit:'g', units:['g','kg','ml','l','шт'], tags:['свіже'] }
  displayUnit.value = 'g'
  inputValue.value = ''
  editingMode.value = 'add'
}

function closeModal(){ activeItem.value = null; inputValue.value='' }
function saveItem(){
  if(!activeItem.value.name.trim()) return alert('Вкажіть назву продукту!')
  activeItem.value.amount = toBase(inputValue.value, displayUnit.value)
  activeItem.value.unit = displayUnit.value
  if(!inventory[activeCategory.value]) inventory[activeCategory.value]=[]
  editingMode.value==='add'?inventory[activeCategory.value].push({...activeItem.value}):Object.assign(activeItem.value.original, activeItem.value)
  closeModal()
}

function press(key){ inputValue.value = key==='⌫'? inputValue.value.slice(0,-1):inputValue.value+key }
function removeItem(item){ const idx = inventory[activeCategory.value].indexOf(item); if(idx!==-1) inventory[activeCategory.value].splice(idx,1) }
function toggleTag(tag){ const i = activeItem.value.tags.indexOf(tag); i!==-1?activeItem.value.tags.splice(i,1):activeItem.value.tags.push(tag) }

</script>

<template>
<div class="min-h-screen bg-gray-100 p-4">

  <!-- CATEGORIES -->
  <div v-if="!activeCategory" class="grid grid-cols-2 sm:grid-cols-4 md:grid-cols-6 gap-4">
    <button v-for="c in categories" :key="c.id" @click="activeCategory=c.id" class="h-full p-5 bg-white rounded-xl shadow-lg flex flex-col items-center justify-center active:scale-95 transition">
      <div class="text-6xl mb-3">{{ c.icon }}</div>
      <div class="text-sm font-semibold line-clamp-2">{{ c.label }}</div>
    </button>
  </div>

  <!-- ITEMS -->
    <div v-else>
    <div class="flex justify-between mb-4 items-center">
      <button class="text-lg font-semibold text-blue-600" @click="activeCategory=null">← Назад</button>
      <button class="px-4 py-2 bg-green-500 text-white rounded-2xl" @click="openAddModal">Додати продукт</button>
    </div>
  <div class="grid grid-cols-2 sm:grid-cols-4 md:grid-cols-6 gap-4">
  <div v-for="item in inventory[activeCategory]" :key="item.name" class="relative flex flex-col items-center relative">
  <button @click="openItem(item)" class="h-full flex flex-col items-center w-full justify-between p-3 rounded-2xl bg-white shadow-lg">
    <div class="text-6xl flex justify-center mt-2">{{ item.icon }}</div>
    <div class="text-center mt-2">
      <div class="text-sm font-semibold line-clamp-2">{{ item.name }}</div>
      <div class="text-base font-bold mt-1">{{ pretty(item) }}</div>
    </div>
    <div class="flex flex-wrap justify-center gap-1 mt-2 max-h-10 overflow-auto">
      <span v-for="tag in item.tags" :key="tag" class="bg-gray-200 text-gray-800 px-2 py-1 rounded-full text-xs">{{ tag }}</span>
    </div>
  </button>
  <button @click.stop="removeItem(item)" class="absolute top-2 right-2 text-red-500 text-xl bg-white rounded-full p-1 shadow">✖</button>
</div>
    </div>

</div>


  <!-- MODAL / NUMPAD -->
  <div v-if="activeItem" class="fixed inset-0 bg-black/40 flex items-end sm:items-center justify-center">
    <div class="bg-white w-full sm:w-[420px] rounded-t-3xl sm:rounded-3xl p-5">
      <div class="text-center mb-2">
        <select v-model="activeItem.icon" class="text-4xl text-center w-full mb-2">
          <option v-for="i in iconList" :key="i" :value="i">{{ i }}</option>
        </select>
        <input v-model="activeItem.name" class="w-full border-b text-center text-xl font-semibold mb-2" placeholder="Назва продукту"/>
      </div>

      <div class="text-center text-4xl font-bold mb-4">{{ inputValue || 0 }}</div>
      <div class="grid grid-cols-3 gap-3 mb-4">
        <button v-for="k in ['1','2','3','4','5','6','7','8','9','.','0','⌫']" :key="k" @click="press(k)" class="bg-gray-100 rounded-2xl p-6 text-2xl font-semibold active:scale-95">{{ k }}</button>
      </div>

      <div class="flex gap-3 mb-4">
        <button v-for="u in activeItem.units" :key="u" @click="displayUnit=u" :class="['flex-1 p-4 rounded-2xl text-xl font-semibold', displayUnit===u?'bg-blue-500 text-white':'bg-gray-100']">{{ u }}</button>
      </div>

      <div class="flex gap-2 flex-wrap mb-4">
        <button v-for="tag in ['свіже','заморожено','мариноване']" :key="tag" @click="toggleTag(tag)" :class="['px-3 py-1 rounded-full text-xs', activeItem.tags.includes(tag)?'bg-blue-500 text-white':'bg-gray-200 text-gray-800']">{{ tag }}</button>
      </div>

      <div class="flex gap-3">
        <button @click="closeModal" class="flex-1 p-4 rounded-2xl bg-gray-200 text-xl">Скасувати</button>
        <button @click="saveItem" class="flex-1 p-4 rounded-2xl bg-green-500 text-white text-xl font-semibold">OK</button>
      </div>
    </div>
  </div>
</div>
</template>
