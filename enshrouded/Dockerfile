#####################################################
# Strombachs Game Server                            #
#####################################################

FROM ubuntu:24.04

ARG PUID=5000

ENV USER=steam
ENV HOMEDIR="/home/${USER}"
ENV STEAMCMDDIR="${HOMEDIR}/steamcmd"

RUN apt-get update \
    && apt-get install -y lib32gcc-s1 curl vim \
    && useradd -u "${PUID}" -m -d "${HOMEDIR}" "${USER}" \
    && su "${USER}" -c "mkdir -p \"${STEAMCMDDIR}\""

WORKDIR ${STEAMCMDDIR}
USER steam
