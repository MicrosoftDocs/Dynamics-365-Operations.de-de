---
title: Wartungsanfragentypen
description: In diesem Artikel wird erläutert, wie Wartungsanfragetypen in Anlagenverwaltung eingerichtet werden.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a2d707cc9c0aa4863968651a8434883cc1322eb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888700"
---
# <a name="maintenance-request-types"></a>Wartungsanfragetypen

[!include [banner](../../includes/banner.md)]

 

Wartungsanfragetypen werden verwendet, um Wartungsanfragen zu kategorisieren. Sie können beispielsweise Wartungsanfragetypen haben, die sich auf vorbeugende Wartung und korrektive Wartung beziehen. Oder Sie haben möglicherweise einen speziellen Wartungsanfragetyp, der verwendet wird, um die Reparatur von Anlagen (Depotreparatur) zu verwalten.

Ein Wartungsanfragetyp definiert die Zuordnung zu einer Wartungsanfrage-Lebenszyklusstatusgruppe (Wartungsanfrage-Lebenszyklusmodell). Wartungsanfrage-Lebenszyklusmodelle definieren die Lebenszyklusstatus, die für eine Wartungsanfrage festgelegt werden können. (Beispiele für Wartungsanfrage-Lebenszyklusstatus sind **Erstellt**, **Aktiv** und **Beendet**.)

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Wartungsanfragen** \> **Wartungsanfragetypen**.
2. Wählen Sie **Neu** aus, um einen Wartungsanfragetyp zu erstellen.
3. Geben Sie im Feld **Wartungsanfragetyp** eine Kennung für den Wartungsanfragetyp ein.
4. Geben Sie im Feld **Name** einen Namen ein.
5. Wählen Sie auf dem Inforegister **Allgemein** im Feld **Wartungsanfrage-Lebenszyklusmodell** ein Wartungsanfrage-Lebenszyklusmodell aus.
6. Wählen Sie im Feld **Arbeitsauftragstyp** einen Arbeitsauftragstyp aus. Wenn eine Wartungsanfrage in einen Arbeitsauftrag konvertiert wird, erhält der Arbeitsauftrag automatisch den Arbeitsauftragstyp aus, der dem Wartungsanfragetyp zugeordnet ist.

Die folgende Abbildung zeigt ein Beispiel der Seite **Wartungsanfragetypen**.

![Seite „Wartungsanfragentypen“.](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]