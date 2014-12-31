a4t (Aim For Today)
===

How many emails should I process today?

So you have come back from holidays, and 152 emails await in your inbox. Of
course a few of them are urgent but you definitely don't want to process all at
once when only 20 come per day on average. How many should you read today? This
script will tell you.

If you ask it every day it learns about your daily charge and instructs you to
read as many that

- you don't get overwhelmed (more than usually) on any particular day, not even
  after holidays;
- nevertheless your inbox keeps a bounded size.

The algorithm is simple: if the number of emails decreased by 5% since
yesterday then the script is happy, and keeps your daily load constant. If it
decreased less, or even increased, then it increases your daily load but only
by 10% at most. If the decrease is more than 5% than we are even happier and
the script decreases the daily load but at most by 8%.

First open a terminal and type in

```
a4t -i [task name]
```

where [task name] can be e.g. "myemails". This will create a ~/.a4t directory
and puts in it some log files about your task. To ask the script about today's
aim, type

```
a4t -a [task name]
```

and type in how many emails you have now. The script then tells you your goal
for today. Once that's achieved, type

```
a4t -c [task name]
```

and when asked, proudly enter where you have just ended up with your task.

If you have Gnuplot installed, then plot_a4t gives you a graphical feedback on
how the quantity of this task evolved in time.

I'm no programmer, so please don't blame me on the quality of the code. :-)
Licensed under GNU GPLv3.
