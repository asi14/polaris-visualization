## Inspiration


Our mission was to expand the nature in which we conveyed data by using various programming languages to create a user-friendly data visualization site. 




## What is it


Our webpage represents up to **50,000 data points** that appear on the paths several _Polaris_ test rides. We took these points and plotted them onto a unique map to show the path that a certain vehicle took over the earth. _Google Maps API_ combined with various code, allows the user to interact with the data by viewing all the paths taken over the course of these test rides. Using a **randomized method**, we are able  to generate different paths that correspond to the data we recieved. Each path includes various categories of information such as the starting position, the total time taken, and the total distance in metres. In addition to this, we have also included a **world-view map** that plots down different points to locate the average areas where these tests take place. These details capture the viewers' attention and provide them with the most important data in a straightforward, yet interesting visualization.



## Process

###Installation

This project requires, at a minimum, a working version of Python 3 with a Linux terminal. You'll also require a JSON dataset from Polaris.

1. `git clone` the repository into a location of your choice.
2. `python -m venv environ` in a directory of your choice
3. `source /path/to/environ/bin/activate` to activate virtual environment
4. `cd` into `polaris-visualization` and run `pip install -r requirements.txt` to install required dependencies
5. `cd` into `polaris` folder (a.k.a. Django folder) and run `python manage.py migrate` to create DB tables
6. `python manage.py runserver` to start project. Go to `http//127.0.0.1:8000` to see website. 

### Dependencies

Follow `requirements.txt`. The software package `RabbitMQ` is also required. Follow your own operating system's instructions for installing RabbitMQ.
Note that due to restrictions with Celery, this repository supports only Linux.

## Challenges


Throughout our process, we encountered many different challenges that eventually changed our end result. But, our main issue was the amount of data that was given to us to place in our site. Each time the randomizer scanned through the data, about 5 minutes was needed to load the page. Not only this, but the JSON file that was associated with this data was too large for the code to process. In the end, we realized the correct method of placing _chunks_ into our code and decided to place a loading bar into our screen during the waiting time that is experienced by the user.



## Accomplishments
During this project, we...


* broke down a large data set into smaller pieces, to allow the computer to scan through the data at a reasonable rate

* used Google Maps API to get the nearby names of cities (those that lie close to our plotted points) 

* implemented a Django to host and distribute an analysis of our data



## Learning

During this project, we learnt...


* how to use **Reverse Geo-Encoding** (recognition of nearby cities using latitude and longitude)




## Materials & Contributing

This project was built with a Pandas & Django backend and a Bootstrap & Google Maps API frontend.
If you wish to contribute, please submit an issue.












