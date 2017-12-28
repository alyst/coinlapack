project('BLAS', 'fortran', version: '3.8.0')

subdir('SRC')

if add_languages('c', required: false)
  # FIXME other fortran standard libraries
  fortran_lib = meson.get_compiler('c').find_library('gfortran')
endif

coinlapack_dep = declare_dependency(link_with: [libcoinlapack],
                                    dependencies: [fortran_lib])
