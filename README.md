# Cord
![Cord v0.0.1](https://github.com/proxikal/Cord/blob/master/spacer.png?raw=true)![Cord v0.0.1](https://github.com/proxikal/Cord/blob/master/cord.png?raw=true)  
A custom programming language specialized for creating your own Discord Bot.  
Inspired by my A.R.S *(Auto Response System)* inside of Echo 2.0 Bot.
  
## Goals
> Our main goal is to create a simplified language That will attempt to compete with top languages such as.. **C, Golang, Ruby, Rust** Yet simple enough to understand like **HTML, Javascript**..  
  
## Wikipedia
> You can view our progress on this language in our Github Wikia!
  
## Example cord script
**File:** *main.q*
```go
Bot.New ( "DiscordBotToken" )
Listen()

var prefix = "+"
var warship = "to the kings of the world!"

cord =>
	Message.Contains(prefix + "hello"):test
	User.ID("146046383726657536", "test2", "ect"):hi
<>

cord =>
	Message.Contains("testing:"):complete
<>

set (hi) =>
	{kick}{/user} you have been warned for saying `Hello`
<>

set (test) =>
	Testing all the good stuff!
<>

set (complete) =>
	We are the one, the true...the proud!
<>
```
