# YAML Smasher

### What does it do?
*YAML Smasher* is a simple command line utility that constructs individual directories from a `.yml` file.

### Why should you care?
YAML is a fantastic format for simple data construction. However, a master `.yml` file may become too unruly or may not be compatible with your workflow.  I built this tool specifically to manage content for the [Roots framework](http://roots.cx/), a terrific static website compiler.

### How to use

- Clone repo

- `cd path/to/repo`

- Make sure [thor](https://github.com/erikhuda/thor) is installed
  - `gem install thor`

- Check thor tasks
  - `thor -T`

- Run YAML Smasher
  - `thor yaml:smash:file FILE.yml`
    - e.g. `thor yaml:smash:file test.yml`
    - append `--force` to forcefully overwrite

### Constructing your own `.yml` files
*YAML Smasher* simply loops over hash sequences in your `.yml` file and looks for two specific key value pairs:
```yaml
folder: foldername
filename: filename
...
=> foldername/filename.yml
```
It will use these special key value pairs to construct the directory and path of the new `.yml` file. All other key value pairs will be the content of the `.yml` file.

### What next?
Most likely, this is where it ends...
