## Website Performance Optimization portfolio project
#############################################################################################################
#Changes made to the index.html file to achieve a 90 or above score in PageSpeed Insights:
#1) Optimize the JS script																				
#		  - since the scripts were small enough the scripts were included in the index.html file to	
#  		  eliminate the render-blocking javascript (can also be loaded async if file is too large).									
#  		- minify the javascript to reduce the size.	
#  																										
#2) Optimize the CSS script 																			
#		- similar to the Javascript the CSS files were small enough and were "inlined" in the index.html.	
#		- minify the CSS.																				
#																										
#3) Optimize images - images where resized and compressed to reduce the size to optimize the loading.	
#
#4) Minify the index.html file - to eliminate any unnecessary characters in the code.
#############################################################################################################


#### 2: Optimize Frames per Second and Time to resize pizzas in pizza.html/main.jas
#############################################################################################################
#Changes made to views/pizza.html and views/js/main.js:																							
#1) Optimize the JS script																					
#  		-  loaded files async when warranted.														
#  																											
#2) Optimize the CSS script 																				
#		- the CSS file was small enough and was "inlined" in the pizza.html.								
#		- minify the CSS.																					
#																										
#3) Optimize images - images where resized and compressed to reduce the size to optimize the loading.	
#																											
#4) DOM elements that were being retrieved insisde the loop were coded instead before the for loop line.
#   var pizzasDiv = document.getElementById("randomPizzas");
#   for (var i = 2; i < 100; i++) {
#   //var pizzasDiv = document.getElementById("randomPizzas");
#   pizzasDiv.appendChild(pizzaElementGenerator(i));
#    
#   //Minimize the retrieval of the pizza container element by just calling it once in this line of code
#   //and assigning it to a variable instead of calling it multiple times inside the for loop
#   var rpc = document.querySelector(".randomPizzaContainer")
#   var dx = determineDx(rpc, size);
#   var newwidth = (rpc.offsetWidth + dx) + 'px';
#5) minify the pizza.html and main.js   

//No need to reiterate the retrieval of the document.body.scrollTop, move it out of the for loop
var docscrollTop = document.body.scrollTop;
#############################################################################################################

##### 2: Optimize Frames per Second in pizza.html
