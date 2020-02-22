# ding-timer-templates
JSON data for Ding Timer Templates

## JSON Format

### Folders
Each folder corresponds with a "category" of timer. These are hard-coded into the app, so adding a new one requires an app update. If you're making a PR with a new template, make your best guess as to the category, but follow the maintainer's direction if the category should be changed.

### Template Information
The JSON data for a template includes the following data:

* `name: String`- **Required**
* `author: String` - **Optional**
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
