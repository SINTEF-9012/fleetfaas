from tensorflow/tensorflow:2.4.0

WORKDIR /opt
COPY . .

ENV TZ=Europe/Oslo
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update && \
    apt-get install -y python3-opencv
    
RUN pip install keras==2.4.3 numpy==1.19.3 pillow==7.0.0 scipy==1.4.1 h5py==2.10.0 matplotlib==3.3.2 opencv-python keras-resnet==0.2.0 && \
    pip install imageai --upgrade

ENTRYPOINT python run.py 
