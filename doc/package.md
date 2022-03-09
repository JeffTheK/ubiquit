# Library Structure

### File Structure

Here is shown a `foo_bar` package example

````
foo_bar
|	readme.md
|	code_of_conduct.md
| 	license.txt
|	package.json
|	taskfile
|	.gitignore
|
|___src
|		foo.ubi
|		bar.ubi
|
|___test
|		test_foo.ubi
|		test_bar.ubi
|
|___doc
|		doc1.md
|		doc2.md


````

### Package specification

Contains useful information about the library.

#### Required Properties:

* `name` - this package's name
* `author` or `authors` - a list of creators
* `version` - current package version

#### Recommended Properties:

* `email`
* `homepage`
* `license`
* `description`



### `package.json` Structure Example	

````json
{
    "package": {
        "name": "foo_bar",
        "version": "1.0.0",
        "license": "MIT",
        "authors": [
            "JeffTheK",
            "Shwaika"
        ],
        "email": "jeff@example.com",
        "homepage": "https://github.com/jeff/foo_bar",
        "ubiquit_version": "3.*",
        "description": "Provides foo and bar"
        "runtime_dependencies": [
            {
                "name": "some_library",
                "version": "1.6.*"
            },
            {
                "name": "other_tool",
                "version": "*"
            }
        ],
        "development_dependencies": [
            {
               	"name": "fast_test",
                "version": "2.0.1"
            }
        ],
        "executables": [ "foo" ],       
        "post_install_message": "Thanks for installing!",
        "requirements": [
            "A good graphics card"
        ]
    }
}
````


