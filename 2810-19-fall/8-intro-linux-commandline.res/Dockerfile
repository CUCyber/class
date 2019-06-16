FROM ubuntu:18.04

RUN useradd -m -s /bin/bash cucyber
RUN mkdir -p /home/cucyber/hello/world/
RUN mkdir -p /home/cucyber/.super_secrets/
RUN echo "2810{f1rst_message!}" >/home/cucyber/first_file
RUN echo "2810{message_deux}" >/home/cucyber/hello/world/second_file
RUN echo "2810{tres_three_tres}" >/home/cucyber/.third_file
RUN echo "2810{fer_is_lonely}" >/home/cucyber/.super_secrets/fourth_file
RUN echo "2810{fifth_isnt_here_long}" >/tmp/fifth_file
RUN echo "2810{six_log_successful}" >/var/log/sixth_file

USER cucyber
WORKDIR /home/cucyber


