# Get Match
**GET** /matches/{{match}}

Returns information about a match, by ID

```js
{
	"date": "3/8/2018 3:57:03 AM",
	"map": {
		"name": "Brightmarsh",
		"icon": "..."
	},
	"region": "North America",
	"id": "220125007",
	"length": 832, // match length in seconds
	"queue": "Competitive",
	"scores": {
		"teamOne": 4,
		"teamTwo": 0
	}
	"players": [{
		"accountLevel": 120
		"team": 1,
		"items": [{
			"name": "Cauterize",
			"level": 3,
			"id": 1234,
			"icon": "..."
		}],
		"damage": {
			"dealtTotal": 123456,
			"dealtByWeapon": 111111,
			"taken": 54321,
			"shielded": 12391
		},
		"credits": 3846,
		"assists": 15,
		"deaths": 8,
		"kills": 13,
		"streak": 7,
		"multikills": {
			"top": 3,
			"singles": 4
			"doubles": 2,
			"triples": 1,
			"quadra": 1,
			"penta": 0
		},
		"rank": {
			"name": "Gold III",
			"tp": 15,
			"gained": 13,
			"wins": 40,
			"losses": 38,
			"icon": "...",
			"border": "..."
		},
		"championLevel": 83,
		"champion": "Ruckus",
		"objectiveTime": 147,
		"talent": [{
			"name": "Rocket Barrage",
			/* etc, same as ites from get items endpoint */
		}]
		"loadoutItems": [{
			"name": "Fuel Reserve",
			"level": 5,
			/* etc, same as ites from get items endpoint */
		}]
	}, { /* continued for all other players */ }]
}
```

# Get Matches Batch
**GET** /matches/{{ids}}

Returns data for multiple matches at once. Id's should be seperated by commas.

# Get Matches by Queue
**GET** /matches/{{queue}}/{{date}}/{{hour}}

Returns match ID's from a specific queue on a speficic date at a certain time

Example response:
```js
[1234, 12412, 4912312, 1239213, 412931, 341231, 23123, 231241, 23124, 21651, 29154]
```