# YAML Smasher

### What does it do?
*YAML Smasher* is a simple command line utility that constructs individual directories from a `.yaml` file.

### Why should I care?
YAML is a fantastic format for simple data construction. However, a master `.yaml` file may become too unruly or may not be compatible with your workflow.  I built this tool specifically to manage content for the [Roots framework](http://roots.cx/), a terrific static website compiler.

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

### What next?
Most likely, this is where it ends...
