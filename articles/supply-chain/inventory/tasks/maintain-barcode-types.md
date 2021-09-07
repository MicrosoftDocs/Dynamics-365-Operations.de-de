---
title: Strichcodetypen verwalten
description: Dieses Verfahren zeigt Ihnen, wie Sie eine neue Barcode-Definition festlegen, die dann als Teil des Berichts für die Kommissionierliste verwendet werden kann.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 052311e15aeb20b927cbed217a2bda600dad60a5
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345649"
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
1. Geben Sie im Feld **Größe** eine Zahl ein.
1. Geben Sie in das Feld **Maximale Länge** eine Zahl ein.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.
1. Gehen Sie zu **Parameter der Bestands- und Lagerortverwaltung**.
1. Geben Sie im Feld **Barcode-Einrichtung** einen Wert ein oder wählen Sie ihn aus.
    * Wählen Sie die Einrichtung für den Barcode, die Sie zuvor erstellt haben, aber beachten Sie, dass das Format des Barcodes mit dem Format des eindeutigen Bezeichners für den verwendeten Datensatz übereinstimmen muss. Für Entnahmerouten sollte das Strichcodeformat zum Beispiel mit dem Format der Entnahmeroutenreferenz übereinstimmen (üblicherweise ein Nummernkreis).  
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]