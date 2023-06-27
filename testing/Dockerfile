# Verwende das Basis-Image mit einer GUI-Umgebung
FROM ubuntu:latest

# Installiere die erforderlichen Pakete für Thunderbird und die GUI-Unterstützung
RUN apt-get update && apt-get install -y \
    thunderbird \
    dbus-x11 \
    x11-xserver-utils \
    mesa-utils \
    xvfb

# Setze die Umgebungsvariablen für die GUI-Unterstützung
ENV DISPLAY=:0

# Starte den X-Server und Thunderbird
CMD sh -c "Xvfb $DISPLAY -screen 0 1024x768x16 & sleep 5 && dbus-launch thunderbird"

