# War Driving Pi

This script is used for automating runing the kismet_server and kismet_client. You will need to have installed and configure kismet.  I specifically created this script to go along with a project I am working on "wardrivingpi".  You can find my article on how to build a wardrivingpi at https://jeremymdyson.wordpress.com/2016/10/21/building-a-war-driving-pi/. 

## Installation

1. Download the zip file
2. Extract the zip file

## Usage

getting the help menu: 

./wardrivingpi - h

displays:

Usage: sudo wardrivingpi -i <interface> [options]  
    -h, --help                       Prints this help page  
    -V, --Version                    Displays version and date of release   
    -C, --check-system               check to see current system setting for kismet  
    -i, --interface=Interface        Interface   
    -p, --prefix=Prefix              log file prefix   
    -c, --client                     Start the Kismet client   

---------------------------------------------------------------------------------------------------
Checking your current system stat for kismet

./wardrivingpi -C

displays:

Checking the kismet.conf files current ncsource setting
Current ncsource is: ncsource=wlan1

Getting WiFi Intfaces.
Your WiFi interfaces are:
["wlx", "wlp2s0"]

Checking to see if any interfaces are in monitor mode:
There are currently no WiFi interfaces in monitor mode.

---------------------------------------------------------------------------------------------------
Starting with just the kismet_server (no client gui), everything will run in the background

sudo ./wardrivingpi -i <interface> 
example: sudo ./wardrivingpi -i wlx

displays:

Interface wlx is now in monitor mode.


The kismet.conf file has been updated with the correct ncsource.


Kismet_server is now running as a background job! PID=2563

----------------------------------------------------------------------------------------------------
Starting kismet with the client cmd gui

sudo ./wardrivingpi -i <interface> -c
example: sudo ./wardrivingpi -i wlx -c

displays:

The Kismet client gui will be loaded in the terminal window.  You might be prompted to say "ok" to a couple of warnings.  You can check the checkbox to not show the warning again.
 
## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

TODO: Write history

## Credits

TODO: Write credits

## License

TODO: Write license
