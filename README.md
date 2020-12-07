# Import-as

To import named export aliases with the as keyword, we add the aliased variable in our import statement.

import { chefsSpecial, isVeg } from './menu';
In orders.js

We import chefsSpecial and isVeg from the Menu object.
Here, note that we have an option to alias an object that was not previously aliased when exported. For example, the isLowSodium object that we exported could be aliased with the as keyword when imported: import {isLowSodium as saltFree} from 'Menu';
Another way of using aliases is to import the entire module as an alias:

import * as Carte from './menu';
 
Carte.chefsSpecial;
Carte.isVeg();
Carte.isLowSodium(); 
This allows us to import an entire module from menu.js as an alias Carte.
In this example, whatever name we exported would be available to us as properties of that module. For example, if we exported the aliases chefsSpecial and isVeg, these would be available to us. If we did not give an alias to isLowSodium, we would call it as defined on the Carte module.


### QQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQ

1.
Within the body of missionControl.js, change each variable to its alias, with the exception of the variable in the import statement.

In the body, change:

availableAirplanes to aircrafts
flightRequirements to flightReqs
meetsStaffRequirements to meetsStaffReqs
meetsSpeedRangeRequirements to meetsSpeedRangeReqs
You will see an error in the console, but we’ll fix this in the next exercise.


Hint
A function with correct aliases should look like:

function displaySpeedRangeStatus() {
  aircrafts.forEach(function(element) {
   console.log(element.name' + ' meets speed range requirements: ' + meetsSpeedRangeReqs(element.maxSpeed, element.minSpeed, flightReqs.requiredSpeedRange));
  });
}
 
displaySpeedRangeStatus();
2.
Now modify the import statement to import aircrafts, flightReqs, meetsStaffReqs, meetsSpeedRangeReqs.


Hint
import { aircrafts, flightReqs, meetsStaffReqs, meetsSpeedRangeReqs} from './airplane';
