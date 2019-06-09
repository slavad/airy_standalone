OBJ= dfnck.o sfnck.o

PROGS = test02 test03

FC = gfortran
FFLAGS = -g -std=legacy
LIB = libslachk.a
SLIB = libairy.a

all: $(PROGS)

clean:
	-$(RM) $(PROGS) $(LIB) $(OBJ) test??.o *.a

$(SLIB):
	$(MAKE) -C ../src
	cp ../$(SLIB) .

$(LIB): $(OBJ)
	ar r $@ $?
	ranlib $@

test02 : test02.o $(LIB) $(SLIB)
	$(FC) -o $@ $< -L. -lslachk -lairy

test03 : test03.o $(LIB) $(SLIB)
	$(FC) -o $@ $< -L.  -lslachk -lairy

