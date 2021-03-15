---
title: Fertigungsaufträge und Abschreibungen
description: In diesem Thema werden Arbeitsaufträge und Anlagen im Anlagenmanagement erläutert.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4eadbdc452a5b7d28adfa0f102a9a727faad3c07
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016702"
---
# <a name="work-orders-and-fixed-assets"></a>Fertigungsaufträge und Abschreibungen

[!include [banner](../../includes/banner.md)]


In der Anlagenbuchhaltung können Anlagen mit Anlagen verknüpft sein, und Sie können Arbeitsaufträge für diese Anlagen anlegen. Wenn Sie diese Funktionalität nutzen, können Sie sich im Modul **Projektverwaltung und Abrechnung** und im Modul **Anlage** in Microsoft Dynamics 365 for Finance and Operations einen vollständigen Überblick über die Anlage, die zugehörigen Investitionsprojekte und die auf den Investitionsprojekten erfassten Kosten verschaffen.

>[!NOTE]
>Das Feld **Anlagennummer** wird auf dem Arbeitsauftragsprojekt nur festgelegt, wenn als Projektart auf dem Arbeitsauftragsprojekt der Typ **Investition** ausgewählt ist.

Die folgende Abbildung veranschaulicht die Beziehung zwischen einem Investitionsprojekt im Modul **Projektverwaltung und Abrechnung** und einem Arbeitsauftragseinzelvorgangsprojekt.

![Abbildung 1](media/24-work-orders.png)

Die folgende Vorgehensweise beschreibt die Beziehung zwischen Anlagen, Arbeitsaufträgen, Arbeitsauftragsprojekten und Anlagen.

1. Sie erstellen eine Anlage, die Sie einer Anlage zuordnen.

![Abbildung 2](media/25-work-orders.png)

2. Wenn Sie Arbeitsauftragsarten einrichten auf der Seite **Arbeitsauftragstypen** (**Anlagenverwaltung** > **Einrichtung** > **Arbeitsaufträge** > **Arbeitsauftragstypen**), legen Sie eine Arbeitsauftragsart für die Investitionsabwicklung an. Siehe auch [Arbeitsauftragsarten](../setup-for-work-orders/work-order-types.md).

![Abbildung 3](media/26-work-orders.png)

3. Wenn Sie Projektgruppen für Arbeitsaufträge auf der Registerkarte **Projektgruppe** der Seite **Arbeitsauftrags-Projekteinstellungen** (**Anlagenverwaltung** > **Einrichtung** > **Arbeitsaufträge** > **Projekteinrichtung**) einrichten, stellen Sie eine Beziehung zwischen der für Investitionen verwendeten Arbeitsauftragsart und der Projektgruppe her, die auf der Seite **Projektgruppen** im Modul **Projektverwaltung und -verrechnung** (**Projektverwaltung und -verrechnung** > **Einrichtung** > **Buchung** > **Projektgruppen**) erstellt wurde.

![Abbildung 4](media/27-work-orders.png)

4. Wenn Sie einen Arbeitsauftrag anlegen, der sich auf eine Anlagen bezieht, wählen Sie die Arbeitsauftragsart, die für die Abwicklung von Investitionen verwendet wird, z.B. **Investition**.

5. Wenn der Arbeitsauftrag angelegt wird, wird die zugehörige Arbeitsauftragsart auf der Seite **Alle Arbeitsaufträge** angezeigt.

![Abbildung 5](media/28-work-orders.png)

6. Wenn der Arbeitsauftrag erstellt wird, wird das Projekt, das dem Arbeitsauftrag zugeordnet ist, auf der Seite **Alle Projekte** im Modul **Projektverwaltung und -verrechnung** erstellt (**Projektverwaltung und -verrechnung** > **Projekte** > **Alle Projekte**). Um projektbezogene Informationen anzuzeigen, wählen Sie den Link im Feld **Projektkennung** auf der Registerkarte **Allgemein** auf dem Inforegister **Positionsdetails** in der Detailansicht der Seite **Alle Arbeitsaufträge** im Modul **Anlagenverwaltung** aus (**Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge**).

![Abbildung 6](media/29-work-orders.png)

7. Um einen Überblick der Projekte anzuzeigen, die einer Anlage zugeordnet sind, wählen Sie **Anlagen** > **Anlagen** > **Anlagen** und dann im Feld **Anlagennummer** den Link für die Anlage aus, um die Detailansicht zu öffnen. Erweitern Sie den Bereich **Zugehörige Informationen** auf der rechten Seite der Seite, und wählen Sie das Inforegister **Zugeordnete Projekte** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]