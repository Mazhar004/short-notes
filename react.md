# React #                  
## Install (Environment in Ubuntu) ##
* ### Web Address for instruction: [Link](https://github.com/nodesource/distributions/blob/master/README.md#installation-instructions) ###
    * #### Install NodeJS: ####
      * ``` sudo apt-get install curl python3-software-properties ```
      * ``` curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash - ```
      * ``` sudo apt-get install nodejs ```
    * #### Check Version: ####
      * nodejs –version
      * npm –version

## React Setup ## 
* ### Install react ###
  * ``` sudo npm i -g create-react-app@1.5.2 ```
* ### Create app with name react-app
  * ``` create-react-app react-app ```
* ### if problem: ###
  * ``` sudo chown -R $USER:$GROUP ~/.npm ```
  * ``` sudo chown -R $USER:$GROUP ~/.config ```
* ### Then Again: ###
  * ``` create-react-app react-app ``` 
  * ``` cd react-app ```
  * ``` npm start ```

## Bootstrap: ##
* ### Install: ###
  * ``` npm install bootstrap@4.1.1  ```
  * ``` npm install bootstrap jquery popper.js --save ```
* ### Import: ###
  * ``` import "bootstrap/dist/css/bootstrap.css"; ```
  * ``` import "bootstrap/dist/js/bootstrap.min.js"; ```

## Font Awesome: ##
* ### Install: ###
  * ``` npm i --save @fortawesome/fontawesome-svg-core ```
  * ``` npm i --save @fortawesome/free-solid-svg-icons ```
  * ``` npm i --save @fortawesome/react-fontawesome ```
* ### Import: ###
  * ``` import { faTasks } from "@fortawesome/free-solid-svg-icons"; ```
  * ``` import { FontAwesomeIcon } from "@fortawesome/react-fontawesome"; ```
  * ``` <FontAwesomeIcon icon={faTasks} /> ```
