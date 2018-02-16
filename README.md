# modal-vue

> A modal dialog component for Vue.js 2.x with large modal option

This is a version of [colin/modal-vue](https://github.com/colinf/modal-vue) modified to allow the usage of Bootstrap Modal's large modal feature.


## installation

```bash
yarn add github:IanBurry/modal-vue
```
Or

```bash
npm install --save github:IanBurry/modal-vue
```

Then, within the `<script>` tag of the component in which you want to use the `modal-vue` component you need to import it, and register it as a component.

```js
import Modal from 'modal-vue'
export default {
  components: { Modal },
  ...rest of component properties
}
```

Refer to [the vuejs documentation page](https://vuejs.org/v2/guide/components.html) for full details of using components.

### properties

One additional property is defined that can be passed to the modal component as an attribute

- largeModal (Boolean)


## usage

Set the **largeModal** attribute to **true** as shown below. The attribute can be bound to data, a computed property, or a method that returns boolean

```vue
<modal :showModal="showSourceDialog" :closeAction="closeSourceDialog" largeModal="true">
  <h1 slot="header">Select Source</h1>
  <select slot="body" :value="database.source" @change="changeSource($event.target.value)">
    <option v-for="source in ['', ...refdata.sources]">{{ source }}</option>
  </select>
</modal>
```

## demo
The included demo has been updated to show the large modal feature:

If you want to play around with the demo, then follow these steps to get it running locally:

```bash
git clone https://github.com/IanBurry/modal-vue.git
cd modal-vue
npm install
npm run demo
```

and then go to [http://localhost:8000](http://localhost:8000) to access it

