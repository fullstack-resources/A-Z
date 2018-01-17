https://github.com/vuejs/vue-devtools#vue-devtools
https://vuejs.org/v2/examples/todomvc.html
https://router.vuejs.org/en/essentials/getting-started.html
https://hackernoon.com/5-free-vuejs-tutorials-3caa8ff865e9
https://www.sitepoint.com/up-and-running-vue-js-2-0/
https://matthiashager.com/complete-vuejs-application-tutorial
https://alligator.io/vuejs/rest-api-axios/




https://stackoverflow.com/questions/43277705/vuejs-difference-between-computed-and-watched-properties
https://codingexplained.com/coding/front-end/vue-js/watchers


https://github.com/vuejs/awesome-vue
https://github.com/vuejs/vuex/tree/master





https://github.com/DivanteLtd/vue-storefront
https://www.figma.com/file/VKyqbHFI55TKIKcQlFLiVpVF/Vue-Storefront---Open-Source
https://www.themexpert.com/blog/vuejs-admin-templates-with-bootstrap


https://medium.com/the-vue-point


















# some important notes:

(Under List Rendering)

Vue does not allow dynamically adding new root-level reactive properties to an already created instance. However, it’s possible to add reactive properties to a nested object using the Vue.set(object, key, value) method. For example, given:
var vm = new Vue({
  data: {
    userProfile: {
      name: 'Anika'
    }
  }
})
You could add a new age property to the nested userProfile object with:
Vue.set(vm.userProfile, 'age', 27)

You can also use the vm.$set instance method, which is an alias for the global Vue.set:
vm.$set(this.userProfile, 'age', 27)
Sometimes you may want to assign a number of new properties to an existing object, for example using Object.assign() or _.extend(). In such cases, you should create a fresh object with properties from both objects. So instead of:
Object.assign(this.userProfile, {
  age: 27,
  favoriteColor: 'Vue Green'
})
You would add new, reactive properties with:
this.userProfile = Object.assign({}, this.userProfile, {
  age: 27,
  favoriteColor: 'Vue Green'
})




