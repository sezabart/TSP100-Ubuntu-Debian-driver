This repo is to help others get a TSP100 thermal printer connected via USB working on Ubuntu / Debian Linux, and to be able to use it normally via CUPS.

### Install steps
1. Open a terminal and use `chmod -X star-cups-driver_3.15.0-2_amd64.deb` to allow execution of the .deb package.
2. Install the deb package by double clicking it or opening it in something like the App Center. It is not signed and so it will warn you of dangers. Proceed at own risk.
3. Make sure the printer is connected.
4. Navigate to `localhost:631` in your webbrowser to access CUPS. Administration > Add Printer, your TSP should show up at Local Printers, select it and continue. Give it a correct name, description and location. Continue and at the bottom select the .ppd file that is in this repo (if your printer is a TSP100, else find yours at your own risk). This should complete succesfully.
5. In your terminal use `sudo apt install libcups-dev` to install a necessary library.
6. Test it out! If you get cut-off result check the media size in the print settings, it should be 80*200mm and portrait.