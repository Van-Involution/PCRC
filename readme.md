PCRC
--------

> PyCraft based Replay Client

~~SARC doesn't work in 1.13+ version so I made this crap~~

An minecraft client that can record a replay file (*mcpr) which can be recognized by replay mod

Great thanks to [SARC](https://github.com/Robitobi01/SARC) for the replay logic stuffs and [pyCraft](https://github.com/ammaraskar/pyCraft) for the minecraft client stuffs

**Supports 1.14.4 server only** tho with a bit modification it works in any version as long as pyCraft supports that

needs python3, at least works on python 3.6.6

## Advantage

- Can be hosted serverside for 24/7 recording
- It starts recording as soon as it login
- It can be set to record only when the player is nearby


## Config

`online_mode` : Use online mode to login or offline mode instead

`username` : Username or email for the used Minecraft account

`password` : Password for the used Minecraft account if login in in online mode

`address` : IP Address of the Minecraft server

`port` : Port of the Minecraft server

`minimal_packets` : PCRC will only record the minimum needed packets for a proper recording when this option is turned on. This should be used to decrease the filesize of recordings while recording long term projects (timelapse)

`daytime` : Sets the daytime once to the defined time in the recording and ignores all further changes from the server. If set to `-1` the normal day/night cycle is recorded

`weather` : Turns weather in the recording on or off

`with_player_only` : Only record packets if there are players nearby

`remove_items` : If set to true, all dropped items wont be recorded. This can potentially decrease filesize

`remove_bats` : If set to true, bats wont be recorded. This can potentially decrease filesize

`upload_file` : If set to true, .mcpr file will be sent to [transfer.sh](transfer.sh) after finishing recording

`auto_relogin` : If this option is enabled and the client gets disconnected, it will automatically reconnect after 3 seconds

`debug_mode` : Outputs debug info

## Command

### Console Command

`start`: start PCRC and start recording

`stop`: stop PCRC and stop recording

`restart`: restart PCRC

`exit`: exit the program

`say <message>`: send chat message `<message>` to the server

`set <option> <value>` set option to value in config.json

### In Game Command

`!!PCRC`: show help

`!!PCRC status`: show status

`!!PCRC here`: emit a "!!here" command

`!!PCRC pos`: show position, might not be 100% accurate

`!!PCRC sepc`: spectator teleport to the player

`!!PCRC stop`: stop PCRC

`!!PCRC url`: print all urls of recorded files