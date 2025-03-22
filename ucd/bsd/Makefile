
all: UTF-8

UTF-8-EAW-FULLWIDTH: map.UTF-8 width.txt LC_CTYPE.C.UTF-8
	localedef -U -c -w ../../dist/UTF-8-EAW-FULLWIDTH-BSD.width.txt -f ./map.UTF-8 -i ./LC_CTYPE.C.UTF-8 ./UTF-8-EAW-FULLWIDTH

UTF-8-EAW-CONSOLE: map.UTF-8 width.txt LC_CTYPE.C.UTF-8
	localedef -U -c -w ../../dist/UTF-8-EAW-CONSOLE-BSD.width.txt -f ./map.UTF-8 -i ./LC_CTYPE.C.UTF-8 ./UTF-8-EAW-CONSOLE

map.UTF-8:
	curl -L -o $@ https://raw.githubusercontent.com/freebsd/freebsd-src/361a8395f0b0e6f254fd138798232529679d99f6/tools/tools/locale/etc/final-maps/map.UTF-8

width.txt:
	curl -L -o $@ https://raw.githubusercontent.com/freebsd/freebsd-src/361a8395f0b0e6f254fd138798232529679d99f6/tools/tools/locale/etc/final-maps/widths.txt

LC_CTYPE.C.UTF-8:
	curl -L -o $@ https://raw.githubusercontent.com/freebsd/freebsd-src/361a8395f0b0e6f254fd138798232529679d99f6/share/ctypedef/C.UTF-8.src
