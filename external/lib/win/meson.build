allegro_args = ['-D ALLEGRO_STATICLINK', '-D ALLEGRO_NO_STD_HEADERS', '-D ALLEGRO_NO_MAGIC_MAIN']
zlib_args = ['-D ZLIB_WINAPI']
preprocessor_flags += [allegro_args, zlib_args]
if host_machine.cpu_family() == 'x86_64'
  if get_option('debug')
  external_objects += files(
      'fmod_vc.lib',
      'liblz4_debug_static.lib',
      'libpng16_static.lib',
      'zlibstat.lib'
    )
  else
    external_objects += files(
      'fmod_vc.lib',
      'liblz4_release_static.lib',
      'libpng16_static.lib',
      'zlibstat.lib',
    )
  endif
else
message('using x86 libs')
  if get_option('debug')
  message('using debug libs')
  external_objects += files(
    'x86/fmodL_vc.lib',
    'x86/liblz4_debug_static.lib',
    'x86/libpng16_static.lib',
    'x86/zlibstat.lib',
    )
  else
    external_objects += files(
     'x86/fmodL_vc.lib',
     'x86/liblz4_release_static.lib',
     'x86/libpng16_static.lib',
     'x86/zlibstat.lib',
    )
  endif
endif
