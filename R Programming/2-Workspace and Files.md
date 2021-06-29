# Workspace and Files

## useful function

### `getwd()`

- print current working directory

### `ls()`

- list object/variable created in the current workspace

### `rm()`

- remove created object/variable.
- e.g. see below

```r
x <- 1
y <- 2
z <- 3
# remove x
rm(x)
# to remove all objects i.e. y, z
rm(list = ls())`
```

### `list.files()`

- show files under current working directory

### `setwd(dir)`

- set current directory to `dir`[^str], a directory address.
- e.g `setwd("testdir")`

### `file.create(filename)`[^str]

- create file with `filename`
- e.g. `file.create("mytest.R")`.

### `file.exists(filename)`

- check if file with filename exists and returns `boolean`.

### `file.info(filename)`

- show file info, e.g `file.info("mytest.R")`.
  - can use `$` to access its attributes such as `mode`
  - e.g. `file.info(filename)$mode`

### `file.rename(old_filename, new_filename)`

- rename file from old filename to new filename
- e.g. `file.rename("mytest.R", "mytest2.R")`, return `boolean`

### `file.copy(original_file, copy_to_file)`

- copy a file to a new file. e.g. `file.copy("mytest2.R", "mytest3.R")`



### `unlink("testdir/", recursive = TRUE)`

- remove a whole directory.

[^str]: `dir` is string
