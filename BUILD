cc_import(
  name = 'liblapacke',
  static_library = 'liblapacke.a',
)

cc_import(
  name = 'liblapack',
  static_library = 'liblapack.a',
)

cc_import(
  name = 'libcblas',
  static_library = 'libcblas.a',
)

cc_import(
  name = 'librefblas',
  static_library = 'librefblas.a',
)

cc_import(
  name = 'libgfortran',
  shared_library = 'libgfortran.so.5',
)

cc_import(
  name = 'libquadmath',
  shared_library = 'libquadmath.so.0',
)

cc_import(
  name = 'libz',
  shared_library = 'libz.so.1',
)

cc_library(
  name = 'faiss',
  hdrs = glob(['faiss/*.h']) 
        + glob(['faiss/impl/*.h']) 
        + glob(['faiss/utils/*.h']) 
        + glob(['faiss/invlists/*.h']) 
        + glob(['faiss/impl/*/*.h']) 
        + glob(['faiss/utils/*/*.h']),
  srcs = glob(['faiss/*.cpp']) 
        + glob(['faiss/impl/*.cpp']) 
        + glob(['faiss/utils/*.cpp']) 
        + glob(['faiss/invlists/*.cpp']) 
        + glob(['faiss/impl/*/*.cpp']) 
        + glob(['faiss/utils/*/*.cpp']),
  includes = [''],
  deps = [
    'liblapacke',
    'liblapack',
    'libcblas',
    'librefblas',
    #'libgfortran',
    #'libquadmath',
    #'libz',
  ],
  copts = ['-DFINTEGER=int'],
  linkopts = ['-lpthread', '-lgomp', '-lgfortran', '-L/usr/lib64'],
  visibility = ["//visibility:public"],
)
