FROM rocker/binder:3.5.1
LABEL maintainer='Steven Kambouris'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/stevekambouris/test-holepunched-ma/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2021-03-02/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
