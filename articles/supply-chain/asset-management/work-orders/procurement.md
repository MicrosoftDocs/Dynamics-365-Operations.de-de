---
title: Beschaffung
description: In diesem Thema wird die Beschaffung im Anlagenmanagement erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875670"
---
# <a name="procurement"></a>Beschaffung


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Im Anlagenmanagement können Sie sich einen Überblick über Bestellanforderungen und Bestellungen zu Arbeitsaufträgen verschaffen. Es ist auch möglich, eine Bestellung oder eine Bestellanforderung aus einem Arbeitsauftrag heraus anzulegen.

In der Liste **Arbeitsauftragsbestellung** (**Anlagenmanagement** > **Allgemein** > **Beschaffung** > **Arbeitsauftragsbestellung**) sehen Sie eine Liste von Bestellanforderungen zu Arbeitsaufträgen.

- Wählen Sie in der Liste **Arbeitsauftrag Bestellanforderung** einen Arbeitsauftrag aus und klicken Sie auf die Schaltfläche **Bestellanforderung**, um die zugehörige Bestellanforderung zu öffnen.  
- Wählen Sie einen Arbeitsauftrag in der Liste **Arbeitsauftrag Bestellanforderung** aus und klicken Sie auf die Schaltfläche **Arbeitsauftrag**, um den zugehörigen Arbeitsauftrag zu öffnen.  
- Wählen Sie einen Arbeitsauftrag in der Liste **Arbeitsauftrag Bestellanforderung** aus und klicken Sie auf die Schaltfläche **Position der Verwendung**, wenn Sie einen Überblick darüber erhalten möchten, wo der Artikel auf der ausgewählten Zeile im Asset Management in Bezug auf Anlagen, Standardwerte für Wartungsaufträge, Ersatzteile und Arbeitsaufträge verwendet wird. 

![Abbildung 1](media/08-work-orders.png)


In der Liste **Arbeitsauftragsbestellung** (**Unternehmensanlagenmanagement** > **Allgemein** > **Beschaffung** > **Arbeitsauftragbestellung**) sehen Sie eine Liste von Bestellungen zu Arbeitsaufträgen.

- Wählen Sie einen Arbeitsauftrag in der Liste **Arbeitsauftrag Bestellung** aus und klicken Sie auf die Schaltfläche **Bestellung**, um die zugehörige Bestellung zu öffnen.  
- Wählen Sie einen Arbeitsauftrag in der Liste **Arbeitsauftrag bestellen** und klicken Sie auf die Schaltfläche **Arbeitsauftrag**, um den zugehörigen Arbeitsauftrag zu öffnen.  
- Wählen Sie einen Arbeitsauftrag in der Bestellliste **Arbeitsauftrag** aus und klicken Sie auf die Schaltfläche **Verwendungsposition**, wenn Sie einen Überblick darüber erhalten möchten, wo der Artikel auf der ausgewählten Zeile im Anlagenmanagement in Bezug auf Anlagen, Wartungsauftragsartenvorgaben, Ersatzteile und Arbeitsaufträge verwendet wird. 

![Abbildung 2](media/09-work-orders.png)


In den oben gezeigten Listen ist in jeder Zeile rechts ein Symbol zur Lieferterminkontrolle angebracht. Wenn das Symbol ein Ausrufezeichen in einem roten Kreis anzeigt, bedeutet dies, dass sich die Lieferung auf die zugehörige Bestellanforderung oder Bestellung verzögern kann.

Auf einer Bestellanforderung finden Sie das Datum zur Berechnung der möglichen Verzögerung im Feld **Bestellanforderungen** Formular > **Bestellanforderungskopf** FastTab > **Bestelldatum**. Dieses Datum wird wie das Bestelldatum mit dem verfügbaren Datum auf dem Arbeitsauftrag oder Arbeitsauftrag verglichen.

Auf einer Bestellung ist das Datum, das zur Berechnung einer möglichen Verzögerung herangezogen wird, das Datum, das sich auf die Bestellzeile bezieht, die im Feld **Bestellung**Formular > Bestellzeile auswählen > **Zeilendetails** FastTab > **Einrichtung** Registerkarte > **Bestätigtes Lieferdatum** angezeigt wird. Wenn dieses Feld nicht ausgefüllt ist, wird das Datum im Feld **Lieferdatum** auf dem **Kopf der Bestellung** FastTab verwendet. Eines dieser Termine wird mit dem verfügbaren Datum auf dem Arbeitsauftrag oder der Arbeitsaufgabe in der folgenden Reihenfolge verglichen:

- Iststartdatum auf dem Arbeitsauftrag oder  

- Geplantes Startdatum für den zugehörigen Arbeitsauftrag oder  

- Geplanter Starttermin auf dem Arbeitsauftrag oder  

- Erwartetes Startdatum auf dem Arbeitsauftrag  


## <a name="create-purchase-order-from-a-work-order"></a>Bestellung aus einem Arbeitsauftrag anlegen

Unter **Alle Arbeitsaufträge** wählen Sie einen Arbeitsauftrag aus und legen eine zugehörige Bestellung oder eine Bestellanforderung an. Dies geschieht, um die Projektbeziehungen zwischen der Bestellung oder Bestellanforderung und dem Arbeitsauftrag sicherzustellen.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie in der Liste **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** den Arbeitsauftrag aus, für den Sie eine Bestellung anlegen möchten, und klicken Sie auf **Bearbeiten**.

3. Wählen Sie im Formular **Arbeitsauftrag** > **Arbeitsauftrag Wartungsaufträge** FastTab den Arbeitsauftrag aus, für den Sie die Bestellung anlegen möchten.

4. Klicken Sie auf **Einzelpostenaufgaben** > **Bestellauftrag aus Arbeitsauftrag**.

5. Klicken Sie auf der Listenseite **Projektbestellungen** auf **Neu**.

6. Legen Sie die Bestellung an.

>[!NOTE]
>Das Anlegen einer Bestellanforderung ist nahezu identisch mit dem Anlegen einer Bestellung. Der einzige Unterschied besteht darin, dass Sie in der obigen Vorgehensweise in Schritt 2 in Schritt 2 auf **Positionsaufgaben** > **Bestellanforderung aus Arbeitsauftrag** klicken.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projektbeziehung zwischen Arbeitsauftrag und Bestellung oder Bestellanforderung

Eine Bestellzeile oder Bestellanforderungszeile ist über das Arbeitsauftragsprojekt und die zugehörige Projektvorgangsnummer mit einem Arbeitsauftrag verknüpft. Wenn Sie eine Bestellung oder Bestellanforderung aus einem Arbeitsauftrag heraus anlegen, ist die zugehörige Projektvorgangsnummer obligatorisch. Die Projektleistungsnummer wird automatisch in eine Bestellung oder Bestellanforderung eingefügt, wenn der zugehörige Arbeitsauftrag Arbeitsaufträge enthält, die alle den gleichen Wartungsjobtyp verwenden. Wenn die Arbeitsaufträge verschiedene Wartungsauftragsarten enthalten, muss die Nummer der Projektleistung manuell eingegeben werden.

Um die Vorgangsnummer zu einer Bestellzeile anzuzeigen oder einzufügen, öffnen Sie **Arbeitsauftrag Bestellung** > wählen Sie den Bestellsatz aus > klicken Sie auf die Bestellung in der Spalte **Bestellung** > **Zeilendetails** FastTab > **Projekt** Registerkarte > **Vorgangsnummer** Feld.


![Abbildung 3](media/10-work-orders.png)


Um die Leistungsnummer zu einer Bestellanforderungszeile eines Arbeitsauftrags anzuzeigen oder einzufügen, öffnen Sie **Bestellanforderung eines Arbeitsauftrags** > wählen Sie den Bestellanforderungssatz aus > klicken Sie auf die Bestellanforderung in der Spalte **Bestellanforderung** > **Zeilendetails** FastTab > **Projekt** Registerkarte > **Aktivitätsnummer** Feld.

