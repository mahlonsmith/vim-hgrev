PLUGIN = hgrev

SOURCE =  plugin/hgrev.vim
SOURCE += doc/hgrev.txt

${PLUGIN}.vba: ${SOURCE}
	- vim --cmd 'let g:plugin_name="${PLUGIN}"' -S build.vim -cq\!
	gzip ${PLUGIN}.vba

install:
	rsync -Rv ${SOURCE} ${HOME}/.vim/

clean:
	rm ${PLUGIN}.vba.gz
