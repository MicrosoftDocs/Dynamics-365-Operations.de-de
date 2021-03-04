---
title: Freigeben von Produktionsaufträgen
description: Ein freigegebener Produktionsauftrag ist ein Auftrag, der für die Produktion autorisiert wurde. Der Begriff "Freigegeben" wird verwendet, um einen Status im Lebenszyklus eines Produktionsauftrags zu beschreiben, in dem der Produktionsauftrag für die Ausführung im Fertigungsbereich und für Lagerortprozesse verfügbar ist.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc6d53fc87bac2e23c0d1e67954be02749042004
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428981"
---
# <a name="release-production-orders"></a>Freigeben von Produktionsaufträgen

[!include [banner](../includes/banner.md)]

Ein freigegebener Produktionsauftrag ist ein Auftrag, der für die Produktion autorisiert wurde. Der Begriff "Freigegeben" wird verwendet, um einen Status im Lebenszyklus eines Produktionsauftrags zu beschreiben, in dem der Produktionsauftrag für die Ausführung im Fertigungsbereich und für Lagerortprozesse verfügbar ist. 

<a name="characteristics-of-the-released-state"></a>Merkmale des Status "Freigegeben"
-------------------------------------

Der Status **Freigegeben** ist ein Status im Lebenszyklus eines Produktionsauftrags. Produktionsaufträge, die sich im Status **Freigegeben** befinden, sind für die Ausführung im Fertigungsbereich und für Lagerortprozesse verfügbar. Der Status **Freigegeben** weist die folgenden Merkmale auf:

-   Ein Produktionsauftrag kann in den Status **Freigegeben** geändert werden, entweder aus dem Produktionsauftrag oder mithilfe eines Stapelverarbeitungsvorgangs. Der Produktionsauftrag kann auch aus geplanten Produktionsaufträgen automatisch aktualisiert werden, die umgewandelt werden, indem Sie das Feld **Sofortanlagezeitraum** auf der Seite **Produktprogrammplan** verwenden.
-   Der Status **Freigegeben** ist das Signal für die Bediener im Fertigungsbereich (Bediener), die Ausführung der Produktionseinzelvorgänge im Fertigungsbereich zu starten.
-   Produktionsunterlagen, wie Arbeitsplanlisten, Arbeitspläne und Listen zu Einzelvorgängen enthalten Informationen zu Produktionseinzelvorgängen und können ausgegeben werden.
-   Für Materialien, die physisch reserviert werden, wird Lagerortarbeit generiert, um Materialien für den Produktionsauftrag zu entnehmen.

## <a name="releasing-jobs-to-the-shop-floor"></a>Freigeben von Einzelvorgängen für die Fertigung
Nachdem ein Produktionsauftrag freigegeben ist, werden Produktionseinzelvorgänge, die dem Auftrag zugeordnet sind, angezeigt und sind zur Registrierung bereit. Die Operatoren Einzelvorgangserfassungen können, z.B. Start und stoppt Abschluss, entweder auf der **Einzelvorgangslistenterminal** Seite vornehmen oder die **Einzelvorgangslistengerät** Seite. Die erfasste Zeit und die Menge werden automatisch aus den Erfassungsseiten auf Produktionserfassungen übertragen, die verbrauchte Zeit und Menge zu verfolgen.

## <a name="route-cards"></a>Arbeitsplanlisten
Eine Arbeitsplanliste bietet einen Überblick über die Informationen aus den Einstellungen der Arbeitspläne und Arbeitsgänge sowie aus der Grob- und Feinterminierung.

## <a name="route-jobs"></a>Arbeitsplan-Einzelvorgänge
Ein Arbeitsplan führt alle Einzelvorgänge eines Arbeitsgangs detailliert auf und enthält Rüstzeit, Bearbeitungszeit, Wartezeit und Transportzeiten. Ein Arbeitsgang, wie etwa ein Anstrich, erfordert möglicherweise bestimmte Einzelvorgänge, wie Einrichtungszeit, Ausführungszeit für den Anstrichprozess und Wartezeit für das Trocknen.

## <a name="job-cards"></a>Einzelvorgangslisten
In einer Einzelvorgangsliste werden die jeweiligen Einzelvorgangsnummern eines bestimmten Arbeitsgangs aufgeführt. Ein Einzelvorgang wird auf jeder Seite dargestellt. Die in einer Einzelvorgangsliste enthaltenen Einzelvorgänge sowie deren geschätzte Zeiten stammen aus den Einstellungen für den Arbeitsplan sowie aus den Einstellungen für den Arbeitsgang. Von einer Einzelvorgangsliste können Sie die **Produktionserfassungspositionen**, Seite **Einzelvorgangslisten** öffnen. Für die Ausführung betrieblicher Ressourcen zuständige Personen haben die Möglichkeit zum Eingeben von Rückmeldungen bezüglich des Produktionsprozesses. Zu diesem Zweck stehen Felder für Verbrauchsstatistiken sowie für Informationen wie Ausschussmengen zur Verfügung.

## <a name="warehouse-work-for-raw-material-picking"></a>Lagerortarbeit für Rohmaterialentnahme
Arbeit für Rohmaterialentnahme wird während der Freigabe generiert. Vorgang wird nur für die Menge von Materialien generiert, die physisch für den Produktionsauftrag reserviert war, bevor der Auftrag verwendet wurde. Die folgende Einrichtung muss, um Lagerortarbeit für Rohmaterialentnahme zu generieren:

-   Eine Lagerplatzrichtlinie für die Rohmaterialentnahme, die bestimmt, an welchem Lagerort-Lagerplatz die Materialien zu entnehmen sind
-   Eine Wellenvorlage für Rohmaterialen, in denen Richtlinien für die Ausführung der Lagerortarbeit konfiguriert werden
-   Ein Lagerplatz für den Produktionswareneingang, der bestimmt, wo Materialien eingelagert werden






[!INCLUDE[footer-include](../../includes/footer-banner.md)]