# Linux
## GTK
DBeaver is an Eclipse RCP application. Because of it, it may have issues with GTK, here are known workarounds regarding various issues which may arise.
### Fixing screen flickering
* Add `export GTK_IM_MODULE=ibus` to `~/.profile`.  
### Parts of DBeaver are from white/dark on dark/white theme
To fix the issue it's recommended to have a graphical theme which is similar to system one in terms of the color palette
### `GTK-WARNING xxx:Theme parsing error` 
This issue requires you to change GTK-program-style `system settings-appearance-program style`(setting location may vary on different systems)
### `gtk_box_gadget_distribute: assertion size 'size >=0 0' failed in GtkScrollbar`
Requires you to remove the overlay scrollbars in `~/.config/gtk-3.0/settings.ini`
```
[Settings]
gtk-overlay-scrolling = false
```