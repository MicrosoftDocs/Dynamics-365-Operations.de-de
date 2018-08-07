---
title: "Prüfen von zurückgelieferten Artikeln"
description: "Prüfen von zurückgelieferten Artikeln."
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: df209cfdbdef591e9f24161b3651316c43d69ee0
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="take-returned-items-through-inspection"></a>Prüfen von zurückgelieferten Artikeln 

[!include [banner](../includes/banner.md)]


1.  Klicken Sie auf **Lagerverwaltung** \> **Periodisch** \> **Qualitätsmanagement** \> **Quarantäneaufträge**.

2.  Suchen Sie nach der Auftragsposition für den zurückgelieferten Artikel, den Sie gerade untersuchen.

    > [!NOTE]
    > <P>Ein Quarantäneauftrag kann jeweils nur einer Artikelnummer zugeordnet sein. Werden im Rahmen einer einzelnen Lieferung zehn Artikel mit unterschiedlicher Artikelnummer zurückgesendet und in Quarantäne geschickt, werden zehn einzelne Quarantäneaufträge erstellt.</P>

3.  Geben Sie nach der Untersuchung des Artikels im Feld **Dispositionscode** an, wie mit dem Artikel und mit der zugehörigen wertmäßigen Buchung verfahren werden soll. Sie können beispielsweise festlegen, dass der Artikel wieder dem Lager zugeführt werden und der Debitor eine Gutschrift erhalten soll, dass der Artikel verschrottet und ein Ersatzartikel an den Debitor gesendet werden soll oder dass der Artikel ohne Gutschrift an den Kunden zurückgesendet werden soll.
    
    > [!NOTE]
    > <P>Sollte mehreren zurückgelieferten Artikeln eines Stapels mit gleicher Artikelnummer nicht der gleiche Dispositionscode zugewiesen werden können, muss der Quarantäneauftrag aufgeteilt werden (unter <STRONG>Funktionen</STRONG> &gt; <STRONG>Teilen</STRONG>), um den einzelnen Teilmengen jeweils einen eigenen Dispositionscode zuzuweisen.</P>


4.  Klicken Sie nach Abschluss der Untersuchung auf **Fertigmeldung**, um die zurückgelieferten Artikel freizugeben und einen entsprechenden Eintrag für die Wareneingangserfassung zu erstellen. Die Erfassung wird dann von der Person oder Abteilung verarbeitet, von der die Artikel entgegengenommen werden, damit die Artikel wieder dem Bestand zugeführt werden.
    
    - oder -
    
    Beenden Sie den Quarantäneauftrag, und führen Sie die Artikel direkt mithilfe einer der Funktionen für **Lagerartikel** wieder dem Bestand zu.

5.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.

## <a name="see-also"></a>Siehe auch

[Angeben zur Entsorgung zurückgelieferter Artikel](specify-how-to-dispose-of-returned-items.md)

  



