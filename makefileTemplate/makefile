GCC := gcc
CCFLAGS := -std=c11
SRC := main.c
EXE := main
OBJS := $(SRC:.c=.o)

.PHONY : clean cleanall

$(EXE) : $(SRC)
	$(GCC) $(CCFLAGS) -o $@ $^

clean :
	-\rm $(OBJS)

cleanall :
	-\rm $(EXE)
