# TF2 documentation generation

## Premade lists

You can view premade cvarlists, launch options lists and hidden cvarlists.

* [Windows cvarlist](https://docs.mastercomfig.com/page/tf2/cvarlist_win)
* [Windows Launch option list](https://docs.mastercomfig.com/page/tf2/launchopts_win)
* [Linux cvarlist](https://docs.mastercomfig.com/page/tf2/cvarlist_linux)
* [Linux launch option list](https://docs.mastercomfig.com/page/tf2/launchopts_linux)
* [Hidden cvarlist](https://docs.mastercomfig.com/page/tf2/hiddencvars)

## Making your own cvar list

1. Remove mastercomfig VPK and add these launch options: `-novid -autoconfig -default -conclearlog -condebug +clear +cvarlist +quit`.
2. Launch TF2.
3. Remove launch options, add mastercomfig again.
4. Copy and paste `tf/console.log` cvarlist.

## Making your own hidden cvar list

Use the [sm_cvarlist](https://forums.alliedmods.net/showthread.php?p=1298262) SourceMod plugin.

## Making your own launch options list

On Windows you can use the [GetLaunchOptions.bat](https://github.com/AveYo/D-OPTIMIZER/blob/archive/GetLaunchOptions.bat) script.

On Linux you can use following commands: `find . -type f \( -name "*.so" -o -name "hl2_linux" \) -print0 | xargs -0 strings | grep "^\-[a-ZA-Z]" | awk 'NF==1' | sort -u > launch_options.txt`
