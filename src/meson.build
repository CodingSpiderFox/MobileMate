mobilemate_sources = [
  'main.vala',
  'window.vala',
]

mobilemate_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
]

gnome = import('gnome')

mobilemate_sources += gnome.compile_resources('mobilemate-resources',
  'mobilemate.gresource.xml',
  c_name: 'mobilemate'
)

executable('mobilemate', mobilemate_sources,
  vala_args: '--target-glib=2.50',  dependencies: mobilemate_deps,
  install: true,
)
