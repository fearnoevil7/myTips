# How to delete whitespace from a file:
- $ `cat file.txt | tr -d "[:space:]"`

# How to ssh into Windows UTM Virtual Machine:
- $ `ssh -R 127.0.0.1 -p 7777`
	- **How to copy files to the VM**
		- $ `scp -P 5555 ./Test.txt Jonathan@127.0.0.1:/Users/Jonathan`

# How to ssh into Kali Linux UTM Virtual Machine:
- $ `ssh -R 127.0.0.1 -p 5555`
	- **How to copy files to the VM**
		- $ `scp -P 5555 ./Test.txt kurama@127.0.0.1:/home/kurama/Backups`

