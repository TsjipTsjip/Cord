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
	set prefix = "+"!
	set user = "["146046383726657536", "001100"]"!
	set channel = "["285116606349049856", "02200", "0111"]"!
	set roles = "["Management", "Admin"]"!

	inherit "funcs.q"!
	
	// Testing command for new features.
	Bot.Command ("var(prefix)hi")
		if (User.ID == var(user)) && (User.HasRole == var(roles)) {
			Channel.Send(m.ChannelID, "Testing stuff out! break; It worked?!?!?!")
		}
	end!

	Bot.Command ("var(prefix)hello")
		Channel.Send(m.ChannelID, "Love long in prosper.")
	end!

	Bot.Command ("var(prefix)update")
		System.Reload()
		Channel.Send(m.ChannelID, "<@m.UserID> You have restarted the cord script. All updates are live.")
	end!

	Bot.Command ("var(prefix)pm")
		User.Send(m.UserID, "<@m.UserID> You are awesome.")
	end!
)!
```
  
**File:** *funcs.q*
```go
init cord!

set cars = "world"!

	Bot.Command ("var(prefix)wreck")
		if (User.ID == var(user)) && (User.HasRole == var(roles)) {
			Channel.Send(m.ChannelID, "You got this!")
		}
	end!
```
