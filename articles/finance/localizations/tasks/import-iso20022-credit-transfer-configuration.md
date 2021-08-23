---
title: ISO20022-Banküberweisungskonfiguration importieren
description: Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Kreditorenzahlung importieren.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffc86ba9dade0ae494ca4ace8d9f562da9c9527a4731493d892b60112293af3f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781135"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>ISO20022-Banküberweisungskonfiguration importieren

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]