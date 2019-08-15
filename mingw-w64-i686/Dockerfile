FROM ubuntu:19.04
RUN dpkg --add-architecture i386
RUN apt-get update -y 
RUN apt-get -y install make cmake git m4 python perl wget patch pkg-config build-essential vim
RUN apt-get -y install gcc-mingw-w64-i686 gfortran-mingw-w64-i686 g++-mingw-w64-i686 wine32 
RUN update-alternatives --set i687-w64-mingw32-g++ /usr/bin/i686-w64-mingw32-g++-posix; update-alternatives --set i686-w64-mingw32-gcc /usr/bin/i686-w64-mingw32-gcc-posix; update-alternatives --set i686-w64-mingw32-gfortran /usr/bin/i686-w64-mingw32-gfortran-posix;  
RUN wine reg add HKCU\\Environment /v PATH /d "z:\\usr\\i686-w64-mingw32\\bin" /f
