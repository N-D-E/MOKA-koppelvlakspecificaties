# Context en werkwijze voor MOKA koppelvlakdocumenten

Dit document legt de context, regels en werkwijze vast voor het opstellen van MOKA koppelvlak specificaties, zodat toekomstige documenten consistent, herhaalbaar en afgebakend zijn.

## Context en scope
- Documenten zijn MORA-gebaseerd, ArchiMate-gericht en implementatie-onafhankelijk.
- Doelgroep is architecten.
- De scope wordt expliciet begrensd tot het procesdeelgebied en de MORA referentiecomponenten die in de platen zijn opgenomen.
- Alleen terminologie uit MORA en de koppelvlakplaten is toegestaan; geen OOAPI/OKE-terminologie of API-termen in de kerntekst.

## Terminologie en ArchiMate objecten
- Gebruik ArchiMate-objecten en -relaties waar mogelijk, en label deze expliciet in captions/legend.
- Gebruik alleen informatieobjecten/dataobjecten uit het informatiemodel en het referentie objectdiagram.
- Voorbeelden van kernobjecten (indien aanwezig in de plaat): Student, Examenafname, Te beoordelen werk, Zittingsverslag, Summatieve beoordeling, Resultaat, Onderwijsresultaat, Examendossier, Medewerker.
- Componenten benoemen zoals in MORA: Toets- en examenafname systeem, Toets- en examen inlever- en beoordelingssysteem, Studentvolgsysteem, Document Management Systeem, Kernregistratie Systeem Studenten.
- ArchiMate-termen die vaak voorkomen: Business Process, Business Role, Application Component, Application Service, Data Object, Business Object, Association, Flow, Access, Realization.

## Documentopbouw (markdown)
- Document moet renderbaar zijn op GitHub markdown.
- Geen HTML page-breaks.
- Gebruik een vaste hoofdstukstructuur met korte, duidelijke koppen.
- Placeholders zijn korte, inhoudelijke tekst (max 2-3 regels).
- Inleiding bevat het documentdoel en het viewpoint (koppelvlak referentiearchitectuur).
- Leeswijzer alleen opnemen indien expliciet gevraagd.

## Viewpoint-beschrijving
- Beschrijf per view kort: doel, concerns, scope, gekozen modeltaal en betrokken objecttypen/relaties.
- Gebruik bij voorkeur een vaste mini-structuur: Viewpoint, Legenda (ArchiMate/UML/ERD), en een korte toelichting.

## AMIGO modellenmatrix en modeltalen
- Hanteer de scheidslijn tussen conceptuele modellen en logische/inrichtingsmodellen.
- Conceptueel: ArchiMate (processen, componenten, concepten).
- Logisch/inrichting: UML/ERD voor gegevensstructuur en klassendiagrammen.
- Interacties: Mermaid om de uitwisseling richting berichtspecificatie te structureren.
- Plaats bij voorkeur de AMIGO modellenmatrix als afbeelding voor herkenbaarheid; voeg een tekstuele mapping toe.
- Gebruik een eenvoudige mappingtabel (Markdown) om MOKA-views te relateren aan AMIGO kolom/rij.

## Afbeeldingen
- Gebruik uitsluitend afbeeldingen uit de `img` folder.
- Plaats afbeeldingen bij het relevante hoofdstuk en voeg een figuurcaption toe.
- Voeg per afbeelding een korte viewpoint-beschrijving en legenda met ArchiMate-objecten toe.
- Bestandsnamen met spaties escapen in links.
 - Als een machine-leesbare variant verwarrend is, kies voor afbeelding + mappingtabel.

## Mermaid diagrammen
- Diagrammen zijn implementatie-onafhankelijk.
- Gebruik alleen MORA-terminologie en objecten uit het klassendiagram/objectdiagram.
- Benoem interacties inclusief reacties (bijv. "verwerkt", "ontvangen", "documentlocatie retour").
- Externe specificaties mogen als bron dienen, maar vertaal altijd naar MORA-terminologie.

## Interactiepatronen (regels)
- Voorbereiding: maak expliciet of gegevens al aanwezig zijn en in welke component de voorbereiding plaatsvindt.
- Afname: toon de overdracht van "te beoordelen werk".
- Beoordeling: expliciteer de rol van medewerker, summatieve beoordeling en vaststelling door gemachtigd orgaan.
- Resultaat: onderscheid "beoordeling" versus "resultaat".
- Dossiervorming: onderwijsresultaat bundelt resultaten en bewijsstukken (zoals zittingsverslag en verwijzing naar beoordeeld werk) en leidt tot examendossier in DMS.
- Verwijs waar mogelijk naar relaties uit het referentie objectdiagram.

## Werkwijze (stapsgewijs)
1. Lees de platen en noteer de exacte termen en objecten.
2. Bepaal de MORA-componenten in scope.
3. Zet de hoofdstukstructuur klaar en plaats de afbeeldingen.
4. Vul alle placeholders met korte, inhoudelijke tekst.
5. Maak een mermaid interactiediagram met MORA-termen en reacties.
6. Controleer dat er geen OOAPI/OKE-termen in de kerntekst staan.
7. Zorg dat alles GitHub-markdown compatible is.
8. Check na iedere prompt of je de prompter goed begrijpt, door je beredenatie uit te leggen. 
9. Formuleer de volgende stap die je gaat zetten vanuit je plan van aanpak en vraag altijd om goedkeuring voor het uitvoeren van die stap aan de prompter.

## Afbakening
- Geen nieuwe begrippen introduceren die niet in de platen voorkomen.
- Geen technische API-uitwerking opnemen in de kerntekst.
- Externe documenten alleen in een apart "Gerelateerde implementaties" stuk, zonder termen over te nemen in de hoofdtekst.


