# kolos.mixins


## Install

npm install kolos.mixins --save;


## Mixins list

+ [triangle](#triangle)
+ [grid](#grid)
+ [for](#for)
+ [placeholder](#placeholder)
+ [pseudo](#pseudo)
+ [bg](#bg)
+ [square](#square)
+ [ellipsis](#ellipsis)
+ [burger](#burger)


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
.grid(~'.gridSelector'; ~'.itemSelector'; 4; 30px);

//create adaptive grid:
@adaptiveState1000px: 1000px, 3, 20px;
@adaptiveState700px: 700px, 2, 10px;
@adaptiveState400px: 400px, 1;

.grid(~'.gridSelector'; ~'.itemSelector'; 4; 30px; @adaptiveState1000px, @adaptiveState700px, @adaptiveState400px);
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
.selector:extend(.square all) {}
```


### ellipsis

```less
.selector:extend(.ellipsis) {}
```


### burger

```less
.selector {
	.m-burger(21px, 13px, 1px, #000);
}
```






