# UOCIS322 - Project 3 #
A vocabulary anagrams game for primary school English Language Learners (ELL).

## Completed by
Lindsay Marean, linzanna@cs.uoregon.edu
Spring 2021

## Overview

A simple anagram game designed for English-language learning students in elementary and middle school. Students are presented with a list of vocabulary words (taken from a text file) and an anagram. The anagram is a jumble of some number of vocabulary words, randomly chosen. Students attempt to type words that can be created from the jumble. When a matching word is typed, it is added to a list of solved words.

The vocabulary word list is fixed for one invocation of the server, so multiple students connected to the same server will see the same vocabulary list but may have different anagrams.

## Operation instructions
### Normal operation
Download (clone) this repository.
You may wish to create your own credentials.ini file, using credentials-skel.ini as a model.
Navigate to the vocab directory. 
### To use Docker
Make sure Docker is installed on your machine (https://docs.docker.com/get-docker/)
Build a Docker image with docker build -t [name of image] . (the . is part of the command).
Run the image with docker run -d -p [your choice of port]:5000 [name of image]
Open a browser and navigate to the address of your machine and the port you've selected.
To end the program, find the process with Docker ps. Then stop the process with docker stop [process number or name]. Then if desired clear the process with docker rm [process number or name].
### To run locally without Docker
Run the program with python3 flask_vocab.py.
Open a browser on your local machine and look in localhost:5000.
To end the program, you may need to use CTRL-c.

### How do I run the tests?
The `tests` directory contains a test suite for the `src` package. There's a `run_tests.sh`, which you can run in your container while it's running. 

## Bugs / Enhancements
Extra credit was offered for printing words with strikethrough once they've been found. This was not implemented.
Extra credit was also offered for not having the text of messages endcoded in either the Python script or the JavaScript. I didn't understand what this meant and didn't implement it. Maybe I was supposed to encode all messages in vocab.html, but not really sure.

I did use a bit of CSS styling to hide the "You found" message at the bottom on initial rendering, only revealing it once a word has been found. 


## Credits

Michal Young, Ram Durairajan, Steven Walton, and Joe Istas designed this project.
Ali Hassani revised it and guided students through its implementation this term.
