# Modifications TazDeck

Fork de https://github.com/Pink-Propeller/Spotify-DeskTHING, branche `tazdeck`. La branche `main` reste identique à l'original.

## Changements dans `SpotifyCarThing.ino`
- Fuseau horaire de Paris.
- Respect de la durée d'attente demandée par Spotify (jusqu'à 6 h) et affichage du temps restant. Le mécanisme de reprise n'annule plus un blocage en cours (seuil de 20 s porté à 45 s).
- Interrogation du lecteur : 3 s en lecture, 10 s en pause, 15 s avec l'écran de veille, aucune requête écran éteint. Un appui sur l'écran relance tout de suite.

## Raison
Le 25/11/2026, Spotify a bloqué l'application (erreur 429 `QUOTA_EXCEEDED`, attente de 8400 s). La carte envoyait environ 22 000 requêtes `/v1/me/player` par jour.

## À ne jamais publier
`SPOTIFY_CLIENT_ID` et `SPOTIFY_CLIENT_SECRET` restent aux valeurs d'exemple dans ce dépôt. Les vraies valeurs ne sont que dans la copie locale utilisée pour flasher.

## Licence
Aucune licence n'est affichée sur le dépôt d'origine : à vérifier avant de rendre ce fork public.
