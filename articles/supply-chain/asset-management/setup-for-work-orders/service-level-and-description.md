---
title: Service Level und Beschreibung
description: In diesem Thema werden Service Level und Beschreibung im Anlagenmanagement erläutert.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0aa23e7fe10e684e110126bd58bd761348e44700
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215492"
---
# <a name="service-level-and-description"></a>Service Level und Beschreibung

[!include [banner](../../includes/banner.md)]

 

Wenn Sie einen Arbeitsauftrag anlegen, möchten Sie möglicherweise die Service Levels für ihn definieren und ihm eine allgemeine Beschreibung hinzufügen. Sie können Service Level für Arbeitsaufträge auf der Seite **Service Level für Arbeitsaufträge** und Beschreibungen auf der Seite **Beschreibung für Arbeitsaufträge** anlegen.

## <a name="create-a-service-level"></a>Erstellen eines Service Levels

1. Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Aufträge** \> **Service Level**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Servicegrad** das Service Level (z.B. eine Nummer) ein.
4. Geben Sie im Feld **Name** einen Namen ein.

    Auf der Registerkarte **Arbeitsaufträge** FastTab können Sie erwartete Start- und Enddaten und -zeiten definieren. Die Felder auf dieser Schnellabfrage definieren den Zeitraum, in dem Arbeitsaufträge gestartet und beendet werden sollen. Sie werden für manuell angelegte Arbeitsaufträge und Arbeitsaufträge verwendet, die aufgrund von Wartungsanforderungen erstellt werden. 

5. Geben Sie im Feld **Starttag** eine Anzahl von Tagen ein, um den Zeitraum zu definieren, in dem der Arbeitsauftrag beginnen soll. Die Anzahl der Tage errechnet sich aus dem Erstellungsdatum des Arbeitsauftrags. Wenn der Arbeitsauftrag beispielsweise beim Erstellen beginnen soll, geben Sie **0** ein. Wenn der Arbeitsauftrag innerhalb einer Woche nach seiner Erstellung beginnen soll, geben Sie **7** ein.
6. Um eine Startzeit für den Arbeitsauftrag festzulegen, stellen Sie zusätzlich zu einem Startdatum die Option **Startzeit einstellen** auf **Ja**. Geben Sie dann die Startzeit in das Feld **Startzeit** ein. Wenn Sie die Option auf **Nein** setzen, wird die aktuelle Tageszeit verwendet.
7. Geben Sie im Feld **Endtag** eine Anzahl von Tagen ein, um den Zeitraum zu definieren, in dem der Arbeitsauftrag enden soll. Die Anzahl der Tage wird ab dem Startdatum des Arbeitsauftrags berechnet. Wenn der Arbeitsauftrag beispielsweise innerhalb einer Woche nach seinem Beginndatum enden soll, geben Sie **7** ein.
8. Um eine Endzeit für den Arbeitsauftrag festzulegen, stellen Sie zusätzlich zu einem Enddatum die Option **Endzeit einstellen** auf **Ja**. Geben Sie dann die Endzeit in das Feld **Endzeit** ein. Wenn Sie die Option auf **Nein** setzen, wird die aktuelle Tageszeit verwendet.
9. Wählen Sie **Speichern**.

![Seite „Arbeitsauftrags-Leistungsebene“](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Erstellen einer Beschreibung

1. Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Aufträge** \> **Beschreibungen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Beschreibung** die Beschreibung ein.
4. Wählen Sie **Speichern**.
