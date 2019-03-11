---
title: ISO20022-Direktbelastungskonfiguration importieren
description: Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Debitorenzahlung importieren.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1757a1477e46f71e327bb70cf4780767b7509e55
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333069"
---
# <a name="import-iso20022-direct-debit-configuration"></a>ISO20022-Direktbelastungskonfiguration importieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Debitorenzahlung importieren. Diese Verfahren verwendet das ISO 20022-Direktbelastungsformat als Beispiel. 



Dieses Verfahren wurde mithilfe des Demodatunternehmens DEMF erstellt, doch es kann ein beliebiges Demodatunternehmen verwenden, um diese Aufgabe abzuschließen.



Dies ist die erste von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Wählen Sie als Konfigurationsanbieter "Microsoft".
3. Klicken Sie auf "Als aktiv festlegen"
4. Klicken Sie auf Repositorys.
5. Klicken Sie auf "Öffnen".
6. Klicken Sie auf "Filter anzeigen".
7. Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert für "ISO20022 Direktbelastung (DE)" im Feld " Konfigurationsname" unter Verwendung des "begins with"-Filteroperators ein
    * Optional können Sie die Konfiguration in der Liste aufrufen, sie auswählen und diesen Schritt übergehen.  
8. Klicken Sie auf Import.
    * Wenn die Importschaltfläche nicht verfügbar ist, bedeutet dies, dass die Konfiguration bereits importiert wurde.  
9. Klicken Sie auf "Ja".

