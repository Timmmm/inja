project('inja', 'cpp', default_options: ['cpp_std=c++17'])


#option('build_tests', type: 'boolean', value: true)
#option('build_benchmark', type: 'boolean', value: true)


inja_dep = declare_dependency(
  include_directories: include_directories('include')
)


inja_test = executable(
  'inja_test',
  'test/unit.cpp',
  'test/unit-files.cpp',
  'test/unit-renderer.cpp',
  dependencies: inja_dep
)

inja_benchmark = executable(
  'inja_benchmark',
  'test/benchmark.cpp',
  dependencies: inja_dep
)


test('Inja unit test', inja_test)
