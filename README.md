# keep

> Keep inputs, selects, textareas data, even if web page is refreshed.

## Usage

### Method 1
Add ```keep``` attribute to the inputs like bellow

``` html
		<label for="name">
			Enter your name
			<input type="text" name="name" id="name" value="" keep>
		</label>
```

and initialize plugin via Javascript like this

``` js
	keep()
```

KeepJS will scan for inputs that have ```keep``` in their attributes and will watch data changes.


### Method 2
We can also do it only in JS ```keep([HTMLElement1_ID, HTMLElement2_ID, HTMLElement3_ID, ...HTMLElements_ID])```
Strings in array are IDs of the inputs.

``` js
	keep([
		'birthday',
		'full_name',
		'gender',
		'description',
		'job',
		'favorite_color'
	])
```

## Options
In this version (1.0.0) of plugin, only one option is available.

#### Lazy keeping
Add ```keep-lazy``` to the tag or in JS
``` js
	keep({
		targets: [ 'birthday', 'full_name', 'gender', 'description', 'job', 'favorite_color' ],
		opts: {
			lazy: Boolean
		}
	})
```

If lazy is falsy, data will be kept on keyup of the inputs.


### Multiple keeps
This option will be available soon.
You'll be able to keep more than one value for an tag and choose one when serving data.

Add ```keep-multiple``` to the tag or in JS
``` js
	keep({
		targets: [ 'birthday', 'full_name', 'gender', 'description', 'job', 'favorite_color' ],
		opts: {
			lazy: Boolean,
			multiple: Boolean
		}
	})
```

NOT AVAILABLE IN V-1.0.0

## Authors

> Jean-jacques AKAKPO (akakpo.jeanjacques@gmail.com)

> An ovaar products
