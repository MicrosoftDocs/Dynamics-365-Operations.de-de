---
title: Arbeitsaufträge aus Wartungsanfragen erstellen
description: In diesem Thema wird erläutert, wie Sie einen Wartungsauftrag aus einer Wartungsanfrage in der Anlagenverwaltung erstellen.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
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
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428764"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Arbeitsaufträge aus Wartungsanfragen erstellen

[!include [banner](../../includes/banner.md)]

 


Nachdem Sie Wartungsanforderungen erstellt haben, können Sie sie ohne Weiteres in Arbeitsaufträge umwandeln. In diesem Thema wird die schnellste Methode beschrieben, um mit Wartungsanfragen zu arbeiten, mehrere Wartungsanfragen gleichzeitig zu aktualisieren und dann einen Arbeitsauftrag für mehrere Wartungsanfragen zugleich zu erstellen. Auf der Seite **Aktive Wartungsanfragen** oder **Meine Wartungsanfragen für funktionale Standorte** können Sie auch mit jeweils einer Wartungsanfrage arbeiten und eine Wartungsanfrage in einen Arbeitsauftrag umwandeln.

> [!NOTE]
> Jede Wartungsanfrage kann sich nur auf einen Arbeitsauftrag beziehen. Allerdings können mehrere Wartungsanfragen in einen Arbeitsauftrag aufgenommen werden, selbst wenn die Wartungsanfragen über verschiedene Anlagen verfügen.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Wartungsanfragen** \> **Alle Wartungsanfragen**.
2. Bevor Sie einen Arbeitsauftrag aus Wartungsanfragen erstellen können, müssen Sie mindestens einen Wartungsauftragstyp für die Wartungsanfragen sowie eine Wartungsauftragstypvariante und eine Facharbeit auswählen, wenn diese Informationen relevant sind. In der Rasteransicht können Sie Informationen für eine Wartungsanfrage leicht aktualisieren.
3. Wenn Sie bereit sind, einen Arbeitsauftrag zu erstellen, wählen Sie die Wartungsanfragen aus, die darin enthalten sein sollen.

    - Wenn Sie mehrere Wartungsanfragen auswählen, um diese in einen Arbeitsauftrag umzuwandeln, müssen die Felder **Anlage** und **Wartungsauftragstyp** gefüllt werden, bevor Sie den Arbeitsauftrag erstellen können.
    - Wenn Sie eine Wartungsanfrage auswählen, um diese in einen Arbeitsauftrag umzuwandeln, muss nur das Feld **Anlage** festgelegt werden, bevor Sie den Arbeitsauftrag erstellen. Wenn Sie jedoch den Arbeitsauftrag erstellen, können Sie einen Wartungsauftragstyp (sowie eine zugehörige Wartungsauftragstypvariante und eine Facharbeit, wenn diese Informationen relevant sind) im Dialogfeld **Arbeitsauftrag erstellen** auswählen.

4. Wählen Sie **Arbeitsauftrag** aus.
5. Legen Sie im Dialogfeld **Arbeitsauftrag erstellen** die Felder fest, und wählen Sie dann **OK**.

    In einer Meldungsleiste werden Sie ggf. darüber informiert, dass ein neuer Arbeitsauftrag erstellt wurde.

    Wenn Sie einen Arbeitsauftrag erstellen, der auf einer Wartungsanfrage basiert und die Anlage, die sich auf die Wartungsanfrage bezieht, in einer Garantievereinbarung enthalten ist, werden Sie außerdem in einer Meldungsleiste über die Garantievereinbarung informiert.

6. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Arbeitsaufträge** \> **Alle Arbeitsaufträge** aus, und öffnen Sie den neuen Arbeitsauftrag.

    ![Neuen Arbeitsauftrag öffnen](media/05-manage-maintenance-requests.png)

