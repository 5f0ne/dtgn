# Description

Creates folder structures and puts data in it.

# Installation

`pip install dtgn`

# Usage

**From command line:**

`python -m dtgn [-h] [--mode {fixed,random}] --path PATH [--rootName ROOTNAME] [--depth DEPTH] [--fileCount FILECOUNT] [--fileMinSize FILEMINSIZE] [--fileMaxSize FILEMAXSIZE]  [--purge | --no-purge | -u]`

| Option | Short | Type | Default | Description |
|---|---|---|---|---|
|--mode | -m | String | fixed | Data Creation Mode <br> **fixed**: all files will be created the same size. Size is taken fom fileMinSize argument. <br> **random**: the files created will have a random size between fileMinSize and fileMaxSize argument. |
|--path | -p | String | - | Path under which the folder structure shall be located |
|--rootName | -r | String | dtgn | The name of the root folder created under path argument |
|--depth | -d | Integer | 1 | The depth of the folder structure |
|--fileCount | -f | Integer | 1 | Nr. of files per folder depth|
|--fileMinSize | -g | Integer | 2000 | The minium file size in bytes |
|--fileMaxSize | -i | Integer | 2000 | The maximum file size in bytes |
|--purge | -u | Boolean | False | If true, all files in path+rootName will be deleted. No folder structure is created. Use it carefully. |


# Example

`python -m dtgn -m random -p ./path/to -r dir -d 5 -f 10 -g 2048 -i 4096`

Creates `5` subfolders under `./path/to/dir` with `10` files per folder with a random size between `2048` and `4096` bytes per file.

```
################################################################################

dtgn (datagen) by 5f0
Creates folder structures and puts data in it

Current working directory: path/to/dtgn

Datetime: 01/01/1970 10:20:30

################################################################################

Mode: random
Create folder structure under ./path/to/dir
Create folder depth of 5
Create 10 files per folder
Size per file: between 2048 and 4096 Bytes

################################################################################

Total File Size created: 162008 Bytes
                         162.008 KB
                         0.162008 MB
                         0.00016200800000000003 GB

################################################################################

Execution Time: 0.004547 sec

```


# License

MIT