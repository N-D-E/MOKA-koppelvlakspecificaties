<!-- ===================== -->
<!-- Titelpagina -->
<!-- ===================== -->
# MOKA Koppelvlak Specificatie Document - DEMO

![MOKA Voorblad](../img/MOKA%20voorblad.png)
## Examen uitvoering en beoordeling

**Versie:** v20260204  
**Datum:** 2026-02-04  
**Status:** Concept  
**Auteur:** Niek Derksen
**Organisatie:** MOKA Werkgroep

---

### Documentdoel

Dit document beschrijft de MOKA koppelvlak specificatie voor een deelgebied van de MORA procesketen Examineren.  
Het document is bedoeld om sectorbreed afspraken vast te leggen over betekenis, structuur en interactie van informatieobjecten, in samenhang met MORA, dienend als referentiepunt voor koppelvlak implementaties, zoals OKE.
In eerste instantie bedoeld ter demo voor de MOKA werkgroep te 05-02-26.


---

<!-- ===================== -->
<!-- Versiehistorie -->
<!-- ===================== -->

## Versiehistorie

| Versie | Datum       | Auteur        | Wijziging |
|------:|------------|---------------|-----------|
| v20260204  | 2026-02-04| Niek Derksen  | Initiële versie van deze koppelvlak specificatie t.b.h.v. MOKA werkgroep Demo i.h.k.v. Klus 43 voortgangsupdate |

---

<!-- ===================== -->
<!-- Inhoudsopgave -->
<!-- ===================== -->

## Inhoudsopgave

- [MOKA Koppelvlak Specificatie Document - DEMO](#moka-koppelvlak-specificatie-document---demo)
  - [Examen uitvoering en beoordeling](#examen-uitvoering-en-beoordeling)
    - [Documentdoel](#documentdoel)
  - [Versiehistorie](#versiehistorie)
  - [Inhoudsopgave](#inhoudsopgave)
  - [1. Inleiding](#1-inleiding)
  - [2. Leeswijzer](#2-leeswijzer)
  - [3. MOKA Koppelvlak Specificatie](#3-moka-koppelvlak-specificatie)
    - [3.1 MORA Procesplaatsing](#31-mora-procesplaatsing)
    - [3.2 MOKA Koppelvlak Specificatie Viewpoint](#32-moka-koppelvlak-specificatie-viewpoint)
      - [3.2.1 Metamodel](#321-metamodel)
      - [3.2.2 MOKA Koppelvlak Specificatie View](#322-moka-koppelvlak-specificatie-view)
      - [3.2.3 MOKA Koppelvlak specifiek informatiemodel view](#323-moka-koppelvlak-specifiek-informatiemodel-view)
      - [3.2.4 MOKA Koppelvlak specifiek referentie objectdiagram view](#324-moka-koppelvlak-specifiek-referentie-objectdiagram-view)
      - [3.2.5 MOKA Koppelvlak interactiepatroon view](#325-moka-koppelvlak-interactiepatroon-view)
  - [3.2.6 Gerelateerde Implementaties en Specificaties](#326-gerelateerde-implementaties-en-specificaties)

---

<!-- ===================== -->
<!-- Hoofdstuk 1: Inleiding -->
<!-- ===================== -->

## 1. Inleiding

*[Tekst volgt]*

---

<!-- ===================== -->
<!-- Hoofdstuk 2: Leeswijzer -->
<!-- ===================== -->

## 2. Leeswijzer

*[Tekst volgt]*

---

<!-- ===================== -->
<!-- Hoofdstuk 3: MOKA Koppelvlak Specificatie -->
<!-- ===================== -->

## 3. MOKA Koppelvlak Specificatie

*[Inleidende tekst volgt]*

---

### 3.1 MORA Procesplaatsing

*[Tekst volgt]*

![MORA Procesketengebied](../img/Procesketengebied%20indicatie%20binnen%20MORA%20hoofdprocesmodel%20-%20v260204.png)

**Figuur 3.1:** Procesketengebied indicatie binnen MORA hoofdprocesmodel

---

### 3.2 MOKA Koppelvlak Specificatie Viewpoint

*[Tekst volgt]*

---

#### 3.2.1 Metamodel

*[Tekst volgt]*

![MORA en MOKA Metamodel](../img/MORA%20en%20MOKA%20metamodel%20met%20toelichting%20-%20v260204.png)

**Figuur 3.2.1:** MORA en MOKA metamodel met toelichting

---

#### 3.2.2 MOKA Koppelvlak Specificatie View

*[Tekst volgt]*

![MOKA Koppelvlak Specificatie View](../img/MOKA%20koppelvlak%20specificatie%20view%20-%20v260204.jpg)

**Figuur 3.2.2:** MOKA koppelvlak specificatie view

---

#### 3.2.3 MOKA Koppelvlak specifiek informatiemodel view

*[Tekst volgt]*

![MOKA Koppelvlak Informatiemodel](../img/Koppelvlak%20specifiek%20informatiemodel%20view%20-%20v20260402.jpg)

**Figuur 3.2.3:** Koppelvlak specifiek informatiemodel view

---

#### 3.2.4 MOKA Koppelvlak specifiek referentie objectdiagram view

*[Tekst volgt]*

![MOKA Koppelvlak Object Diagram](../img/MOKA%20koppelvlak%20specifiek%20object%20diagram%20-%20v260204.png)

**Figuur 3.2.4:** MOKA koppelvlak specifiek object diagram

---

#### 3.2.5 MOKA Koppelvlak interactiepatroon view

Het onderstaande interactiepatroon toont de gegevensuitwisseling tussen de MORA referentiecomponenten binnen de examen uitvoerings- en beoordelingsketen.

**Referentiecomponenten in scope:**
- Toets en examen afname systeem
- Toets en examen inlever & beoordelingssysteem  
- Student volg systeem (SVS)
- Document Management Systeem (DMS)
- Kernregistratie Systeem Studenten (KRS)

```mermaid
sequenceDiagram
    participant KRS as Kernregistratie<br/>Systeem Studenten
    participant SVS as Student volg<br/>systeem
    participant TAS as Toets en examen<br/>afname systeem
    participant TBS as Toets en examen inlever<br/>& beoordelingssysteem
    participant DMS as Document<br/>Management Systeem
    
    Note over KRS,DMS: Examen uitvoering en beoordeling - interactiepatroon
    
    rect rgb(240, 248, 255)
        Note right of KRS: Fase 1: Voorbereiding
        KRS->>SVS: Student gegevens (studentId, primaryCode)
        SVS->>TAS: Examenafname planning<br/>(examenafnameId, startDateTime, endDateTime)
        SVS->>TAS: Student inschrijving<br/>(participatesIn: Student -> Examenafname)
    end
    
    rect rgb(255, 250, 240)
        Note right of TAS: Fase 2: Examen uitvoering
        TAS->>TAS: Student maakt examen
        TAS->>TBS: TeBeoordelenWerk aanleveren<br/>(werkId, representation, createdAt)
        TAS->>TBS: BevoegdheidsRol toewijzing<br/>(personId, role, state)
    end
    
    rect rgb(240, 255, 240)
        Note right of TBS: Fase 3: Beoordeling
        TBS->>TBS: Assessor beoordeelt werk
        TBS->>DMS: Zittingsverslag opslaan<br/>(zittingsverslagId, createdBy: Medewerker)
        TBS->>SVS: SummatieveBeoordeling<br/>(beoordelingId, rawScore, scale, awardedAt)
        TBS->>SVS: SummatieResultaat aanmaken<br/>(resultaatId, resultType, passIndicator)
    end
    
    rect rgb(255, 240, 240)
        Note right of SVS: Fase 4: Resultaatbepaling
        SVS->>SVS: OnderwijsResultaat aggregatie<br/>(aggregationType, GerelateerdeResultaten)
        SVS->>DMS: Examendossier vastleggen<br/>(examendossierId, dossierNumber, status)
        SVS->>KRS: Onderwijsresultaat registratie<br/>(resultaatId, recordedAt)
    end
    
    Note over KRS,DMS: Einde: Resultaat beschikbaar voor student en geregistreerd
```

**Figuur 3.2.5:** Interactiepatroon tussen MORA referentiecomponenten (gebaseerd op OOAPI objectmodel)

---

## 3.2.6 Gerelateerde Implementaties en Specificaties

Voor meer informatie omtrent het koppelvlakprofiel en gerelateerde implementaties:

- Raadpleeg het [OOAPI OKE profiel (specificatie v5)](https://github.com/NetwerkExamineringDigitalisering/NED-OOAPI/tree/main/specification/v5) voor de technische uitwerking.
- Raadpleeg het [OKE MBO Toetsafname Specificatie Document (conceptversie 1.0, 9 september 2024, PDF)](https://www.edustandaard.nl/app/uploads/2024/09/OKE-MBO-toetsafname-specs-v1.0_20240909conceptversie.pdf), specifiek de paragrafen **3.3** ("Globale gegevensuitwisselingen tussen systemen") en **3.4** ("Koppelvlak-definitie").

Deze documenten bevatten de actuele technische specificaties en koppelvlakeisen voor de OKE-keten.


<!-- ===================== -->
<!-- Einde document -->
<!-- ===================== -->
