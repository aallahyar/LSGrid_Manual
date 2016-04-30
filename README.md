# LSGrid Manual
A very brief guide for Life Science Grid usage. See [here](https://grid.surfsara.nl/wiki/index.php/Using_the_Grid/Grid_storage#Deleting_files_from_a_Storage_Element) for more details.

### List files
Listing files and directories, e.g. to see all the files that are stored:

```bash
lfc-ls -l /grid/lsgrid/<your_username>
```

### Delete files
To delete a file from all storage elements, do

```bash
lcg-del -a lfn:/grid/lsgrid/<your_username>/<target_file.txt>
```
The -a option makes sure that all replicas of a file are removed. See the lcg-del man-page for more options.
