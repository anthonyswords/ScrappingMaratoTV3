# Web Scrapping de la Marató de TV3 2023 - Activitats Solidàries

Aquest repositori conté informació recollida mitjançant web scraping sobre les activitats solidàries organitzades a Catalunya per a la Marató de TV3 2023.

## Estructura del Repositori

- `laMarato_Scrapping2023.ipnyb`: Codi Python per realitzar el web scraping i recopilar la informació de les activitats.

- `dadesMaratoTV3.json`: Fitxer JSON amb les dades recollides. Conté la informació organitzada per comarques, poblacions, i organitzadors d'activitats solidàries (amb detalls com la data, hora, lloc i recaudació total).

## Com Utilitzar les Dades

Pots utilitzar les dades recopilades per explorar i visualitzar les activitats solidàries a Catalunya en el marc de la Marató de TV3 2023.

A continuació, un exemple senzill d'accés a les dades en Python:

```python
import json

# Carrega les dades des del fitxer JSON
with open('datos.json', 'r', encoding='utf-8') as file:
    datos = json.load(file)

# Accedeix a les dades, per exemple, mostra les comarques disponibles
comarques = list(datos.keys())
print(f'Comarques disponibles: {comarques}')
