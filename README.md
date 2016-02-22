# kolos.mixins


## Import

@import (reference) "mixins";


## Mixins list

+ [triangle](#triangle)
+ [grid](#grid)
+ [for](#for)
+ [placeholder](#placeholder)
+ [pseudo](#pseudo)
+ [bg](#bg)
+ [bg](#input)


## Usage

### triangle

.figure {
	.triangle(top, 22px);
}


### grid

//create simple grid:
.grid(simpleGrid; simpleGrid__col; 4; 30px);

//create adaptive grid:
@adaptiveState1000px: 1000px, 3, 20px;
@adaptiveState700px: 700px, 2, 10px;
@adaptiveState400px: 700px, 1;

.grid(adaptiveGrid; adaptiveGrid__col; 4; 30px; @adaptiveState1000px, @adaptiveState700px, @adaptiveState400px);


### for

@colors: #1abc9c, #2ecc71, #3498db, #9b59b6;

.for(@colors, {
	.color-@{i} {
		color: @value;
	}
});


### placeholder

.input {
  .placeholder(red);
}


### pseudo

.selector:after:extend(.pseudo) { }


### bg

.selector {
	.bg();
}





