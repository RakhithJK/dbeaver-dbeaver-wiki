# Linux
## GTK
DBeaver is an Eclipse RCP application. Therefore, it may have issues with GTK. Here are known workarounds regarding various issues which may arise.
### Fixing screen flickering.
* Add `export GTK_IM_MODULE=ibus` to `~/.profile`.  
### Parts of DBeaver are white/dark on dark/white theme
To fix the issue, we recommended having a graphical theme which is similar to system one in terms of the color palette.
### `GTK-WARNING xxx:Theme parsing error` 
This issue requires you to change the GTK-program-style `system settings-appearance-program style`(the setting location may vary for different systems).
### `gtk_box_gadget_distribute: assertion size 'size >=0 0' failed in GtkScrollbar`
Requires you to remove the overlay scrollbars in `~/.config/gtk-3.0/settings.ini`.
```
[Settings]
gtk-overlay-scrolling = false
```