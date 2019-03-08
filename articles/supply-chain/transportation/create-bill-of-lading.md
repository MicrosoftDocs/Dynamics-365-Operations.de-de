---
title: Einen Frachtbrief erstellen
description: In diesem Thema wird beschrieben, wie Sie einen Frachtbrief erstellen, wenn der Lagerortverwaltungsprozess verwendet wird.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d5caed5553ad1c7aec5db83591024129aab1264
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "352596"
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



