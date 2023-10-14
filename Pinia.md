# Pinia

## Установка

```npm i pinia```

## Подключение к Vue3

```import { createPinia } from 'pinia';
import { createInertiaApp } from '@inertiajs/vue3';

createInertiaApp({
  setup({ el, App, props, plugin }) {
    const a = createApp({ render: () => h(App, props) })
      .use(plugin)
      .use(createPinia())
      .mount(el);
  },
})
```

Теперь pinia глобально установлена.

## Создание хранилища

```import { defineStore } from 'pinia';

const useBaseStore = defineStore('baseStore', {
	state() {
		return {
			name: 'Alfa',
		}
	}
});

export default useBaseStore;
```

## Подключаем созданное хранилище

```import useBaseStore from './baseStore';

const baseStore = useBaseStore();
```

Дальше переменная baseStore используется как обычно.
