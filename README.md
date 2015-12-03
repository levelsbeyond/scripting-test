#Levels Beyond Scripting Test

Write script that processes all of the files in a directory. Inside this directory, some files start with a number then an underscore:

```
10_someStuff.txt
```

Some don't:

```
SomeMoreStuff.txt
```

I want a script that accepts a path to this directory, then makes three sub-directories in it:

1. fizz/
2. buzz/
3. fizzbuzz/

For Each file in the directory, do one of four things:

1. If the leading number is a multiple of three, copy the file into the 'fizz/' directory
2. If the leading number is a multiple of 5, copy the file into the 'buzz/' directory
3. If the leading number is a multiple of both 3 and 5, copy the file into the 'fizzbuzz/' directory.
4. If the file does not start with a number, or that number is not divisible by 3 or 5, then print the name of that file to standard output.

Use any scripting language you want, and provide instructions to execute your script. I should be able to run it easily:

```bash
/path/to/your/script /path/to/directory/of/files
```

This project contains a directory, 'files_for_processing', that you should use to develop your script.

##Bonus

Inside each sub-directory (fizz, buzz, and fizzbuzz), include a sidecar file called `metadata.json`. That file should include a list of all the files, and metadata about them. Include at least an md5 checksum of the file in them metadata structure, plus any other metadata you might want to add.

```json
{
	"files": [{
		"1_somefile.txt": {
			"checksum": "dda3b7f8b64db22dfdf84facc2159238"
		}
	}, {
		"2_someOtherFile.txt": {
			"checksum": "dda3b7f8b64db22dfdf84facc2159238"
		}
	}]
}
```
