```
$$\  $$$$$$\                  $$\ 
\__|$$  __$$\                 $$ |
$$\ $$ /  \__| $$$$$$\   $$$$$$$ |
$$ |\$$$$$$\  $$  __$$\ $$  __$$ |
$$ | \____$$\ $$$$$$$$ |$$ /  $$ |
$$ |$$\   $$ |$$   ____|$$ |  $$ |
$$ |\$$$$$$  |\$$$$$$$\ \$$$$$$$ |
\__| \______/  \_______| \_______|

v0.1.0
```
iSed (interactive sed) is a small script that allows you to see what your sed command will change, before making those changes.

The script wraps sed and [icdiff](https://github.com/jeffkaufman/icdiff).

## Demo
![A demo of the script running in the terminal](https://github.com/Mochitto/iSed/blob/main/docs/demo.png?raw=true)
![A demo of the script running in the terminal](https://github.com/Mochitto/iSed/blob/main/docs/long%20demo.png?raw=true)

## Installation

- Install `icdiff` using `pip`.
```bash
pip install icdiff
```
- Clone this repository.
```bash
git clone https://github.com/Mochitto/iSed.git 
```
- Turn the script into an executable.
- Move it to your bin directory to run it with `iSed`.

## Usage

iSed has the same interface as `sed`.

Once you define your command, you will be shown a git-style diff, where you can evaluate if to continue or not.

To do this, the script pipes the output of sed to a temporary file, that overwrites the original if the changes are deemed correct.

### Notice!
It will not prevent you from changing the file in place with `sed`'s `-i` flag.  
It's also important to put the file to change as last argument (I'm new to scripting, hopefully someone can help make this better).
```bash
iSed -r "s/foo/bar/g" my_file.txt
```

## Contributing

Pull requests are super welcome. 💕  
For major changes, please open an issue first, to discuss what you would like to change.

## License

This project's license: [GPL3](https://choosealicense.com/licenses/gpl-3.0/).

You can also find the license of `icdiff` [here](https://github.com/jeffkaufman/icdiff/blob/master/LICENSE).
