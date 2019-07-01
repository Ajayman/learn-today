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
      
      
# Reboot
   -  Element specific changes to the html
      eg. in <table> element -> .table-border
   
# components
   - Alert, Badge , breadcrumb

# 2019/4/23
# Json object and array filter
    - data= {one:{ id:1,name:'hiro', age:25}, two:{id:2,name:'hira',age:15}}; //assign data with object
    - datas.filter(data => data.age <20 )      //ES6 method to filter
    - datas.filter(function(data){if(data.age<25){return data}})  //using filter function
    - for (var i=0; i<datas.length; i++){ if (datas[i].age < 25) {filter_data.push(datas[i])}} //using for loop



# 2019/4/24
   #gulp pipe
      perform multiple task simultaneously
   #gulp-plumber
      execute task even when error using error handler
      
# 2019/4/25
   owl-carousel
      - No need to wrap in class="col" inside the owl-carousel class
      
# 2019/5/30
fixed first column and header -> https://www.cssscript.com/fix-table-header-column/

# 2019/6/3
SEO basics              -> https://moz.com/beginners-guide-to-seo/why-search-engine-marketing-is-necessary

# 2019/6/10
# Html Forms  
- html form for collecting user input, form element, input type, input attribute 
- form elements like type text,radio,submit and more    -> https://www.w3schools.com/html/html_forms.asp
# form validation
- form validation to send exact data to the server 
   eg. numeric validation, constraint validation(max,disabled,min),  -> https://www.w3schools.com/js/js_validation.asp
   
# Js Events
  - onclick, oninput(type and display simultaneously), onchange, mouse hover -> https://www.w3schools.com/js/js_htmldom_events.asp
# Created simple accordion using js add and remove css class\


# dom manipulation (2019/6/19)
   - get dom element's property using class name or tag name      https://www.w3schools.com/js/js_htmldom.asp
   - accessed the list of same named class using document.getElementsByClassName("ClassName");


#collaborator for other git account(2019/6/25)
   - setting and collaborator and search name and collaborate


# issue in mozilla of daterange picker(6/26)             http://www.daterangepicker.com/
   - dropdown list flicks because of dropdownlist knows only layout of body not above modal so need to add option in script
         "parentEl": "#modal Id"

# git command to pull data from forked repo(6/27)
   - git remote -v      -> shows current remote repo for you fork       https://help.github.com/en/articles/configuring-a-remote-for-a-fork
   - git remote add upstream http://(forked remote repo url)      -> new upstream that will be synced with the fork 
   - git remote -v       -> shows added upstream in remote
   
   - git pull upstream master       -> pull the changes made by other repo that you forked from

# JS api to get data from url endpoint(6/30)             https://www.taniarascia.com/how-to-connect-to-an-api-with-javascript/
   - it is an example to retrieve Json data from endpoint url 
   
# how to see server response in browser(7/1)    https://www.mkyong.com/computer-tips/how-to-view-http-headers-in-google-chrome/ 
   - from which url and the response the data is responded all are shown in network tab
