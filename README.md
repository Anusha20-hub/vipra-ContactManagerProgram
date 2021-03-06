# vipra-CPM
 This is a Contact Manager Program built as a part of interview task. This will allow the user to add, edit, delete and view the saved contacts

# Technologies Used
Node.js, Express.js, MongoDB, Mongoose, EJS and jQuery AJAX REST API.

# Installation in local
As a pre-requisite, You need to have NodeJS, NPM and MongoDB installed on your System to run the program

## To Install

Run `npm install` to install the Node Package Module

## Run

once we connect Mongo DB with the local server run `npm start` to confirm the connection

## Test

Run `./node_modules/.bin/mocha` in the terminal to run the test cases

 * The test results will be shown as below


    `vipra contacts test.`
    `√ should create contacts (49ms)`
    `√ should return all contacts`
    `√ should update contact`
    `√ should delete contact`
    ` 4 passing (110ms)`

Code is Running on 
+ http://localhost:3000/

# REST API
 1. POST/api/contact/
    This is the API used by the user to submit the input file to create the contacts, which has three fields to be filled to add the Contact, namely - Name, Email and Mobile number.
    
   # Response:200 OK
      * POST /api/contact HTTP/1.1
        Host: localhost:3000
        Content-Type: application/json
        Cache-Control: no-cache
        Postman-Token: ba5ada52-707e-8279-d5a5-570fa805a23b

        {
	     "name":"tom",
	     "email":"tom123@vipra.com",
	     "mobile":"99860786543"
        }
      "Success: Contact created successfully"  

 2. GET/api/contact/1
    This is the API used by the user to retrieve the contacts from the Database.

 3. PUT/api/contact/<:id>
    This is the API used by the user to update the contact details by specifying the object unique id.

    # Response:200 OK "Updated contact successfully"
       * Before updating:   
         {
	   "name":"john",
	   "email":"john123@vipra.com",
	   "mobile":"98760786543"
	  }
    
      * After updated:
         {
	    "name":"john",
	    "email":"john101@vipra.com",
	    "mobile":"98760786543"
	  } 
	  
   4. DELETE/api/contact/<:id>
      This is API used by the user to delete the existing contact.  

      
      # Response:200 OK
      
      * DELETE /api/contact/1 HTTP/1.1
        Host: localhost:3000
        Content-Type: application/json
        Cache-Control: no-cache
        Postman-Token: 6dd4d91f-4e0d-2b7b-4d04-e6a6665b568f

     {
	"name":"tom",
	"email":"tom123@vipra.com",
	"mobile":"99860786543"
     }
      "Success" "Deleted contact successfully"  
