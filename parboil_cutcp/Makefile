# (c) 2007 The Board of Trustees of the University of Illinois.

#LANGUAGE=cuda
#SRCDIR_OBJS=main.o histo_final.o histo_intermediates.o histo_main.o histo_prescan.o util.o
#APP_CUDACFLAGS=-arch compute_20

all:
	cc -std=gnu99 -I/opt/nvidia/cudatoolkit/5.5.20-1.0402.7700.8.1/include -I. -c parboil_cuda.c excl.c cutcpu.c readatom.c output.c main.c
	nvcc -I. -c cutoff6overlap.cu
	cc -o parboil_cutcp -L/opt/cray/nvidia/default/lib64/ -lcuda parboil_cuda.o excl.o cutcpu.o readatom.o output.o main.o cutoff6overlap.o
