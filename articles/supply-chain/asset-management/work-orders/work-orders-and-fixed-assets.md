---
title: Fertigungsaufträge und Abschreibungen
description: In diesem Thema werden Arbeitsaufträge und Anlagen im Anlagenmanagement erläutert.
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
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250828"
---
# <a name="work-orders-and-fixed-assets"></a>Fertigungsaufträge und Abschreibungen


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


In der Anlagenbuchhaltung können Anlagen mit Anlagen verknüpft sein, und Sie können Arbeitsaufträge für diese Anlagen anlegen. Wenn Sie diese Funktionalität nutzen, können Sie sich im Modul **Projektverwaltung und Abrechnung** und im Modul **Anlage** einen vollständigen Überblick über die Anlage, die zugehörigen Investitionsprojekte und die auf den Investitionsprojekten erfassten Kosten verschaffen.

>[!NOTE]
>Das Feld **Anlagennummer** wird auf dem Arbeitsauftragsprojekt nur ausgefüllt, wenn als Projektart auf dem Arbeitsauftragsprojekt der Typ „Investition“ ausgewählt ist.

![Abbildung 1](media/24-work-orders.png)

Die folgende Vorgehensweise beschreibt die Beziehung zwischen Anlagen, Arbeitsaufträgen, Arbeitsauftragsprojekten und Anlagen.

1. Sie legen eine Anlage an, die Sie auf eine Anlage beziehen, wie in der folgenden Abbildung dargestellt.

![Abbildung 2](media/25-work-orders.png)

2. Wenn Sie Arbeitsauftragsarten einrichten (**Anlagenmanagement** > **Einrichtung** > **Aufträge** > **Auftragsarten**), legen Sie eine Arbeitsauftragsart für die Investitionsabwicklung an. Siehe auch [Arbeitsauftragsarten](../setup-for-work-orders/work-order-types.md).

![Abbildung 3](media/26-work-orders.png)

3. Wenn Sie Projektgruppen für Arbeitsaufträge einrichten (**Anlagenmanagement** > **Setup** > **Arbeitsaufträge** > **Projekteinrichtung** > **Projektgruppe** Link), stellen Sie eine Beziehung zwischen der für Investitionen verwendeten Arbeitsauftragsart und der für Investitionen angelegten Projektgruppe im Modul **Projektmanagement und Rechnungswesen** her (**Projektmanagement und Rechnungswesen** > **Einrichtung** > **Buchung** > **Projektgruppen**).

![Abbildung 4](media/27-work-orders.png)

4. Wenn Sie einen Arbeitsauftrag anlegen, der sich auf ein Anlagenobjekt bezieht, wählen Sie die Arbeitsauftragsart, die für die Abwicklung von Investitionen verwendet wird, z.B. „Investition“.

5. Wenn der Arbeitsauftrag angelegt wird, wird die zugehörige Arbeitsauftragsart unter **Alle Arbeitsaufträge** angezeigt.

![Abbildung 5](media/28-work-orders.png)

6. Wenn der Arbeitsauftrag angelegt wird, wird das auf den Arbeitsauftrag bezogene Projekt in **Projektverwaltung und Abrechnung** > **Alle Projekte** angelegt. Projektbezogene Informationen erhalten Sie, wenn Sie auf den Link **Projekt-ID** auf den Arbeitsauftrag klicken (in **Anlagenmanagement**, öffnen Sie den Arbeitsauftrag in der Detailansicht > **Zeilendetails** FastTab > **Allgemein** Registerkarte > **Projekt-ID** Feld).

![Abbildung 6](media/29-work-orders.png)

7. Unter **Abschreibung** erhalten Sie eine Übersicht über die mit einer Anlage verbundenen Projekte (**Abschreibung** > **Abschreibung** > **Abschreibung** > Klicken Sie auf die Anlage im Feld **Anlagennummer** > sehen Sie die Inhalte im Abschnitt **Verwandte Informationen** Bereich > **Verbundene Projekte**).

