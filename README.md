# aradict
Open Source Arabic word dictionary for Information Technology

## Distribution
All tranlations are for now organized in a simple format allowing easy addition for beginners and nearly no need for conflects managent.

### Content Fornat

Just add a new file with the English word you want to tanslate with a .json extension (all in lowercase), example to translate the word `sample` add a file `sample.json` under translation folder, the file will have a simple json data composed of list of an object with  fields:
- `context` a phrase or explanatory text for the word's usage
- `translation` the translation in Arabic
- `usage` example of usage in Arabic or a translation of the context
- `dual` the dual form if the word is countable (Arabic has singular, dual and plural forms)
- `plural` the dual form if the word is countable 

For example the content of the `sample.json` file should be 

```json
[
	{
		"context": "This file includes a sample of the test data",
		"translation": "عينة",
		"usage": "هذا الملف يحتوي على عينة من بياتات الاختبار",
		"dual": "عينتان",
		"plural": "عينات"
	}
]
```

## Access translation

There are multiple options for accessing the data the most obvious way is cloning the repository and pull regulary to check for new translations.

An other option is to check if the tranlation exist using `curl` or other cli tool and as a simple api.

```bash 
curl -L --fail https://github.com/ezzarghili/aradict/raw/master/translation/sample.json
```

This will fail if the translation file does not exist or return the tranlation data if it exists.

We will be adding new dict release formats that are automatically generated from the tranlation folder once there are enough data.


## License

All code would is licensed under MIT

All translations a.k.a content under translation folder will be licensed under [CC0 1.0 - التخصيص للملك العام
](https://creativecommons.org/publicdomain/zero/1.0/) 
