# simple-logout   
![20241126_00:32:51_screenshot](https://github.com/user-attachments/assets/8ca4c7de-8623-4813-aa72-9ef8f3edf43c)     
  
A simple GTK3 logout menu for Wayland.

## Dependencies
- `gtk3`
- `python-gobject`
- `gobject-introspection`
- `gtk-layer-shell`

## Installation
- copy `simple-logout` to `/usr/bin`
- copy `config.json`, `style.css` and `icons/` to `~/.config/simple-logout` (and optionally `/usr/share/simple-logout` as backup)

## Configuration
Edit `~/.config/simple-logout/config.json`. The default looks like this:
```json
{
  "max_buttons_per_row": 3,
  "show_images": true,
  "show_labels": true,
  "buttons": [
    {
      "name": "lock",
      "image": "icons/lock.png",
      "label": "Lock",
      "command": "gtklock"
    },
    {
      "name": "hibernate",
      "image": "icons/hibernate.png",
      "label": "Hibernate",
      "command": "systemctl hibernate"
    },
    {
      "name": "shutdown",
      "image": "icons/shutdown.png",
      "label": "Shutdown",
      "command": "systemctl shutdown"
    },
    {
      "name": "suspend",
      "image": "icons/suspend.png",
      "label": "Suspend",
      "command": "systemctl suspend"
    },
    {
      "name": "logout",
      "image": "icons/logout.png",
      "label": "Logout",
      "command": "hyprctl dispatch exit"
    },
    {
      "name": "reboot",
      "image": "icons/reboot.png",
      "label": "Reboot",
      "command": "systemctl reboot"
    }
  ]
}
```

## Styling
Edit `~/config/simple-logout/style.css`. The default looks like this:
```css
window {
    border-radius: 10px;
    border: 2px solid #3B3431;
}

button {
    padding: 25px;
}
```
