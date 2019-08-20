---
title: Anlagenansicht
description: In diesem Thema wird die Anlagenansicht in Asset Management beschrieben.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63e5ec5b2a47706763df8105932d722986535a9b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783291"
---
# <a name="asset-view"></a>Anlagenansicht

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In diesem Thema wird die Anlagenansicht in Asset Management beschrieben. Die Seite **Anlagenansicht** enthält aktive Anlagen und funktionale Standorte in einer Baumstruktur. Auf diese Weise erhalten Sie eine schnelle Übersicht über die Anlagenbeziehungen zu funktionalen Standorten. Zudem können Sie detaillierte Informationen über funktionale Standorte, Anlagen und die zugehörigen Stücklisten (BOMs) anzeigen. Darüber hinaus erhalten Sie einen schnellen Überblick über die aktiven Wartungsanfragen und Arbeitsaufträge, die einer Anlage zugeordnet sind.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Anlagenansicht**.
2. Um die Ansicht auf der Seite zu ändern, wählen Sie einen neuen Wert im Feld **Ansicht** aus.

    > [!NOTE]
    > Die Standardansicht, die angezeigt wird, wenn Sie die Seite **Anlagenansicht** öffnen, hängt von dem Wert ab, der im Feld **Ansicht** auf der Registerkarte **Anlagen** der Seite **Anlagenverwaltungsparameter** aktiviert ist (**Anlagenverwaltung** \> **Einstellungen** \> **Anlagenverwaltungsparameter**).

Rechts auf der Seite zeigen Inforegister Details der ausgewählten Ansicht an.

Die Breadcrumb-Spur, die über der Strukturansicht angezeigt wird, zeigt die aktuelle Auswahl in der Strukturansicht an. Diese Breadcrumb-Spur verwendet das folgende Format:

Kennung des funktionalen Standorts/Kennung des funktionalen Standorts (falls es mehr als einen funktionalen Standort gibt) \> Anlagenkennung/Anlagenkennung (falls es mehr als eine Anlage gibt) – Artikelnummer.

Wenn Sie eine Anlage in der Baumstruktur ausgewählt haben, können Sie **Aktive Anfragen** oder **Aktive Arbeitsaufträge** auswählen, um die Wartungsanfragen oder die Arbeitsaufträge anzuzeigen, die der Anlage zugeordnet sind. Sie können auch **Öffnen** \> **Funktionaler Standort**, **Anlage** oder **Anlagenstückliste** auswählen, um die zugehörige Ansicht zu öffnen.

Die Option **Funktionale Standorte der Anlage**, die Sie im Feld **Ansicht** auswählen können, ist ebenfalls bei jeder Anlagensuche verfügbar, in der Sie eine Anlage auswählen können. Die Strukturansicht wird auf einer Registerkarte **Anlagenansicht** angezeigt, auf der Sie beispielsweise [eine Anlage erstellen](../objects/create-an-object.md), eine Wartungsanfrage erstellen oder einen Arbeitsauftrag erstellen.