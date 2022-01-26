# Reading 14 - Data Visualization

## MatPlotlib

**matplotlib** - ale to visual data from Python

**IPython** - interactive shell that contains:
1.named inputs and outputs
2.access to shell commands
3.improved debugging
4.interactive matplotlib sessions

**pyplot** - interface to the matplotlib plotting library

### Simple Plot

  import numpy as np

  X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
  C, S = np.cos(X), np.sin(X)

X is now a NumPy array with 256 values ranging from -π to +π (included). C is the cosine (256 values) and S is the sine (256 values).

### Changing colors and widths

  plt.figure(figsize=(10,6), dpi=80)
  plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
  plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")

Cosine is blue and slightly thicker line for both of them. Also makes the figure size more horizontal.

### Setting limits

  plt.xlim(X.min()*1.1, X.max()*1.1)
  plt.ylim(C.min()*1.1, C.max()*1.1)

Makes space in order to clearly see all the data points.

### Setting ticks

  plt.xticks( [-np.pi, -np.pi/2, 0, np.pi/2, np.pi])
  plt.yticks([-1, 0, +1])

### Setting Tick Labels

to make tickets more *explicit* (regex example below):

  plt.xticks([-np.pi, -np.pi/2, 0, np.pi/2, np.pi],
        [r'$-\pi$', r'$-\pi/2$', r'$0$', r'$+\pi/2$', r'$+\pi$'])

  plt.yticks([-1, 0, +1],
        [r'$-1$', r'$0$', r'$+1$'])

This provides a corresponding label in the second argument list.

### Moving Spines

  ax = plt.gca()
  ax.spines['right'].set_color('none')
  ax.spines['top'].set_color('none')
  ax.xaxis.set_ticks_position('bottom')
  ax.spines['bottom'].set_position(('data',0))
  ax.yaxis.set_ticks_position('left')
  ax.spines['left'].set_position(('data',0))

**spines** - connects the axis tick marks; also indicates the boundaries of the data area. This example changes them so that they are in the middle.

### Add Legend

  plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-", label="cosine")
  plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-", label="sine")

  plt.legend(loc='upper left', frameon=False)

Add keyword argument label to plot commands

### Annotate Points

  t = 2*np.pi/3
  plt.plot([t,t],[0,np.cos(t)], color ='blue', linewidth=1.5, linestyle="--")
  plt.scatter([t,],[np.cos(t),], 50, color ='blue')

  plt.annotate(r'$\sin(\frac{2\pi}{3})=\frac{\sqrt{3}}{2}$',
              xy=(t, np.sin(t)), xycoords='data',
              xytext=(+10, +30), textcoords='offset points', fontsize=16,
              arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))

  plt.plot([t,t],[0,np.sin(t)], color ='red', linewidth=1.5, linestyle="--")
  plt.scatter([t,],[np.sin(t),], 50, color ='red')

  plt.annotate(r'$\cos(\frac{2\pi}{3})=-\frac{1}{2}$',
              xy=(t, np.cos(t)), xycoords='data',
              xytext=(-90, -50), textcoords='offset points', fontsize=16,
              arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))

1. Code draws marker on the curve as well as a straight dotted line.
2. Annotate command displays some text with something.


### Figure, Subplots, Axes and Ticks

**Figure** - the whole window in user interface

[Figures](./images/figures.png)

**Subplots** - contained in figure. Positions plot in grid

**Axes** - allows free placement within figure

gca() - function of matplotlib that gets the current axes

gcf() - function of gca that gets the current figure

[<==BACK](README.md)
