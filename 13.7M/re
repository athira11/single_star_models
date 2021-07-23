#!/bin/bash

function check_okay {
	if [ $? -ne 0 ]
	then
		exit 1
	fi
}
if [ $1 ]
then
    echo $1 > .restart
fi
check_okay
date "+DATE: %Y-%m-%d%nTIME: %H:%M:%S"
if [[ -e binary.exe ]];then
	./star.exe | tee output
else
	./star | tee output
fi
date "+DATE: %Y-%m-%d%nTIME: %H:%M:%S"
