---
title: Strichcodetypen verwalten
description: Dieses Verfahren zeigt Ihnen, wie Sie eine neue Barcode-Definition festlegen, die dann als Teil des Berichts für die Kommissionierliste verwendet werden kann.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571112"
---
# <a name="maintain-bar-code-types"></a>Strichcodetypen verwalten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt Ihnen, wie Sie eine neue Barcode-Definition festlegen, die dann als Teil des Berichts für die Kommissionierliste verwendet werden kann. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Wenn Sie USMF verwenden, können Sie die Beispielswerte verwenden, die angezeigt werden. Diese Aufgaben werden normalerweise von einem Lagerortleiter ausgeführt.

1. Gehen Sie zu **Barcodes**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Barcode-Einrichtung** einen Wert ein.
1. Geben Sie im Feld **Beschreibung** einen Wert ein.
1. Wählen Sie im Feld **Barcode-Typ** eine Option.
    * Wenn Sie USMF verwenden, können Sie "Code 39" auswählen.
1. Geben Sie im Feld **Maskenkennung** die Kennung der Strichcodemaske an. Strichcodemasken werden verwendet, um Strichcodes erstellen und Strichcodes schnell erkennen, die in einem Verkaufsstellensystem (POS) gescannt werden. Einzelheiten finden Sie unter [Barcodemasken einrichten](../../../commerce/set-up-bar-code-masks.md).
1. Geben Sie im Feld **Größe** eine Zahl ein.
1. Geben Sie in das Feld **Maximale Länge** eine Zahl ein.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.
1. Gehen Sie zu **Parameter für Lager- und Lagerortverwaltung**.
1. Geben Sie im Feld **Barcode-Einrichtung** einen Wert ein oder wählen Sie ihn aus.
    * Wählen Sie die Einrichtung für den Barcode, die Sie zuvor erstellt haben, aber beachten Sie, dass das Format des Barcodes mit dem Format des eindeutigen Bezeichners für den verwendeten Datensatz übereinstimmen muss. Für Entnahmerouten sollte das Strichcodeformat zum Beispiel mit dem Format der Entnahmeroutenreferenz übereinstimmen (üblicherweise ein Nummernkreis).  
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
