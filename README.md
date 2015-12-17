# gb-run
Plugin to http://getgb.io to allow easy running of tools used to working with a $GOPATH

## Installation

    go get github.com/dlclark/gb-run/...

## Pre-reqs

	go get github.com/constabulary/gb/...

## Usage
When you run the gb run command the environment is setup with the $GOPATH based on the current gb project and the first argument is executed.  A common use would be to launch Sublime Text in a way that GoSublime ([see my fork for better goto def](http://github.com/dlclark/GoSublime/) will work with gb projects

	cd /my/project/source/folder/
	gb run subl .

Sublime text will open your gb project directory in the side bar and GoSublime will use the $GOPATH environment variable set by gb run for all its features (goto definition, find usages, on-save hooks, etc).  Make sure you don't set a GOPATH in the Sublime settings file (GoSublime.sublime-settings under "env" : { "GOPATH" : "something" }) otherwise it won't pick it up from the environment.  

## Read more
gb has its own site, [getgb.io](http://getgb.io/), head over there for more information.
