--- 
title: " Basispreis und Handelsvereinbarungen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen von kanalspezifischen Verkaufspreis-Handelsvereinbarungen."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 81c70921718e41719470c7428c05a9f7ae77354a
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---
# <a name="base-price-and-trade-agreements"></a> Basispreis und Handelsvereinbarungen

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen von kanalspezifischen Verkaufspreis-Handelsvereinbarungen. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Navigieren Sie zu Einzelhandel und Handel > Preise und Rabatte > Preisgruppen > Alle Preisgruppen.
    * Preisgruppen zeigen an, wie Handelsvereinbarungen bestimmten Kanälen zugewiesen sind. Das Verwenden von Preisgruppen, um Handelsvereinbarungen zu einem Kanal zuzuweisen, aktiviert die kanalspezifische Preisgestaltung.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Preisgruppen" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.
7. Navigieren Sie zu Einzelhandel und Handel > Kanäle > Einzelhandelsgeschäfte > Alle Einzelhandelsgeschäfte.
8. Wählen Sie in der Liste "New York" aus
9. Klicken Sie im Aktivitätsbereich auf "Shop".
10. Klicken Sie auf "Preisgruppen".
11. Klicken Sie auf "Neu".
12. Klicken Sie im Feld "Preisgruppen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.
16. Schließen Sie die Seite.
17. Navigieren Sie zu Einzelhandel und Handel > Produkte und Kategorien > Freigegebene Produkte nach Kategorie.
18. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
19. Klicken Sie auf Bearbeiten.
20. Schalten Sie die Erweiterung des Verkaufs-Abschnitts ein/aus.
21. Geben Sie im Feld "Preis" eine Zahl ein.
    * Dieser Preis wird verwendet, wenn keine entsprechenden Handelsvereinbarungen gefunden werden.  
22. Klicken Sie auf "Speichern".
23. Klicken Sie im Aktivitätsbereich auf "Verkaufen".
24. Klicken Sie auf "Handelsvereinbarungen erstellen".
25. Klicken Sie auf Neu.
26. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
27. Wählen Sie in der Liste "Einzelhandel'' aus.
    * In den Demodaten hat das Journal "Einzelhandel" die standardmäßige Relation "Preis (Verkauf)". Das bedeutet, dass alle erstellten neuen Positionen standardmäßig auf Verkaufspreis-Handelsvereinbarungen festgelegt werden.  
28. Klicken Sie auf "Positionen".
29. Wählen Sie im Feld "Kontocode" die Option "Gruppe" aus.
30. Klicken Sie im Feld Konto-Auswahl auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
31. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Damit wird die Verknüpfung von Kanal zu Preisgruppe zu Handelsvereinbarung abgeschlossen.  
32. Geben Sie im Feld "Artikelrelation" einen Wert ein.
33. Geben Sie eine Zahl in das Feld "Betrag in Währung" ein.
34. Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Weitersuchen".
    * Wenn "Weitersuchen" auf "Ja" festgelegt ist, sucht das Preiskalkulationsmodul weiter nach gültigen Handelsvereinbarungen mit einem niedrigeren Verkaufspreis. Wenn "Weitersuchen" auf "Nein" festgelegt ist, stellt das Preismodul die Suche ein und verwendet die Handelsvereinbarung.  
35. Klicken Sie auf "Buchen".
36. Klicken Sie auf "OK".
37. Schließen Sie die Seite.
38. Klicken Sie im Aktivitätsbereich auf "Verkaufen".
39. Klicken Sie auf "Verkaufspreis".


