# This library is meant for developers who want a quick way to filter out and remove swearwords.
  
Here's an example of a chat app without filters:  
  
OtherPerson: shit  
  
We don't want any of this vulgar language in our chats.  
## To filter out swearwords, use swearfilter. If you want to use the default filter (That is explained below), type this:  
  
```py
import swearfilter
swearFilter = swearfilter.Filter()
while True:
         chatMsg = input('OtherPerson: ')
         retValue = swearFilter.DefaultFilter(chatMsg)
         print(retValue)
```
  
This will be the output when someone sends a message:  
  
OtherPerson: ****  
  
## If you want to use a custom filter, type this:  

```py
import swearfilter
swearFilter = swearfilter.Filter()
  
swearlist = ['fuck', 'shit']
  
while True:
    chatMsg = input('OtherPerson: ')
    retValue = swearFilter.ConfigureFilter(chatMsg, swearlist)
    print(retValue)
```
  

### What do these functions mean?

+ `DefaultFilter()` - Filter out a swearword found in the message, look in the pre-made list of swearwords.
+ `ConfigureFilter()` - Filter out a swearword found in the message, look in a self-made list that you need to define yourself.
+ `GetListLength()` - Get the length of any list, this could be handy for a number of reasons.
+ `PrintPremade()` - Print the premade list.

You can choose whether you want to use the default or configure filter.

## Get length of a list

This is a simple and straight forward function.
If you need to know the length of a list (How many words there are in the list), use this function.

```py
import swearfilter
swearFilter = swearfilter.Filter()

swearlist = ['fuck', 'shit']

swearFilter.GetListLength(swearlist)
```

## Get premade list

```py
import swearfilter
swearFilter = swearfilter.Filter()

swearfilter.PrintPremade()
```

# History

--- V0.5 ---

Updated package because of major error.

--- V0.4 ---

- DefaultFilter() :: Changed entire filter, so it will filter any message.
- ConfigureFilter() :: Changed entire filter, so it will filter any message.
- GetListLength()
- PrintPremade() :: Print the premade list if you want to add it to your custom filter.

--- V0.3 ---

- DefaultFilter()
- ConfigureFilter()
- GetListLength()
