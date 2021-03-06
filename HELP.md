Help on package denonavr:

NAME
    denonavr - Automation Library for Denon AVR receivers.

DESCRIPTION
    :copyright: (c) 2016 by Oliver Goetz.
    :license: MIT, see LICENSE for more details.

PACKAGE CONTENTS
    denonavr

DATA
    __title__ = 'denonavr'

VERSION
    0.1.6

====================================================================================

Help on module denonavr.denonavr in denonavr:

NAME
    denonavr.denonavr - This module implements the interface to Denon AVR receivers.

DESCRIPTION
    :copyright: (c) 2016 by Oliver Goetz.
    :license: MIT, see LICENSE for more details.

CLASSES
    builtins.object
        DenonAVR
    
    class DenonAVR(builtins.object)
     |  Representing a Denon AVR Device.
     |  
     |  Methods defined here:
     |  
     |  __init__(self, host, name=None)
     |      Initialize MainZone of DenonAVR.      
     |      Variable definition:
     |      host: IP or HOSTNAME.
     |      name: string (Optional - otherwise FriendlyName of device is used).
     |  
     |  mute(self, mute)
     |      Mute receiver via HTTP get command.
     |  
     |  next_track(self)
     |      Send next track command to receiver command via HTTP post.
     |  
     |  power_off(self)
     |      Turn off receiver via HTTP get command.
     |  
     |  power_on(self)
     |      Turn off receiver via HTTP get command.
     |  
     |  previous_track(self)
     |      Send previous track command to receiver command via HTTP post.
     | 
     |  set_input_func(self, input_func)
     |      Set input_func of device.      
     |      Valid values depend on the device and should be taken from
     |      "input_func_list".
     |      Return "True" on success and "False" on fail.
     |	 
     |  toggle_play_pause(self)
     |      Toggle play pause media player.
     |  
     |  update(self)
     |      Get the latest status information from device.      
     |      Method queries device via HTTP and updates instance attributes.
     |      Returns "True" on success and "False" on fail.
     |  
     |  volume_down(self)
     |      Volume down receiver via HTTP get command.
     |  
     |  volume_up(self)
     |      Volume up receiver via HTTP get command.
     |  
     |  ----------------------------------------------------------------------
     |  Class methods defined here:
     |  
     |  get_status_xml(host, command) from builtins.type
     |      Get status XML via HTTP and return it as XML ElementTree.
     |  
     |  send_get_command(host, command) from builtins.type
     |      Send command via HTTP get to receiver.
     |  
     |  send_post_command(host, command, body) from builtins.type
     |      Send command via HTTP post to receiver.
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
     |  
     |  album
     |      Return album name of current playing media as string.
     |  
     |  artist
     |      Return artist of current playing media as string.
     |  
     |  band
     |      Return band of current radio station as string.
     |  
     |  frequency
     |      Return frequency of current radio station as string.
     |  
     |  image_url
     |      Return image URL of current playing media when powered on.
     |  
     |  input_func
     |      Return the current input source as string.
     |      &
     |      Setter function for input_func to switch input_func of device.	 
     |  
     |  input_func_list
     |      Return a list of available input sources as string.
     |  
     |  muted
     |      Boolean if volume is currently muted.      
     |      Return "True" if muted and "False" if not muted.
     |  
     |  name
     |      Return the name of the device as string.
     |  
     |  power
     |      Return the power state of the device.      
     |      Possible values are: "ON", "STANDBY" and "OFF"
     |  
     |  state
     |      Return the state of the device.     
     |      Possible values are: "on", "off", "playing", "paused"
     |      "playing" and "paused" are only available for input functions
     |      in PLAYING_SOURCES.
     |  
     |  station
     |      Return current radio station as string.
     |  
     |  title
     |      Return title of current playing media as string.
     |  
     |  volume
     |      Return volume of Denon AVR as float.      
     |      Volume is send in a format like -50.0.
     |      Minimum is -80.0, maximum at 18.0


