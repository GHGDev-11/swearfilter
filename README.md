# This library is meant for developers who want a quick way to filter out and remove swearwords.
\
Here's an example of a chat app without filters: \
\
OtherPerson: shit \
\
We don't want any of this vulgar language in our chats. \
## To filter out swearwords, use swearfilter. If you want to use the default filter (That is explained below), type this: \
\
`import swearfilter`
`swearFilter = swearfilter.Filter()`  
`while True:`  
`    chatMsg = input('OtherPerson: ')`  
`    retValue = swearFilter.DefaultFilter(chatMsg)`  
`    print(retValue)`  
  
This will be the output when someone sends a message:  
  
OtherPerson: ****  
  
## If you want to use a custom filter, type this:  

`import swearfilter`  
`swearFilter = swearfilter.Filter()`  
  
`swearlist = ['fuck', 'shit']`  
  
`while True:`  
`    chatMsg = input('OtherPerson: ')`  
`    retValue = swearFilter.ConfigureFilter(chatMsg, swearlist)`  
`    print(retValue)`  
  
## What do these functions mean?

+ `DefaultFilter()` - Filter out a swearword found in the message, look in the pre-made list of swearwords.
+ `ConfigureFilter()` - Filter out a swearword found in the message, look in a self-made list that you need to define yourself.

You can choose whether you want to use the default or configure filter.
