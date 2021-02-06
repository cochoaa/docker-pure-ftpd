FROM stilliard/pure-ftpd
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 
RUN localedef -i es_PE -c -f UTF-8 -A /usr/share/locale/locale.alias es_PE.UTF-8
ENV LANG es_PE.utf8
ENV TZ="America/Lima"
# e.g. you could change the defult command run:
CMD /run.sh -l puredb:/etc/pure-ftpd/pureftpd.pdb -E -j -R -P $PUBLICHOST