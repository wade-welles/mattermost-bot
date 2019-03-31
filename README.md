# Simple Matttermost Bot
A simple Mattermost bot with plans to eventually open it up to support any Chat software that is implemented as a library used by a CLI tool. 

In the command line tools developers can for now register their own regex event driven functionality.

```go
		app.Bot = app.Bot.RegisterHook(bot.RegexFunction{
			Name:  "HelloResponder",
			Regex: `(?:^|\W)hello(?:$|\W)`,
			Function: func(post *model.Post) {
				app.Bot.SendMessageToChannel("hello dawg, you send the following post :"+post.Message, "")
			},
		})
```

Currently an example plugin for rolling dice is implemented as an example and to
provide a simple structure for further custom functionality to be built from. 
