FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y apache2

#after executing the apache2ctl command, replace this bash with bash. 
#So that we dont havan un necessary bash ancestry
RUN echo '#!bin/sh \n apache2ctl start \n exec /bin/sh' > startup.sh
RUN chmod a+x startup.sh

EXPOSE 80
CMD []

ENTRYPOINT ["./startup.sh"]
