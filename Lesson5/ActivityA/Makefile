install:
	virtualenv testing
	. testing/bin/activate
	pip install --user -r requirements.txt

jenkins_test:
	#ls -la testing/bin
	find . -name "nose*"
	testing/bin/nosetests app/ -v
