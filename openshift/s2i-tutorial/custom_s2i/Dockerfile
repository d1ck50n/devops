FROM node:12.18.2

EXPOSE 8080

RUN mkdir /app && chown -R 1001:1001 /app

COPY ./s2i/bin/ /usr/libexec/s2i
USER 1001

CMD ["/usr/libexec/s2i/usage"]
