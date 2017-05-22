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
	set warship = "hello"!
	set master = "the kings"!
	set user = ["146046383726657536", "001100"]!
	set channel = ["290690164945190913", "02200", "0111"]!
	set roles = ["Management", "Admin"]!

	inherit "commands.q"!

	Bot.Command ("var(prefix)test")
		if (User.ID == ["146046383726657536"]) {
			Channel.Send(m.ChannelID, master.ToUpper() => "Testing: " => warship.ToUpper())
		}
	end!

)!
```
  
**File:** *commands.q*
```go
init cord!

	// Testing command for new features.
	Bot.Command ("var(prefix)hi")
		if (User.ID == var(user)) && (Channel.ID == var(channel)) {
			Channel.Send(m.ChannelID, "Testing stuff out! break; It worked?!?!?!")
		} else {
			Channel.Send(m.ChannelID, "Nope!")
		}
	end!

	Bot.Command ("var(prefix)hello")
		if (User.ID == var(user)) || (Channel.ID == var(channel)) {
			Channel.Send(m.ChannelID, var(warship) => " " => master.ToUpper() => " The World!")
		} else {
			Channel.Send(m.ChannelID, "Nope!")
		}
	end!

	Bot.Command ("var(prefix)update")
	if (User.ID == ["146046383726657536"]) {
		System.Reload()
		Channel.Send(m.ChannelID, "<@m.UserID> You have restarted the cord script.")
	} else {
		Channel.Send(m.ChannelID, "You're not allowed to use this command.")
	}
	end!

	Bot.Command ("var(prefix)pm")
		User.Send(m.UserID, "<@m.UserID> You are the shit.")
	end!
```
