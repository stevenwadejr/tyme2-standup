Tyme2 Daily Standup Report
===============================================================================
> Generating a standup report from my Tyme2 application using AppleScript

The applescript fetches yesterdays work from [Tyme2][tyme2] and returns it in
a format ready for my Slack standup channel. On Monday, it will fetch all tasks
over the weekend as well.

## Quick start

Add the `bin` folder to your path and then run `standup`.

```bash
export PATH="/Users/craig/Projects/tyme2-standup/bin:$PATH"
```

This will fetch the previous days work (with special weekend handling) and will
prompt you for todays tasks. Press enter to stop entering new tasks. It will
then prompt you about any blockers you're experiencing. Press enter to have
`none`. Once you've finished with the prompts, the morning standup report will
be in your clipboard and ready to share.

## Background

The script uses `log` to print the message to the terminal, and returns the
content as well so that it may be copied to the clipboard with osx `pbcopy`.
Use the supplied `bin/standup` to have to content of the app be automatically
copied to the clipboard.

## Development

* Open the `Script Editor` application in OSX and open the
  `daily-standup.applescript` file.
* Edit the file
* Choose `File > Export...` and then choose the `bin/daily-standup.scpt` file
  and be sure to change the *File Format* to `Script`
* -*OR*-
* Run the `compile` script found in this repo

[tyme2]: http://tyme-app.com/
