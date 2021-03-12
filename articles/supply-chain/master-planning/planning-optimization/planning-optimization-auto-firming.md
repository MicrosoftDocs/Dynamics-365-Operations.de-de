---
title: Automatische Umwandlung mit Planungsoptimierung
description: In diesem Abschnitt wird erläutert, wie Sie die automatische Fixierung mit der Planungsoptimierung verwenden.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: d014fcd542462e092f6e88232dff8fd5ee2253c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963459"
---
# <a name="autofirming-with-planning-optimization"></a>Automatische Umwandlung mit Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Mit der automatischen Fixierung können Sie Planaufträge im Rahmen des Masterplanungsprozesses fixieren (d.h. freigeben). Wenn Planaufträge fixiert werden, werden sie in Ist-Bestellungen, Transportaufträge oder Fertigungsaufträge umgewandelt. Bei der Planungsoptimierung werden Planaufträge während eines Masterplanungslaufs fixiert, wenn das Auftragsdatum (d.h. das Startdatum) innerhalb des Zeitfensters für die Fixierung liegt.

> [!NOTE]
> Die automatische Bestätigung einer geplanten Bestellung kann nur erfolgen, wenn die Position einem Lieferanten zugeordnet ist.

## <a name="turn-on-autofirming"></a>Automatische Umwandlung

Um die automatische Bestätigung einzuschalten, gehen Sie wie folgt vor.

1. Wählen Sie im Arbeitsbereich **Feature-Management** auf der Registerkarte **Neu** **Automatische Umwandlung zur Planungsoptimierung** in der Liste. Wenn die Funktion nicht auf der Registerkarte **Neu** erscheint, schauen Sie auf die Registerkarten **Nicht aktiviert** und **Alle**.
1. Wählen Sie **Jetzt aktivieren**. Alternativ können Sie auch **Terminplanung** wählen und dann die Zeit auswählen, zu der die Funktion eingeschaltet werden soll.

## <a name="set-up-the-firming-time-fence"></a>Den Fixierzeitanschlag einrichten

Der Fixierungszeitrahmen wird aus dem Laufdatum der Masterplanung vorwärts berechnet. Sie wird durch die Anzahl der Tage definiert, die Sie eingeben. Sie können den Fixierungszeitanschlag wie folgt steuern:

- Um den voreingestellten Fixierungszeitrahmen für eine Deckungsgruppe zu definieren, gehen Sie zu **Masterplanung** \> **Einrichtung** \> **Deckung** \> **Deckungsgruppen** und wählen eine Deckungsgruppe aus. Geben Sie dann auf der Registerkarte **Anderes** Inforegister im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.
- Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe eines bestimmten Artikels definiert ist, gehen Sie zu **Produktinformationsmanagement** \> **Freigegebene Produkte**, wählen Sie dann aus dem Aktionsbereich **Plan** und wählen Sie dann **Artikelabdeckung**. Wählen Sie dann auf der Registerkarte **Allgemein** **Überschreibungszeitraum** und geben Sie im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.
- Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe und die Artikelabdeckung für einen bestimmten Produktionsplan definiert ist, gehen Sie zu **Masterplanung** \> **Setup** \> **Masterpläne** und wählen Sie einen Produktionsplan. Legen Sie dann auf dem Inforegister **Zeitfenster in Tagen** **Bestätigen** auf **Ja** fest und geben Sie die Anzahl der Tage ein.

Wenn die Automatische Umwandlung für eine Produktprogrammplanung, die die Planungsoptimierung verwendet, eingeschaltet ist, wird der Automatische Umwandlung-Prozess gemäß dem Automatische-Umwandlung-Setup durchgeführt. Wenn Automatische Umwandlung nicht eingeschaltet ist oder wenn die Planung von der Seite **Netzanforderungen** aus gestartet wird, wird der Automatische Umwandlung-Vorgang übersprungen.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Planungsoptimierung im Vergleich zur integrierten Supply Chain Management Planungs-Engine

Sowohl die Planungsoptimierung als auch die in Microsoft Dynamics 365 Supply Chain Management eingebaute Planungs-Engine können zur automatischen Bestätigung von Planaufträgen verwendet werden. Jedoch gibt es mehrere wichtige Unterschiede. Während die Planungsoptimierung beispielsweise anhand des Auftragsdatums (d.h. des Startdatums) ermittelt, welche Planaufträge zu fixieren sind, verwendet die integrierte Supply Chain Management Planungs-Engine das Bedarfsdatum (d.h. das Enddatum). Hier ist eine Zusammenfassung der Unterschiede.

**Planungsoptimierung**

- Die automatische Bestätigung basiert auf dem Auftragsdatum (Startdatum).
- Da das Auftragsdatum (Startdatum) die Fixierung auslöst, müssen Sie die Durchlaufzeit nicht als Teil des Fixierungszeitfensters betrachten.
- Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen eine Woche betragen.

**Integrierte Supply Chain Management Planungs-Engine**

- Die automatische Bestätigung basiert auf dem Bedarfsdatum (Enddatum).
- Um eine rechtzeitige Auftragsfeststellung zu gewährleisten, muss der Fixierungszeitrahmen länger als die Vorlaufzeit sein.
- Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen die Durchlaufzeit plus eine Woche sein.
