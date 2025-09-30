# lähtöimage, ns. base image
FROM ubuntu:24.04

# työhakemisto
WORKDIR /omadir

# päivitetään riippuvuudet ja asennetaan yt-dlp
RUN apt update && apt install -y curl python3
RUN curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp
RUN chmod a+rx /usr/local/bin/yt-dlp

# ylikirjoitetaan käynnistys komento
ENTRYPOINT ["/usr/local/bin/yt-dlp"]

# CMD ["https://youtube.com/shorts/vIoo7rvXO7s?si=YusFm3TiWrwByDaN"]