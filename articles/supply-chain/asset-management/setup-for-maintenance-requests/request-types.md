---
title: Wartungsanfragetypen
description: In diesem Thema wird erläutert, wie Wartungsanfragetypen in Asset Management eingerichtet werden.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d353f084e0d3e056f1b5ff5af6437ba211def8ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428815"
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

![Seite „Wartungsanfragentypen“](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]