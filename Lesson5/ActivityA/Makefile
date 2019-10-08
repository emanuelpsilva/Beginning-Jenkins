install:
	virtualenv testing
	. testing/bin/activate
	pip install --user -r requirements.txt

jenkins_test:
	python `which nosetests`
	testing/bin/nosetests app/ -v
