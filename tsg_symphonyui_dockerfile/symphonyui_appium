FROM appium/appium
MAINTAINER GLU-TSGQA

USER root

RUN apt update && apt dist-upgrade -y
RUN apt install -y --no-install-recommends \
        git cmake build-essential \
    && rm -rf /var/lib/apt/lists/*
RUN npm i -g opencv4nodejs --allow-root --unsafe-perm=true

CMD [ "appium", "--relaxed-security" ] # for adb shell

EXPOSE 4723