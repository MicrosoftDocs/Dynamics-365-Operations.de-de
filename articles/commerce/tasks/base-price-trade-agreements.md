---
title: " Basispreis und Handelsvereinbarungen"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen von kanalspezifischen Verkaufspreis-Handelsvereinbarungen.
author: josaw1
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 282cbe0cb115d6204137613f4754068b8a9a321400d24808eb67266a83d7bcc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730730"
---
# <a name="base-price-and-trade-agreements"></a> Basispreis und Handelsvereinbarungen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen von kanalspezifischen Verkaufspreis-Handelsvereinbarungen. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Gehen Sie im **Navigationsbereich** Sie zu **Module > Einzelhandel und Handel > Verwaltung von Preisen und Rabatten > Preisgruppen > Alle Preisgruppen**. Preisgruppen zeigen an, wie Handelsvereinbarungen bestimmten Kanälen zugewiesen sind. Das Verwenden von Preisgruppen, um Handelsvereinbarungen zu einem Kanal zuzuweisen, aktiviert die kanalspezifische Preisgestaltung.  
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Preisgruppen** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Klicken Sie auf **Speichern**.
6. Schließen Sie die Seite.
7. Gehen Sie im **Navigationsbereich** zu **Module > Einzelhandel und Handel > Kanäle > Geschäfte > Alle Geschäfte**.
8. Wählen Sie in der Liste "New York" aus
9. Klicken Sie im Aktivitätsbereich auf **Shop**.
10. Klicken Sie auf **Preisgruppen**.
11. Klicken Sie auf **Neu**.
12. Klicken Sie im Feld **Preisgruppen** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Klicken Sie auf **Speichern**.
15. Schließen Sie die Seite.
16. Schließen Sie die Seite.
17. Gehen Sie im **Navigationsbereich** zu **Module > Einzelhandel und Handel > Produkte und Kategorien > Freigegebene Produkte nach Kategorie**.
18. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
19. Klicken Sie auf **Bearbeiten**.
20. Erweitern Sie das Inforegister **Verkaufen**.
21. Geben Sie im Feld **Preis** eine Zahl ein. Dieser Preis wird verwendet, wenn keine entsprechenden Handelsvereinbarungen gefunden werden.  
22. Klicken Sie auf **Speichern**.
23. Klicken Sie im **Aktivitätsbereich** auf **Verkaufen**.
24. Klicken Sie auf **Handelsvereinbarungen erstellen**.
25. Klicken Sie auf **Neu**.
26. Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
27. Wählen Sie in der Liste **Commerce** aus. In den Demodaten hat das Journal **Commerce** die standardmäßige Relation **Preis (Verkauf)**. Das bedeutet, dass alle erstellten neuen Positionen standardmäßig auf Verkaufspreis-Handelsvereinbarungen festgelegt werden.  
28. Klicken Sie im **Aktivitätsbereich** auf **Positionen**.
29. Wählen Sie im Feld **Parteicodetyp** die Option „Gruppe“ aus.
30. Klicken Sie im Feld **Konto-Auswahl** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
31. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Damit wird die Verknüpfung von Kanal zu Preisgruppe zu Handelsvereinbarung abgeschlossen.  
32. Geben Sie im Feld **Artikelrelation** einen Wert ein.
33. Geben Sie eine Zahl in das Feld **Betrag in Währung** ein.
34. Auf dem Inforegister **Details** aktivieren oder deaktivieren Sie das Kontrollkästchen **Weitersuchen**. Wenn **Weitersuchen** auf „Ja“ festgelegt ist, sucht das Preiskalkulationsmodul weiter nach gültigen Handelsvereinbarungen mit einem niedrigeren Verkaufspreis. Wenn **Weitersuchen** auf „Nein“ festgelegt ist, stellt das Preismodul die Suche ein und verwendet die Handelsvereinbarung.  
35. Klicken Sie auf **Buchen**.
36. Klicken Sie auf **OK**.
37. Schließen Sie die Seite.
38. Klicken Sie im Aktivitätsbereich auf **Verkaufen**.
39. Klicken Sie auf **Verkaufspreis**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]