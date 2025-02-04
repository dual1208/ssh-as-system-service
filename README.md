Here's the polished version of your README:

# SSH as a System Service
For macOS and Linux

Ensure this is done after the network is established.

## macOS
Create a plist file with the following content and place it in `/Library/LaunchAgents/com.blabla.plist`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>org.blabla.on-dhcp-renew</string>
    <key>ProgramArguments</key>
    <array>
        <string>/Users/your_user_name/blabla.sh</string>
    </array>
    <key>WatchPaths</key>
    <array>
        <string>/var/run/resolv.conf</string>
    </array>
</dict>
</plist>
```

Replace `/Users/your_user_name/blabla.sh` with the path to your SSH port forwarding script.
