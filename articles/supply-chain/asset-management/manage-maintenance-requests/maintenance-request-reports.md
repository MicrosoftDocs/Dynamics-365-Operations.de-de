---
title: Wartungsanfrageberichte
description: In diesem Thema wird erläutert, wie Wartungsanfrageberichte in Asset Management erstellt werden.
author: josaw1
manager: tfehr
ms.date: 10/31/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5abb62e7f92f62d4635309625d765e1c081052eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428761"
---
# <a name="maintenance-request-reports"></a>Wartungsanfrageberichte

[!include [banner](../../includes/banner.md)]

 

In Asset Management können Sie zwei Berichte generieren, die sich auf Wartungsanfragen beziehen. Ein Bericht zeigt Details an, während der andere Bericht eine Liste bereitstellt, die für die Planung und Nachverfolgung verwendet werden kann.

## <a name="create-a-maintenance-request-details-report"></a>Erstellen eines Berichts zu Wartungsanfragedetails

Der Bericht **Wartungsanfragedetails** zeigt verschiedene Informationen, die sich auf Wartungsanfragen beziehen.

1. Wählen Sie **Anlagenverwaltung** \> **Berichte** \> **Wartungsanfragen** \> **Wartungsanfragedetails**.
2. Im Inforegister **Einzuschließende Datensätze** können Sie bestimmte Wartungsanfragen auswählen, die in den Bericht einbezogen werden sollen.
3. Im Inforegister **Im Hintergrund ausführen** können Sie die Berichterstellung bei Bedarf als Stapelverarbeitungsauftrag einrichten.
4. Klicken Sie auf **OK**, um den Bericht zu generieren.

Die folgende Abbildung zeigt ein Beispiel für den Bericht **Wartungsanfragedetails**.

![Wartungsanfrage-Detailbericht](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a>Erstellen eines Listenberichts zu Wartungsanfragen

Der Bericht **Wartungsanfragenliste** zeigt eine Liste aller Wartungsanfragen mit demselben Anfragetyp an.

1. Wählen Sie **Anlagenverwaltung** \> **Berichte** \> **Wartungsanfragen** \> **Wartungsanfragenliste**.
2. Im Inforegister **Einzuschließende Datensätze** können Sie Wartungsanfragen auswählen, die in den Bericht einbezogen werden sollen.
3. Im Inforegister **Im Hintergrund ausführen** können Sie die Berichterstellung bei Bedarf als Stapelverarbeitungsauftrag einrichten.
4. Klicken Sie auf **OK**, um den Bericht zu generieren.

Die folgende Abbildung zeigt ein Beispiel für den Bericht **Wartungsanfragenliste** für alle aktiven Wartungsanfragen.

![Wartungsanfrage-Listenbericht](media/10-manage-maintenance-requests.png)
