## Vue router
  ``` bash
  is the official router for vuejs. It deeply integrates with vue.js core to make building single page applications.
  ```
  
 ### Getting Started
 ```
  Creating a single page application is dead simple. Map our component to the routes and vue router know where to render them.
  #### Process
    1. If using a module system import Vue and VueRouter and then call Vue.use(VueRouter)
    2. Define router components
    3. Define some routes
    4. Create the router instance and pass the routes options
    5. Create and mount the root instance
  ```
  
 
 ### Dynamic Route Matching
  ```
  We may have user component which should be rendered for all users but with different user IDs. 
  A dynamic segment is denoted by a colon :.
  routes can be defined as { path: '/user/:id', component: User }
  When a route  is matched, the value of the dynamic segments will be exposed as this.$route.params in every component
  ```
