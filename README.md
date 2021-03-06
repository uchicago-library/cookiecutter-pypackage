# cookiecutter-pypackage [![v0.7.3](https://img.shields.io/badge/version-0.7.3-blue.svg)](https://github.com/uchicago-library/cookiecutter-pypackage/releases)

[![Build Status](https://travis-ci.org/uchicago-library/cookiecutter-pypackage.svg?branch=master)](https://travis-ci.org/uchicago-library/cookiecutter-pypackage)

My [cookiecutter](https://github.com/audreyr/cookiecutter) template for python packages

# Whats it get me?
- [Github](https://github.com/) integration
- [TravisCI](https://travis-ci.org/) integration
- [Coveralls](https://coveralls.io/) integration
- (optional) [Sphinx](http://www.sphinx-doc.org) documentation
    - With a minimal autodocs setup
    - Ready for use with [readthedocs](https://readthedocs.org/)
- A minimal README
- A virtual environment (python >= 3.3)
- Packages for common development tasks
    - [pip](https://pip.pypa.io/en/latest/)
    - [bumpversion](https://github.com/peritus/bumpversion)
    - [wheel](http://pythonwheels.com/)
    - [flake8](http://flake8.pycqa.org/en/latest/)
    - [coverage](https://coverage.readthedocs.io/en/coverage-4.4.1/)
    - [pytest](https://docs.pytest.org/en/latest/)
    - [twine](https://pypi.python.org/pypi/twine)
    - [check-manifest](https://github.com/mgedmin/check-manifest)

# Quickstart

- Requirements For These Instructions
    - [Cookiecutter](https://github.com/audreyr/cookiecutter)
    - [Github](https://github.com/) account
    - [TravisCI](https://travis-ci.org/) account
    - [Coveralls](https://coveralls.io/) account
    - [readthedocs](https://readthedocs.org/) account
- Steps
    - Create a github repo named $YOUR_PROJECT_NAME
    - Enable repository monitoring on Travis
    - Enable repository monitoring on coveralls
    - Enable repository monitoring on readthedocs
    - ```$ cookiecutter https://github.com/uchicago-library/cookiecutter-pypackage```
    - Fill in the prompts
    - ```$ cd $YOUR_PROJECT_NAME```
    - ```$ source venv/bin/activate```
        - if python < 3.3 create your own venv here
    - ```$ pip install -r requirements_dev.txt```
    - ```$ git init```
    - ```$ git add */.*```
    - ```$ git commit -m "first commit"```
    - ```$ git remote add origin $YOUR_REPO_ADDRESS```
    - ```$ git push -u origin master```
    - Begin developing your package!

# Functionalities

Any of the following can be run off the bat from the project root

* ```./quick_test.sh```: Run tests, generate coverage stats, run flake8
* ```py.test```: Run tests
* ```bumpversion $PART```: Bump the version number of the project
    * ```git push && git push --tags``` to upload/release to git
* ```autopep8 .```: Automatically fix some pep8 errors
* ``` check-manifest .```: Check that your manifest file is correct
    * the ```-c``` option will create one, if it doesn't exist
    * the ```-u``` option will update an existing file, or create one

## Uploading to pypi

I'll not hazard a short answer here, as there are too many options.

[This](https://hynek.me/articles/sharing-your-labor-of-love-pypi-quick-and-dirty/) blog
entry provides a good breakdown of uploading a package to pypi. All of the referenced
tools should be installed by a ```pip -r requirements_dev.txt``` in your project
virtualenv.

Inspiration (and some code) taken from [audreyr's pypackage template](https://github.com/audreyr/cookiecutter-pypackage)
