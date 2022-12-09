---
title: Erstellen von Blankoschecks
description: In diesem Artikel wird erläutert, wie Sie Blankoschecks für ein Bankkonto erstellen.
author: angelad116
ms.date: 10/24/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 86020d9088d8135c83716128a77090608536a78f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804017"
---
# <a name="create-checks-that-have-blank-status"></a>Erstellen von Blankoschecks

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Blankoschecks erstellen. Sie müssen möglicherweise einen Blankoscheck erstellen, um einen Scheck zu erfassen, der beschädigt wurde und nicht zur Zahlung verwendet werden kann.

Auf der Seite **Schecks** führen Sie Verwaltungsaufgaben für Schecks aus. Sie können beispielsweise neue Schecknummern erstellen und Schecks löschen. Sie können auch Schecks erstellen, die den Status **Leer** haben. Nach der Erstellung eines Blankoschecks können sie diesen nicht im System löschen oder erneut verwenden.

> [!NOTE]
> Diese Funktion ist nur auf der Seite **Schecks** verfügbar, wenn Sie die Funktion **Blankoschecks auf der Seite „Schecks“ erstellen** auf der Seite **Funktionsverwaltung** aktivieren. Wenn die Funktion nicht aktiviert ist, können Sie Schecks mit dem Status **Leer** nur über das Dialogfeld **Zahlung per Scheck** während des Zahlungsgenerierungsprozesses in Kreditorenkonten erstellen.

Um die Seite **Schecks** zu öffnen, navigieren Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten** und wählen dann im Aktivitätsbereich auf der Registerkarte **Zahlungen verwalten** in der Gruppe **Zugehörige Informationen** die Option **Schecks** aus. Alternativ können Sie auch **Bargeld- und Bankverwaltung \> Abfragen und Berichte \> Schecks** verwenden.

Zur Anfertigung von Schecks mit dem Status **Leer** wählen Sie im Aktivitätsbereich die Option **Blankoschecks erstellen** aus. Während des Erstellvorgangs wird das zugehörige Bankkonto vorübergehend deaktiviert. Dieses Verhalten verringert das Risiko, dass gleichzeitig Zahlungen und Blankoschecks erstellt werden. Wenn die Verarbeitung abgeschlossen ist, wird das zugehörige Bankkonto wieder aktiviert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
