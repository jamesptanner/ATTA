#A Twitter Text Adventure.
If there is one thing that twitter excels at, it is giving value to the written word. A trait shared with text adventure games long ago. So why not combine them...

This project attempts to do just that allowing a Text adventure game to be run via a twitter user.

#Features
Nothing is yet implemented :(

#Plans 
Run from a twitter User.
Save Game states between application sessions.
Allow user generated stories via JSON objects that provide the game data.

##Far future.
multiple game stories at one time.

#Story Format. (Probably will change)

The adventures will be built from JSON objects provided.
Something like:


```
{
	'location' : [{
		'locid' : 'warehouse',
		'desc' : 'an abandoned warehouse deep behind enemy lines',
		'items' : ['spoon','boxes'],
		'connections' : 
		{
			'north': 'forest',
			'south': 'emptyRoad'
		},
		'myVariables' : {
			'enemies' : 12,
			'anythingyouwant' : 'pie'		
		}	
	},
	{
		'locid' : 'emptyRoad',
		'desc' : ' a long forgotten road stretching far into the distance',
		'connections' :
		{
			'north' : 'warehouse'
		}
		...
	}],
	'items' :{[
		'itemid' : 'spoon',
		'desc' : 'It looks like a spoon that has seen alot of tea in its time.',
		'myVariables' : {
			'shiny' : true,
			'weight' : 1		
		}	]
	},
	'events' :{
		//I am going to have to think about this one.
	}
	
}
```