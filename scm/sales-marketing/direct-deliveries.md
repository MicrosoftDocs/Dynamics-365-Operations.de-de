---
title: Direktlieferungen
description: "Dieser Artikel enthält Informationen über Direktlieferungen. Dirketlieferungen sind Lieferungen, die direkt vom Kreditor an den Debitor gesendet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fd1e98f677835f2ef3449adbb452d536441b0a65
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="direct-deliveries"></a>Direktlieferungen

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen über Direktlieferungen. Dirketlieferungen sind Lieferungen, die direkt vom Kreditor an den Debitor gesendet werden.

Direkte Lieferungen lassen sich Lieferzeiten verkürzen und Lagerhaltungskosten verringern, da die Produkte vor dem Versand an den Debitor nicht am eigenen Lagerort gelagert werden müssen.  

Sie können direkte Lieferungen über die Seite **Auftrag** erstellen. Erstellen Sie zuerst einen Auftrag und Bestellpositionen. Wählen Sie dann im Aufgabenbereich auf der Registerkarte **Auftrag** den Eintrag **Direkte Lieferung**. Geben Sie schließlich die Positionen an, die als Direktlieferung behandelt werden sollen. Daraufhin wird eine Verknüpfung zwischen den Auftragspositionen der Direktlieferung und den entsprechenden Bestellpositionen erstellt.  

**Hinweis:** Wenn ein Teil der bestellten Menge bereits geliefert wurde, müssen Sie die Restmenge aufteilen. Erstellen Sie eine neue Position für die Menge, die direkt geliefert werden muss, und subtrahieren Sie diese Menge von der Menge in der ursprünglichen Position. Wenn beispielsweise die ursprüngliche Menge 15 war und fünf geliefert wurden, müssen Sie eine neue Position für die Restmenge von 10 erstellen, und dann die ursprüngliche Menge um diesen Betrag verkleinern.  

Nachdem Sie die Direktlieferungsverbindung zwischen den Auftragspositionen und den Bestellpositionen erstellt haben, können Sie den Auftrag aktualisieren, indem Sie einen Lieferschein verwenden. Führen Sie entweder eine Lieferscheinaktualisierung oder eine Rechnungsaktualisierung aus der Bestellung aus. Sie müssen eine Rechnungsaktualisierung des Auftrags über die Seite **Auftrag** durchführen. Eine Rechnungsaktualisierung kann nicht bewirken, dass die Auftragsmenge die Menge überschreitet, die als empfangen erfasst ist. So weist beispielsweise eine Auftragsposition 10 Exemplare auf, aber es wurden nur 5 Stück aus der Auftragsposition mit einem Lieferschein aktualisiert. Wenn Sie **Alle** in der Liste **Menge** bei der Rechnungsaktualisierung des Auftrags auswählen, werden nur die Artikel rechnungsaktualisiert, die tatsächlich eingegangen sind oder die über einen Lieferschein aktualisiert wurden. Es wird nicht die gesamte Auftragsposition aktualisiert.

## <a name="delivery-date"></a>Lieferdatum
Durch Aktualisieren des Felds **Angefordertes Wareneingangsdatum** in der Auftragsposition wird auch das Feld **Lieferdatum** in der entsprechenden Bestellposition aktualisiert. Ebenso werden durch Aktualisieren des Felds **Bestätigt** in der Bestellposition auch die Felder **Bestätigtes Wareneingangsdatum** und **Bestätigtes Lieferdatum** in der entsprechenden Auftragsposition aktualisiert.

## <a name="delivery-address"></a>Lieferadresse
Die Lieferadresse für einen Auftrag ist typischerweise die Adresse des Unternehmens. Wenn Sie eine Direktlieferung erstellen, geben Sie jedoch die Adresse des Debitors als Lieferadresse ein. Wenn Sie die Lieferadresse in einer Bestellposition ändern, die als Liefertyp **Direkte Lieferung** aufweist, wird die Lieferadresse in der entsprechenden Auftragsposition ebenfalls aktualisiert. Ebenso wird, wenn Sie die Lieferadresse in einer Auftragsposition ändern, die Lieferadresse in der entsprechenden Bestellposition ebenfalls aktualisiert.

## <a name="deleting-order-lines"></a>Löschen von Auftragspositionen
Beim Versuch, eine Auftragsposition mit dem Liefertyp **Direkte Lieferung** zu löschen, wird eine Meldung angezeigt, dass Bestellpositionen mit dieser Position verknüpft sind. Ist für die Auftragsposition eine Teillieferung erfolgt, ist weder das Löschen der Auftragsposition noch das Löschen der zugeordneten Bestellpositionen möglich.

## <a name="warehouse"></a>Lagerort
Beim Erstellen einer Direktlieferung kommen die Artikel, die Sie verkaufen, niemals physisch an Ihrem Lagerort an. Sie müssen allerdings trotzdem einen Lagerort in der Auftragsposition angeben. Ebenso können Entnahmeanforderungen in der Artikelmodellgruppe für den Artikel angegeben werden. Da jedoch die Artikel niemals physisch am Lagerort eingehen, werden diese Anforderungen ignoriert, wenn der Auftrag eine Direktlieferung ist.




