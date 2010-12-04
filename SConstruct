import os, sys

outputfile = 'sdfont'

env = Environment()
env.Append(CCFLAGS = ['-g3'])
env.Append(LIBS = ['freetype'])
env.Append(CPPPATH = ['/usr/include/freetype2'])

list = Split("""main.cpp
	stb_image.c
	BinPacker.cpp
	lodepng.cpp""")

list.sort(lambda x, y: cmp(x.lower(),y.lower()))

outputprogram = env.Program(outputfile, list)

