# Production Tools Templates
This repo includes template for Bash files, makefile, CMakeLists that I used frequently.

## Bash Template
### cleanGitignore.bash
```shell
chmod 700 cleanGiignore.bash
./cleanGiignore.bash < .gitignore
```
**Note**: In gitignore file, make sure to have new line at the end so the bash file can read the last line with filename

## makefile Template
### makefile
```shell
make 
```

### Multiple files
```make
cc := gcc
ccflags := -std=c11 -Wall
src := ccadd.c ccitem.c ccstat.c 
dest := build

all : $(dest)/ccadd $(dest)/ccitem $(dest)/ccstat

$(dest)/ccadd : ccadd.c
	$(cc) $(ccflags) -o $@ $<

$(dest)/ccitem : ccitem.c
	$(cc) $(ccflags) -o $@ $<

$(dest)/ccstat : ccstat.c
	$(cc) $(ccflags) -o $@ $<
```

## CMakeLists Template
### CMakeLists.txt
```shell
mkdir build
cd build
cmake ../
make
```





