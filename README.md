# Tip Calculator

Create a simple tool to calculate tip/gratuity at a restaurant or for a service.

## Difficulty
Easy

## Prerequisites
- HTML structures and attributes
- Basic CSS styling
- Changing Elements in HTML using DOM
- JS Functions
- Variables
- Return Statements
- JS Math Methods
- Arithmetic

## Setup
1. Create the following files:
  - index.html (provided)
  - style.css
  - script.js

2. Check to see if your CSS and JS files are linked correctly in index.html

## Part I: HTML
1. Most of the code in the index.html file has been provided for your convenience. Look through the code and make sense of it. Ask your mentor questions if you do not understand something.

2. Write percentage values in the value attributes and messages in the option tags (around lines 24-29).
     - Make sure value attributes are in decimal form
     - Ex. 20% is 0.20, 42% is 0.42, etc.
     - Refer to screenshot for an idea of how to create your rating system.
                    
## Part II: CSS
1. Target the ```body``` element
     - set ```text-align``` to ```center```
     - set ```background-color``` to a color of your choice
    
2. Target the ```container``` id
     - set ```max-width``` to ```800px```
     - set ```margin``` to ```16px auto```
     - set ```background``` to color of choice
     - set ```padding``` to ```30px```
     - set ```border-radius``` to ```10px```
     
3. Target the ```boxes``` id
     - set ```display``` to ```flex```
     
4. Target the ```input-sections``` class 
     - set ```padding``` to ```16px```
     - set ```border``` to ```1px color of choice```
     - set ```margin-right``` to ```16px```
     - set ```border-radius``` to ```16px```
     
5. Target the ```calculate-button``` id
     - set ```margin-top``` to ```16px```

## Part III: JS
1. Create a function called calculateTip that takes in no arguments. This will calculate the tip per person. In this function create the following:
     - Set the value of the ```bill``` element in a ```var``` variable called "bill" using the DOM method ```document.getElementById("yourelementid").value```
     - Set the value of the ```rating``` element in a ```var``` variable called "serviceRating" using the DOM method ```document.getElementById("yourelementid").value``` 
     - Set the value of the ```people``` element in a ```var``` variable called "numOfPeople" using the DOM method ```document.getElementById("yourelementid").value```
     - ```ex. var variableName = document.getElementById("yourelementid").value```
     - Now that we have the values of the 3 things we need to calculate the tip each person owes, we can use arithmetics to calculate that. Do the following:
       -  Create a ```var``` variable called "tipPerPerson"
       -  Set that variable to equal to ```(bill * serviceRating) / numOfPeople```
       -  How would we deal with numbers that are more than 2 decimal places? We will use JS math methods to round to the nearest hundredth and then make them 2 decimal places with the following code:
       - ```javascript
         //round to nearest hundredth
         tipPerPerson = Math.round(tipPerPerson * 100) / 100;
         // 2 decimal plaes
         tipPerPerson = tipPerPerson.toFixed(2);
         ```
When this function is called, it will return the value in tipPerPerson.

2. Create a function called calculateBill that takes in no arguments. This will calculate the total bill each person has to pay. In this function create the following:
     - Set the value of the ```bill``` element in a ```var``` variable called "bill" using the DOM method ```document.getElementById("yourelementid").value```
     - Set the value of the ```people``` element in a ```var``` variable called "numOfPeople" using the DOM method ```document.getElementById("yourelementid").value```
     - ```ex. var variableName = document.getElementById("yourelementid").value```
     - Create a ```var``` variable called "tipPerPerson"
     - Call the ```calculateTip``` function and set that in the tipPerPerson variable.
     - Use the ```parseFloat``` method on tipPerPerson
     -  ```javascript
          tipPerPerson = parseFloat(tipPerPerson); //converts string into float :)
        ```
     - Now that we have the values of the 3 things we need to calculate the total bill each person owes, we can use arithmetics to calculate that. Do the following:
       -  Create a ```var``` variable called "billPerPerson"
       -  Set that variable to equal to ```(bill / numOfPeople) + tipPerPerson```
       -  How would we deal with numbers that are more than 2 decimal places? We will use JS math methods to round to the nearest hundredth and then make them 2 decimal places with the following code:
       - ```javascript
         //round to nearest hundredth
         billPerPerson = Math.round(billPerPerson * 100) / 100;
         // 2 decimal plaes
         billPerPerson = billPerPerson.toFixed(2);
         ```
When this function is called, it will return the value in billPerPerson.

3. Create an onlick event function when the calculate button is clicked. This will display the results of the calculations.
     ``` javascript
     document.getElementById("calculate").onclick = function() {
       //code here
     };
     ```
     - Inside the function, do the following:
       - ```document.getElementId("tip").innerHTML```
       - Call the ```calculateTip``` function and set that to equal to the line above
       - ```document.getElementId("perPersonBill").innerHTML```
       - call the ```calculateBill``` function and set that to equal to the line above
       - Example:
       ```javascript
       documeent.getElementId(yourelementid) = function call
       ```
     
## Completed Screenshot
https://github.com/yhanessaanne/tip-calculator/blob/main/Screen%20Shot%202023-01-20%20at%207.53.51%20PM.png?raw=true
     
## Stretch Goals
1. Create an option where you can input your own custom tip percentage where the user can type in a number that is not already in the options list.
2. Sometimes people will put in the negative numbers or leave a section blank. Create error messages of these invalid inputs by using if statements and conditions.

## Credits
This tip calculator is a variation of: https://codepen.io/cphemm/pen/reNwWd
