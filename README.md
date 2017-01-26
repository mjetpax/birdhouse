# Birdhouse
A super light weight CSS flexbox responsive grid

* HTML5
* CSS3
* SASS
* Compass

Demo: http://mjetpax.github.io/birdhouse/


## The Grid and Column Classes

By default Birdhouse uses a 14 column grid. This can be easily adjusted in the _variables.scss file, but does require a recompile.

All column sizes have standard column class names, with the prefix columns. Then the breakpoint size of the column, followed by the number of columns wide.

* columns-xsmall-1
* columns-small-1
* columns-medium-1
* columns-large-1
* columns-xlarge-1
* columns-lazy-1

Lazy columns let the browser control various aspects of column management. Making it quick and easy to set up a responsive grid where design is less of a concern.

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
        <div class="columns-small-4">
        </div>
    </div>
</div>
```

### Class Aliases

In addition, all column classes have an aliase to allow for rapid creation of HTML and lessening the amount of typing needed to utilize the Birdhouse classes.

* cxs1
* csm1
* cmd1
* clg1
* cxl1
* clz1 

#### Example usage
```
<div class="birdhouse">
    <div class="row">
        <div class="cxsm4">
        </div>
        <div class="csm4">
        </div>
        <div class="csm4">
        </div>
        <div class="csm4">
        </div>
    </div>
</div>
```

### Combining Classes

You can combine classes to generate different layouts based on device size.

#### Example usage
```
<div class="birdhouse">
    <div class="row">
        <div class="cxsm2 clg12">
        </div>
        <div class="csm1 clg1">
        </div>
        <div class="csm1 clg1">
        </div>
        <div class="csm12 clg2">
        </div>
    </div>
</div>
```