<template>
    <div>

      <TabMenu :model="items" />
      <Nuxt/>
      
    </div>
  </template>
  
  <script>
  export default {
      data() {
          return {
              items: [
                  {label: 'Home', icon: 'pi pi-fw pi-home', to: '/home'},
                  {label: 'Gastos', icon: 'pi pi-sliders-h', to: '/gastos'},
                  {label: 'User', icon: 'pi pi-user', to: '/user'},
              ]
          }
      }
  }
  </script>
  
  <style scoped>
  
  </style>