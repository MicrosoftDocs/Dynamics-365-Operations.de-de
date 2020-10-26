---
title: Aktivieren der verzögerten Steuerberechnung in Erfassungen
description: In diesem Thema wird erläutert, wie Sie die Funktion Verzögerte Steuerberechnung aktivieren, um die Leistung der Steuerberechnung zu verbessern, wenn die Anzahl der Erfassungspositionen groß ist.
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
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d4ce0343ac766b30d532be0866a381dc520fd462
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977142"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Aktivieren der verzögerten Steuerberechnung in Erfassungen
[!include [banner](../includes/banner.md)]


In diesem Thema wird erläutert, wie Sie die Mehrwertsteuerberechnung in Erfassungen verzögern können. Diese Funktion kann die Leistung von Steuerberechnungen verbessern, wenn viele Erfassungspositionen vorhanden sind.

Standardmäßig werden Mehrwertsteuerbeträge in Erfassungspositionen berechnet, sobald steuerbezogene Felder aktualisiert werden. Diese Felder enthalten die Felder für Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen. Jede Aktualisierung einer Erfassungsposition führt dazu, dass Steuerbeträge für alle Erfassungspositionen neu berechnet werden. Obwohl dieses Verhalten Benutzern hilft, Steuerbetragsberechnungen in Echtzeit anzuzeigen, kann es sich auch auf die Leistung auswirken, wenn die Anzahl der Erfassungspositionen sehr groß ist.

Mit der Funktion Verzögerte Steuerberechnung können Sie die Steuerberechnung für Erfassungen verzögern und damit Leistungsprobleme beheben. Wenn diese Funktion aktiviert ist, werden Steuerbeträge nur dann berechnet, wenn ein Benutzer **Mehrwertsteuer** auswählt oder die Erfassung bucht.

Sie können die Berechnung der Mehrwertsteuer auf drei Ebenen verzögern:

- Juristische Person
- Journal
- Erfassungskopf

Das System gibt der Einrichtung für den Erfassungskopf Vorrang. Standardmäßig wird diese Einstellung aus dem Journal übernommen. Standardmäßig wird die Einstellung für das Journal aus der Einstellung auf der Seite **Hauptbuchparameter** übernommen, wenn das Journal erstellt wird. In den folgenden Abschnitten wird erklärt, wie eine verzögerte Steuerberechnung für juristische Personen, Journale und Erfassungsköpfe aktiviert wird.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Aktivieren der verzögerten Steuerberechnung auf der Ebene der juristische Person

1. Wechseln Sie zu **Hauptbuch \> Sachkonto-Einstellungen \> Hauptbuchparameter**.
2. Legen Sie auf der Registerkarte **Mehrwertsteuer** im Inforegister **Allgemein** die Option **Verzögerte Steuerberechnung** auf **Ja** fest.

![Hauptbuchparameter – Bild](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Aktivieren der verzögerten Steuerberechnung auf der Ebene des Journals

1. Wechseln Sie zu **Hauptbuch \> Erfassungseinstellungen \> Journale**.
2. Legen Sie im Inforegister **Allgemein** im Abschnitt **Mehrwertsteuer** die Option **Verzögerte Steuerberechnung** auf **Ja** fest.

![Journale – Bild](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Aktivieren der verzögerten Steuerberechnung auf der Ebene des Erfassungskopfes

1. Wechseln Sie zu **Hauptbuch \> Journaleinträge \> Allgemeine Erfassungen**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie ein Journal aus.
4. Legen Sie auf der Registerkarte **Einstellungen** die Option **Verzögerte Steuerberechnung** auf **Ja** fest.

![Allgemeine Erfassung – Seitenbild](media/delayed-tax-calculation-journal-header.png)
