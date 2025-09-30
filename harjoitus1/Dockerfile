# Aloitetaan Alpine linux kuvasta
FROM alpine:3.21

# määritellään /usr/src/app työhakemistoksi, kaikki jatkossa olevat komennot suoritaan tässä hakemistossa
WORKDIR /usr/src/app

# kopioidaan hello.sh hostilta, työhakemistoon. Luoden /usr/src/app/hello.sh
COPY hello.sh .

# suoritetaan komento, käyttäen '/bin/sh -c' prefixiä.
RUN touch additional.txt

# Määrittelee aloituspisteen (start point / run point) docker containerille
CMD ./hello.sh

