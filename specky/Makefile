PLUGIN = specky

SOURCE =  syntax/rdoc.vim
SOURCE += syntax/specrun.vim
SOURCE += doc/specky.txt
SOURCE += plugin/specky.vim

${PLUGIN}.vba: ${SOURCE}
	vim --cmd 'let g:plugin_name="${PLUGIN}"' -s build.vim
	gzip ${PLUGIN}.vba

install:
	rsync -Rv ${SOURCE} ${HOME}/.vim/

clean:
	rm ${PLUGIN}.vba
