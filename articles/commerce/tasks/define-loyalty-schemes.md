---
title: " Definieren von Treueschemas"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Definieren eines Treueschemas.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bec8653c05d7684202c0e63d049ddb517e12834
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412606"
---
# <a name="define-loyalty-schemes"></a> Definieren von Treueschemas

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Definieren eines Treueschemas. Treueschemas sind Belohnungserwerbs- und -einlöseregeln für ein Treueprogramm. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Navigieren Sie zu Retail und Commerce > Debitoren > Treue > Treueschemas.
2. Klicken Sie auf Neu.
3. Geben Sie im Feld "Schemakennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Sie können mehrere Treueschemas für ein Treueprogramm haben. Treueschemas können für alle Kanäle oder nur eine Teilmenge Kanäle sein.  
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie auf Speichern.
9. Klicken Sie auf "Position hinzufügen".
10. Wählen Sie im Feld "Aktivitätstyp" eine Option aus.
    * Wählen Sie Einkaufsprodukte nach Betrag aus, wenn Debitoren Belohnungen auf Basis, wie viel sie ausgeben, erhalten sollen. Wählen Sie Einkaufsprodukte nach Menge aus, wenn Debitoren Belohnungen auf Basis, wie viele Produkte sie kaufen, erhalten sollen.  Wenn Debitoren Belohnungen für jede Verkaufsbuchung erwerben sollen, unabhängig davon, was oder wie viel eingekauft wird, wählen Sie "Verkaufsbuchung" aus.  
    * Wählen Sie eine Kategorie. Die Kategorie beschränkt, für welche Produkte diese Erwerbsregel gilt.  
    * Falls die Erwerbsregel für alle Produkte gelten soll, lassen Sie dieses Feld leer.  
11. Geben Sie im Feld "Aktivitätsbetrag/-menge" eine Zahl ein.
    *  Für den Aktivitätstyp "Verkaufsbuchungsanzahl" sollten Sie immer einen Wert von "1,0" verwenden. Für die Aktivitätstypen "Einkauf nach Betrag" oder "Einkauf nach Menge", lösen Buchungen, die geringer sind als der eingegebene Wert, keine Erwerbsregel aus. Wenn beispielsweise der Aktivitätstyp "Einkauf nach Betrag" ist, und Sie "10,00 "eingeben, erhält die Verkaufsbuchung für "9,00" keine Belohnungen für diese Erwerbsregel.  
12. Geben Sie im Feld "Aktivitätswährung" einen Wert ein.
13. Klicken Sie im Feld "Belohnungspunktkennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
15. Geben Sie im Feld "Belohnungspunkte" eine Zahl ein.
    * Für Belohnungs-Punkte vom Typ "Betrag" werden erworbene Beträge mit Dezimalstellen erfasst. Wenn beispielsweise die Erwerbsregel 1 Belohnungspunkt pro 1 Euro angibt und der Debitor 1,25 Euro ausgibt, erhält der Debitor 1,25 Belohnungspunkte. Für Belohnungs-Punkte vom Typ "Menge" werden erworbene Beträge mit Ganzzahlen erfasst. Wenn beispielsweise die Erwerbsregel 1 Belohnungspunkt pro 1 Euro angibt und der Debitor 1,25 Euro ausgibt, erhält der Debitor 1,0 Belohnungspunkte.  
16. Klicken Sie auf "Speichern".
17. Klicken Sie auf "Position hinzufügen".
    * Tilgungsregeln werden verwendet, wenn die Treuezahlungsmethode verwendet wird.  
18. Klicken Sie im Feld "Belohnungspunktkennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Nur einlösbare Belohnungspunkte werden angezeigt.  
19. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
20. Geben Sie im Feld "Belohnungspunkte" eine Zahl ein.
21. Wählen Sie im Feld "Tilgungstyp" eine Option aus.
    * Bei Auswahl von Zahlung nach Betrag wird das Feld "Betrag" oder "Menge" als Währungswert behandelt. In diesem Fall ist der Belohnungspunktebetrag, der pro Währungseinheit oder Zahlung verwendet wird, ein festgelegtes Verhältnis. Bei Auswahl von Zahlung nach Menge wird das Feld "Betrag" oder "Menge" als Mengenwert behandelt. In diesem Fall ist der Belohnungspunktebetrag pro Artikelmenge ein festes Verhältnis, allerdings kann der Betrag in der Währung abweichen, wenn der Preis der Artikel, die mit Treuebelohnungspunkten bezahlt wurden, um die gleiche Menge variiert. Der Einlösungstyp "Treuepunkterabatt" ist nur gültig, wenn der Konfigurationsschlüssel für länder-/regionsspezifische Funktionen für das Land "Russland" aktiviert ist, und die POS-Funktionsprofile einen ISO-Code von "RU" haben.  
    * Wählen Sie eine Kategorie. Die Kategorie beschränkt, für welche Produkte diese Einlöseregel gilt.  
    * Falls die Einlöseregel für alle Produkte gelten soll, lassen Sie dieses Feld leer.  
22. Geben Sie im Feld "Betrag oder Menge" eine Zahl ein.
23. Geben Sie im Feld "Währung" einen Wert ein.
24. Klicken Sie auf "Speichern".
25. Klicken Sie auf "Position hinzufügen".
    * Wählen Sie mindestens einen Knoten aus der Liste "Verfügbare Organisationsknoten" aus und verschieben Sie ihn in die Liste "Ausgewählte Organisationsknoten", indem Sie auf den Pfeil zwischen den zwei Listen klicken.  
26. Klicken Sie auf "OK".
27. Klicken Sie auf "Speichern".
    * Immer wenn Sie die Kanäle für ein Treueschema ändern, müssen Sie Prozesstreueschemas ausführen. Auf diese Weise werden für die Kanäle aktualisierte Treueschemas abgerufen.  

