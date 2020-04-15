## Component Design Pattern
  1. Use object props syntax rather than array of string props syntax
    eg. props: {
      image: {
        type: String,
        // required: true,        //if there is default value no need to define require property
        default: 'movie.jpg'
      },
      title: {
        type: String,
        required: true
      }
    }
    
    rather than
    eg. props: ['image', 'title']
    
    
 ## Token Based Authentication using JWT
