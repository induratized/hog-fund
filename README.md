# Step to perform eslint

##  Install eslint dependencies
  **Install eslint globally**

    npm i eslint -g

  **Install other dependencies - navigate to src/main/ folder and run**

    npm install

##  Run eslint for you file/project folder
  **For all js files under webapp**

    npm run eslint -- <webapp_js_folder_path>
      
  **For specific file/folder**

    npm run eslint -- <file_folder_path>

  **For AUTO-FIXes that eslint can do (for ex. semi colons , single quotes)** 

    npm run eslintfix -- <file_folder_path>

##  Ignore file/folder from eslint parsing

    To make eslint ignore any file or folder include there path in '.eslintignore' file. 
    For more info see - https://eslint.org/docs/user-guide/configuring#ignoring-files-and-directories


# Common angular/js style guide as prescribed by eslint 

- The indexController controller should follow this pattern: /[A-Z].*Controller$/

  `controller name should start with capital letter.`

- You should use the function syntax for DI

  to force user to abide by the function syntax under controller definition 
  
  `.controller([ [<injection_names_string,>[, <injection_names_string>]] , function([<injection_names_string,>[, <injection_names_string>]] )])`
  
  used the eslint rule "angular/di" - see .eslintrc

##  Best for testing purpose
_ **You should use the `$window` service instead of the default `window` object**
  
  https://docs.angularjs.org/api/ng/service/$window

_ **You should not set properties on $scope in controllers. Use controllerAs syntax and add data to "this"**
  
  https://toddmotto.com/digging-into-angulars-controller-as-syntax/ 

_ **You should not use "this" directly. Instead, assign it to a variable called "vm"**
  
  https://github.com/Gillespie59/eslint-plugin-angular/blob/master/docs/rules/controller-as-vm.md

_ **You should use the `$interval` service instead of the default `window.setInterval` method**

_ **You should use the `$timeout` service instead of the default `window.setTimeout` method**

_ **Using $$-prefixed Angular objects/methods are not recommended**

  eg. ` $location.$$search(<paran_name>) ` don't use them

_ **You should use the "log" method of the AngularJS Service $log instead of the console object**
  inject $log service and use `$log.log`, `$log.info`, `$log.error` etc instead of `console` object's methods

_ **You should use the `angular.toJson` method instead of `JSON.stringify`**

_ **You should use the `angular.fromJson` method instead of `JSON.parse`**

_ **You should not use directly the "undefined" keyword. Prefer angular.isUndefined or angular.isDefined**
