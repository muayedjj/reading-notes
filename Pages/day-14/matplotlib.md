# Data Visualization: Matplotlib 

### Introduction
`matplotlib` is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats. We are going to explore `matplotlib` in interactive mode covering most common cases. [1]

### IPython
`IPython` is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, improved debugging and much more. It allows interactive `matplotlib` sessions that have Matlab/Mathematica-like functionality. [1]

### pyplot
`pyplot` provides a convenient interface to the `matplotlib` object-oriented plotting library. It is modeled closely after Matlab(TM). Therefore, the majority of plotting commands in `pyplot` have Matlab(TM) analogs with similar arguments. Important commands are explained with interactive examples. [1]

### Simple plot
In this section, we want to draw the cosine and sine functions on the same plot. Starting from the default settings, we'll enrich the figure step by step to make it nicer. all using the `plot()` command. [1]

## Figures, Subplots, Axes and Ticks [2]

### Figures
A figure is the windows in the GUI that has "Figure #" as title. Figures are numbered starting from 1 as opposed to the normal Python way starting from 0. This is clearly MATLAB-style. There are several parameters that determine what the figure looks like.
The defaults can be specified in the resource file and will be used most of the time. Only the number of the figure is frequently changed.

### Subplots
With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. Note that the gridspec command is a more powerful alternative.

### Axes
Axes are very similar to subplots but allow placement of plots at any location in the figure. So if we want to put a smaller plot inside a bigger one we do so with axes.

### Ticks
Well formatted ticks are an important part of publishing-ready figures. Matplotlib provides a totally configurable system for ticks. There are tick locators to specify where ticks should appear and tick formatters to give ticks the appearance you want. Major and minor ticks can be located and formatted independently from each other. By default minor ticks are not shown, i.e. there is only an empty list for them because it is as NullLocator. 

### Tick Locators
There are several locators for different kind of requirements:

- NullLocator	
No ticks.

- IndexLocator	
Place a tick on every multiple of some base number of points plotted.

- FixedLocator	
Tick locations are fixed.

- LinearLocator	
Determine the tick locations.

- MultipleLocator	
Set a tick on every integer that is multiple of some base.

- AutoLocator	
Select no more than n intervals at nice locations.

- LogLocator
Determine the tick locations for log axes.

## Animation [2]

For quite a long time, animation in matplotlib was not an easy task and was done mainly through clever hacks. However, things have started to change since version 1.1 and the introduction of tools for creating animation very intuitively, with the possibility to save them in all kind of formats (but don't expect to be able to run very complex animations at 60 fps though).

### Drip drop
A very simple rain effect can be obtained by having small growing rings randomly positioned over a figure. Of course, they won't grow forever since the wave is supposed to damp with time. To simulate that, we can use a more and more transparent color as the ring is growing, up to the point where it is no more visible. At this point, we remove the ring and create a new one.




 _For more on the subject of **Matplotlib**, see this [**Amazing Repository**](https://github.com/rougier/matplotlib-tutorial/blob/master/README.rst/)  on **GithHub**

#

### Things I want to know more about:
1. Matplotlib.
2. Seaborn.
3. Bokeh.
4. NumPy data types.

#

[1]: https://github.com/rougier/matplotlib-tutorial/blob/master/README.rst
[2]: https://github.com/rougier/matplotlib-tutorial/blob/master/README.rst#figures-subplots-axes-and-ticks
[3]: https://github.com/rougier/matplotlib-tutorial/blob/master/README.rst#animation