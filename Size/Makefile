CCflags = -c -depend !Depend -IC: -IRiksLib: -throwback -fafh -apcs 3/32/fpe2/swst/fp/nofpr
Linkflags = -aif
ObjAsmflags = -throwback -depend !Depend
Squeezeflags =
cc = cc
asm = objasm
rm = rm
Binary = size

CommonObjFiles =

NormalObjFiles = o.Main 

CommonLibs =	C:o.Stubs

NormalLibs =

# Final targets:
.SUFFIXES:	.o .c .s .m

all:	$(Binary)

$(Binary):\
	$(NormalLibs) $(CommonLibs) $(CommonObjFiles) $(NormalObjFiles)
	Link $(LinkFlags) -o $(Binary) \
	$(NormalLibs) $(CommonLibs) $(CommonObjFiles) $(NormalObjFiles)
	Squeeze $(Squeezeflags) $(Binary)
	copy $(Binary) <Boot$Dir>.Library.* FR~V~C

Clean:
	rm $(CommonObjFiles)
	rm $(NormalObjFiles)
	rm $(MCObjFiles)
	trim -file MakeFile -line "<35> Dynamic dependencies:"

# Static dependencies:

.c.o:;	$(cc) $(ccflags) -o $@ $<
.s.o:;	$(asm) $(asmflags) -from $< -to $@


# Dynamic dependencies:
