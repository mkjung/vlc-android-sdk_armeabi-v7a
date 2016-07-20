# vlc-android-sdk_armeabi-v7a
===============

VLC Android SDK armeabi-v7a for slimness

( from https://github.com/mrmaffen/vlc-android-sdk )

Get it via Maven Central
------------------------
Just add this dependency to your project and you're good to go.

<pre>dependencies {
    compile 'io.github.mkjung:vlc-android-sdk_armeabi-v7a:0.0.1'
}</pre>

Building the LibVLC Android SDK armeabi-v7a yourself
----------------------------------------

To build a fresh version of the LibVLC Android SDK armeabi-v7a,
please make sure that you have setup your machine correctly.
(You can ignore the steps after and including 'Building'):
https://wiki.videolan.org/AndroidCompile

Afterwards run this commands

```
mkdir -p ~/workspace && cd ~/workspace
git clone https://github.com/mkjung/vlc-android-sdk_armeabi-v7a.git
cd vlc-android-sdk_armeabi-v7a
./gradlew buildLibVlc
vim vlc-android/compile-libvlc.sh
'''
/NDKv # find 'NDKv'
change 11*) -> 11*|12*)
'''
wget -P vlc-android/vlc/contrib/tarballs https://ftp.gnu.org/gnu/nettle/nettle-3.2.tar.gz
./gradlew buildLibVlc
./gradlew assemble
```
