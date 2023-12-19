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
with open('dadesMaratoTV3.json', 'r', encoding='utf-8') as file:
    datos = json.load(file)

# Accedeix a les dades, per exemple, mostra les comarques disponibles (obtindrem els id's de les comarques)
comarques = list(datos.keys())
print(f'Comarques disponibles: {comarques}')

# Selecciona la comarca d'interès (canvia 'Baix llobregat' amb la comarca desitjada d'acord amb el seu id)
comarca_interes = 'baix-llobregat'

# Verifica si la comarca d'interès existeix
if comarca_interes in datos:
    # Obtenir dades només per la comarca d'interès
    resultats = {comarca_interes: datos[comarca_interes]}
    
    # Mostra els resultats
    print(json.dumps(resultats, ensure_ascii=False, indent=4))
else:
    print(f"La comarca '{comarca_interes}' no existeix a les dades.")
```

## Contribucions i Suport

Si tens suggeriments, millores o vols contribuir amb més informació, si us plau, obre un issue o envia una pull request. També pots contactar amb nosaltres si necessites assistència.

Aquest projecte és proporcionat amb l'esperança que sigui útil per a altres que vulguin conèixer i participar en les activitats solidàries de la Marató de TV3 2023.

Nota: Aquest README és un exemple i pot ser personalitzat segons les necessitats específiques del teu projecte.
