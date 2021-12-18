###  A Mini Microservice App


####  Table of Content
  * [Overview](#overview)
  * [Architecture](#architecture)
  

### Overview 
In this project, the objective is to understand the basic of microservice  architecture by implementing a very simple blog application ; Where user can create a blog post and allowing users to create comments on them . When an user first come to our application we are gonna show a below  form through which user can create posts . 

![Home screen ](https://raw.githubusercontent.com/ditikrushna/A-Mini-Microsrevice-App/main/assets/project%20home%20screen.png)

Once they do so, we're then going to display the posts they just created down here at the bottom,
the screen. That would be the post that was just created. We'll show the title, the post will show the number of comments it was associated with it, and we'll also have a little forum right here to add some comments to that individual post.
![application with posts and comments ](https://raw.githubusercontent.com/ditikrushna/A-Mini-Microsrevice-App/main/assets/full%20images.png)

### Architecture

I have built the back-end on microservice architecture where we have majorly four components and those are the following:  
- Post Service 
- Comment Service 
- Query Service
- Moderation Service
- Event Bus 

**Post Service :** 
The post service is responsible for  creating post and listing the posts ; 

**Comment Service :**
This comment service is responsible for creating comments and listing comments of a particular posts 

**Query Service:**
the goal of this service, we want to have one service that we can make a request to to get a full listing of all the different posts and their associated comments. The one request, all the data we need to actually implement this thing. We're going to give it to different route handlers, one handlers going to receive events from our event bus. Our service is going to care about events of type post created and come and create it whenever it sees these events. It's going to take the data contained inside the event itself and then assemble it all into some very asy to access data structure. 

![query service](https://raw.githubusercontent.com/ditikrushna/A-Mini-Microsrevice-App/main/assets/query%20service.png)

**Event Bus:** 



**Architecture Diagram**

![enarchtecture diagram](https://raw.githubusercontent.com/ditikrushna/A-Mini-Microsrevice-App/main/assets/diagram%20with%20event%20bus.png)



