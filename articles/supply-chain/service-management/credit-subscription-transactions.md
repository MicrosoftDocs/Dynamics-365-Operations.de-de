---
title: Gutschreiben von Dauerauftragsbuchungen
description: In diesem Thema wird gezeigt, wie Gutschriftdauerauftragsbuchungen erstellt werden.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 898dd8f689a89430c4f307a414fe865a4a15a995
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675739"
---
# <a name="credit-subscription-transactions"></a>Gutschreiben von Dauerauftragsbuchungen 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a>Gutschreiben von Dauerauftragsbuchungen

1.  Klicken Sie auf **Servicemanagement** \> **Gemeinsam** \> **Daueraufträge** \> **Alle Daueraufträge**.

2.  Wählen Sie den Dauerauftrag aus, der der Dauerauftragsbuchung zugeordnet ist, für die eine Gutschrift erstellt werden soll.

3.  Wählen Sie die Registerkarte **Analysieren** aus, und klicken Sie im Aktivitätsbereich auf die Schaltfläche **Gebührenbuchungen**.

4.  Wählen Sie im Formular **Gebührenbuchungen** die Buchung aus, für die die Gutschrift erstellt werden soll.

5.  Klicken Sie auf **Funktionen** \> **Für Gutschrift auswählen**.

6.  Wählen Sie im Formular **Für Gutschrift auswählen** die Buchung aus, die gutgeschrieben werden soll, und klicken Sie anschließend auf **OK**.


> [!NOTE]
> <P>Achten Sie beim Erstellen der Gutschrift darauf, dass Sie <STRONG>Gutschriften</STRONG> auswählen. Diese Option befindet sich im Dialogfeld <STRONG>Rechnung erstellen</STRONG> in der Liste <STRONG>Rechnungsstellungsmethode</STRONG>.</P>

Ist im Formular **Serviceverwaltungsparameter** das Feld **Abgrenzungen bei Gutschrift zurücksetzen** auf **Manuell** festgelegt, müssen vor dem Erstellen eines Gutschriftvorschlags für die Buchung alle Buchungen für den antizipierten Umsatzerlös einzeln storniert werden.

## <a name="see-also"></a>Siehe auch

[Fakturieren von Dauerauftragsbuchungen](invoice-subscription-transactions.md)


 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]