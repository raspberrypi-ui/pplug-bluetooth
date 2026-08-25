gtk = dependency('gtk+-3.0')
gtkmm = dependency('gtkmm-3.0', version: '>=3.24')
lxpanel = dependency('lxpanel-pi')
wfpanel = dependency('wf-panel-pi')

sources = files(
  'bluetooth.c'
)

lsources = files(
  'bluetooth_lxp.c'
)

ldeps = [ gtk, lxpanel ]

largs = [ '-DPACKAGE_DATA_DIR="' + lresource_dir + '"', '-DGETTEXT_PACKAGE="lpplug_' + meson.project_name() + '"' ]

shared_module(meson.project_name(), [ sources, lsources ],
        dependencies: ldeps,
        install: true,
        install_dir: get_option('libdir') / 'lxpanel-pi',
        c_args : largs,
        name_prefix: ''
)

wsources = files(
  'bluetooth.cpp'
)

wdeps = [ gtkmm, wfpanel ]

wargs = [ '-DPACKAGE_DATA_DIR="' + wresource_dir + '"', '-DGETTEXT_PACKAGE="wfplug_' + meson.project_name() +'"' ]

shared_module('lib' + meson.project_name(), [ sources, wsources ],
        dependencies: wdeps,
        install: true,
        install_dir: get_option('libdir') / 'wf-panel-pi',
        c_args : wargs,
        cpp_args : wargs,
        name_prefix: ''
)
