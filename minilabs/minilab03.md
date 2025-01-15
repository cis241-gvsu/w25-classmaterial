# Minilab 3

### Command Line Utility Practice

The purpose of this minilab is to help you practice some of
the linux utilities we've covered so far.  You'll do this
by doing some simple processing on your command history.

* Run the `history` command to access your commnad history
  and redirect the output to a file (name of your choice).
* Use a command to select only the 200 most recent commands
  and put them in a file. The most recent commands are
  located at the bottom of the `history` output.
* Use `wc` to count how many commands are in the file from
  the previous step.
* Use `tr -s ' '` to squish multiple spaces into one --
  you'll need to use both input and output redirection
* Use `cut` to extract just the commands (literally just the
  main command -- not the numbers, options, nor arguments)
  and redirect the output to a file
* Use `sort -u` on the resulting file to get the unique lines
  and redirect the output to a file
* Use `wc` to count the unique commands.
