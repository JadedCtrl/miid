# miid

miid's a simple IRC bot (hackily) written in shell.
It turns an irc room into a MUD/MUSH/IF-esque room, or at least it tries.

## Running
Use [ii](https://tools.suckless.org/ii/) to connect to your IRC server and
channel of choice― make sure to set up the nick and everything.

Then, you can just run miid every time the channel's output is updated:

	$ miid irc/$IRC_NETWORK/$IRC_CHANNEL $BOT_NICK

It helps to have inotifywait installed, so this can be done automatically:

	$ while inotifywait -e close_write irc/$IRC_NETWORK/$IRC_CHANNEL/out; \
	  do \
	 	 sh miid irc/$IRC_NETWORK/$IRC_CHANNEL/ $BOT_NICK; \
	  done

## Commands
Check the ./helpdoc.

## License
CC-0
