# Requirements

1. passwordless ssh access:

	```
	$ ssh-keygen
	$ ssh-copy-id -i hpc.nbi.ac.uk
	```

   After this, `$ ssh hpc.nbi.ac.uk` shouldn't ask for password.

2. conda environment with dependencies:

	```
	$ name=something123
	$ conda create -p $HOME/$name jupyter paramiko
	$ source activate $HOME/$name
	```

# Usage

	```
	$ headNode=v0523
	$ python2 pynb.py -p 8888 -r localhost:8885 $headNode
	```

