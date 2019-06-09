OBJ =  ai.o  aie.o  csevl.o  d9aimp.o  dai.o  daie.o  dcsevl.o fdump.o initds.o\
	   inits.o j4save.o r9aimp.o  xermsg.o xercnt.o xerhlt.o xerprn.o xersve.o\
	   xgetua.o

LDFLAGS= -lgfortran

OBJM = d1mach.o r1mach.o i1mach.o
FFLAGSM = -fno-range-check

FCA = gfortran
FFLAGSA =

FC  = gfortran
FFLAGS = -O -std=legacy
TARGET_STAT = ../libairy.a
TARGET_DYN = ../libairy.so

all : $(TARGET_STAT) $(TARGET_DYN)

$(TARGET_STAT) : $(OBJ) $(OBJM)
	ar r $@ $?
	ranlib $@

$(TARGET_DYN) : $(OBJ) $(OBJM)
	$(CC) -shared ${LDFLAGS} -o $@  $?

$(OBJM):
	$(FC) $(FFLAGSM) -c $*.f

clean:
	-$(RM) $(TARGET_STAT) $(TARGET_DYN) $(OBJ) $(OBJM)

