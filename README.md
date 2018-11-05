# avaya-sip
Tips for connecting Avaya 96xx phones in a 3rd party call control environment

This repository contains a sample 46xxsettings.txt file to connect Avaya 96xx phones to a PBX via a SIP proxy.  It also contains a Kamailio SIP proxy configuration file.

My reason for creating this SIP proxy configuration file is that when Avaya 96xx phones are connected to a PBX in "SIPPING 19" mode as they call it, they don't properly display caller name information.  This proxy configuration file adds the P-Asserted-Identity header to INVITEs sent to the phone and INVITE replies sent to the phone so that the user can see who is calling or who they called (the who they called part only works for 3CX PBX in my configuration file).
