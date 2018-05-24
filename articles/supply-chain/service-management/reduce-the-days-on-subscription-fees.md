---
title: "Verringern der Tage für Dauerauftragsgebühren"
description: "Sie können zum Verringern der Anzahl von Tagen einer vorhandenen Dauerauftragsgebühr eine neue Buchung zum Entfernen des Zeitraums erstellen, der nicht mehr dem Intervall für die Dauerauftragsgebühr angehören soll."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a>Verringern der Tage für Dauerauftragsgebühren 

[!include [banner](../includes/banner.md)]


Sie können zum Verringern der Anzahl von Tagen einer vorhandenen Dauerauftragsgebühr eine neue Buchung zum Entfernen des Zeitraums erstellen, der nicht mehr dem Intervall für die Dauerauftragsgebühr angehören soll.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Verringern der Tage für eine Dauerauftragsgebühr

1.  Klicken Sie auf **Servicemanagement** \> **Gemeinsam** \> **Daueraufträge** \> **Alle Daueraufträge**. Wählen Sie den Dauerauftrag aus, und klicken Sie im Aktivitätsbereich auf **Dauerauftragsgebühren**.

2.  Wählen Sie im Feld **Dauerauftragstyp** **Minderungstage** aus.

3.  Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** das Datumsintervall der Dauerauftragsgebühr ein, das aus der Periode für die Dauerauftragsgebühr entfernt werden soll, und klicken Sie anschließend auf **OK**.

Klicken Sie zum Anzeigen der erstellten Buchung im Formular **Dauerauftrag** auf  und anschließend auf **Gebührenbuchungen**.

## <a name="example"></a>Beispiel

Angenommen, die Periode einer Dauerauftragsbuchung reicht vom 1. bis zu 31. Januar und soll um 10 Tage verkürzt werden. Erstellen Sie hierzu eine neue Buchung mit einer Verringerungsperiode vom 1. bis zum 10. Januar. (Die Verringerungsperiode könnte jedoch auch vom 5. bis zum 15. Januar reichen oder einen beliebigen anderen Zeitraum von zehn Tagen umfassen).

Ist dagegen der Wert im Feld **Von Datum** für die Verringerungsperiode auf den 21. Januar festgelegt (also 31 minus 10), kann der Wert für **Bis Datum** auf ein beliebiges Datum nach dem 31 Januar festgelegt werden, und dennoch werden die 10 Tage aus der Gebührenbuchungsperiode entfernt.

## <a name="see-also"></a>Siehe auch

[Minderungstage – Beispiel](reduction-days-example.md)

  



