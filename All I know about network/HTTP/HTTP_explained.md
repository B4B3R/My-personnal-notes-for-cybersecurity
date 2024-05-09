
- Hyper Text Transfer Protocol
- Ce protocole sert principalement à échanger des images, du texte, des vidéos et bien plus par le biais de fichiers html.
- Pour que ce protocole puisse fonctionner, il nous faut un client et un serveur (on peut aussi rajouter des proxies qui serviront d'intermédiares entre le client et le serveur)
![[client_serveur_requete.jpg]]
- Vous entrer une url dans votre navigateur qui utilise le protocole http = votre navigateur (le client) viens d'envoyer une requête HTTP pour avoir que le serveur vous donne accès à une ressource spécifique.
- Il est important de préciser que le client doit envoyer une demande HTTP séparée pour chaque ressource requise. (Plus le site contiendra des ressources, plus le temps de chargement augmentera en conséquence)

# Il existe plusieurs types de requêtes HTTP :
### GET 
--> "obtenir", demande de ressource
### HEAD
--> données d'en-tête du fichier demandées
### POST
-->  

# Inside an HTTP response

- an HTTP status code
- HTTP response headers
- optional HTTP body
# status code HTTP

- 1xx Informational
- 2xx Success
- 3xx Redirection
- 4xx Client Error
- 5xx Server Error



#### Sources:
- http.dev
- 