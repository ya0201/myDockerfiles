FROM chainer/chainer:latest-python3
MAINTAINER me <me@abc.com>

# working directory
# mount application root directory on here (/app)
RUN mkdir /app
WORKDIR /app

# installation of git
RUN apt-get update && apt-get -y install git

# installation of requirements
RUN pip3 install numpy
RUN pip3 install librosa
RUN pip3 install pysptk
RUN pip3 install pyworld
RUN pip3 install fastdtw
RUN pip3 install nnmnkwii
RUN pip3 install matplotlib
RUN pip3 install chainerui

# installation of world4py
RUN git clone https://github.com/yamachu/WORLD4py.git
RUN cd WORLD4py
RUN python3 setup.py install
RUN cd ../ && rm -rf WORLD4py

# the default command that runs when docker container starts
CMD echo "This is become-yukarin docker image..."
# CMD ["python", "train.py"]
