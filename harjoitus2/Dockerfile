# lähtöimage, ns. base image
FROM ubuntu:24.04

# työhakemisto
WORKDIR /omadir

# päivitetään riippuvuudet ja asennetaan yt-dlp
RUN apt update && apt install -y curl python3 && \
 curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp && \
 chmod a+rx /usr/local/bin/yt-dlp && \
 useradd -m appuser && chown -R appuser . && \
 apt clean && apt purge -y --auto-remove curl && \
 rm -rf /var/lib/apt/lists/*
USER appuser


# ylikirjoitetaan käynnistys komento
ENTRYPOINT ["/usr/local/bin/yt-dlp"]

# CMD ["https://youtube.com/shorts/vIoo7rvXO7s?si=YusFm3TiWrwByDaN"]