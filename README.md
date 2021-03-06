# Data Engineering Notes, Spring 2015

## Lecture 1

#### Topics around data engineering:
* Social Networks
* Data Analytics - sampling (made possible my statistics), machine learning 
* Storage - NoSQL (document, graph, key-value stores, columnar)
* Data Collection and Cleaning (character encodings, etc.)
* Infoviz - D3, Tableau, Excel, R

Data Modeling is hard.

#### Data Lifecycle
Question (curation, triage, persistence) -> collection/generation -> clean up -> storage -> processing/analysis -> query+visualize+act -> (back to beginning)

#### HTTP request and response cycle
http:// <-> http request or response (networking protocol, GET/POST/PUT/DELETE) -> HTML

## Lecture 2

#### HTTP request and response cycle cont'd

Browser <--> Web/App Server <--> Handler

1. Browser sends request with relevant parameters to Server  
  - ebay.com/Products/10 where ebay.com is the address of Server and Products/10 are relevant parameters.  
2. Wait for Handler response  
  - HTML, files, etc., eg. index.html  
3. Browser does what it can, but will make more requests as needed   
  - Eg. when encountering \<img>, \<script>, etc. in index.html.

#### REST: REpresentational State Transfer

[REST](http://en.wikipedia.org/wiki/Representational_state_transfer "Wiki Link") is an architecture for creating webservices which allow anything connected to the network to cummunicate via a common communications protocol (HTTP, etc.). 

URI - > Identifies the name of a resource representation.

Resources have methods similiar to or the same as HTTP: 
  * Create
  * Read
  * Update
  * Destroy

**REST Example:**
```
Resource: /users (all) or /users/id (specific)
Operations on /users:

GET    - Read           (Return current state)
POST   - Create {DATA}  (Create user with appropriate data)
PUT    - Update         (Update existing user)
DELETE - Destroy        (Delete user)
```

**Considerations when designing service:**  
 1. What database type?  
 2. How to handle new contact ids?  
 3. What inputs are acceptable?  
 4. How to format outputs?  
 5. How to implement error handling?  
 

#Lecture 9

###Gist created to clarify Javascript's this variable: 

Four ways of setting this: 
Default Binding
Implicit Binding
Explicit Binding
Constructor

###Contacts Web API:

Cleaned up the app because too cluttered. 
Used RequireJS, which tackles problems w/ script tags, JS libraries, and managing the files created because of code modularization.
Bower downloads middleware.
RequireJS uses module IDs.

###IIFE: Immediately Invoked Function Expression
Common convention in JS is module pattern.
Only functions create new scope in JS (blocks do not, etc.).

### Getting Data from Twitter (PART 1):
Go to dev.twitter.com -> Manage your apps (at bottom) -> Create New App
Create access token after modifying read/write permission.

#Lecture 10

Consumer keys and access tokens used by OAuth. OAuth is a web-based security protocol. CK identifies an application while AT identifies specific user. 

Bunch of supporting programs to help with management. 

Bunch of Ruby implementation stuff.

#Lecture 11


Looking at twitter data collection framework. 5 REST API endpoints 2 Streaming API endpoints. Handles twitter rate limits. Provides implementations of working w/ timelines and working with cursors. 

Description of framework. 

#Lecture 14

###MongoDB Presentation

Document based DB. Stores in BSON. Row replaced with document. No schema. BD indexes are data structures. Very scalable. 

CAP THEOREM: Consistency and Availability compete

Collection thought of as table with dynaic schema. Each dog has special key"_id". 











