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
   
# array filter JS(2019/7/8)
   - https://alligator.io/js/filter-array-method/
   
# Creating branch(2019/7/17)                       https://www.atlassian.com/ru/git/tutorials/using-branches
   - git branch <branch name> create branch in the origin
   - git branch -b <branch name> create branch and switch to <branch name> at a time
   - git checkout <branch name> switch to <branch name>
   
   
# Show commit history ->  git log
# Reset code to previous commited code -> git reset --hard



# Data Type JS 
  - String 
      name : 'ajay' or name : "ajay"
      
  - Int
      age : 28 ,
      
  - boolean
     boolean = true or boolean = false
  
  - undefined 
     value not assigned declared as undefined
     var car;
     
  - array 
     written by square bracket.
     index starts with 0
     array means list of different data type 
     array = ['name',3,{name: 'ajay', id : 3, gender: 'male'}, {name: 'bijay', address: 'kamalbinayak'}]
     
  - object 
     object are written by curly bracket
     written as key: value seperated by comma
     obj = {device: 'laptop', price: "20k", id: 1, boolean : true, model : undefined, person: []}
     object = {citizenship_no. : {name: 'ajay', address: 'kamalbinayak', number: 9841110000}};
     
# Static data type:(C++, java)
     static data means data type is declared before you can use them.
     statically typed language perform type checking at compile time(converting to executable code).
      boolean result = true;
      
# Dynamic data type:(js, python)
      dynamic data type means data type is automatically changed according to assigned data 
      dynamically typed language perform type checking at runtime(at the time of when executable code is running)
      
   compile time and runtime    http://net-informations.com/python/iq/checking.htm

# request and response in server (http request)
     it is like request to the bank and response by the the bank
      Example: if you registered in bank with NPR account, if you deposit in dollar and there is no option to accept dollar by the bank then you are rejected or there is an error according to programming logic 
      OR if you request for dollar they have option to convert and give dollar then they accept and there is no error 
   
   
# run python server
   Run python server in windows
```

    venv\Scripts\activate           -- to activate venv
    pip install -r requirements.txt
    python.exe manage.py migrate
    python.exe manage.py users
    python.exe manage.py runserver      -- to run server
    python.exe manage.py runserver 0:8000   -- to run in external ip address need to IPV4 address of PC + port
```

# nano scroll wont work on drop down  (nano scroll reference -- https://jamesflorentino.github.io/nanoScrollerJS/)
   you need to initialize nano while bootstrap dropdown is clicked 
    -- https://stackoverflow.com/questions/37183971/nano-scroller-is-not-working-in-bootstrap-dropdown-and-model-box
    
    
# zoom effect owl carousel while hover and other sibling decreasing opacity --https://www.trysmudford.com/blog/fade-out-siblings-css-trick/
 .parent:hover > * {
   opacity: 0.5;
   }
   .parent:hover > *:hover {
      transform: scale(1.1);
      opacity: 1;
   }
  
# owl carousel height can be increased by
   https://stackoverflow.com/questions/47739738/owl-carousel-div-height-for-image-hover 
   
  .owl-stage-outer {
    padding: 10px;
   }

2019/11/4 create env(while you want to access the local or cloud backend code in your frontend server/project)
# env create to host_name, server_protocol, app_debug to access from cloud or from local storage

2019/11/20 venv install in python project
#(code) virtualenv.exe venv  -> to install vitual environment(venv) in python project

2019/11/20 Live template in webstorm/pycharm 
# go to setting -> editor -> live template 
# fill abbreviation(shortform), description, template code
