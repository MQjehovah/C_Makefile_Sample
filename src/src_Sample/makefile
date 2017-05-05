################################################################################
# Sample Makefile
################################################################################
# All of the sources participating in the build are defined here
-include project.mk

SUBDIRS = src/
# All Target
all: $(TARGET)

# Tool invocations
$(TARGET): $(SUBDIRS)
	$(MAKE) -C $(OBJPATH)
	-@echo make finished

.PHONY: $(SUBDIRS)
$(SUBDIRS):
	$(MAKE) -C $@

clean:
	-rm -rf $(OBJPATH)/*.o $(BINPATH)$(TARGET)
	-@echo clean finished
	-@echo ' '

.PHONY: all clean 
