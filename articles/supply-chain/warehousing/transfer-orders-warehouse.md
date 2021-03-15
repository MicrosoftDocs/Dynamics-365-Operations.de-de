---
title: Einrichten von Lagerorten für Umlagerungsaufträge
description: In diesem Thema wird beschrieben, wie Sie Lager für Transportaufträge einrichten können.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 7dfb215683b4ee5d186626492bd90116d1a06a1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976837"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Einrichten von Lagerorten für Umlagerungsaufträge 

[!include [banner](../includes/banner.md)]

Mithilfe von Lagerortebenen kann eine Hierarchie erstellt werden, die Umlagerungsaufträge zwischen Lagerorten unterstützt. Basierend auf dieser Einstellung berechnet die Produktprogrammplanung den Artikelbedarf auf den einzelnen Lagerortebenen und generiert geplante Umlagerungsaufträge von einem zugeordneten Quelllagerort, um diesen Artikelbedarf zu erfüllen.

1.  Klicken Sie auf **Bestandsverwaltung > Einstellungen > Lageraufschlüsselung > Lagerorte**.

2.  Wählen Sie den Lagerort aus, der aufgefüllt werden soll.

3.  Aktivieren Sie auf der **Masterplanungs**-FastTab das Kontrollkästchen **Nachfüllen**.

4.  Wählen Sie im Feld **Hauptlager** das Lager aus, das Sie als Nachfülllager zuordnen möchten. Die Produktprogrammplanung berechnet eine Umlagerungsanforderung für den ausgewählten Lagerort und generiert einen geplanten Umlagerungsauftrag vom zugewiesenen **Hauptlager**.
   
    > [!NOTE]
    > <P>Wenn Sie das Feld <STRONG>Wird aufgefüllt</STRONG> deaktivieren lassen, wird dem ausgewählten Lagerort eine Lagerortebene in Bezug zum <STRONG>Auffülllagerort</STRONG> zugewiesen, der <STRONG>Auffülllagerort</STRONG> wird jedoch nicht als Lagerort für Auffüllungen eingerichtet.</P>

5.  Schließt die Seite, um die neuen Einstellungen zu übernehmen.


> [!TIP]
> <P>Wenn Sie ein Lager zum Nachfüllen zuordnen möchten, müssen Sie das Lager zunächst als Lagerdimension auf der Seite <STRONG>Lagerdimensionsgruppen</STRONG> einrichten. Wählen Sie auf dieser Seite das Feld <STRONG>Aktiv</STRONG> und das Feld <STRONG>Deckungsplan nach Dimension</STRONG> für das Lager aus.</P>

## <a name="set-up-transport-lead-time"></a>Transportvorlaufzeit einrichten

Außerdem müssen Sie die Transportvorlaufzeit zwischen den Lagern auf der Seite **Transporttage** einstellen. 
1. Gehen Sie zu **Bestandsverwaltung > Einrichtung > Verteilung > Transporttage**.
2. Wählen Sie im Feld **Empfangsstelle** die Option **Lager**.
3. Wählen Sie das **Versandlager**, das **Eingangslager** und die **Transporttage** aus. 
4. (Optional) Sie können die Transportzeit je nach Lieferart auch unter der Registerkarte **Transporttage pro Lieferart** einstellen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]