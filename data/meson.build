lui_dir = join_paths(lresource_dir, 'ui')
install_data('lxplug-bluetooth.ui', install_dir: lui_dir)
wui_dir = join_paths(wresource_dir, 'ui')
install_data('lxplug-bluetooth.ui', install_dir: wui_dir)

install_subdir('icons', install_dir: share_dir)
gnome = import ('gnome')
gnome.post_install (gtk_update_icon_cache : true)

