# learn-today
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
