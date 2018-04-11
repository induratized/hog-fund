# Step to perform eslint

##  Install eslint 
  1. Locally - under your sandbox/src/main/ folder via the below npm code

    `npm i -D eslint`
  2. Globally 

    `npm i -D eslint -g`

##  Run eslint for you file/project folder
  **Via local eslint install change to your src/main folder**
  1. For all js files under webapp

      `eslint ./`
      
  2. For specific file/folder

      `eslint <file_folder_path>`

  **Via global eslint**
  1. For all files and folder

      `eslint <file_folder_path>`

  **Auto-fix**
  1. to perform fixes that eslint can do (for ex. semi colons , single quotes), suffix 
  `--fix` flag to the above two eslint syntax

##  Ignore file/folder from parsing
    To make eslint ignore any file or folder include there path in '.eslintignore' file. 
    For more info see - https://eslint.org/docs/user-guide/configuring#ignoring-files-and-directories


# Common angular/js style guide as prescribed by eslint 

_ **The indexController controller should follow this pattern: /[A-Z].*Controller$/**
      controller name should start with capital letter.
_ **You should use the function syntax for DI**
    to force user to abide by the function syntax under controller definition `.controller([ [<injection_names_string,>[, <injection_names_string>]] , function([<injection_names_string,>[, <injection_names_string>]] )])`
    used the eslint rule "angular/di" - see .eslintrc

##  Best for testing purpose
_ You should use the `$window` service instead of the default `window` object https://docs.angularjs.org/api/ng/service/$window

_ You should not set properties on $scope in controllers. Use controllerAs syntax and add data to "this" https://toddmotto.com/digging-into-angulars-controller-as-syntax/ 

_ You should not use "this" directly. Instead, assign it to a variable called "vm" ,  https://github.com/Gillespie59/eslint-plugin-angular/blob/master/docs/rules/controller-as-vm.md

_ You should use the `$interval` service instead of the default `window.setInterval` method 

_ You should use the `$timeout` service instead of the default `window.setTimeout` method

_ Using $$-prefixed Angular objects/methods are not recommended
  eg. ` $location.$$search(<paran_name>) `
_ You should use the "log" method of the AngularJS Service $log instead of the console object
  inject $log service and use `$log.log`, `$log.info`, `$log.error` etc instead of `console` object's methods

_ You should use the `angular.toJson` method instead of `JSON.stringify`

_ You should use the `angular.fromJson` method instead of `JSON.parse`
