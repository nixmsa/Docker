FROM oraclelinux:7-slim
LABEL maintainer="nixmsa@gmail.com"
ARG ORACLE_HOME=/u01/app/oracle/prod/12.2.0.1/db_1
ARG DATA_LOCATION=/u02/oradata 

ENV ORACLE_HOME=${ORACLE_HOME} \
    DATA_LOCATION=${DATA_LOCATION} 

#RUN mkdir -p /u01/app/oracle && \
 #   mkdir -p /u02/oradata
RUN mkdir -p ${ORACLE_HOME} && \
    mkdir -p ${DATA_LOCATION}
