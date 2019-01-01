# aradict
Open Source Arabic dictionary for Information Technology

## format
All tranlations are for now organized in a simple format allowing easy addition for beginners and nearly no need for conflects managent.

### create a new translation

just add a new file with the english word you want to tanslate with a .json extension, example to translate `sample` add a file `sample.json` under translation folder, the file will have a simple json data composed of three fields:
- `s` meaning singular
- `d` meaning dual (Arabic has singular, dual and plural forms)
- `p` meaning plural

For example the content of the `sample.json` file should be 

```json
{
	"s": "عينة",
	"d": "عينتان",
	"p": "عينات"
}
```
Or in a more compact way

```json
{"s": "عينة","d": "عينتان","p": "عينات"}
```

## Access translation

There are multiple options for accessing the data the most obvious way is cloning the repository and pull regulary to check for new translations.

An other option is to check if the tranlation exist using `curl` or other cli tool and as a simple api. 
```bash 
curl -L --fail https://github.com/ezzarghili/aradict/raw/master/translation/sample.json
```

This will fail if the translation file does not exist or return the tranlation data if it exists.

We will be adding new dict release formats that are automatically generated from the tranlation folder once there are enough data.
