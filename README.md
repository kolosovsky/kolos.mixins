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
+ [square](#square)


## Usage

### triangle

```less
.figure {
	.triangle(top, 22px);
}
```


### grid

```less
//create simple grid:
.grid(simpleGrid; simpleGrid__col; 4; 30px);

//create adaptive grid:
@adaptiveState1000px: 1000px, 3, 20px;
@adaptiveState700px: 700px, 2, 10px;
@adaptiveState400px: 700px, 1;

.grid(adaptiveGrid; adaptiveGrid__col; 4; 30px; @adaptiveState1000px, @adaptiveState700px, @adaptiveState400px);
```



### for

```less
@colors: #1abc9c, #2ecc71, #3498db, #9b59b6;

.for(@colors, {
	.color-@{i} {
		color: @value;
	}
});
```


### placeholder

```less
.input {
  .placeholder(red);
}
```


### pseudo

```less
.selector:after:extend(.pseudo) { }
```


### bg

```less
.selector {
	.bg();
}
```


### square

```less
.selector:extend(.square) {}
```






