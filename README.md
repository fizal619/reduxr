#Reduxr

![](https://media.giphy.com/media/TjXDDtM9Xt0k0/giphy.gif)

##Introduction

After a great introduction to Redux by [Jason](http://github.com/yono38), you feel so inspired that you're ready to launch a reluctantly built micro-blogging platform. **Reduxr** obeys the startup naming convention of using the suffix *r* shamelessly, and is your brainchild. But it's not yet ready for investors!

##Setup

* You should clone the boilerplate [repository](https://github.com/yono38/react-redux-boilerplate). 
* Make sure that no other webpack-dev-server isn't running on port 8080.
* **Helpful:** Go through the **REASONABLY SHORT** [video tutorial](https://egghead.io/courses/getting-started-with-redux) as prep if you can.  

##Outline

* Your app should be able to save a tweet from an input. 
* Your app should be able to output a list of tweets.   

#####Bonus Goal
* Make your app able to delete tweets. 

##Steps

Great! Now that you're fully briefed, let's get into the thick of it. 

1. First thing's first, take a look back at the working version of the counter app and note the directory structure and how every file was laid out and connected.
2. Next create your **stateless** React components. You'll need two to make your app a reality: 
* `MicroBlog.jsx` - The provider component. 
* `Tweetlist.jsx` - Where we'll have our input and list of tweets. 

3. If you're not sure where to start linking the files together just remember you should only need a single `action` file and a single `fixture`.  
4. Your `store` should hold a state like the following:
```
{
	tweets: [...],
	currentID: 0 //each new post should increment off of this 
}
```
5. Now that you've got those set up, make sure you set up the **MicroBlog** component to be the **Provider** abd have **TweetList** as a child. 
6. **TweetList** should interact with the store through the **Provider**, to save strings from an input box or forms into the store. Then display them in an unordered list. So this should mean that the **TweetList** component would have a value from the store passed into it with an array of objects as follows. 
```
[	
	{
		text: "something",
		id: 1 //computed by incrementing currentID in the store
	},
	{
		text: "something else",
		id: 2
	}
]
```	
6 . TEST TEST TEST AFTER EVERY ITERATION!

####Bonus
* Implement a delete button to delete a given post by id. 

##Tips:

* You can use the spread operator to help you add tweets to the tweet array in the store. Slide 36 in Jason's Redux class.  
* Make your React app static before diving into the functionality! It'll keep you sane, since you only have to worry about taming Redux afterwards.
* Remember your component need not be a class or have state. 
* If tackling the bonus, just remember that the filter function is pure, since it makes a copy of the original.
 
##Grading

You will be assessed on implementation of the Redux architecture; since as a new developer just implementing this might be challenging enough. Good luck! Let's hope **Reduxr** gets funded. 

**Make sure to submit your assignment as a link to a git repository.**

   
  
