CC=gcc
AFLAGS=-Wall -g
LDFLAGS= -lmysqlclient
OBJS= add.cgi del.cgi mod.cgi sel.cgi addscore.cgi selscore.cgi delscore.cgi modscore.cgi   addcourse.cgi selcourse.cgi modcourse.cgi delcourse.cgi addschool.cgi  selschool.cgi modschool.cgi delschool.cgi


all:$(OBJS)

$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)

.PHONY:clean
clean:
	rm ./*.cgi

install:
	cp *.cgi /usr/lib/cgi-bin/sx/
	cp *.html /usr/lib/cgi-bin/sx/
	sudo cp  *.html /var/www/html/

	sudo cp ~/github/cgi-stu/stu/index.html /var/www/html/index.html
	sudo cp ~/github/cgi-stu/stu/information.html /var/www/html/information.html
	sudo cp ~/github/cgi-stu/stu/score.html /var/www/html/score.html
	sudo cp ~/github/cgi-stu/stu/course.html /var/www/html/course.html
	sudo cp ~/github/cgi-stu/stu/student.html /var/www/html/student.html
	sudo cp ~/github/cgi-stu/stu/teacher.html /var/www/html/teacher.html
	sudo cp ~/github/cgi-stu/stu/ad.html /var/www/html/ad.html
