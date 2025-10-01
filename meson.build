project(
  'plyvel',
  'cpp',
  version: run_command(
    'python', '-c',
    'import os; exec(open(os.path.join(meson.source_root(), "plyvel/_version.py")).read()); print(__version__)',
    check: true
  ).stdout().strip(),
  license: 'BSD-3-Clause',
  meson_version: '>=0.58.0',
)

py = import('python').find_installation(pure: false)
py_dep = py.dependency()

subdir('plyvel')