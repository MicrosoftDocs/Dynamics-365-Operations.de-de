---
title: ISO20022-Banküberweisungskonfiguration importieren
description: Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Kreditorenzahlung importieren.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848790"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>ISO20022-Banküberweisungskonfiguration importieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Kreditorenzahlung importieren. Das deutsche ISO 20022-Banküberweisungsformat wird als Beispiel verwendet. Diese Prozedur kann für andere verfügbare elektronisches Berichterstellungsformat verwendet werden. 

Diese Aufgabe wurde mithilfe des Demodatunternehmens DEMF erstellt, doch es kann ein beliebiges Demodatunternehmen verwenden, um diese Aufgabe abzuschließen.

Dies ist der erste von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Wählen Sie als Konfigurationsanbieter "Microsoft".
3. Klicken Sie auf "Als aktiv festlegen"
4. Klicken Sie auf Repositorys.
5. Klicken Sie auf "Öffnen".
6. Klicken Sie auf "Filter anzeigen".
7. Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert für "ISO20022 Kreditübertragung (DE)" im Feld " Konfigurationsname" unter Verwendung des "begins with"-Filteroperators ein
    * Oder Sie suchen die Konfiguration in der Liste, wählen diese aus und verschieben sie zur Importaufgabe.  
8. Klicken Sie auf Import.
    * Wenn die Importschaltfläche nicht verfügbar ist, bedeutet dies, dass die Konfiguration bereits importiert wurde.  
9. Klicken Sie auf "Ja".

