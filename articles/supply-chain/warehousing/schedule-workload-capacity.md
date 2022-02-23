---
title: Arbeitsauslastungskapazität planen
description: In diesem Thema wird erläutert, wie Sie die Auslastung der Mitarbeiter in einem Lager oder für ein ganzes Lager einrichten und einplanen.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8db243949b2aeee0a8263276234d439652905449
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965576"
---
# <a name="schedule-workload-capacity"></a>Arbeitsauslastungskapazität planen

[!include[banner](../includes/banner.md)]

Sie können die Arbeitsauslastungskapazität für Lagerorte planen und auch die aktuelle und zukünftige Arbeitsauslastungen für die Arbeitskräfte in einzelnen Lagerorten prognostizieren. Sie können die Arbeitsauslastung für das gesamte Lager prognostizieren, oder Sie können die Arbeitsauslastung für ein- und ausgehende Arbeitsauslastungen separat prognostizieren.

Um Arbeitsauslastung das Projekt für ausgewählte Lagerorte zu prognostizieren, müssen Produktprogrammplanungslaufdaten für die ausgewählten Lagerorte verfügbar sein. Weitere Informationen finden Sie unter [Masterplanübersicht](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Arbeitsauslastungen für einen Lagerort planen und anzeigen

Um die Arbeitsauslastungskapazität für einen Lagerort zu planen, erstellen Sie eine Arbeitsauslastungseinstellung für einen oder mehrere Lagerorte, und ordnen die Arbeitsauslastungseinstellung einem Produktprogrammplan zu. In der Arbeitsauslastungskapazitätseinstellung können Sie Limits für Paletten, Gewicht oder Volumen für ein- und ausgehende Transaktionen definieren. Sie können auch mehr als eine Einrichtung für jeden Lagerort erstellen, und dann die Einstellung einzelnen Produktprogrammplänen zuordnen. Sie können diesen Ansatz beispielsweise verwenden, um saisonale Veränderungen in der Belegschaft zu berücksichtigen.

Wenn die Arbeitskräfte für einen Lagerort mit Buchungen für ein- und ausgehende Arbeitsauslastungen arbeiten, können Sie die Lagerortkapazitätseinstellung so konfigurieren, dass die Arbeitsauslastung in einer kombinierten Ansicht geplant wird.

Um Arbeitsauslastungen für Lagerorte zu planen und anzuzeigen, müssen Sie die folgenden Aufgaben ausführen:

1. Erstellen Sie eine Arbeitsauslastungskapazitätseinstellung und definieren Sie Arbeitsauslastungskapazitätsgrenzen für einen oder mehrere Lagerorte.
2. Ordnen Sie die Arbeitsauslastungskapazitätseinstellung einem Produktprogrammplan zu, um Arbeitsauslastungsprojektionen zu erstellen und anzugeben, wie lange die Prognosen gelten.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Erstellen einer Arbeitsauslastungskapazitätseinstellung für einen Lagerort

1. Wählen Sie **Lagerverwaltung** \> **Einrichten** \> **Lagerortüberwachung** \> **Arbeitsauslastungskapazität**.
2. Wählen Sie im Aktionsbereich **Neu**, um eine Konfiguration der Arbeitslastkapazität zu erstellen.
3. Wählen Sie auf dem Inforegister **Lagerorte** die Option **Neu**, und geben Sie dann in der Zeile Werte ein, um ein Lager mit der Einstellung der Auslastung zu verknüpfen.
4. Aktivieren Sie das Kontrollkästchen **Kombinierte ein- und ausgehende Arbeitsauslastung**, wenn der Bericht **Arbeitsauslastungskapazität** die Gesamtlast für eingehende und ausgehende Transaktionen in einer Ansicht anzeigen soll.
5. Wählen Sie auf dem Inforegister **Transaktionsarten** die Arten von ein- und ausgehenden Transaktionen aus, für die die Arbeitslastgrenzen gelten sollen.

    > [!NOTE]
    > Sie müssen sowohl für die eingehende als auch für die ausgehende Arbeitslast mindestens eine Transaktionsart auswählen.

#### <a name="define-limits-for-volume-or-weight"></a>Grenzen für Volumen oder Gewicht festlegen

Sie können Limits für Volumen oder Gewicht einrichten, je nachdem, welche Limits für die Lagerbelegschaft relevant sind. Die Limits, die Sie angeben, sind in der Lastprognose enthalten, die Sie im Bericht **Arbeitsauslastung** einsehen können.

Um Informationen zu Volumen und Gewicht für Artikel zu prognostizieren, müssen Lagerartikel, Volumen eines Lagerartikels und Gewicht eines Lagerartikels für alle Produkte spezifiziert werden. Die erforderlichen Felder sind in den folgenden Feldgruppen auf dem Inforegister **Lagerbestand verwalten** der Seite **Details für freigegebene Produkte** verfügbar:

- Handhabung
- Physische Dimensionen
- Gewichtsmessungen

Wenn diese Informationen nicht korrekt angegeben sind, erhalten Sie eine Meldung, wenn Sie den Bericht zur **Arbeitsauslastungskapazität** generieren. Aus dem Bericht heraus können Sie dann die fehlenden Informationen aufschlüsseln, die für die Projektion der zukünftigen Arbeitsbelastung erforderlich sind.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Zuordnen einer Arbeitsauslastungskapazitätseinstellung zu einer Produktprogrammplanung

1. Wählen Sie **Lagerverwaltung** \> **Periodisch** \> **Arbeitslast planen**.
2. Wählen Sie im Feld **Masterplan** den Masterplan aus, der für die Arbeitslastprognose verwendet werden soll.
3. Geben Sie im Feld **Anzahl Tage** die Anzahl der Tage an, die die Arbeitslastprognose abdeckt.
4. Wählen Sie im Feld **Arbeitslast** die Arbeitslast, die mit dem Masterplan verknüpft werden soll.

### <a name="view-workload-capacity"></a>Arbeitsauslastungskapazität anzeigen

1. Wählen Sie **Lagerverwaltung** \> **Anfragen und Berichte** \> **Physische Bestandsberichte** \> **Arbeitsauslastungskapazität**.
2. Geben Sie im Feld **Anzahl der Spalten** die Anzahl der Spalten an, die im Bericht angezeigt werden sollen.
3. Wählen Sie im Feld **Auftragsart** die Option **Geplant und bestätigt**, **Geplant** oder **Bestätigt**, um die Art der zu projizierenden Aufträge auf dem Bericht anzugeben.
4. Wählen Sie im Feld **Auslastungstyp** eine Auslastungstyp aus, um festzulegen, ob die Auslastungskapazität für Volumen oder Gewicht hochgerechnet werden soll.
5. Wählen Sie im Feld **Arbeitslastkapazität** eine Auslastungskapazitätseinstellung aus.
