# Get Champion Info
**GET** /champion/{{name}}

Returns information about a champion such as their ID, legendaries, abilities.

Example response:
```js
{
	"abilities": [{
		"description": "A six shot semi-automatic revolver that deals 580 damage per shot every .36s. Effective at Short Range.",
		"id": 12489,
		"name": "Revolver",
		"cooldown": 0, // no cooldown
		"icon": "https://web2.hirez.com/paladins/champion-abilities/revolver.jpg",
		"type": "primary" // altfire, ultimate, ability 1, ability 2? 
	}, { /* continued for other abilites */ }],
	"legendaries": [{ /* talents for this character stripped from get items */ }],
	"cards": [{	/* cards for this character stripped from get items */ }],
	"icon": "https://web2.hirez.com/paladins/champion-icons/androxus.jpg",
	"health": 2100,
	"lore": "Once a noble lawman of the Outer Tribunal circuit judges, Androxus and his former partner, Lex, were relentless in their pursuit of criminals and threats to the natural order. After a tragic confrontation with a deceitful goddess, though, he became afflicted with an otherworldly disease dooming him with an endless hunger for souls. Now he wanders the realm adrift to feed that hunger, stripped of his rank and duties with the Tribunal, and condemned to live with the curse for all time.",
	"name": "Androxous",
	"class": "flank", // damage, frontline, support
	"speed": 380,
	"title": "The Godslayer",
	"id": 2205,
	"onRotation": false,
	"isNew": false
}
```

# Get Champions Stats
**GET** /champion/{{name}}/{{player}}

Returns statistics a player has on a champion

Example response:
```js
{
	"name": "Jenos",
	"assists": 1600,
	"deaths": 800,
	"kills": 800,
	"losses": {
		"ranked": 50,
		"casual": 30,
		"tdm": 5,
		"onslaught": 3
	},
	"wins": {
		"ranked": 50,
		"casual": 30,
		"tdm": 5,
		"onslaught": 3
	},
	"level": 26,
	"playTime": 58124.32 // minutes
	"experience": {
		"total": 12345, // total xp gathered
		"nextLevel": 14021 // xp for next level
	}
}
```

# Get Champions
**GET** /champions/

Returns information on each champion rather than just one

Example response:
```js
[{ /* data from get champion info for every champion */ }]
```

# Get Champions Stats
**GET** /champions/{{player}}

Returns stats on each champion rather than just one for a player

Example response:
```js
[{ /* data from get champion stats for every champion */ }]
```