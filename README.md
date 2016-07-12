quartus-linux-install: Altera Quartus II Web Edition linux batch installation scripts
=====================================================================================

Download Quartus 13.1 or Quartus 15.0 installation files
from https://www.altera.com/downloads/download-center.html
into Quartus-13.1 or Quartus-15.0 subdir respectively.

Check your Quartus installation files. E.g.:

    $ cd quartus-linux-install/Quartus-13.1
    Quartus-13.1 $ md5sum -c MD5SUMS
    arria_web-13.1.0.162.qdz: OK
    cyclonev-13.1.0.162.qdz: OK
    cyclone_web-13.1.0.162.qdz: OK
    max_web-13.1.0.162.qdz: OK
    ModelSimSetup-13.1.0.162.run: OK
    QuartusSetup-13.1.4.182.run: OK
    QuartusSetupWeb-13.1.0.162.run: OK

Install ```expect```:

    # apt-get install expect


Install i386 support for Debian amd64:

    # dpkg --add-architecture i386
    # apt-get update
    # apt-get install libc6:i386
    # apt-get install libpng12-0:i386
    # apt-get install libfreetype6:i386
    # apt-get install libsm6:i386
    # apt-get install libxrender1:i386
    # apt-get install libfontconfig1:i386
    # apt-get install libxext6:i386
    # apt-get install libxtst6:i386


Install Quartus 13.1.4:

    Quartus-13.1 # ./install-quartus-13.1.4.182.exp /opt/altera/13.1

Install Quartus 15.0:

    Quartus-15.0 # ./install-quartus-15.0.2.153.exp /opt/altera/15.0
