---
title: Artikelverwendungsort
description: In diesem Thema erfahren Sie, wie Sie sich einen Überblick darüber verschaffen können, wo ein Artikel im Asset Management verwendet wird.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: aa1f00ba6b8259221aa2b1ee460be43ee9a311b2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205469"
---
# <a name="item-where-used"></a>Artikelverwendungsort

[!include [banner](../../includes/banner.md)]

 

Sie können eine Kalkulation für einen bestimmten Artikel durchführen, um sich einen Überblick zu verschaffen, wo in Asset Management der Artikel verwendet wurde. Die Ergebnisse zeigen den Kontext, in dem der Artikel während seiner Lebensdauer verwendet wurde. Die Seite **Artikelverwendungsort** kann vom Anlagenmanagement-Hauptmenü geöffnet werden, ist auch über die folgenden Seiten zugänglich:

- [Anlagenstücklisten](../objects/object-BOM.md)

- [Ersatzteile in Anlagentypstandardeinstellungen](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [Kategorien von Wartungsaufträgen und Arten von Wartungsaufträgen, Variationen von Wartungsaufträgen, Handel von Wartungsaufträgen und Wartungsprüflisten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Wartungsprognose](../work-orders/maintenance-forecasts.md)

- [Beschaffung](../work-orders/procurement.md)

- [Arbeitsauftrag – Einkauf](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Erstellen Sie eine Artikelverwendungsort-Berechnung

1. Klicken Sie **Anlagenverwaltungsparameter** > **Abfragen** > **Artikelverwendungsort**, oder wählen Sie die Schaltfläche **Artikelverwendungsort** auf einer der Seiten aus, die oben genannten werden.

2. Im Dialogfeld **Artikelverwendungsort** wählen Sie den Artikel aus, für den Sie die Berechnung im Feld **Artikelnummer** vornehmen wollen.

3. Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Artikelpositionen bezüglich funktionaler Standorte sein sollen. 

    Wenn Sie z.B. die Nummer „1“ in das Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden auf der obersten Ebene alle Artikelpositionen zu einem funktionalen Standort angezeigt. Daher kann die Relation/Menge auf einer Position von funktionalen Standorten auf einer niedrigeren Ebene summiert werden. 
    
    Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Artikelpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.

4. Wählen Sie im Abschnitt **Einbeziehen** „Ja“ auf den Umschaltflächen aus, die Sie in die Berechnung einbeziehen möchten.

5. Klicken Sie auf **OK**, um die Berechnung zu starten.

6. Wählen Sie auf der Registerkarte **Artikelverwendungsort** die **Gruppieren nach…**-Schaltflächen aus, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

7. Wenn Sie die Dimensionen anzeigen möchten, die dem Artikel zugeordnet werden, klicken Sie auf **Dimensionen anzeigen** und wählen die Dimensionen aus, die angezeigt werden sollen.

## <a name="example"></a>Beispiel

Im nachfolgenden Screenshot finden Sie ein Beispiel für eine Artikelverwendungsort-Berechnung für Artikelnummer „1000“.

![Beispiel einer Artikelverwendungsort-Berechnung](media/12-controlling-and-reporting.png)

