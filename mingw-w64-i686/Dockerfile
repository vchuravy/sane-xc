FROM ubuntu:19.04
RUN sed -i "1s;^;deb mirror://mirrors.ubuntu.com/mirrors.txt disco main restricted universe multiverse\n;" /etc/apt/sources.list; \
    sed -i "1s;^;deb mirror://mirrors.ubuntu.com/mirrors.txt disco-updates main restricted universe multiverse\n;" /etc/apt/sources.list; \
    sed -i "1s;^;deb mirror://mirrors.ubuntu.com/mirrors.txt disco-backports main restricted universe multiverse\n;" /etc/apt/sources.list; \
    sed -i "1s;^;deb mirror://mirrors.ubuntu.com/mirrors.txt disco-security main restricted universe multiverse\n;" /etc/apt/sources.list;
RUN dpkg --add-architecture i386
RUN apt-get update -y 

RUN apt-get -y install make cmake git m4 python perl wget patch pkg-config build-essential vim

ENV WINEARCH=win32
RUN apt-get -y install gcc-mingw-w64-i686 gfortran-mingw-w64-i686 g++-mingw-w64-i686 wine32 
RUN apt-get -y install winbind
RUN update-alternatives --set i686-w64-mingw32-g++ /usr/bin/i686-w64-mingw32-g++-posix; \
    update-alternatives --set i686-w64-mingw32-gcc /usr/bin/i686-w64-mingw32-gcc-posix; \
    update-alternatives --set i686-w64-mingw32-gfortran /usr/bin/i686-w64-mingw32-gfortran-posix;
RUN wine reg add HKCU\\Environment /v PATH /d "z:\\usr\\i686-w64-mingw32\\bin" /f
