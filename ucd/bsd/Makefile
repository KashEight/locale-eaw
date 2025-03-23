.PHONY: setup
setup:
	mkdir -p /usr/local/share/locale/ja_JP.UTF-8

.PHONY: UTF-8-EAW-FULLWIDTH
UTF-8-EAW-FULLWIDTH: setup map.UTF-8 width.txt LC_CTYPE.C.UTF-8
	localedef -U -c -w ../../dist/UTF-8-EAW-FULLWIDTH-BSD.width.txt -f ./map.UTF-8 -i ./LC_CTYPE.C.UTF-8 ./UTF-8-EAW-FULLWIDTH
	chmod 755 ./UTF-8-EAW-FULLWIDTH/LC_CTYPE
	cp ./UTF-8-EAW-FULLWIDTH/LC_CTYPE /usr/local/share/locale/ja_JP.UTF-8/

.PHONY: UTF-8-EAW-CONSOLE
UTF-8-EAW-CONSOLE: setup map.UTF-8 width.txt LC_CTYPE.C.UTF-8
	localedef -U -c -w ../../dist/UTF-8-EAW-CONSOLE-BSD.width.txt -f ./map.UTF-8 -i ./LC_CTYPE.C.UTF-8 ./UTF-8-EAW-CONSOLE
	chmod 755 ./UTF-8-EAW-CONSOLE/LC_CTYPE
	cp ./UTF-8-EAW-CONSOLE/LC_CTYPE /usr/local/share/locale/ja_JP.UTF-8/

.PHONY: map.UTF-8
map.UTF-8:
	curl -sSL -o $@ https://raw.githubusercontent.com/freebsd/freebsd-src/361a8395f0b0e6f254fd138798232529679d99f6/tools/tools/locale/etc/final-maps/map.UTF-8

.PHONY: width.txt
width.txt:
	curl -sSL -o $@ https://raw.githubusercontent.com/freebsd/freebsd-src/361a8395f0b0e6f254fd138798232529679d99f6/tools/tools/locale/etc/final-maps/widths.txt

LC_CTYPE.C.UTF-8:
	curl -sSL -o $@ https://raw.githubusercontent.com/freebsd/freebsd-src/361a8395f0b0e6f254fd138798232529679d99f6/share/ctypedef/C.UTF-8.src

.PHONY: clean
clean:
	rm /usr/local/share/locale/ja_JP.UTF-8/LC_CTYPE
	rm -rf UTF-8-EAW-FULLWIDTH
	rm -rf UTF-8-EAW-CONSOLE
	rm -f map.UTF-8
	rm -f width.txt
	rm -f LC_CTYPE.C.UTF-8
