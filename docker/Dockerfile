FROM bids/ndmg:v0.0.37-1
MAINTAINER Greg Kiar <gkiar@jhu.edu>

USER root

RUN pip install setuptools==33.1.1
RUN apt-get -y install python2.7 python-pip python-dev
RUN apt-get -y install ipython ipython-notebook git &&\
		pip install --upgrade pip
RUN pip install jupyter

RUN useradd -m -s /bin/bash sic-user

RUN pip install ndmg==0.0.39

RUN mkdir -p /home/sic-user/.jupyter
COPY jupyter_notebook_config.py /home/sic-user/.jupyter
COPY sic_ndmg.ipynb /home/sic-user
WORKDIR /home/sic-user

ENV TINI_VERSION v0.6.0
ADD https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini /usr/bin/tini
RUN chmod +x /usr/bin/tini
ENTRYPOINT ["/usr/bin/tini", "--"]

USER sic-user

EXPOSE 8888
CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0"]

