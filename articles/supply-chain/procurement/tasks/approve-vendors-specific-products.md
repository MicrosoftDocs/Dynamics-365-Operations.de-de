---
title: Händler für bestimmte Produkte genehmigen
description: Diese Prozedur zeigt Ihnen an, wie Sie Händler für bestimmte Produkte genehmigen.
author: GalynaFedorova
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5092012f27dd03343410d30d15cae11ad20ce052
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670152"
---
# <a name="approve-vendors-for-specific-products"></a>Händler für bestimmte Produkte genehmigen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen an, wie Sie Händler für bestimmte Produkte genehmigen. Dies ermöglicht es Ihnen, zu steuern, welche Händler verwendet werden können, wenn das Produkt einer Bestellung hinzugefügt wird. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. In der Regel wird diese Aufgabe von einem Einkaufsleiter ausgeführt.

1. Wechseln Sie im Navigationsbereich zu **Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Erweitern Sie das Inforegister **Einkauf**. Wenn im Feld **Kreditor** ein primärer Kreditor angezeigt wird, müssen Sie diesen Kreditor als genehmigten Kreditor in den folgenden Schritten hinzufügen. Notieren Sie die Kreditornummer, sofern sie angezeigt wird.  
5. Klicken Sie im Aktionsbereich auf **Einkauf**.
6. Klicken Sie auf **Einstellungen**.
7. Klicken Sie auf **Hinzufügen**.
8. Geben Sie im Feld "Händler" einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie den genehmigten Kreditor aus. Es muss mindestens eine der Positionen der primäre Händler sein, wenn sich einer im Produktdatensatz befand. Wenn Sie zuvor die Händlernummer notierten, wählen Sie diese hier aus.  
9. Geben Sie im Feld **Ablauf** ein Datum ein. Wählen Sie ein Datum aus, das mehrere Monate in der Zukunft liegt.  
10. Klicken Sie auf **Hinzufügen**.
11. Geben Sie im Feld **Kreditor** einen Wert ein, oder wählen Sie einen Wert aus.
12. Geben Sie im Feld **Ablauf** ein Datum ein. Wählen Sie ein Datum aus, das sich vom vorherigen Ablaufdatum unterscheidet.  
13. Schließen Sie die Seite.
14. Klicken Sie im Aktivitätsbereich auf **Genehmigte Kreditoren**.
15. Geben Sie im Feld **Ablauf** ein Datum ein. Dieses Datum dient als ein Filter, damit Sie sehen können, wer bis zu einem bestimmten Datum die genehmigten Kreditoren sind.  
16. Schließen Sie die Seite.
17. Klicken Sie im Aktivitätsbereich auf **Effektive Periode**.
18. Geben Sie im Feld **Anzeigen der Kreditoren (abgelaufen zum)** ein Datum ein. Sie können diese Seite verwenden, um Händler identifizieren, bei denen der Genehmigungsstatus nach einem bestimmten Datum abläuft.  
19. Schließen Sie die Seite.
20. Klicken Sie auf **Bearbeiten**.
21. Wählen Sie im Feld **Überprüfung genehmigter Kreditoren** eine Option aus. In diesem Feld können Sie die Richtlinie auswählen, die bestimmt, was geschehen soll, wenn das Produkt einer Bestellpostion hinzugefügt wird, wobei der Händler kein genehmigter Kreditor ist.  
22. Klicken Sie auf **Speichern**.
23. Schließen Sie die Seite.
24. Schließen Sie die Seite.
25. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Kreditoren > Kreditor/Artikelrelationen > Übersicht genehmigter Kreditoren 'nach Artikel'**. Diese Seite enthält einen Überblick über alle Produkte und die genehmigten Kreditoren.  
26. Schließen Sie die Seite.
27. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Kreditoren > Alle Kreditoren**. Sie können von einem Händler aus beginnen und dann zur Liste der genehmigten Produkten für dieses Kreditorenkonto wechseln.  
28. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
29. Klicken Sie im Aktivitätsbereich auf **Beschaffung**.
30. Klicken Sie auf **Übersicht genehmigter Kreditoren 'nach Kreditoren'**.
31. Schließen Sie die Seite.
32. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]