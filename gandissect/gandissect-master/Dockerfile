#Follow Djordje's instructions in the emails
#You must pull a specific image. Run this command:
#docker pull pytorch/pytorch:2.2.0-cuda12.1-cudnn8-devel
#Make sure you have enough space on your computer! (18 GB ish)
#Then create image from this Dockerfile

#We have to use devel (developer), as it has compiler configured correctly
FROM pytorch/pytorch:2.2.0-cuda12.1-cudnn8-devel

#Install
RUN pip3 install matplotlib

RUN pip3 install scikit-image==0.19.3

RUN pip3 install scipy==1.11

RUN pip3 install IPython

RUN pip3 install Ninja

RUN pip3 install numpy==1.21.6

#Create a working directory.
RUN mkdir /app
WORKDIR /app

COPY ./client ./client
COPY ./client_dist ./client_dist
#COPY ./dataset ./dataset
COPY ./dissect ./dissect
#COPY ./doc ./doc
COPY ./models ./models
COPY ./netdissect ./netdissect
#COPY ./netdissect.egg-info ./netdissect.egg-info
#COPY ./script ./script

#Set the default command to python3.
#CMD ["python3", "./kopi_af_gandissect_solutions1.py", "./netdissect"]
CMD ["python3", "./netdissect"]

#in command prompt (Open wsl! Did not work in Command Prompt for me):
#docker run --rm --gpus=all -it --init --volume="$PWD:/app" colab1 python3 kopi_af_gandissect_solutions1.py
#docker run --rm --gpus=all -it --init --volume="$PWD:/app" blackbox python3 -m netdissect --gan --model "netdissect.proggan.from_pth_file('models/karras/livingroom_lsun.pth')" --outdir "dissect/livingroom" --layer layer1 layer4 layer7 --size 1000


#above will run kopi_af_gandissect_solutions1.py
#python -m netdissect --gan --model "netdissect.proggan.from_pth_file('models/karras/livingroom_lsun.pth')" --outdir "dissect/livingroom" --layer layer1 layer4 layer7 --size 1000
#the above command creates a container and runs the script,
#but '--rm' ensures that the container is deleted when done running
#unsure if this is better than letting the container exist but whatevs im tired