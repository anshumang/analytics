# (c) 2007 The Board of Trustees of the University of Illinois.

#LANGUAGE=cuda
#SRCDIR_OBJS=main.o histo_final.o histo_intermediates.o histo_main.o histo_prescan.o util.o
#APP_CUDACFLAGS=-arch compute_20

all:
	nvcc -I./ -I/opt/nvidia/cudatoolkit/5.5.20-1.0402.7700.8.1/include -o parboil_histo -arch compute_20 histo_final.cu histo_intermediates.cu histo_main.cu histo_prescan.cu main.cu parboil_cuda.c util.cu -L/opt/cray/nvidia/default/lib64/ -lcuda
