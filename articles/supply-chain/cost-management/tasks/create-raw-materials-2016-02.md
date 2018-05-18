--- 
title: "Rohmaterialien erstellen (nur Februar 2016)"
description: Diese Aufgabe konzentriert sich auf das Erstellen der Komponenten fertiger und halbfertiger Produkte.
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 8ed33e2e80915a80eb4c6de014091f1884799098
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---
# <a name="create-raw-materials-february-2016-only"></a>Rohmaterialien erstellen (nur Februar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabe konzentriert sich auf das Erstellen der Komponenten fertiger und halbfertiger Produkte. Es ist die dritte Aufgabe in der Stücklistenberechnungsserie. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.


## <a name="create-the-first-material"></a>Das erste Material erstellen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Produktnummer" einen Wert ein.
    * Geben Sie für dieses Beispiel ITEM_A ein.  
4. Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie STD aus. STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.  
5. Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie z. B. „Audio” aus. Dies hat keine Auswirkungen auf Kostenberechnungen.  
6. Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie „SiteWH” aus. Nur „Standort” und „Lagerort” werden für die Demonstration verwendet.  
7. Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet. Wählen Sie „Keine” aus.  
8. Klicken Sie auf "OK".
9. Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".
10. Klicken Sie auf "Standardmäßige Auftragseinstellungen".
11. Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
12. Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
13. Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
14. Schließen Sie die Seite.
15. Schließen Sie die Seite.
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Klicken Sie auf ITEM_A.  
17. Erweitern Sie den Abschnitt „Kosten verwalten”.
18. Geben Sie im Feld „Kostengruppe” einen Wert ein.
    * Geben Sie für dieses Beispiel M2 ein.  
19. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
20. Klicken Sie auf „Artikelpreis”.
21. Klicken Sie auf "Neu".
22. Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel 10 aus. Dies ist der standardmäßige Nachkalkulationstyp.  
23. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
24. Geben Sie im Feld "Preis" eine Zahl ein.
    * Geben Sie für dieses Beispiel 10 ein.  
25. Klicken Sie auf "Speichern".
26. Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.
27. Schließen Sie die Seite.
28. Schließen Sie die Seite.

## <a name="create-the-second-material"></a>Das zweite Material erstellen
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Produktnummer" einen Wert ein.
    * Geben Sie für dieses Beispiel ITEM_B ein.  
3. Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie STD aus. STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.  
4. Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie z. B. „Audio” aus. Dies hat keine Auswirkungen auf Kostenberechnungen.  
5. Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie „SiteWH” aus. Nur „Standort” und „Lagerort” werden für dieses Beispiel verwendet.  
6. Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet. Wählen Sie „Keine” aus.  
7. Klicken Sie auf "OK".
8. Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".
9. Klicken Sie auf "Standardmäßige Auftragseinstellungen".
10. Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
11. Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
12. Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
13. Schließen Sie die Seite.
14. Schließen Sie die Seite.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Klicken Sie auf ITEM_B.  
16. Erweitern Sie den Abschnitt „Kosten verwalten”.
17. Geben Sie im Feld „Kostengruppe” einen Wert ein.
    * Geben Sie für dieses Beispiel M2 ein.  
18. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
19. Klicken Sie auf „Artikelpreis”.
20. Klicken Sie auf "Neu".
21. Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel 10 aus. Das ist der standardmäßige Nachkalkulationstyp.  
22. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
23. Geben Sie im Feld "Preis" eine Zahl ein.
    * Geben Sie für die Demonstration 10 ein.  
24. Klicken Sie auf "Speichern".
25. Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.
26. Schließen Sie die Seite.
27. Schließen Sie die Seite.

## <a name="create-the-third-material"></a>Das dritte Material erstellen
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Produktnummer" einen Wert ein.
    * Geben Sie für die Demonstration ITEM_C ein  
3. Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie STD aus. STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.  
4. Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie z. B. „Audio” aus. Dies hat keine Auswirkungen auf Kostenberechnungen.  
5. Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie „SiteWH” aus. Nur „Standort” und „Lagerort” werden für die Demonstration verwendet.  
6. Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet. Wählen Sie „Keine” aus.  
7. Klicken Sie auf "OK".
8. Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".
9. Klicken Sie auf "Standardmäßige Auftragseinstellungen".
10. Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
11. Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
12. Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
13. Schließen Sie die Seite.
14. Schließen Sie die Seite.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Klicken Sie auf ITEM_C.  
16. Erweitern Sie den Abschnitt „Kosten verwalten”.
17. Geben Sie im Feld „Kostengruppe” einen Wert ein.
    * Geben Sie für dieses Beispiel M1 ein.  
18. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
19. Klicken Sie auf „Artikelpreis”.
20. Klicken Sie auf "Neu".
21. Geben Sie im Feld „Version” einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel 10 aus. Das ist der standardmäßige Nachkalkulationstyp.  
22. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Standort 1” aus.  
23. Geben Sie im Feld "Preis" eine Zahl ein.
    * Geben Sie für dieses Beispiel 10 ein.  
24. Klicken Sie auf "Speichern".
25. Klicken Sie auf „Ausstehende(n) Preis(e) aktivieren”.
26. Schließen Sie die Seite.
27. Schließen Sie die Seite.


