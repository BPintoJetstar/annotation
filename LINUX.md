## Find a process and filter by name 
ps -A | grep firefox
## Kill a process by id 
kill PID
## Run the job in background
<command> `&`
After you done  excute command `jobs` to find your job

## Run Commands on romote machine
It's possible to excute commands on remote machine via ssh. You'll continuo on local terminal.

`ssh <host_name>  <command>`

## PATCH FILE 
Patch is a command that is used to apply patch files to the files like source code, configuration. Patch files holds the difference between original file and new file. In order to get the difference or patch we use diff tool.


## INTERESTING COMMANDS
- `watch --differences ps -ef | grep ansible | grep -v grep`
  - `watch --differences` Executes a command each 2 seconds the option highlights the output differences 
  - `ps -ef` show processes 
  - `grep ansible` filter by ansible keyword
  - `grep -v grep` filter by everything that has no grep keyword. Since `ps -ef`will show ever process including from grep command. 
-`ls -althr`

## Whatch
watch runs command repeatedly, displaying its output and errors (the
first screenfull). This allows you to watch the program output change
over time. By default, the program is run every 2 seconds. By
default, watch will run until interrupted.
