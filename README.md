# Using modules globally

If you want to use packages for your self you need to install your package with `pip install`. Then you can simply write `import my_package` and use all the functionallity from your package.

# Installing the package

Open the terminal in the root folder of the project and type `pip install .`. This line will look for the `setup.py` and afterwards install the package in you package registry.

# Uploading package to PyPi
Navigate to the folder with your `setup.py` and open the terminal. Inside the terminal type `python setup.py sdist`. A new folder `dist` will appear with a `*.tar.gz` file. In order to upload your package to PyPi you will have to install the `twine` package via `pip install twine`. 

## Upload to test PyPi
Open the terminal and type `twine upload --repository-url https://test.pypi.org/legacy/ dist/*` after running this command you will have to provide your PyPi credentials.

## Upload to PyPi
Open the terminal and type `twine upload dist/*` after running this command you will have to provide your PyPi credentials.
