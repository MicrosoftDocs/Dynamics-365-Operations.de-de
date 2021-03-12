---
title: Massenerstellung von Verkaufsangeboten
description: Diese Verfahren zeigt, wie Sie Angebote, die eine Gruppe von Produkte oder Dienstleistungen enthalten und an mehrere Debitoren gesendet werden sollen, effizient erstellen.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ea50500ed52069ab9f6aae0dfb2d6cffc47cbff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006839"
---
# <a name="mass-create-sales-quotations"></a>Massenerstellung von Verkaufsangeboten

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie Sie Angebote, die eine Gruppe von Produkte oder Dienstleistungen enthalten und an mehrere Debitoren gesendet werden sollen, effizient erstellen. Diese Massenangebotserstellung basiert auf Angebotsvorlagen. Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.


## <a name="create-a-quotation-template"></a>Erstellen einer Angebotsvorlage
1. Wechseln Sie zu Vertrieb und Marketing > Einstellungen > Angebote > Vorlagengruppen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Gruppenkennung" eine Kennung Ihrer Wahl ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.
7. Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".
8. Klicken Sie auf "Neu".
9. Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.
10. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
11. Klicken Sie auf "OK".
    * Damit ein Angebot eine Vorlage wird, müssen Sie die Einrichtungsschritte im Angebotskopf ausführen. Dies muss ausgeführt werden, bevor Sie Positionen zum Angebot hinzufügen.   
12. Klicken Sie im Aktivitätsbereich auf "Optionen".
13. Klicken Sie auf "Ansicht ändern".
14. Klicken Sie auf die Kopfzeilenansicht.
15. Erweitern Sie den Abschnitt 'Einstellungen'.
16. Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.
17. Geben Sie im Feld "Vorlage" einen Wert ein.
18. Wählen Sie "Ja" im Feld "Aktiv".
    * Nur aktive Vorlagen können verwendet werden wenn Sie eine Vorlage auf ein neues Verkaufsangebot anwenden.  
19. Klicken Sie im Aktivitätsbereich auf "Optionen".
20. Klicken Sie auf "Ansicht ändern".
21. Klicken Sie auf Positionsansicht.
22. Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.
23. Geben Sie im Feld "Artikel einen Wert ein.
24. Schließen Sie die Seite.
25. Geben Sie im Feld "Rabatt in Prozent" eine Zahl ein.
26. Klicken Sie auf "Position hinzufügen".
27. Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.
28. Geben Sie im Feld "Artikel einen Wert ein.
29. Schließen Sie die Seite.
30. Geben Sie im Feld "Preis je Einheit" einen neuen Preis ein oder ändern Sie den aktuellen.
31. Klicken Sie auf "Position hinzufügen".
32. Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.
33. Geben Sie im Feld "Artikel einen Wert ein.
34. Schließen Sie die Seite.
35. Geben Sie im Feld "Menge" eine Zahl ein.
36. Geben Sie im Feld "Rabatt" einen Zahl ein.
37. Klicken Sie auf "Speichern".

## <a name="apply-the-template-to-create-a-single-quotation"></a>Anwenden der Vorlage, um ein einzelnes Angebot zu erstellen
1. Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".
    * Beachten Sie, dass das Angebot, das Sie soeben erstellt haben, als Vorlage markiert ist.  
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.
4. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
5. Erweitern Sie den Abschnitt "Vorlage".
6. Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.
7. Geben Sie im Feld "Vorlagenname" einen Wert ein, oder wählen Sie einen Wert aus.
8. Wählen Sie im Feld "Berechnungsmethode" "Basierend auf Vorlagenwerten" aus.
9. Klicken Sie auf "OK".
    * Das neue Angebot ist jetzt basierend auf den Daten und den Bedingungen der Vorlage erstellt.  
10. Schließen Sie die Seite.
11. Schließen Sie die Seite.

## <a name="apply-the-template-to-mass-create-quotations"></a>Anwenden der Vorlage zur Massenerstellung von Angeboten
1. Wechseln Sie zu Vertrieb und Marketing > Verkaufsangebote > Angebotsaktualisierung > Massenerstellung von Angeboten.
2. Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.
3. Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.
4. Geben Sie im Feld "Vorlagenname" einen Wert ein, oder wählen Sie einen Wert aus.
5. Wählen Sie im Feld "Berechnungsmethode" "Basierend auf Vorlagenwerten" aus.
6. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
7. Klicken Sie auf "Filter".
8. Lesen Sie im Feld "Kriterien" den Filter fest, um den Bereich von Debitoren abzudecken, die Sie in diese Massen-Angebotserstellung einbeziehen möchten. Verwenden Sie das folgende Format: "Kunde1..KundeN."
    * So können Sie beispielsweise den folgenden Filter festlegen: US-001..US-004  
9. Klicken Sie auf "OK".
10. Klicken Sie auf "OK".
11. Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".
    * Überprüfen Sie, ob Angebote für alle Debitoren erstellt wurden, die in der Massenaktualisierungsroutine angeben sind.  

