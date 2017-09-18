FROM okdocker/nginx:mainline

ADD entrypoint.sh /entrypoint
ADD etc/nginx /etc/nginx
ADD var/www /var/www

ENTRYPOINT [ "/bin/bash", "/entrypoint" ]
CMD []
