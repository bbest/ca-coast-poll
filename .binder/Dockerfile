FROM rocker/binder:3.6.0
LABEL maintainer='Ben Best'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/bbest/ca-coast-poll/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-11-04/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
