---
title: Aktivieren der verzögerten Steuerberechnung in der Erfassung
description: In diesem Thema wird erläutert, wie Sie die Funktion **Verzögerte Steuerberechnung in der Erfassung aktivieren** verwenden, um die Leistung der Steuerberechnung zu verbessern, wenn die Anzahl der Erfassungspositionen groß ist.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177871"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Aktivieren der verzögerten Steuerberechnung in der Erfassung
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion **Verzögerte Steuerberechnung in der Erfassung aktivieren** verwenden, um die Leistung der Steuerberechnung zu verbessern, wenn die Anzahl der Erfassungspositionen groß ist.

Das aktuelle Mehrwertsteuerberechnungsverhalten in der Erfassung wird in Echtzeit ausgelöst, wenn der Benutzer steuerbezogene Felder wie Mehrwertsteuergruppe/Artikel-Mehrwertsteuergruppe aktualisiert. Jede Aktualisierung auf Erfassungspositionsebene berechnet den Steuerbetrag für alle Erfassungspositionen neu. Dies ermöglicht ermöglicht dem Benutzer die Anzeige des in Echtzeit berechneten Steuerbetrags, kann jedoch auch zu Performanceproblemen führen, wenn die Anzahl der Erfassungspositionen groß ist.

Diese Funktion ermöglicht das Verzögern der Steuerberechnung, um Performanceproblem zu beheben. Wenn diese Funktion aktiviert ist, wird der Steuerbetrag nur dann berechnet, wenn Benutzer auf den Befehl „Mehrwertsteuer“ klickt oder die Erfassung bucht.

Der Benutzer kann den Parameter auf drei Ebenen aktivieren/deaktivieren:
- Nach juristischer Person
- Nach Erfassungsname
- Nach Erfassungskopf

Das System betrachtet den Parameterwert im Erfassungskopf als endgültig. Der Parameterwert im Erfassungskopf wird standardmäßig aus dem Erfassungsnamen entnommen. Der Parameterwert im Erfassungsnamen wird standardmäßig aus dem Hauptbuchparameter entnommen, wenn der Erfassungsname erstellt wird.

Die Felder „Tatsächlicher Mehrwertsteuerbetrag“ und „Berechneter Mehrwertsteuerbetrag“ in der Erfassung werden ausgeblendet, wenn dieser Parameter aktiviert ist. Auf diese Weise soll eine Verwirrung des Benutzers verhindert werden, da der Wert dieser beiden Felder immer 0 ist, bevor der Benutzer die Steuerberechnung auslöst.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Aktivieren der verzögerten Steuerberechnung nach juristischer Person

1. Wechseln Sie zu **Hauptbuch > Hauptbucheinstellungen > Hauptbuchparameter**.
2. Klicken Sie auf die Registerkarte **Mehrwertsteuer**.
3. Suchen Sie unter **Allgemeines** den Parameter **Verzögerte Steuerberechnung**, und aktivieren/deaktivieren Sie ihn.

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Aktivieren der verzögerten Steuerberechnung nach Erfassungsname

1. Wechseln Sie zu **Hauptbuch > Erfassung einrichten >Erfassungsnamen**.
2. Suchen Sie unter **Allgemeines** den Parameter **Verzögerte Steuerberechnung**, und aktivieren/deaktivieren Sie ihn.

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Aktivieren der verzögerten Steuerberechnung nach Erfassung

1. Wechseln Sie zu **Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen**.
2. Klicken Sie auf **Neu**.
3. Auswählen eines Erfassungsnamens
4. Klicken Sie auf **Einstellungen**.
5. Suchen Sie den Paramater **Verzögerte Steuerberechnung**, und aktivieren/deaktivieren Sie ihn.

![](media/delayed-tax-calculation-journal-header.png)
