# PACKAGES IN PYTHON
![Alt text](https://miro.medium.com/max/580/0*Kt5_0uGLlCFAgbt6.png "a title")

## Defination
*Packages are a way of structuring many packages and modules which helps in a well-organized hierarchy of data set, making the directories and modules easy to access. Just like there are different drives and folders in an OS to help us store files, similarly packages help us in storing other sub-packages and modules, so that it can be used by the user when necessary.*
![Alt text](https://www.tutorialsteacher.com/Content/images/python/package.png "a title")
## Creating of Packages
**Create a new folder named D:\MyApp.
Inside MyApp, create a subfolder with the name 'mypackage'.
Create an empty __init__.py file in the mypackage folder.
Using a Python-aware editor like IDLE, create modules greet.py and functions.py**
![Alt text](https://media.geeksforgeeks.org/wp-content/uploads/Python-Packages.jpg "a title")
## CODING 
**1.Then we need to create modules.**
**2. To do this we need to create a file with the name Bmw.py and create its content by putting this code into it**
# Python code to illustrate the Modules
class Bmw:
	# First we create a constructor for this class
	# and add members to it, here models
	def __init__(self):
		self.models = ['i8', 'x1', 'x5', 'x6']

	# A normal print function
	def outModels(self):
		print('These are the available models for BMW')
		for model in self.models:
			print('\t%s ' % model)
**Then we create another file with the name Audi.py and add the similar type of code to it with different members.**
![Alt text](https://media.geeksforgeeks.org/wp-content/uploads/20191226170910/python-packages1.png "a title")
# Python code to illustrate the Module
class Audi:
	# First we create a constructor for this class
	# and add members to it, here models
	def __init__(self):
		self.models = ['q7', 'a6', 'a8', 'a3']

	# A normal print function
	def outModels(self):
		print('These are the available models for Audi')
		for model in self.models:
			print('\t%s ' % model)
**Then we create another file with the name Nissan.py and add the similar type of code to it with different members.**		

# Python code to illustrate the Module
class Nissan:
	# First we create a constructor for this class
	# and add members to it, here models
	def __init__(self):
		self.models = ['altima', '370z', 'cube', 'rogue']

	# A normal print function
	def outModels(self):
		print('These are the available models for Nissan')
		for model in self.models:
			print('\t%s ' % model)
from Bmw import Bmw
from Audi import Audi
from Nissan import Nissan
![Alt text](https://i.ytimg.com/vi/vM3ScLNTGoQ/maxresdefault.jpg "a title")
**3.Finally we create the __init__.py file. This file will be placed inside Cars directory and can be left blank or we can put this initialisation code into it.**
# Import classes from your brand new package
from Cars import Bmw
from Cars import Audi
from Cars import Nissan
**Now, let’s use the package that we created. To do this make a sample.py file in the same directory where Cars package is located and add the following code to it:**
# Create an object of Bmw class & call its method
ModBMW = Bmw()
ModBMW.outModels()

# Create an object of Audi class & call its method
ModAudi = Audi()
ModAudi.outModels()

# Create an object of Nissan class & call its method
ModNissan = Nissan()
ModNissan.outModels()

# import in Packages

**Suppose the cars and the brand directories are packages. For them to be a package they all must contain __init__.py file in them, either blank or with some initialization code. Let’s assume that all the models of the cars to be modules. Use of packages helps importing any modules, individually or whole.
Suppose we want to get Bmw i8
SYNTAX:-'import' Cars.Bmw.x5
While importing a package or sub packages or modules, Python searches the whole tree of directories looking for the particular package and proceeds systematically as programmed by the dot operator.
If any module contains a function and we want to import that
Example :- a8 has a function get_buy(1) and we want to import that
Syntax:-import Cars.Audi.a8
Cars.Audi.a8.get_buy(1)**
![Alt text](https://files.realpython.com/media/imports-colab-pip_importer.9d9fd1760f1b.png "a title")
# ‘from…import’ in Packages

**Now, whenever we require using such function we would need to write the whole long line after importing the parent package. To get through this in a simpler way we use ‘from’ keyword. For this we first need to bring in the module using ‘from’ and ‘import’
from Cars.Audi import a8
Now we can call the function anywhere using
a8.get_buy(1)
There’s also another way which is less lengthy. We can directly import the function and use it wherever necessary. First import it using:There’s also another way which is less lengthy. We can directly import the function and use it wherever necessary. First import it using:
from Cars.Audi.a8 import get_buy
Now call the function from anywhere:
get_buy(1)**
