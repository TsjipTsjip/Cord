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
init cord!

Bot.New ( "DiscordBotTokenHere" )!
Bot.MessageCreate (
	set prefix = "+"
	set warship = "hello"
	set master = "the kings"
	set user = ["146046383726657536", "001100"]
	set channel = ["290690164945190913", "02200", "0111"]
	set roles = ["Management", "Admin"]

	Command (prefix + "hi")
	if (User.ID == var(user)) {
		Channel.Send(m.ChannelID, "Testing this shit out, perhaps one day we will win! " + master)
	} else {
		Channel.Send(m.ChannelID, "Maybe not!")
	}
	end!
)!
```
