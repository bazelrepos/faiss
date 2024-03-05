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
  static_library = 'libgfortran.a',
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
    'libgfortran',
  ],
  copts = ['-DFINTEGER=int'],
  linkopts = ['-lpthread', '-lgomp'],
  visibility = ["//visibility:public"],
)
