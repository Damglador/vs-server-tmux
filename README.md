# Vintage Server launcher/manager in tmux
Created this simple script because the official one didn't work and entering commands in the terminal of the running VS server binary is not pleasant.
# Basic outline of the functionality
Runs playit, server command line and the server itself

**playit** can be disabled by changing `ENABLE_PLAYIT="1"` value to 0. It also runs in a separate window, basically a tab in tmux, so you can't see it while you're commanding the server

**server command line accepts** commands you input, puts `/` at the beginning and sends them to the server. If you input `exit` it stops the server, `killserver` kills the tmux session. It also has it's own history separate from bash.

**VS Server** just runs on the top panel, if it stops, the tmux session stops (so `exit` stops the session).

# Instructions
- Get the all scripts in one directory (`vss-konsole vss-tmux vsscmd` konsole is optional)
- Make sure tmux is installed
- Make sure `SERVER_BIN` in the script points to your VS server binary
- Make the script executable (using `chmod +x vss-tmux vsscmd vss-konsole`, or your file manager)
- Run the script in a terminal or doublecluick vss-konsole