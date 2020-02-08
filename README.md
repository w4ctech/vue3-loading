# vue3-loading

## Start

```bash
yarn add vue3-loading -S
```

## user

```app.vue
<script>
    mounted:{
        this.bus.$emit('loading', true,'拼命加载中');
    }
</script>
```

Or you can install it in your `main.js`

```javascript
// main.js
import Vue from 'vue'
import VueLoading from 'vue3-loading'
Vue.use(VueLoading)
```

## License

MIT
