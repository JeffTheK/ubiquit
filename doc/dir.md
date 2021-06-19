# Dir

Library `CoreDir`. Loaded and used by default.

### Functions

`static Bool is_dir(String path)` - returns true if provided path exists and false if not

`static Null delete(String path)` - deletes the provided dir path if exists

`Null constructor(String path)` - opens a directoryif exists or creates a new one if not

`Array list_files` - lists files of the directory
