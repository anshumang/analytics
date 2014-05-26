# (c) 2010 The Board of Trustees of the University of Illinois.
#LANGUAGE=cuda
#SRCDIR_OBJS=main.o readatom.o output.o excl.o cutcpu.o cutoff6overlap.o
#APP_CUDALDFLAGS=-lm
all:
	cc -std=gnu99 -I/opt/nvidia/cudatoolkit/5.5.20-1.0402.7700.8.1/include -I. -c parboil_cuda.c
	nvcc -I. -c -arch compute_20 histo_main.cu histo_final.cu histo_intermediates.cu histo_prescan.cu util.cu main.cu
	cc -o parboil_histo -L/opt/cray/nvidia/default/lib64/ -lcuda parboil_cuda.o util.o main.o histo_main.o histo_final.o histo_intermediates.o histo_prescan.o
