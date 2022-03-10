---
title: Einen Frachtbrief erstellen
description: In diesem Thema wird beschrieben, wie Sie einen Frachtbrief erstellen, wenn der Lagerortverwaltungsprozess verwendet wird.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b79408e21e9acda12617cf35464007e58ae1b5fe
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573128"
---
# <a name="create-a-bill-of-lading"></a>Einen Frachtbrief erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie einen Frachtbrief erstellen, wenn der Lagerortverwaltungsprozess verwendet wird.  

Ein Frachtbrief ist ein Vertrag zwischen dem Unternehmen, das den Artikel versendet und dem Spediteur. Das Dokument liegt den Versandartikeln bei und dient als Lieferbeleg, wenn die Artikel am Zielort ausgeliefert werden. Wenn Sie die Lagerortverwaltung verwenden, gibt es zwei Möglichkeiten, einen Frachtbrief zu generieren:

  -   Erstellen Sie den Bericht manuell über die Seite **Frachtbrief**.
  -   Generieren Sie den Bericht aus **Ladungsplanungsworkbench**.

Wenn Sie den Frachtbrief aus dem **Ladungsplanungsworkbench** generieren, muss der Ladungsstatus **. Versendet** sein. Wenn mehr als eine Lieferung für die Auslastung vorhanden sind, wird ein Frachtbrief für jede Lieferung erstellt. Nachdem ein Frachtbrief erstellt wurde, können Sie die auf der Seite **Frachtbrief** Änderungen vornehmen.

## <a name="master-bill-of-lading"></a>Hauptfrachtbrief
Wenn mehr als eine Lieferung in einer Ladung enthalten ist, können Sie einen Hauptfrachtbrief generieren. Dieser hat das gleiche Layout und die Informationen wie ein Frachtbrief, aber enthält den zusammengefassten Inhalt aller Lieferungen. Wenn die Option **Erstellen Sie einen Hauptfrachtbrief, wenn mehr als eine Lieferung in einer Ladung enthalten ist.** auf **Ja** auf der Seite **Transportverwaltungsparameter** festgelegt ist, wird automatisch ein Hauptfrachtbrief generiert, wenn Sie einen Frachtbrief aus dem **Ladungsplanungsworkbench** erstellen und es mehrere Lieferung gibt. Sie können eine Liste der Frachtbriefe auch abrufen, indem Sie auf **Zugehörige Informationen** &gt; **Frachtbrief** klicken. Wenn Sie Frachtbriefe manuell erstellen, können Sie einen Hauptfrachtbrief auf der Seite **Frachtbrief** erstellen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]