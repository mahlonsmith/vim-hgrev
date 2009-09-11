PLUGIN = glimpse

SOURCE  = doc/glimpse.txt
SOURCE += plugin/glimpse.vim

${PLUGIN}.vba: ${SOURCE}
	- vim --cmd 'let g:plugin_name="${PLUGIN}"' -S build.vim -cq\!
	gzip ${PLUGIN}.vba

install:
	rsync -Rv ${SOURCE} ${HOME}/.vim/

clean:
	rm ${PLUGIN}.vba.gz
