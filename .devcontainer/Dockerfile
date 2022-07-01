FROM eclipse-temurin:17-jdk

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update; \
  apt-get -y install locales dialog apt-utils man-db bc zsh zip unzip sudo vim git lsb-release curl httpie jq; \
  apt-get -y dist-upgrade; \
  echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; \
  locale-gen; \
  update-locale LANG=en_US.UTF-8; \
  apt-get autoremove -y; \
  apt-get clean -y; \
  rm -rf /var/lib/apt/lists/*

  ENV DEBIAN_FRONTEND=

  CMD ["/bin/bash"]
  