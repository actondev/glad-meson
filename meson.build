project('glad', 'c')

system = host_machine.system()

glad_deps = []
if system == 'darwin'
    # glad_deps += dependency('appleframeworks', modules: [
    #   'OpenGL',
    # ])
endif

glad = library(
  'glad',
  sources: 'src/glad.c',
  include_directories: 'include',
  c_args: [
    '-DGLAD_GLAPI_EXPORT=1',
    '-DGLAD_GLAPI_EXPORT_BUILD=1',
  ]
)

glad_dep = declare_dependency(
  link_with: glad,
  include_directories: 'include',
  dependencies: [glad_deps],
)
