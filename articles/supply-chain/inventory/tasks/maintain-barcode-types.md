---
title: Strichcodetypen verwalten
description: Dieses Verfahren zeigt Ihnen, wie eine neue Strichcodedefinition eingerichtet wird, die dann als Teil des Kommissionierlistenberichts verwendet werden kann.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 979726a1d094146b546bbc6d31963367de2c59f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428962"
---
# <a name="maintain-barcode-types"></a>Strichcodetypen verwalten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt Ihnen, wie eine neue Strichcodedefinition eingerichtet wird, die dann als Teil des Kommissionierlistenberichts verwendet werden kann. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Wenn Sie USMF verwenden, können Sie die Beispielswerte verwenden, die angezeigt werden. Diese Aufgaben werden normalerweise von einem Lagerortleiter ausgeführt.

1. Wechseln Sie zu Strichcodes.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Strichcodeeinstellung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Strichcodetyp " eine Option aus.
    * Wenn Sie USMF verwenden, können Sie "Code 39" auswählen.  
6. Geben Sie im Feld "Größe" eine Zahl ein.
7. Geben Sie im Feld "Höchstlänge" eine Zahl ein.
8. Klicken Sie auf Speichern.
9. Schließen Sie die Seite.
10. Wechseln Sie zu "Parameter für Lager- und Lagerortverwaltung".
11. Geben Sie im Feld 'Strichcodeeinstellung' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die Strichcodeeinrichtung, die Sie vorher erstellt haben. Beachten Sie ab, dass das Strichcodeformat mit dem Format des eindeutigen Bezeichners für den Datensatz in Fertigung übereinstimmen muss. Für Entnahmerouten sollte das Strichcodeformat zum Beispiel mit dem Format der Entnahmeroutenreferenz übereinstimmen (üblicherweise ein Nummernkreis).  
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]