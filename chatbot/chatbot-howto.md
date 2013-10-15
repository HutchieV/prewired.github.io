# Getting Started with Chatbots#

## Getting the files##

Check that you have Python 2.7 installed. Type

	% python

at the terminal. If you get something like this

	Python 2.7.5 (default, Aug  1 2013, 01:01:17)
	[GCC 4.2.1 Compatible Apple Clang 4.1 ((tags/Apple/clang-421.11.66))] on darwin
	Type "help", "copyright", "credits" or "license" for more information.
	>>>

then you are good to go. Otherwise, install Python 2.7
[using these instructions](http://www.python.org/getit/releases/2.7.5/).

In order to skip the (minor) hassle of installing
[NLTK](http://nltk.org/install.html), we've prepared a zip archive of
just the files you need for running the chatbots. Make a directory (say, `prewired`) where you want to do your work,  [download this
zip file](http://data.inf.ed.ac.uk/catalog/storage/f/2013-10-15T11%3A50%3A03.026Z/chat.zip) into it, and unzip it.

```bash
% mkdir prewired
[download chat.zip]
% cd prewired
% unzip chat.zip
```

## Running a chatbot ##

First, make sure you are in the directory (e.g., `prewired`) where you downloaded and unzipped `chat.zip`.

The quickest way to run the chatbots is to call `chat` as a module (using the `-m` option):

```bash
% python -m chat

Which chatbot would you like to talk to?
  1: Eliza (psycho-babble)
  2: Iesha (teen anime junky)
  3: Rude (abusive bot)
  4: Suntsu (Chinese sayings)
  5: Zen (gems of wisdom)
```

Pick a number and play around with some of the bots. Once you've got a
feeling for what they can and cannot do, have a look at the code of
one of them, such as `chat/eliza.py`. See if you can figure out just from the
`pairs` data what is going on. 

Make a copy of one of the bots, and call it  `mybot.py`:

```bash
% cp chat/rude.py chat/mybot.py
```

Now you can edit and modify `mybot.py` using your favourite editor. A
simple way to test your modified version is via the file `test.py`
which should be sitting in the `prewired` directory where you
downloaded `chat.zip`. This just calls the `demo()` function:

```python

from chat.mybot import demo

if __name__ == "__main__":
    demo()
```

If you used a different name than `mybot.py`, modify this file accordingly.




