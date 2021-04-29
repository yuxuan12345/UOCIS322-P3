# UOCIS322 - Project 3 #
A vocabulary anagrams game for primary school English Language Learners (ELL).

## Overview

A simple anagram game designed for English-language learning students in elementary and middle school. Students are presented with a list of vocabulary words (taken from a text file) and an anagram. The anagram is a jumble of some number of vocabulary words, randomly chosen. Students attempt to type words that can be created from the jumble. When a matching word is typed, it is added to a list of solved words.

The vocabulary word list is fixed for one invocation of the server, so multiple students connected to the same server will see the same vocabulary list but may have different anagrams.

## Getting started

`flask_vocab.py` is an example of the anagram game, with the template `vocab.html`. This example uses a conventional interaction through a form, interacting only when the user submits the form.

### Exploring the container
You can jump directly into your running container using the following command:

```shell
docker exec -it YOUR_CONTAINER_ID /bin/bash
```

This way you can run the tests, run another script, and really experiment with what goes on inside your container.

## Tasks

* Familiarize yourself with `flask_vocab.py` and `flask_minijax.py` by running them separately. You need to understand them to do this project.

* Your task is to replace the form interaction (in `flask_vocab.py`) with AJAX interaction on each keystroke using `flask_minijax.py`.

* Revise `Dockerfile`.

* As always, submit your `credentials.ini` through Canvas. It should contain your name and git repo URL.

* As always, revise the README file.

## FAQ
### What is `src`?
This is a sub-package which contains modules related to the game. You should not make any changes there, but feel free to review them to get a better understanding.

### What is `data`?
This directory contains a few word lists in the form of text files. You should not make any changes to the ones that already exist. However, you can add your own (but don't have to). You can change the word list file in your `credentials.ini`.

### What is minijax?

`flask_minijax.py`, along with its template `templates/minijax.html`, is a tiny example of using JQuery with flask for an AJAX application. They should not be included in the version of the project you turn in. You can use this example to figure out how to implement an AJAX version of the game. Delete the two (along with `static/img`) when you're done with the project.

### How do I run the tests?
The `tests` directory contains a test suite for the `src` package. There's a `run_tests.sh`, which you can run in your container while it's running. However, it is not required, since you will not be changing anything in `src`.

## Grading Rubric

* If your code works as expected: 100 points. This includes:
	* AJAX in the frontend (`vocab.html`)
	* Logic in the backend (`flask_vocab.py`)
	* Frontend to backend interaction (with correct requests and responses) between `vocab.html` and `flask_vocab.py`.

* If the JQuery logic is not working, 30 points will be docked off.

* If the html file (replacing the original form interaction, i.e., replacing the button with JQuery code) is wrong or is missing in the appropriate location, 30 points will be docked off.

* If none of the functionalities work, 40 points will be given assuming
    * the `credentials.ini` is submitted with the correct URL of your repo,
    * the `Dockerfile` builds without any errors, and

* If the `Dockerfile` doesn't build or is missing, 20 points will be docked off.

* If `credentials.ini` is not submitted or the repo is not found, 0 will be assigned.

* EXTRA CREDIT:
	* Remove (strikethrough) the words that are found from the word list at the top.
	
	* No HTML or response text in your JavaScript and Flask app.
	 

## Credits

Michal Young, Ram Durairajan, Steven Walton, Joe Istas.
