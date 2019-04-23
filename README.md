# learn-today
#2019/4/22
#Theming Bootstrap 4
1. Can be customize with our new built-in sass variable for global style
- Variable
   eg. $body-bg: #000;
    @import "../node_modules/bootstrap/scss/bootstrap";
- maps
    eg. $theme-colors:(
    "primary": #0074d9,
    "danger": #ff4136,
    );
    adding color be like:
    $theme-colors:(
    "custom-color": #900
    );
- mixins
   for reuse the code
   @mixin transform($property){
      transform: $property
   }
   call the transform from
      .box{@include transform(rotate(30deg));}
      
      
   #Reboot
   -  Element specific changes to the html
      eg. in <table> element -> .table-border
   
   #components
   - Alert, Badge , breadcrumb

 #2019/4/23
 #Json object and array filter
    - data= {one:{ id:1,name:'hiro', age:25}, two:{id:2,name:'hira',age:15}}; //assign data with object
    - datas.filter(data => data.age <20 )      //ES6 method to filter
    - datas.filter(function(data){if(data.age<25){return data}})  //using filter function
    - for (var i=0; i<datas.length; i++){ if (datas[i].age < 25) {filter_data.push(datas[i])}} //using for loop
