
 Version : 1.0
 Name    : Jquery scroll paging
 Author  :  Satyam Kumawat <satyam2707@gmail.com>
 ===================================================

 This program is free package
 This program is distributed in the hope that it will be useful,
 This package is based on JQUERY AND AJAX
 

=======================
 GENERAL INTRUCTIONS 
=======================

PUT THE WHOLE FOLDER IN YOUR HTDOCS(xampp-php) and run in browser.

EXAMPLE: 
==============
$(function() {
              	    var offset = 2;
	                $(document).scrollPaging({
								                url :   'content.php', //required
								                totalRecordCount : 20,//required
								                offset :offset, //required
								                data :'key=value',//you can pass extra params here
								                beforeSend : function(){
								                	 var loader = $('<div id="scrollLoader">loading please wait ....</div>')
								               		 $('#wrapper').append(loader);
	                							},
	                							success : function(result) { //required
	                								
	                								 $('#scrollLoader').remove();
								                	 $('#wrapper').append(result);
								                }
	                });
                });

1. OFFSET :- It is just like a limit(number of records you want to fetch on each scroll)
2. totalRecordCount  :- Total number of records (disable the scrolling once reach this number)
3. data  :- not required but you can send extra parameter in your request
4. beforeSend  : Put your code which need to execute before each request.
5.  success : Put your code which need to execute after each request.


Important Note :-
===================
All the paramerter used in this plugin is same as a NORMAL AJAX REQUEST SO YOU CAN PASS PARAMETER .