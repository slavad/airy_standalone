OBJ =  ai.o aie.o ali.o alnrel.o csevl.o d9aimp.o dai.o daie.o dcsevl.o e1.o\
	   ei.o fdump.o initds.o inits.o j4save.o r9aimp.o xermsg.o xercnt.o\
	   xerhlt.o xerprn.o xermax.o xersve.o xsetf.o xsetun.o xgetua.o spenc.o\
	   sindg.o r9ln2r.o r9atn1.o psi.o cot.o poch.o poch1.o r9lgmc.o gamr.o\
	   gamma.o fac.o exprel.o algams.o xgetf.o xerclr.o gamlim.o alngam.o gamit.o\
	   gamic.o gami.o r9gmic.o r9gmit.o r9lgit.o r9lgic.o erf.o daws.o cosdg.o\
	   chu.o cbrt.o r9upak.o r9pak.o r9chu.o erfc.o binom.o bie.o bi.o betai.o\
	   beta.o albeta.o besk1.o besk1e.o beskes.o besks.o r9knus.o besi1.o besi1e.o\
	   besi0.o besi0e.o besk0.o besk0e.o dpoch1.o dpoch.o dpsi.o dsindg.o dspenc.o\
	   d9lgmc.o dcot.o dexprl.o dfac.o dgamma.o dgamr.o dlgams.o dlnrel.o dlngam.o\
	   dgamlm.o de1.o dei.o derf.o dgami.o dgamic.o dgamit.o dli.o d9gmic.o d9gmit.o\
	   d9lgic.o d9lgit.o derfc.o d9ln2r.o d9atn1.o ddaws.o dcosdg.o dchu.o dcbrt.o\
	   dbskes.o d9chu.o d9knus.o d9pak.o d9upak.o dbi.o dbie.o dbinom.o dbsi0e.o\
	   dbsi1e.o dbsk0e.o dbsk1e.o dbesi1.o dbesi0.o dbesk0.o dbesk1.o dbesks.o\
	   dbeta.o dbetai.o dlbeta.o

LDFLAGS= -lgfortran

OBJM = d1mach.o r1mach.o i1mach.o
FFLAGSM = -fno-range-check

FCA = gfortran
FFLAGSA =

FC  = gfortran
FFLAGS = -O -std=legacy
TARGET_STAT = ../libairy.a
TARGET_DYN = ../libairy.so

all : $(TARGET_STAT) #$(TARGET_DYN)

$(TARGET_STAT) : $(OBJ) $(OBJM)
	ar r $@ $?
	ranlib $@

# $(TARGET_DYN) : $(OBJ) $(OBJM)
# 	$(CC) -shared ${LDFLAGS} -o $@  $?

$(OBJM):
	$(FC) $(FFLAGSM) -c $*.f

clean:
	-$(RM) $(TARGET_STAT) $(TARGET_DYN) $(OBJ) $(OBJM)

