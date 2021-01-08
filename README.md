jquery-multiselect2side
========================

bring [http://www.senamion.com/blog/jmultiselect2side.html](https://web.archive.org/web/*/http://www.senamion.com/blog/jmultiselect2side.html) to github


# multiselect2side plugin: documentation and demo page

## Demo Search - Full demo select multiple double side with search option true (20 elements; can be expanded to 1,000+)

Select multiple="multiple" modified by multiselect2side
```
<select name="searchable" id="searchable" multiple="multiple" size="6" style="display: none;">
	<option value="1">Option strawberry 1 - India</option>
	<option value="2">Option apricot 2 - Italy</option>
	<option value="3">Option cherry 3 - USA</option>
	<option value="4">Option pineapple 4 - Holland</option>
	<option value="5">Option pineapple 5 - Mexico</option>
	<option value="6">Option pineapple 6 - Holland</option>
	<option value="7">Option pineapple 7 - USA</option>
	<option value="8">Option apricot 8 - India</option>
	<option value="9">Option pear 9 - Japan</option>
	<option value="10">Option melon 10 - Canada</option>
	<option value="11">Option melon 11 - Canada</option>
	<option value="12">Option melon 12 - China</option>
	<option value="13">Option apple 13 - Japan</option>
	<option value="14">Option orange 14 - Italy</option>
	<option value="15">Option cherry 15 - Canada</option>
	<option value="16">Option pear 16 - Germany</option>
	<option value="17">Option orange 17 - Italy</option>
	<option value="18">Option apricot 18 - Italy</option>
	<option value="19">Option orange 19 - Mexico</option>
	<option value="20">Option pineapple 20 - Germany</option>
</select>
```

This is the javascript code to launch multiselect2side to #searchable select:


```
$(function(){
    $('#searchable').multiselect2side({'search': 'Search: '});
});
```

## Demo 1 - Full demo select multiple double side

Select multiple="multiple" modified by multiselect2side
```
<select name="firstSelect" id="first" multiple="multiple" size="6" style="display: none;">
	<optgroup label="Group1">
		<option value="1">First Option</option>
		<option value="2">Option 2th</option>
		<option value="3" selected="">Option selected 3</option>
	</optgroup>
	<optgroup label="Group 10-19">
		<option value="14">Option 14</option>
		<option value="15">Option 15</option>
		<option value="16">Option 16</option>
		<option value="17" selected="">Option selected 17</option>
		<option value="18">Option 18</option>
	</optgroup>
	<optgroup label="Group 20-29">
		<option value="24">Option 24</option>
		<option value="25">Option 25</option>
		<option value="26">Option 26</option>
		<option value="27" selected="">Option selected 27</option>
		<option value="28">Option 28</option>
	</optgroup>
	<optgroup label="Group 30-39">
		<option value="34">Option 34</option>
		<option value="35">Option 35</option>
		<option value="36">Option 36</option>
		<option value="37">Option 37</option>
		<option value="38">Option 38</option>
	</optgroup>
	<optgroup label="Group 40-49">
		<option value="41">Option 41</option>
		<option value="42">Option 42</option>
		<option value="43">Option 43</option>
		<option value="44">Option 44</option>
		<option value="45">Option 45</option>
		<option value="46">Option 46</option>
		<option value="47">Option 47</option>
		<option value="48">Option 48</option>
	</optgroup>
</select>
```

This is the javascript code to launch multiselect2side to #first select:


```
$(function(){
    $('#first').multiselect2side({
    	optGroupSearch: "Group: ",
    	search: "<img src='img/search.gif' />"
    });
});
```


## Demo 2 - select multiple double side - moveOptions: false, autoSort: true

Move buttons are disabled but is enable autoSort. Header label not present.
```
<select name="secondSelect" id="second" multiple="multiple" size="8" style="display: none;">
	<option value="1">Option a 1</option>
	<option value="3">Option c 3</option>
	<option value="5">Option e 5</option>
	<option value="6">Option f 6</option>
	<option value="7">Option g 7</option>
	<option value="8">Option h 8</option>
	<option value="9">Option i 9</option>
	<option value="2">Option b 2(sel)</option>
	<option value="4">Option d 4 (sel)</option>
	<option value="10">Option l 10 (sel)</option>
</select>
```

This is the javascript code to launch multiselect2side to #second select:


```
$(function(){
    $('#second').multiselect2side({
    	selectedPosition: 'right',
    	moveOptions: false,
    	labelsx: '',
    	labeldx: '',
    	autoSort: true,
    	autoSortAvailable: true
    });
});
```


## Demo 3 - select multiple double side - selectedPosition: 'left'

Elements selected are in the left, label of move buttoms are modified.
```
<select name="thirdSelect" id="third" multiple="multiple" size="6" style="display: none;">
	<option value="1">1Option 1</option>
	<option value="2" selected>Option 2 (sel)</option>
	<option value="3">a Option 3</option>
	<option value="4" selected>This Option 4 (sel)</option>
	<option value="5">Optaion 5</option>
	<option value="6">Option 6</option>
	<option value="7">Odption 7</option>
	<option value="8">Optaion 8</option>
	<option value="9">Optdion 9</option>
	<option value="10" selected>Option 10 (sel)</option>
	<option value="test1" selected>test selected</option>
	<option value="test2">test not selected</option>
</select>
```

This is the javascript code to launch multiselect2side to #third select:


```
$(function(){
    $('#third').multiselect2side({
    	selectedPosition: 'left',
    	moveOptions: true,
    	labelTop: '+ +',
    	labelBottom: '- -',
    	labelUp: '+',
    	labelDown: '-',
    	labelsx: '* Selected *',
    	labeldx: '* Available *',
    	search: "Find: "
    });
    $('#third')
    	.multiselect2side('addOption', {name: 'test selected', value: 'test1', selected: true})
    	.multiselect2side('addOption', {name: 'test not selected', value: 'test2', selected: false});
});
```


## Demo 4 - Select multiple double side with limited number of selectionable options

Select multiple="multiple" with parameter maxSelected, selectionable options limited to 4
```
<select name="fourthSelect" id="fourth" multiple="multiple" size="6" style="display: none;">
	<option value="1">First Option</option>
	<option value="2">Option 2th</option>
	<option value="3" selected>Option selected 3</option>
	<option value="4">Option 4</option>
	<option value="5">Option 5</option>
	<option value="6">Option 6</option>
	<option value="7" selected>Option selected 7</option>
	<option value="8">Option 8</option>
	<option value="test1" selected>test selected</option>
	<option value="test2">test not selected</option>
</select>
```


This is the javascript code to launch multiselect2side to #fourth select:


```
$(function(){
$('#fourth').multiselect2side({maxSelected: 4});

$('#fourth')
	.multiselect2side('addOption', {name: 'test selected', value: 'test1', selected: true})
	.multiselect2side('addOption', {name: 'test not selected', value: 'test2', selected: false});
});
```


## Documentation

To use this jquery plugin:

- include the js in the head section of the page:

```
<head>
<link rel="stylesheet" href="css/jquery.multiselect2side.css" media="screen">
<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
<script src="js/jquery.multiselect2side.js"></script>
</head>
```
- in the read function launch the multiselect2side (select multiple double side) relative at your element:
		

```
<script>
$(function(){
$("select").multiselect2side();
});
</script>
```

For comments, view the following original blog URL in archive.org:
[http://www.senamion.com/blog/2010/02/20/jquery-select-multiple-double-side/](https://web.archive.org/web/2020*/http://www.senamion.com/blog/2010/02/20/jquery-select-multiple-double-side/)
### Options:

- **optGroupSearch:** use optgroup label to select elements - default false
- **minSize:** default minSize of selects - default 6
- **selectedPosition:** position of selected elements - default 'right'
- **moveOptions:** show move options - default true
- **labelTop:** label of top buttom - default 'Top'
- **labelBottom:** label of bottom buttom - default 'Bottom'
- **labelUp:** label of up buttom - default 'Up'
- **labelDown:** label of down buttom - default 'Down'
- **labelSort:** label of sort buttom - default 'Sort'
- **maxSelected:** number of max selectable options
- **labelsx:** Left label - default '\* Selected \*'
- **labeldx:** Right label - default '\* Available \*'
- **autoSort:** Automatic sort of selected options - default false
- **autoSortAvailable:** Automatic sort of available options - default false
- **search:** string for add search funcionality - default false = no search
- **caseSensitive:** type of search - default false
- **delay:** the delay in milliseconds the search option waits after a keystroke to activate itself - default 200


### Methods:

- **destroy:** destroy multiselect2side
- **addOption:** add option to select(s). See example #fourth and #third selects above. Options:
    - **name:** name of new value
    - **value:** value of new value
    - **selected:** if true option is inserted in "selected" list, else in "available"


## Release
- **1.2** - Jan 07 2021 - Modernized for jQuery 3.x
- **1.1** - May 04 2011 - correct some little bugs
- **1.0** - Apr 04 2011 - new optGroupSearch and minSize options, new methods destroy and addOption
- **0.16** - Mar 15 2011 - new autoSortAvailable option
- **0.15** - Mar 14 2011 - new search options
- **0.14** - Feb 2 2011 - correct FF autoSort bug
- **0.13** - Jan 26 2011 - new autoSort parameter
- **0.12** - Nov 19 2010 - correct opera bug + new demo
- **0.11** - Aug 26 2010 - correct ie6 bug
- **0.10** - Jul 20 2010 - correct ie8 bug (padding-top)
- **0.9** - Jul 16 2010 - new labels button (left and right label)
- **0.8** - May 17 2010 - new sort button (if moveOptions is true)
- **0.7** - May 16 2010 - correct order options bug
- **0.6** - Avr 16 2010 - correct bug with optgroup
- **0.5** - Avr 15 2010 - Now move and updown options are vertically centered
- **0.4** - Avr 12 2010 - New option maxSelected
- **0.3** - Avr  1 2010 - New CSS
- **0.2** - Mar 25 2010 - New parameters moveOptions (default true)
- **0.1** - Mar 22 2010 - New parameters selectedPosition (default 'right')
- **0.0** - Feb 19 2010 - First release of multiselect2side (select multiple double side)


## License

Dual licensed under the MIT and GPL licenses.
