# Docker Networking Lab
## Co zrobiłem
 Sprawdziłem jak działa sieć miedzy kontenerami Dockera 

## Sieci Dockera
| Sieć | Opis |
|---|---|
| `bridge` | Odzielna wewnetrzna siec, kontenery sa w niej i gadaja ze soba, ale zeby wyjsc do internetu m>
| `host` | Kontener nie ma swojej sieci, używa bezposrednio karty sieciowej hosta. Zero izolacji |
| `none` | Odcięcie od sieci, kontener jest totalnie odizolowany |

## Custom bridge vs domyślny bridge

Custom bridge network daje automatyczny DNS między kontenerami, można pingować po nazwie zamiast po IP
Domyślna sieć bridge tego nie ma

## Komendy których użyłem
| Komenda | Co robi |
|---|---|
| `docker network create mynetwork` | Tworzy siec o nazwie mynetwork, i jest deafult bridge |
| `docker run -d --name container1 --network mynetwork nginx` | Uruchamianie kontenera o nazwie container1 w sieci o nazwie mynetwork z obrazu nginx   |
| `docker network inspect mynetwork` | Sprawdzenie szczegółów sieci mynetwork  |
| `docker network disconnect mynetwork container1` | Odłaczenie container1 od mynetwork |

## Czego się nauczyłem
 - Jak zarzadzac siecia Docker
 - Jakie sa rodzaje sieci Docker
 - Kontenery w tej samej sieci custom bridge moga pingowac sie po nazwach
## Problemy które napotkałem
 - Brak
