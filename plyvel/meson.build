cython_sources = [
  '_plyvel.pyx',
]

cpp_sources = [
  'comparator.cpp',
]

leveldb_dep = dependency('leveldb', required: true)

py.extension_module(
  '_plyvel',
  cython_sources,
  cpp_sources,
  dependencies: [leveldb_dep, py_dep],
  cpp_args: ['-Wall', '-g', '-std=c++11', '-fno-rtti'],
  install: true,
  subdir: 'plyvel',
)

py.install_sources(
  [
    '__init__.py',
    '_version.py',
    'errors.py',
    '_plyvel.pyi',
  ],
  subdir: 'plyvel'
)