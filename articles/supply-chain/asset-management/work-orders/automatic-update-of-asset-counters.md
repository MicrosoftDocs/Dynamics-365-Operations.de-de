---
title: Die automatische Aktualisierung von Anlagenzählern
description: In diesem Thema wird die automatische Aktualisierung von Anlagenzählern in Asset Management beschrieben.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875679"
---
# <a name="automatic-update-of-asset-counters"></a>Die automatische Aktualisierung von Anlagenzählern

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Im vorherigen Abschnitt wurde die manuelle Erfassung von Anlagenzählern beschrieben. Das Einrichten von Anlagenzählern wird unter [Zähler](../setup-for-objects/counters.md) beschrieben.

Zählerwerte können auch aus Produktionserfassungen automatisch aktualisiert werden, die auf Produktionsstunden oder Produktionsmenge basieren. Dies erfolgt unter **Anlagenzähler aktualisieren**. Sie können eine oder mehrere Anlagen aktualisieren, indem Sie den Parameter **Von Datum** einfügen. Dieser Parameter gibt das Startdatum für Produktionserfassungen (Stunden oder produzierte Menge) an, d. h. das Anfangsdatum, ab dem Zählerwerte aktualisiert werden sollen.

Alle Anlagen, die einer Ressource zugeordnet sind *und* Anlagenzähler enthalten, die so eingerichtet wurden, das sie basierend auf der erzeugten Menge oder den Produktionsstunden aktualisiert werden, werden in einer automatischen Aktualisierung berücksichtigt und neue Zählerwerte werden erstellt.

Bezüglich der Zähler, die auf der Produktionsmenge basieren, werden die Gutmenge sowie die erfasste Ausschussmenge in die Zählung einbezogen. Wenn die Einheit, die für die Erfassung der produzierten Menge verwendet wird, sich von der Einheit unterscheidet, die im Zähler verwendet wird, wird die Menge konvertiert, um der Zählereinheit zu entsprechen.

Wie bereits angegeben können automatische Zähler aus Produktionserfassungen aktualisiert werden. Daher muss die Anlage, für die Sie automatisch Zähler aktualisieren möchten, einer Ressource (Maschine) zugeordnet werden. Die folgenden Beschreibungen bieten einen Überblick über die Einstellungen und die Verarbeitung von Produktionsaufträgen (im Modul **Produktionssteuerung**), das als Grundlage für die automatische Aktualisierung von Zählern für eine Anlage im Modul **Anlagenverwaltung** verwendet wird.

Bei produzierte Mengen oder Produktionsstunden für die Ressource erfasst wurden, können Sie die zugehörigen Anlagenzähler aktualisieren.

1. Klicken Sie auf **Anlagenverwaltung** > **Periodisch** > **Anlagen** > **Anlagenzähler aktualisieren**.

2. Wählen Sie das Startdatum der automatischen Aktualisierung im Feld **Von Datum** aus.

>[!NOTE]
>Das Datum in diesem Feld ist das Datum „In Bearbeitung“ aus **Arbeitsplanbuchungen** (Feld **Produktionssteuerung** > **Abfragen und Berichte** > **Produktion** > **Arbeitsplanbuchungen** > **Physisches Datum**).

3. Wenn Sie bestimmte Anlagen, Anlagentypen oder Ressourcen auswählen möchten, klicken Sie auf **Filtern** auf dem Inforegister **Einzuschließende Datensätze** und nehmen die zutreffende Auswahl vor.

4. Bei Bedarf können Sie die automatische Aktualisierung als Batchauftrag auf dem Inforegister **Im Hintergrund ausführen** einrichten.

![Abbildung 1](media/12-work-orders.png)

5. Klicken Sie auf **OK**. Wenn die automatische Aktualisierung von Anlagenzählern erfolgt, können Sie die Zählererfassungen, die sich auf die Anlage beziehen, unter **Anlagenzähler** (**Anlagenverwaltung** > **Allgemein** > **Anlagen** > **Alle Anlagen** > Anlage auswählen > Schaltfläche **Zähler** auswählen).

Unter **Anlagenzählersummen** können Sie einen Überblick der letzten Erfassung abrufen, die für alle Zählertypen für alle Anlagen erstellt wurde. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Aggregierter Wert für Anlage**. Die Ansicht ist **Anlagenzähler** sehr ähnlich, aber Sie können in **Aggregierter Wert für Anlage** keine Erfassungen hinzufügen oder bearbeiten. Es ist nur für den Überblick.

![Abbildung 2](media/13-work-orders.png)


- Es ist trotzdem möglich, manuelle Zählerwerterfassungen für Zählertypen zu erstellen, die automatisch aktualisiert werden. Weitere Informationen finden Sie im Abschnitt „Die manuelle Aktualisierung von Anlagenzählern“.
- Sie können Zähler einrichten, die sich auf einen anderen beziehen Zähler, was bedeutet, dass, wenn ein Zähler aktualisiert wird, zugehörige Zähler automatisch gleichzeitig aktualisiert werden. Informationen zum Einrichten der zugehörigen Zähler finden Sie unter [Zähler](../setup-for-objects/counters.md).
