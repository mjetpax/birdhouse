# Birdhouse
A super light weight no conflict CSS flexbox responsive grid.

* Mobile first design
* HTML5
* CSS3
* SASS
* Compass

Demo: http://mjetpax.github.io/birdhouse/


## Quick Start

Quickly get Birdhouse up and running with ease.

1) Add the following CSS style link to the head of your HTML document.
```
<head>
    <link rel="stylesheet" href="https://cdn.rawgit.com/mjetpax/birdhouse/v0.7.4/css/birdhouse.min.css">
</head>
```

2) Add the following HTML to the body of your HTML document.
```
<body>
    <div class="birdhouse">
        <div class="row">
            <div class="columns-small-12">Hello World!</div>
        </div>
    </div>
</body>
```

3) You're all set! Now go have some fun!!


## The Grid and Column Classes

By default Birdhouse uses a 12 column grid system. This can be easily adjusted in the _variables.scss file, but does require a recompile. Birdhouse supports both fluid and fixed width layouts. Use .birdhouse for fixed width and .birdhouse .fluid for fluid layouts.

All column sizes have standard column class names, with the prefix columns. Then the breakpoint size of the column, followed by the number of columns wide.

* columns-xsmall-1
* columns-small-1
* columns-medium-1
* columns-large-1
* columns-xlarge-1
* columns-lazy-1

#### Example usage
```
<div class="birdhouse">
    <div class="row">
        <div class="columns-small-4">
        </div>
        <div class="columns-small-4">
        </div>
        <div class="columns-small-4">
        </div>
    </div>
</div>
```

### Class Aliases

In addition, all column classes have an alias to allow for rapid creation of HTML and lessening the amount of typing needed to utilize the Birdhouse classes. The .row class also has a .r alias that can be used.

* r
* cxs1
* csm1
* cmd1
* clg1
* cxl1
* clz1 

#### Example usage
```
<div class="birdhouse">
    <div class="r">
        <div class="cxs4">
        </div>
        <div class="csm4">
        </div>
        <div class="csm4">
        </div>
    </div>
</div>
```

### Lazy Columns

Lazy columns let the browser control various aspects of column management. Lazy columns wrap to the next line as the display area gets smaller. Lazy columnns automatically choose how many columns will be displayed per row, based on the size of the device screen. You can specify any number of colums per row and lazy columns will automatically decide how to break the columns up across x number of rows. This automated behavior makes it quick and easy to set up a responsive grid where strict column positioning is less of a concern.

#### Example usage
```
<div class="birdhouse">
    <div class="row">
        <div class="columns-lazy-4">
        </div>
        <div class="columns-lazy-4">
        </div>
        <div class="columns-lazy-4">
        </div>
        <div class="columns-lazy-4">
        </div>
        <div class="columns-lazy-4">
        </div>
        <div class="columns-lazy-4">
        </div>
        <div class="columns-lazy-4">
        </div>
        <div class="columns-lazy-4">
        </div>
    </div>
</div>
```

### Combining Classes

You can combine classes to generate different layouts based on device size.

#### Example usage
```
<div class="birdhouse">
    <div class="r">
        <div class="cxs2 clg8">
        </div>
        <div class="csm1 clg1">
        </div>
        <div class="csm1 clg1">
        </div>
        <div class="csm8 clg2">
        </div>
    </div>
</div>
```

### Grid Gutters

By default, there are no gutters defined for Birdcage. This provides maximum flexibility to designers and developers. There is no need to wrestle with altering preset values. Gutters are simple enough to define in your custom style.css file. Simply add a ruleset like the following CSS example.

#### Example CSS
```
[class*="columns-"], 
[class*="clz"], 
[class*="cxs"], 
[class*="csm"], 
[class*="cmd"],
[class*="clg"], 
[class*="cxl"] {
    padding-right: .5rem;
    padding-bottom: .5rem;
}
```

### Hide/Show Elements

Birdhouse allows you to hide and show elements at specific breakpoints using the following classes.

#### Hide at x breakpoint

* .hide-xsmall, .hd-xs
* .hide-small, .hd-sm
* .hide-medium, .hd-md
* .hide-large, .hd-lg
* .hide-xlarge, .hd-xl

#### Show at x breakpoint

* .show-xsmall, .sh-xs
* .show-small, .sh-sm
* .show-medium, .sh-md
* .show-large, .sh-lg
* .show-xlarge, .sh-xl

##### Example usage

```
<div class="birdhouse">
    <div class="hide-medium">
        <p>This is only shown to mobile devices.</p>
    </div>
</div>
```
Or
```
<div class="birdhouse">
    <div class="hide-medium">
        <div class="row">
            <div class="column-xsmall-12">
                <p>This is only shown to mobile devices.</p>
            </div>
        </div>
    </div>
    <div class="show-medium">
        <div class="row">
            <div class="column-xsmall-12">
                <p>This is never shown to mobile devices.</p>
            </div>
        </div>
    </div>
</div>
```