render_sources = files(
  '4J_Render.cpp',
  'stdafx.cpp',
)
root_inc = include_directories('../..') 

lib_render = static_library(
  '4J_Render',
  render_sources,
  include_directories: [render_inc, root_inc], 
  dependencies: [sdl2_dep, gl_dep, thread_dep],
  cpp_args: fourj_cpp_args + fourj_cpp_defs + [
    '-include', meson.current_source_dir() / '../../4J.Render/stdafx.h',
  ],
)

render_dep = declare_dependency(
  link_with : lib_render,
  include_directories : include_directories('.'),
)
