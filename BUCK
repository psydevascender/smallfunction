# Generated by Buckaroo - https://buckaroo.pm
include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'smallfunction',
  header_namespace = 'smallfunction',
  srcs = glob([
    'smallfunction/src/**/*.cpp',
  ]),
  headers = subdir_glob([ # private include files
    ('smallfunction/detail', '**/*.h'), # they are only accesible inside the library
    ('smallfunction/detail', '**/*.hpp'),
  ]),
  exported_headers = subdir_glob([ # public include files
    ('smallfunction/include', '**/*.h'), # those will be exported
    ('smallfunction/include', '**/*.hpp'), # and accessible via <smallfunction/header.h>
  ]),
  deps = BUCKAROO_DEPS,
  visibility = ['PUBLIC']
)

cxx_binary(
  name = 'main',
  srcs = ['smallfunction/apps/main.cpp'],
  deps = [':smallfunction'],
  linker_flags = ['-lpthread'],
  visibility = ['PUBLIC']
)
