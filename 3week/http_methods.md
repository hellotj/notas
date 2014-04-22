##HTTP Methods
####4.21.14 // Hannah	


**GET**	
	
	GET - request information
	1.0 -> 
	Form <a href="yahoo.com">
	GET
	
**POST**

	Submit Data
	1.0 ->
	Form
	
**PUT**

	1.1 
	URI
	Sending
	Update - don't want to post another one, you want to change what's already there. Like editing a wikipedia entry. can't do it within HTML, just javascript. 
	
**DELETE**

	Delete resource
	-> success
	-> didn't

**HEAD**

	Request metadata
	1.0

**Patch**

	Partial update
	1.1 -> 2010
	
**Server Game**

	1.1 -> 2010
	
	ID of lambshank
	SI "get '/'"
	SI Get /albums
	SI Get /albums/17
	SI Get /photos/63
	
	Create task "finish the lesson"
	S2 get '/'
	S2 POST "/todolist" - Create the lesson
	
	Created
	
	} id: 72
	Description: ""Finish the lesson"
	
	Task Organizations
	S3 Get "/"
	S3 Get "/articles"
	
	
**Why is this useful?**

Because in angular or jQuery you're going to be making manual API requests.  