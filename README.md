# ding-timer-templates
JSON data for Ding Timer Templates

## JSON Format

### Template Information
The JSON data for a template includes the following data:

* `name: String`- **Required**
* `author: String` - **Optional**
* `category: String` - **Required**
* `steps: Array of TimerSteps` - **Required**

A step contains the following information:

* `name: String` - **Required**
* `length: String - form of hour:min:sec` - **Required**
* `pauseOnFinish: Bool`- **Required** - the last step's value will be ignored

#### Example
```json
{
	"name": "Example Timer",
	"author": "Joel Fischer",
	"category": "Food",
	"steps": [{
			"name": "Step 1",
			"length": "5:00",
			"pauseOnFinish": false
		},
		{
			"name": "Step 2",
			"length": "1:20",
			"pauseOnFinish": false
		}
	]
}
```

### Categories
The list of categories is currently as follows:
* "Food"
* "Utilities"
