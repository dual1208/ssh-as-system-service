# ssh-as-system-service
for mac and linux

should consider AFTER network is established

## Mac
write sth. like
"""
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
"""
into your /Library/LaunchAgents/com.blabla.plist, where /Users/your_user_name/blabla.sh is the script for your ssh port forwarding.
