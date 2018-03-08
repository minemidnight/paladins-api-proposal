# Get Player Friends
**GET** /players/{{username}}/friends

Returns an array of usernames representing all the friends of a particular user

Example response:
```js
["minemidnight", "Kusqt"]
```

# Get Match History
**GET** /players/{{username}}/matches

Returns recent matches of a player (this won't conflict with match id's because usernames cannot start with numbers)

```js
[
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
	}
]
```
