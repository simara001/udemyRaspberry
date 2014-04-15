### PYTHON

#### Introduction

I must admit there are a lot of scripting languages that can be selected here. One of my first choices will always be Ruby, which in my opinion is very versatile, dynamic, scalable. However, for Raspberry and its community, most of the libraries are made primarily thinking in Python structures and trends, so let’s continue that tradition and continue the development using this beautiful language.

#### Installing

The first thing in this process is to check if you have already installed Python.

```bash
$ which python
$ python –-version
> /usr/bin/python
```

I should notice that it exists a big difference between Python **3++** and **2.7++**, and some things that work on Python 2.7++ won’t probably work on Python 3++ without some grooming.

In case you have not **Python** installed on your **Raspberry** you can find the instructions next.

```bash
$ sudo apt-get install python-setuptools
# After this, you can install this other tools that will be needed.
$ sudo apt-get install python-dev
$ sudo apt-get install python-pip
$ sudo apt-get install python-rpi.gpio
```
#### Using Python

There are two ways in which you can use Python. The first one is using the Terminal directly, the second one is to call Python #nameOfTheProgram from the terminal, or simply creating a cronjob for it.

In order to practice a couple of things in Python, we can make exercises to become familiar with the language.

```python
$ python
>>> 1 + 2
>>> 1 + 2 + 3
>>> print “hello world”
>>> d = 5 * 4
>>> print “the value of 20 is “ + str(d)
```

Now, let's create a project and call it from the terminal

```bash
$ cd /path/to/my/project
$ nano test1.py
print "hello world";
# press ctrl + o
# press ctrl + x
# type yes
$ python test1.py
> hello world
```

You should see the `"hello world"` string on your terminal. In the next chapter we are going to create a **Cron Job** that is going to call the file `test1.py` every certain time. Keep on reading.