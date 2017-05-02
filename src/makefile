################################################################################
# SRC Path Makefile 
################################################################################
###########################
# head file include
###########################
#export INCLUDES += -I $(shell pwd)


###########################
# subdir include
###########################
#include all subdir
SUBDIRS=$(shell ls -l | grep ^d | awk '{print $$9}')
#include specified subdir
#SUBDIRS = 


###########################
# src file include
###########################
#include all .c file
SRCS = ${wildcard *.c}
#include specified .c file
#SRCS = main.c 

###########################
# objs form SRCS
###########################
OBJS = $(patsubst %.c,%.o, $(SRCS))

all: $(SUBDIRS) $(OBJS)

.PHONY: $(SUBDIRS)
$(SUBDIRS):
	$(MAKE) -C $@
	
$(OBJS):%.o:%.c
	@echo 'Building file: $<'
	$(CC) $(INCLUDES) $(CFLAGS) -c -o $(OBJPATH)$@ $^
	@echo 'Finished building: $<'
	@echo ' '
