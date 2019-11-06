---
title: Erstellen von Blankoschecks
description: In diesem Thema wird erläutert, wie Sie auf der Seite „Schecks“ Blankoschecks für ein Bankkonto erstellen.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 47d54524f87cf718b9b41462b5133df267d5dd9e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570286"
---
# <a name="create-checks-that-have-blank-status"></a>Erstellen von Blankoschecks

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Blankoschecks erstellen. Sie müssen möglicherweise einen Blankoscheck erstellen, um einen Scheck zu erfassen, der beschädigt wurde und nicht zur Zahlung verwendet werden kann.

Auf der Seite **Schecks** führen Sie Verwaltungsaufgaben für Schecks aus. Sie können beispielsweise neue Schecknummern erstellen und Schecks löschen. Sie können auch Schecks erstellen, die den Status **Leer** haben. Nach der Erstellung eines Blankoschecks können sie diesen nicht im System löschen oder erneut verwenden.

> [!NOTE]
> Diese Funktion ist nur auf der Seite **Schecks** verfügbar, wenn Sie die Funktion **Blankoschecks auf der Seite „Schecks“ erstellen** auf der Seite **Funktionsverwaltung** aktivieren. Wenn die Funktion nicht aktiviert ist, können Sie Schecks mit dem Status **Leer** nur über das Dialogfeld **Zahlung per Scheck** während des Zahlungsgenerierungsprozesses in Kreditorenkonten erstellen.

Um die Seite **Schecks** zu öffnen, navigieren Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten** und wählen dann im Aktivitätsbereich auf der Registerkarte **Zahlungen verwalten** in der Gruppe **Zugehörige Informationen** die Option **Schecks** aus. Alternativ können Sie auch **Bargeld- und Bankverwaltung \> Abfragen und Berichte \> Schecks** verwenden.

Um anschließend Schecks mit dem Status **Leer** zu erstellen, wählen Sie im Aktivitätsbereich **Blankoschecks erstellen** aus. Während das System Blankoschecks erstellt, wird das zugehörige Bankkonto vorübergehend deaktiviert. Dieses Verhalten verringert das Risiko, dass gleichzeitig Zahlungen und Blankoschecks erstellt werden. Wenn die Verarbeitung abgeschlossen ist, wird das zugehörige Bankkonto wieder aktiviert.
