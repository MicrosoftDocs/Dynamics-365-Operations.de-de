---
title: EUR-00015 Einrichtung der MwSt Kennung
description: Diese Verfahren zeigt die MwSt.-ID-Erfassungsvoraussetzungen, z. B. das Einrichten eines Erfassungstyps und Zuweisen zu einer Erfassungskategorie.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
ms.openlocfilehash: 26120765b61a27cab544c37163a34a0ef18da30a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283787"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR-00015 Einrichtung der MwSt Kennung

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt die MwSt.-ID-Erfassungsvoraussetzungen, z. B. das Einrichten eines Erfassungstyps und Zuweisen zu einer Erfassungskategorie. Zusätzliche Informationen zu Erfassungskennungen und der Verarbeitung von Erfassungskennungen, einschließlich der erforderlichen Voraussetzungen, finden Sie im Hilfethema „Erfassungs-IDs“. 

Diese Informationen gelten für alle europäischen Länder/Regionen. Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Deutschland erstellt. Diese Aufgabe richtet sich an Systemadministratoren. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.

1. Navigieren zur Organisationsverwaltung > Globales Adressbuch > Erfassungstypen > Erfassungstypen.
2. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
3. Geben Sie im Feld Name "MwSt.-ID" ein.
4. Geben Sie im Feld "Beschreibung "MwSt.-Nummer" ein.
5. Wählen Sie im Feld Name/Region "DEU" aus oder geben Sie einen Wert ein.
6. Wählen Sie "Ja" im Feld "Eindeutig".
    * Aktivieren Sie dieses Kontrollkästchen, um sicherzustellen, das die Mehrwertsteuerkennung eindeutig ist.  
7. Wählen Sie "Ja" im Feld "Primär für Land".
    * Aktivieren Sie dieses Kontrollkästchen, wenn die Mehrwertsteuer-ID für alle Adressen gültig ist, die zum angegebenen Land/Region gehören.  
8. Klicken Sie auf "Erstellen".
9. Klicken Sie auf Hinzufügen.
10. Wählen Sie im Feld Name/Region "ITA" aus oder geben Sie einen Wert ein.
11. Geben Sie im Feld 'Format' den Wert '###########' ein.
    * Wenn Sie einer Erfassungskennung dieses Typs für das ausgewählte Land/Region eingeben, wird die Erfassungskennung gegen dieses Format geprüft.  
12. Aktivieren Sie das Kontrollkästchen "Eindeutig".
    * Aktivieren Sie dieses Kontrollkästchen, um sicherzustellen, das die Mehrwertsteuerkennung eindeutig ist.  
13. Aktivieren Sie das Kontrollkästchen "Primär für Land".
    * Aktivieren Sie dieses Kontrollkästchen, wenn die Mehrwertsteuer-ID für alle Adressen gültig ist, die zum angegebenen Land/Region gehören.  
14. Klicken Sie auf "Speichern".
15. Navigieren zur Organisationsverwaltung > Globales Adressbuch > Erfassungstypen > Erfassungskategorien.
16. Klicken Sie auf "Neu".
17. Wählen Sie im Feld Name/Region "MwSt.-ID, DEU" aus oder geben Sie einen Wert ein.
18. Wählen Sie im Feld "Registrierungskategorie" die Option "MwSt.-ID" aus.
    * Weisen Sie den Journaltyp zu, den Sie eben für eine vordefinierte Erfassungskategorie erstellt haben.  
19. Klicken Sie auf "Neu".
20. Wählen Sie im Feld Name/Region "MwSt.-ID, ITA" aus oder geben Sie einen Wert ein.
21. Wählen Sie im Feld "Registrierungskategorie" die Option "MwSt.-ID" aus.
    * Weisen Sie den Journaltyp zu, den Sie für eine vordefinierte Erfassungskategorie erstellt haben.  
22. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
