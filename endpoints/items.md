# Get items
**GET** /items

Returns a list of all items in the game (talents, cards, in-game store items, etc)

Example response:
```js
[{
	"description": "Your weapon shots deal {scale=50|50}% increased Damage to Deployables.",
	"for": "Weapon", // removed from brackets at start of description
	"name": "Bulldozer",
	"icon": "https://web2.hirez.com/paladins/champion-items/bulldozer.jpg",
	"type": "item",
	"price": 200,
	"id": 13079
}, {
	"description": "When you take lethal damage Ghost Walk activates and heals you for 15% of your maximum Health.",
	"for": "Armor", // removed from brackets at start of description
	"name": "Wraith",
	"id": 16425,
	"type": "talent",
	"champion": "Grohk",
	"icon": "https://web2.hirez.com/paladins/champion-cards/wraith.jpg"
}, {
	"description": "Rend Soul heals you for {scale=8|8}% more.",
	"for": "Rend Soul", // remove from brackets at start of description
	"name": "Essence Rip",
	"id": 16845,
	"icon": "https://web2.hirez.com/paladins/champion-cards/essence-rip.jpg",
	"champion": "Seris",
	"type": "card"
}]
```

# Get item
**GET** /items/{{item id}}

Example response:
```js
{
	"description": "Your weapon shots deal {scale=50|50}% increased Damage to Deployables.",
	"for": "Weapon", // removed from brackets at start of description
	"name": "Bulldozer",
	"icon": "https://web2.hirez.com/paladins/champion-items/bulldozer.jpg",
	"type": "item",
	"price": 200,
	"id": 13079
}
```