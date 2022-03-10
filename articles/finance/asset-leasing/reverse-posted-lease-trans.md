---
title: Gebuchte Leasingtransaktionen stornieren
description: In diesem Thema wird erläutert, wie Sie eine gebuchte Leasingtransaktion stornieren. Jede Transaktion, die durch Anlagenleasing erstellt wird, kann rückgängig gemacht werden.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f76b75a968e9ee9a3c545f646077c16282b5b185aa88025653f7443fbcfd9581
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770664"
---
# <a name="reverse-posted-lease-transactions"></a>Gebuchte Leasingtransaktionen stornieren

[!include [banner](../includes/banner.md)]

Jede Transaktion, die durch Anlagenleasing erstellt wird, kann rückgängig gemacht werden. Transaktionen, die durch Anlagenleasing rückgängig gemacht werden, aktualisieren Ihre Leasingdaten. Daher aktualisieren sie auch die Buchwerte der Leasingverbindlichkeit und des Nutzungsrechts am Leasingobjekt.

Führen Sie die folgenden Schritte aus, um eine Stornierungstransaktionsdaten für einen Mietvertrag zu erstellen.

1. Wählen Sie entweder auf der **Anlagentransaktionen**-Seite oder der **Verbindlichkeitentransaktionen**-Seite die Transaktion und dann **Transaktion stornieren** aus.
2. Im daraufhin angezeigten Dialogfeld können Sie das Datum bearbeiten, an dem der Stornoeintrag gebucht wird. Standardmäßig wird das **Datum**-Feld auf das Transaktionsbuchungsdatum der von Ihnen ausgewählten Transaktion gesetzt. Der Stornoeintrag kann nicht vor dem ursprünglichen Buchungsdatum der ausgewählten Transaktion gebucht werden.
3. Wählen Sie **OK**. Es wird ein Journaleintrag gebucht, der den von Ihnen ausgewählten Eintrag storniert. Die Stornierung wird auf der **Anlagentransaktionen**- oder **Verbindlichkeitentransaktionen**-Seite gezeigt, und die Nettosumme des aktuellen Kontostands, der auf der Seite angezeigt wird, wird aktualisiert.

Wenn Sie **Rückverfolgung** auswählen wird ein Dialogfeld angezeigt, in dem sowohl die ursprünglichen als auch die stornierten Transaktionen zusammen mit einer verknüpften Nummer angezeigt werden, die als *Tracenummer* bezeichnet wird. Um das Verständnis der Stornierungen zu erleichtern und die Sichtbarkeit zu verbessern, können Sie Stornierungen auch mithilfe der Mietpläne verfolgen.

Das **Neueste Erfassungsnummer**-Feld auf der **Zeitplan**-Seite zeigt die Erfassungsnummern der Transaktionen. Wenn eine Transaktion storniert wird, wird dieses Feld mit der Erfassungsnummer einer stornierenden Transaktion aktualisiert. Darüber hinaus wird das Kontrollkästchen **Storniert** aktiviert, um anzuzeigen, dass die Transaktion storniert wurde, und das Feld **Gebucht** wird ausgewählt.

## <a name="revoke-a-reversed-transaction"></a>Widerrufen einer Stornierungstransaktion

Führen Sie die folgenden Schritte aus, um eine stornierte Transaktion zu widerrufen.

1. Wählen Sie entweder auf der Seite **Zeitplan** oder der **Transaktionen**-Seite die ursprüngliche Transaktion.
2. Führen Sie einen dieser Schritte aus:

    - Wenn Sie die Transaktion auf der **Zeitplan**-Seite ausgewählt haben, befolgen Sie die Schritte zum Erstellen einer Erfassung in [Monatliche Erfassungseinträge in einem Batch erstellen](create-monthly-journals-batch.md). Sie müssen die Erfassung manuell buchen.
    - Wenn Sie die Transaktion auf der **Transaktionen**-Seite ausgewählt haben, wählen Sie **Transaktion stornieren**. Sie erhalten eine Nachricht, die besagt, dass dieser Widerruf ein Widerruf einer früheren Stornierung ist und dass Sie das Buchungsdatum für diesen Widerruf bearbeiten können. Allgemeine Geschäftsüberprüfungen wirken sich jedoch auf die Daten aus, die in das Feld **Datum** eingegeben werden können. 

3. Wählen Sie **OK**. Es wird ein Journaleintrag gebucht, der den von Ihnen ausgewählten Eintrag storniert. Die Stornierung wird auf der **Transaktionen**-Seite gezeigt, und die Nettogesamtbilanz wird auf den Stand vor der ersten Stornierung zurückgesetzt. Daher wird die Auswirkung der Stornierung auf die Salden negiert.

Wenn Sie **Rückverfolgung** auswählen wird ein Dialogfeld angezeigt, in dem sowohl die ursprünglichen als auch die stornierten Transaktionen zusammen mit einer verknüpften Tracenummer angezeigt werden.

Sie können Widerrufe auch mithilfe der entsprechenden **Zeitpläne**-Seite verfolgen. Das **Wiederrufen**-Feld wird gelöscht, während das **Erfassung gebucht**-Feld ausgewählt wird. Darüber hinaus wird das **Neueste Erfassungsnummer** Feld mit der Erfassungsnummer der Widerrufstransaktion aktualisiert und das Feld **Erfassungsnummer** wird mit der Erfassungsnummer des Wiederrufs aktualisiert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
