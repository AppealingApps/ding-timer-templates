# ding-timer-templates
JSON data for Ding Timer Templates

## JSON Format

### Template Information
The JSON data for a template includes the following data:

* `name: String`- **Required** - must be unique
* `author: String` - **Optional**
* `category: String` - **Required** - should be one of the existing categories noted below.
* `steps: Array of TimerSteps` - **Required** - must be in the correct order

A step contains the following information:

* `name: String` - **Required** - does not have to be unique
* `length: String - form of HH:mm:ss` - **Required** - See RFC 3339
* `pauseOnFinish: Bool`- **Required** - the last step's value will be ignored

#### Example
```json
{
	"name": {
		"en-us": "Example Timer"
	}
	"author": "Joel Fischer",
	"category": {
		"en-us": "Food"
	}
	"steps": [{
			"name": {
				"en-us": "Step 1"
			}
			"length": "5:00",
			"pauseOnFinish": false
		},
		{
			"name": {
				"en-us": "Step 2"
			}
			"length": "1:20",
			"pauseOnFinish": false
		}
	]
}
```

### Categories
The list of categories is currently as follows:
* "Food"
* "Household"
* "Utilities"
