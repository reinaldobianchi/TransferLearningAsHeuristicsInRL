EXEC	= learn3D
OFILES	=  mcar3D.o learn3D.o

CC	= g++ 

LIBS	=	-lm 

$(EXEC)	: $(OFILES)
	echo "linking $<"
	$(CC) -O2 -o $(EXEC) $(OFILES)  $(LIBS) $(INCLUDE)
	echo -n "make finished at "; date

mcar3D.o : mcar3D.cpp mcar3D.h
	$(CC) -c mcar3D.cpp

map2Dto3D.o : learn3D.cpp learn3D.h
	$(CC) -c learn3D.cpp

# Clean up after making.
clean:
	echo "removing" *.o
	$(RM) *.o
	if [ -d /tmp/$(USER)tmp ]; \
	 then echo "clearing /tmp/$(USER)tmp"; $(MAKE) tclean; fi


# Time your make.
time:
	/usr/bin/time $(MAKE)




