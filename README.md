# API ANAF
Librarie PHP pentru verificarea gratuita a contribuabililor care sunt inregistrati conform art. 316 din Codul Fiscal

Data care pot fi obtinute:
  - Denumire/Adresa companie
  - Platitor/Neplatitor TVA
  - Platitor TVA la incasare
  - Platitor Split TVA
  - Data inregistrare TVA
  - Status Societate (Activa/Inactiva)
  - etc.
  
:heart: Daca iti este de folos te rog sa oferi o stea :star:
  
# Instalare
composer require itrack/anaf

# Exemplu de folosire

- Initializare librarie

$anaf = new \Itrack\Anaf\Client(); <br><br>

- Pentru a verifica doar un cui urmati foloseste metoda $anaf->addCui(CUI VALOARE INTEGER, "DATA VERIFICARE") conform exemplului de mai jos:

$anaf->addCui(123456, "2017-12-31"); <br>
print_r($anaf->getResults());<br><br>

- Pentru a verifica mai multe CUI-uri in acelasi timp foloseste metoda $anaf->addCui(CUI VALOARE INTEGER, "DATA VERIFICARE") de mai multe ori:

$anaf->addCui(123456, "2017-12-31"); <br>
$anaf->addCui(654321, "2017-11-24"); <br>
print_r($anaf->getResults());

# Linkuri utile
https://blog.turma.ro/api-anaf/
https://static.anaf.ro/static/10/Anaf/Informatii_R/documentatie_SW_01112017.txt
