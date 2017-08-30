## Usage

To build, form this directory type:

`docker build -t brainhack101/scratch-the-dura .`

To run, from any directory type:

`docker run -ti -p 8888:8888 brainhack101/scratch-the-dura`

After running, it will print a url to your console, which you should copy and paste into your web browser
to enter a Jupyter interface. There will be no notebooks there, but you can (should) add one!

In order to mount your data so that it's available within Docker, instead run with the command:

`docker run -ti -v /path/to/my/data:/home/brainhacker/data -p 8888:8888 brainhack101/scratch-the-dura`

where you replace `/path/to/my/data` with the folder of your dataset on your computer.


## Examples 

- [BIDS App with continuous integration, version control, and docker hub](https://github.com/BIDS-Apps/ndmg)
