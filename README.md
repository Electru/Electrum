Electrum - Lightweight Bitcoin client
Licence: MIT Licence
Author: Thomas Voegtlin
Language: Python (>= 3.6)
Homepage: https://electrum.org/
Build Status Test coverage statistics Help translate Electrum online
Getting started
(If you've come here looking to simply run Electrum, you may download it here.)

Electrum itself is pure Python, and so are most of the required dependencies, but not everything. The following sections describe how to run from source, but here is a TL;DR:

sudo apt-get install libsecp256k1-0
python3 -m pip install --user .[gui,crypto]
Not pure-python dependencies
If you want to use the Qt interface, install the Qt dependencies:

sudo apt-get install python3-pyqt5
For elliptic curve operations, libsecp256k1 is a required dependency:

sudo apt-get install libsecp256k1-0
Alternatively, when running from a cloned repository, a script is provided to build libsecp256k1 yourself:

sudo apt-get install automake libtool
./contrib/make_libsecp256k1.sh
Due to the need for fast symmetric ciphers, either one of pycryptodomex or cryptography is required. Install from your package manager (or from pip):

sudo apt-get install python3-cryptography
If you would like hardware wallet support, see this.

Running from tar.gz
If you downloaded the official package (tar.gz), you can run Electrum from its root directory without installing it on your system; all the pure python dependencies are included in the 'packages' directory. To run Electrum from its root directory, just do:

./run_electrum
You can also install Electrum on your system, by running this command:

sudo apt-get install python3-setuptools python3-pip
python3 -m pip install --user .
This will download and install the Python dependencies used by Electrum instead of using the 'packages' directory. It will also place an executable named electrum in ~/.local/bin, so make sure that is on your PATH variable.

Development version (git clone)
Check out the code from GitHub:

git clone git://github.com/spesmilo/electrum.git
cd electrum
git submodule update --init
Run install (this should install dependencies):

python3 -m pip install --user -e .
Create translations (optional):

sudo apt-get install python-requests gettext
./contrib/pull_locale
Finally, to start Electrum:

./run_electrum
Creating Binaries
Linux (tarball)
See contrib/build-linux/sdist/README.md.

Linux (AppImage)
See contrib/build-linux/appimage/README.md.

Mac OS X / macOS
See contrib/osx/README.md.

Windows
See contrib/build-wine/README.md.

Android
See contrib/android/Readme.md.
