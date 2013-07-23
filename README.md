=========

To compile vim with python, ruby, perl support you can follow these steps below. First we need to get the dependencies:

      sudo apt-get install libncurses5-dev libgnome2-dev libgnomeui-dev \
      libgtk2.0-dev libatk1.0-dev libbonoboui2-dev \
      libcairo2-dev libx11-dev libxpm-dev libxt-dev python-dev ruby-dev mercurial

You now have the dependencies installed, you can get vim from mercurial and proceed with the installation

      cd ~
      hg clone https://code.google.com/p/vim/
      cd vim
      ./configure --with-features=huge \
            --enable-rubyinterp \
            --enable-pythoninterp \
            --enable-perlinterp \
            --enable-gui=gtk2 --enable-cscope --prefix=/usr
      make VIMRUNTIMEDIR=/usr/share/vim/vim73
      sudo make install
