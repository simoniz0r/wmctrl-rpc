# wmctrl-rpc

A wrapper for [EasyRP](https://github.com/Pizzabelly/EasyRP) that gets window titles using `wmctrl` for Discord RPC.

# Usage

**Dependencies**: curl (used for downloading EasyRP on first run and grabbing list of icons from [here](https://github.com/simoniz0r/wmctrl-rpc/blob/master/wmctrl-rpc-icons.sh) on each run), wmctrl (for getting window titles), xprop (for selecting window to track).

Just run `wmctrl-rpc`, and it will automatically update your Discord RPC status based on the title of the chosen window.  Run `wmctrl-rpc win` to select a new window to track or edit `~/.local/share/wmctrl-rpc/wmctrl-rpc.conf` and instert a valid window class manually.  Run `wmctrl-rpc stop` to stop `wmctrl-rpc`.

On first run, `~/.local/share/wmctrl-rpc` will be created, and EasyRP will be downloaded to `~/.local/share/wmctrl-rpc`. If the title of the window changes, the window is closed, or a new window is chosen to track, `wmctrl-rpc` updates EasyRP's config file with the new information. 

# Icons

If an application you use is not listed in [wmctrl-rpc's icon list](https://github.com/simoniz0r/wmctrl-rpc/blob/master/wmctrl-rpc-icons.sh), please create [an issue](https://github.com/simoniz0r/wmctrl-rpc/issues/new) with a link to the application's official icon in png format.  As far as I'm aware, Discord RPC has no limit to the amount of icons that can be uploaded, so all requests should be granted as long as the icon is the official icon.

# Troubleshooting

## Is it not working but you're not getting any errors or anything?

Please ensure under Discord Settings -> Game Activity -> "Display currently running game as a status message" is enabled/turned-on.
If this option isn't set, you will be very confused as to why it's not working.

