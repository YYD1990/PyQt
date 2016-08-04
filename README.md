# PyQt
安装PyQt5的流程
  1. 下载 PyQt5 source http://www.riverbankcomputing.co.uk/software/pyqt/download5  ,
     sip source http://www.riverbankcomputing.co.uk/software/sip/download  ,
     Qt5 http://qt-project.org/downloads  
  2. 安装 sip 
     tar -zxvf sip-4.16.3.tar.gz
     cd sip-4.16.3
     python configure.py
     make
     sudo make install
   3.安装Qt5
   4.安装Pyqt5
    tar -zxvf PyQt-gpl-5.3.2.tar.gz
    cd PyQt-gpl-5.3.2
    sudo python configure.py -q /Users/boteng/Qt/5.3/clang_64/bin/qmake -d         /Library/Python/2.7/site-packages/ --sip             /System/Library/Frameworks/Python.framework/Versions/2.7/bin/sip --verbose
问题
Project ERROR: Could not resolve SDK path for 'macosx10.8'
解决办法
~/Qt/5.3/clang_64/mkspecs/qdevice.pri



change the following line:

!host_build:QMAKE_MAC_SDK = macosx10.8
to this:

!host_build:QMAKE_MAC_SDK = macosx10.9


sip/QtPrintSupport/qprinter.sip:28:10: fatal error: 'qprinter.h' file not found
http://www.riverbankcomputing.com/pipermail/pyqt/2014-March/033970.html
最后还没找到如何修改

使用brew 安装  前提需要安装python 3
brew install -v pyqt5
Installing PyQt

You will need the latest version of Python(currently 3.3.3). Make sure this is installed and that you add the executable to the system path. This option is automatically available from within the installer.

