# Get Usage Statistics
**GET** /usage

Returns information about how API limits and your current statistcs for the day.

Example response:
```js
{
	"limits": {
		"requestsPerDay": 7500
	},
	"stats": {
		"requestsToday": 250
	}
}
```