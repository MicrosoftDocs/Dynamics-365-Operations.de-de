---
title: Systemgruppierung in einer offenen Arbeitsliste
description: "In diesem Thema wird beschrieben, wie die offenen Arbeitslisten auf einem mobilen Gerät gefiltert werden."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Systemgruppierung in einer offenen Arbeitsliste

[!include[banner](../includes/banner.md)]

Wenn Sie ein Systemgruppenfeld verwenden, können Sie eine offene Arbeitsliste filtern ohne dass Sie die die Menüoption des mobilen Geräts bearbeiten müssen.
Sofern dies zutrifft, funktioniert die Systemgruppierung zum Filtern einer Arbeitsliste auf einem einzelnen Arbeitskopffeld. Sie können die Systemgruppierung nicht verwenden, um online Ebenefelder zu filtern.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Systemgruppierung in einer offenen Arbeitsliste einrichten
Diese Schritte ausführen, um Systemgruppierung in einer offenen Arbeitsliste einzurichten.

-   Über eine Menüoption des mobilen Geräts wählen Sie **Modus: Indirekt** und **Aktivitäts-Code: Offene Arbeitsliste anzeigen** aus. Die folgenden Optionen sind verfügbar. Diese Optionen sind für die Systemgruppierung einer offenen Arbeitsliste erforderlich. 

| Mit der folgenden Option...        | Beschreibung   | 
| ------------- | ------------- |
| Systemgruppierung zulassen   | Aktiviert die Systemgruppierung für eine ausgewählte Arbeitslistenmenüoption.| 
| Systemgruppierungsfeld   | Verfügbar, wenn **Systemarbeit zulassen** auf **Ja** festgelegt ist. Wählen Sie das Feld aus, das bestimmt, wie Entnahmearbeit für die Arbeitskraft gruppiert wird. Wenn Sie beispielsweise das Feld **ShipmentId** auswählen, scannt die Arbeitskraft die Lieferkennung, um die Entnahmearbeit zu gruppieren. Alle Arbeit für die Lieferung wird dann der Arbeitskraft zugewiesen. Dieses Feld setzt voraus, dass Sie eine Menüoption erstellen, um vorhandene Arbeit zu nutzen, die vom System gruppiert wird. Verwenden Sie das Feld **Systemgruppierungsbeschriftung**, um die Arbeitskraft zu informieren, was zu scannen ist. |
| Systemgruppierungsbezeichnung   | Verfügbar, wenn **Systemarbeit zulassen** auf **Ja** festgelegt ist. Geben Sie die Information für den Arbeiter ein, was zu scannen ist, wenn Entnahmearbeit gruppiert wird. Wenn Sie beispielsweise das Feld **Lieferungs-ID** verwenden, um Entnahmearbeit nach Lieferung zu gruppieren, können Sie Lieferkennung in das Feld Lieferungs-ID eingeben. Dieses Feld setzt voraus, dass Sie eine Menüoption erstellen, um vorhandene Arbeit zu nutzen, die vom System gruppiert wird. Sie müssen auch das Feld auswählen, um nach **Systemgruppierung** zu gruppieren.|

