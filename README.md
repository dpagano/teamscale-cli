# Teamscale Command Line Interface

The Teamscale command line interface is used to enable integration into text editors such as VIM, Emacs or Sublime, by providing findings in a standard error format that can be interpreted like compile time errors. 

## Setup

1. Install ```jq```: https://stedolan.github.io/jq/download/
2. Clone this repository:
 ```bash
 $ git clone https://github.com/cqse/teamscale-cli.git
 ```
 
3. Copy the ```.teamscale-cli.config``` to your user directory:
 ```bash
 $ cp .teamscale-cli.config ~ 
 ```
 Now edit it and insert all the necessary data.

4. Put the ```teamscale-cli``` shell script anywhere that is on your local $PATH, so that it can easily be executed.

5. In your editor you can run this as a compile command, but be sure to provide the absolute path to the file in the current editor as the first argument: 

```bash
$ teamscale-cli /home/user/project/src/foo/AssumptionViolatedException.java
AssumptionViolatedException.java:30:0: error: Avoid leaving deprecated classes / methods / fields
AssumptionViolatedException.java:21:0: error: Avoid leaving deprecated classes / methods / fields
```

