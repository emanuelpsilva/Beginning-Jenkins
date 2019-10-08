install:
	virtualenv testing
	. testing/bin/activate
	pip install --user -r requirements.txt

jenkins_test:
	ls -la testing/bin
	testing/bin/nosetests app/ -v
