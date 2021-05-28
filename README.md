
# CarRecon
#### Semester 4 Eksamens Projekt CPH Business Lyngby 2021
#### By Nicolas (cph-na157), Andreas (cph-aa344), Christoffer (cph-cf161) and Benjamin(cph-bc105)
This is a proof of concept. With this module, you are able to take a jpg file of a car, the module will then guess witch car, is in the picture, and find similar cars on the website https://www.bilbasen.dk/. The module will return a printed list of cars, that has been scraped from the website, with some data of the price, year of production and mileage. on top of that, it will return a plot, that shows the median price and mileage per production year.

### Technologies:
	 - Keras
	 - Selinium
	 - Beautifulsoup4
	 - pyplot
	 - numpy
	 - glob
	 - cv2
	 - random
	 - requests
	 - time
	 - os
	 - pandas

### How to install:
This project was created within the python environment that the teacher gave out the first week of this semester:
https://github.com/Hartmannsolution/docker_notebooks/
Install docker engien and use "docker-compose up --build"  in the root of the project above after you have cloned it.
Clone CarRecon in to the directory "notebooks". Everything should work as intended, since the dockerfile, from docker_notebooks, will handle the installation of the above mentioned technologies.

### User Guide:
Install the project as mentioned above.
located the CarRecon module 
Use the predict function on a jpg image, witch will return a string of what the guessed car was. Use this return value on the function find_car, witch will then scrape https://www.bilbasen.dk/, for any cars similar to the one guessed. find_car wil return a pandas dataframe with price, year and mileage. This dataframe can then be used on the statistic_data function, which will return a plot of the price and mileage median per production year


### Status:
At this stage, the module is able to predict 2 cars, Audi R8 and Fiat 500, with an accuracy of 75%. Further more, the module prints only: the price, production year, and mileage. This model, will not scrape all cars from https://www.bilbasen.dk/, since they use different names for their div tags, depending on witch page you are on.

### list of challenges:
One of the main challenges we had with this project, was to get the best accuracy we could get, with the knowledge and processing power we had available, out of the CNN. The model has a lot of space for improvement, but for a proof of concept, we found that this model was more then okay for the task.
An other big challenge we had with the project, was the scrapping part. We had to come up with a little "workaround", do to buttons being behind div- or p tags




