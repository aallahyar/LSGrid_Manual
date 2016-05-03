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

# Port Forwarding 
(from: http://unix.stackexchange.com/a/118650)


__Local:__ -L Specifies that the given port on the local (client) host is to be forwarded to the given host and port on the remote side.

ssh -L sourcePort:forwardToHost:onPort connectToHost means: connect with ssh to connectToHost, and forward all connection attempts to the local sourcePort to port onPort on the machine called forwardToHost, which can be reached from the connectToHost machine.

<img src="http://i.stack.imgur.com/a28N8.png" alt="Local port forwarding" width="50%"/>

__Remote:__ -R Specifies that the given port on the remote (server) host is to be forwarded to the given host and port on the local side.

ssh -R sourcePort:forwardToHost:onPort connectToHost means: connect with ssh to connectToHost, and forward all connection attempts to the remote sourcePort to port onPort on the machine called forwardToHost, which can be reached from your local machine.

<img src="http://i.stack.imgur.com/4iK3b.png" alt="Remote port forwarding" width="50%"/>
