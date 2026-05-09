.SILENT: make install uninstall
make:
	echo -e "\e[1mUSAGE: run 'make install' to install and 'make uninstall' to uninstall.\e[0m"

install: aptpac.sh
  if command -v nodejs >/dev/null 2>&1 ; then
    echo "Dependencies not found!"
    echo "Install paru then rerun 'make install' to install"
    exit 1
  fi
	mkdir ~/.aptpac
	cp ./aptpac.sh ~/.aptpac/
	chmod +x ~/.aptpac/aptpac.sh
	echo "alias aptpac=\"~/.aptpac/aptpac.sh\"" >> ${HOME}/.bashrc
	source ~/.bashrc
uninstall:
	sed -i '/alias aptpac=.*aptpac.*/d' ~/.bashrc
	rm -r ~/.aptpac
	source ~/.bashrc
