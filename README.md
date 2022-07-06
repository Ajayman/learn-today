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
   
# Creating (2019/7/17)                       https://www.atlassian.com/ru/git/tutorials/using-branches
   - git branch <branch name> => create branch in the origin
   - git branch -b <branch name> => create branch and switch to <branch name> at a time
   - git checkout <branch name> => switch to <branch name>
   - git branch -d localBranchName => delete branch locally
   - git push origin --delete remoteBranchName => delete branch remotely

# Merging (2020/3/25)
   - git merge <branch name>
   
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
    python.exe manage.py createsuperuser
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

2020/1/20 HTML5 Web Storage
# With Web Storage, web data can store data locally within the users browser
# Before HTML5 data had to be stored in cookies, included in every server request. Web storage is more secure and large storage 
can be stored locally
   There are two options to store data locally.
      window.sessionStorage
      Window.localStorage
 To set on local Storage
   localStorage.setItem("firstName", "Ajay")

2020/2/12 axios get from api
# axios({
                method: 'GET',
                headers: {'Authorization': 'Token 58b4e11dde2013b8b0d72c3d7760d85399fa09b9'},
                url: 'http://kasi.localhost:8001/api/v1/restaurant/restaurant-tables/' + this.uuid + '/'
            })
                .then((function (response) {
                    this.restaurant1 = response.data;
                    console.log(this.restaurant1);
                }).bind(this))
                .catch(function (error) {
                    console.log(error);
                })
     here this.restaurant doesnot work as function in then only works after api response. So this.restaurant must bind to 
     external this object instance 
     
     token: Cookies.get("token"),
     getEmployeeSetting(uuid) {
                this.showSelect = false;
                axios({
                    method: "GET",
                    headers: {Authorization: `Token ${this.token}`},
                    url:
                        "http://kasi.localhost:8001/api/v1/employee/employee-restaurant-settings/" +
                        uuid +
                        "/"
                })
                    .then(
                        function (response) {
                            this.update_employee.selectedStore = response.data.primary_store.uuid;
                            this.update_employee.selectedBuilding =
                                response.data.primary_restaurant_building.uuid;
                            this.update_employee.selectedFloor = response.data.primary_restaurant_floor.uuid;
                            this.update_employee.selectedFloorSection =
                                response.data.primary_restaurant_floor_section.uuid;
                            this.update_employee.selectedPosRegister = response.data.primary_pos_register.uuid;
                            this.showFloorSectionSelect = false;
                            this.showPosRegisterSelect = false;
                            this.getStoreList(response.data.primary_store.uuid);
                        }.bind(this)
                    )
                    .catch(function (error) {
                        console.log(error);
                    });
            },
 # install quasar cli
   npm i -g '@quasar/cli'(should enclose with '')
   
   not -> npm i -g @quasar/cli 
   
 # upgrade quasar version
   yarn policies set-version (update to latest version) https://classic.yarnpkg.com/en/docs/cli/policies/#toc-policies-set-version
   
  quasar forum (all info on quasar)    https://forum.quasar-framework.org/topic/3309/v1-a-guide-for-quasar-dotenv


# for gulp 4 version must matches to node(>12) version   https://stackoverflow.com/questions/55921442/how-to-fix-referenceerror-primordials-is-not-defined-in-node

# for running gulp 4 task running is different from gulp 3 task running
   as the gulp 4 requires .series or .parallel function
   
   
# Element UI form validation
   the prop name must be same with the model name to validate
   
# Javascript Events
   onchange => when input value change and focus on other input field
   onblur => when input field is out of focus to other input field without input field value change
   onload => when browser has completely loaded its page.

# Image type (2020/1/3)
   svg => stands for scalar vector graphics. SVG uses two dimensional vector graphics format created by WWC.
      It describes image using text format based on XML. 

# upgrade yarn globally through npm
   npm update --global yarn
   
   
# date format with vue-moment 
   https://github.com/brockpetrie/vue-moment?ref=madewithvuejs.com
   
# Asyc wait
   async before function means a function always returns a promise. 
   https://javascript.info/async-await
   
   
# scss import and export variable
   [scss features of import export] (https://vueschool.io/articles/vuejs-tutorials/globally-load-sass-into-your-vue-js-applications/)
   
# Gulp 4 
   installation is similar to previous version
   required var gulp = require('gulp');
   ```
      var nunjucksRender = require('gulp-nunjucks-render');
      var data = require('gulp-data');
      var watches = require('gulp-watch');
      var cleanCSS = require('gulp-clean-css');
      var autoprefixer = require('gulp-autoprefixer');
      var concat = require('gulp-concat');
      var rename = require('gulp-rename');
      var minify = require('gulp-minify');
      var uglify = require('gulp-uglify');
      var imagemin = require('gulp-imagemin');
      var cache = require('gulp-cache');
      var browserSync = require('browser-sync').create();
   ```
   # dont use uglify and minify on js at the same time
   
   ### For the error
   ```
   Replace Autoprefixer browsers option to Browserslist config.Use browserslist key in package.json or .browserslistrc file.
      replace 
   ```
   
   
   # create virtualenv for python 3.8
   ```
      1. install python3.8
      C:\Users\Ajay\AppData\Local\Programs\Python\Python38\python.exe -m pip install --upgrade pip

      2. install virtualenv

      C:\Users\Ajay\AppData\Local\Programs\Python\Python38\Scripts\pip.exe install virtualenv

      3. create virtualenv
      C:\Users\Ajay\AppData\Local\Programs\Python\Python38\Scripts\virtualenv.exe venv




      If lib magic issue in windows

    This worked for me:

    pip uninstall python-magic
    pip install python-magic-bin==0.4.14

   ```
   
   # lipipoint.com isotopes issues fixes
      load the isotopes code at first
      [design reference] (https://codepen.io/aylinmarie/pen/NjwOGv)
      
   # point to be noted on weekness(everest canvas)
   ```
      1. text color inconsistent
      2. focus text
      3. hover on similar text
      4. look and feel(similar layout pattern) in all the pages
      5. copy reference as it
      6. follow complete bootstrap documentation
      7. detail data in the detail page
      8. top nav bar should not cover more height in mobile
      9. product list clickable from whole section
      
   ```
   
   # flex wrap(2020/10/14)
     [flexwrap](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
     
   # issue while creating virtual venv(rcssmin issue)(2020/10/15)
      [link](https://www.danhuazhou.cn/article/2019/8/15/18.html)
      ```
         pip install wheel
         pip install rcssmin --install-option="--without-c-extensions"
         pip install rjsmin --install-option="--without-c-extensions"
      ```
   # Url Configuration in python project
      ```
         Create a url in config>urls.py
            path("canvas/size-and-price-guide/", pages.CanvasSizeAndPriceGuidePrintView.as_view(),
                       name='canvas_single_print')
         Url calls CanvasSizeAndPriceGuidePrintView.as_view() 
         Add a template assigned in template_name 
      ```

   # Print Specific Div 
   ```
   [Githublink] (https://gist.github.com/andrewlimaza/490a69417d9fe2df3f668195a7661605)
   1. Can be used using JS code but button not worked in normal preview
   2. Better to use CSS @media print media query to display: none to specific div and show to specific div
   
   ```
   
   # Use Vue in django template
   ```
      add delimiters and replace to {{ }}
      var appcustom = new Vue({
         delimiters: ['[[',']]'],
         el: '#appcustom',
         data: {
           message: 'Hello Vue!'
         }
       })
   ```
   [stacklink] (https://stackoverflow.com/questions/49948261/vuejs-data-wont-display/51007652)
   
   # Service Worker 
   ```
      Rich Offline Experice, Periodic Background sync, push notifications that require native application
      1. scripts work in background seperate from web page
      2. dont need user interaction
      
      Service worker include
      1. javascript worker can't access DOM directly instead Service worker communicate with postMessage and it can access DOM.
      2. programmable network proxy allowing how network request are handled from your page.
      3. terminated when not in use and restarted when next needed. when restart can be accessed from the indexedDB API.
   ```
   2022/6/20
   
   # Secure Shell
      SSH is used to creawte a secure channel between a local and remote computeer, White SSH is commonly used for secure terminal accress and file transfers, it can also be used to create a secure tunnel between computers for forwarding other netwoek connections that are not normally encrypted
   `
   add .gitignore to add node_modules to ignore node_modules folder to github
   `

   # share codes of node projects to github, friends, and clients
      `
      1. copy all file of project except node_modules and zip and share to the friends
      unzip the file and write npm install code in new project
   `
   # in github
      `
         1. git init
         2. add .gitignore file in the project
         3. 
         
      `

     # host node project in Heroku
      1. push project in github
      2. Create Heroku app `heroku create "app_name"`
   `  3.  in package.json in scripts add `start: node path_app.js`
      4. port should be specified as : `Process.env.port`
      5.  

   # First class function
      ` First cflass funtion is called when funcitons in that language are treated like anyu other variable. For example in such a language, a function 
      can be p[assed as an argument to other funcitons, can be returned by another function can be assigned as a value to a variable.
      
      const foo = funciton(){
      // something 
      } 
      
      foo(); // invoke it using the variable
      `
      
   # Promises in JS
      Promises are used to handle asynchronous operations in JS. They are easy to manage when dealing with multiple asynchronous operations where callbacks can 
      create callback hell leading to unmanageable code. 
      A Promise is an object that keeo track about whether a certain event has happended already or not.
      Determines what happens after the eveents has happened.
      
      `Three stages in Promises
         1. Pending
         2. Resolved -> Fulfilled
         3. Reject
      `
      // executor
      // promise produce
      cosnt pobjq = new Promise((resolve, reject) => {

      setTimeout(( ) => {
      let roll_no = [1,2,3,4,5];
      resolve(roll_name);
      reject('Error while communicating');
      }, 2000);
}

  //promise consume
    pobj1.then((rollno)=> {
        console.log(rollno);
        return getBiodata(rollno[1]);
        // getBiodata(rollno[1]).then((kuchbhi)=> {
        //     console.log(kuchbhi);
        }).then((kuchbhi)=> {
            console.log(kuchbhi);
        })
    .catch((error)=> {
        console.log(error);
    })
   

   # Async/Await
      There's a special syntax to work with promises in a more comforatble fashion, called async/await.  It's surprisingly easy to understand and use.
      
      The word "async before a funciton means one simple thing: a functoin always returns a promise.
      So the async keyword is added to functions to tell then to return a promise rather than directly returning the value 
      
      we can use await when calling any function that returns a Promise, including web API funcitons
      
      the keyword await makes JS wait until that proimise settles and returns its result.
      
 #   for create post we use app.post [http post request]
   `
      app.post("/router_path", async(req, res)=> {
         try{
             const user = new Student(req.body);
             const createUser = await user.save();
             res.status(201).send(createUser);
        }catch(e){
            res.status(400).send(e);
        }
      })
   `
   
   # Get Http request and retrieve list
  # read the data from registered students
  `
   app.get("/students", async (req, res)=> {
    try{
       const studentsData = await Student.find();
        res.send(studentsData);
      }catch(e){
        res.send(e);
      }
   })
`

// get the individual student data using id
app.get("/students/:id", async(req, res)=> {
    try{
        const _id = req.params.id;
        // console.log(req.params.id);
        const studentData = await Student.findById(_id);
        if(!studentData){
            return res.status(404).send();
        }else{
            res.send(studentData);
        }
    }catch(e){
        res.status(500).send(e);
    }
})

app.delete("/students/:id", async(req, res)=> {
    try{
        const _id = req.params.id;
       const deleteStudent = await Student.findByIdAndDelete(req.params.id);
       if(!req.params.id){
        return res.status(400).send();
       }
       res.send(deleteStudent);
    }catch(e){
        res.status(500).send();
    }
})

app.patch("/students/:id", async(req, res)=> {
    try{
        const _id = req.params.id;
        const updateStudents = await Student.findByIdAndUpdate(_id, req.body, {
            new: true
        });
        res.send(updateStudents);
    }catch(e){
        res.status(404).send(e);
    }
})    
 # Delete request in REST API using NodeJS & MongoDB

      
