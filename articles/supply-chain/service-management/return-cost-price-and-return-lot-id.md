---
title: Rücklieferungseinstandspreis und Rücklieferungsloskennung
description: Unter Umständen sollen die Kosten der zurückgegebenen Produkte jedoch den Produktkosten zum Zeitpunkt des Verkaufs an den Debitor entsprechen. Sie können dies über die **Rücklieferungsloskennung** tun.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eff30383e06677793313e8abac0339c6032c2a7f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965829"
---
# <a name="return-cost-price-and-return-lot-id"></a>Rücklieferungseinstandspreis und Rücklieferungsloskennung        

[!include [banner](../includes/banner.md)]



Die Kosten von Produkten, die an das Lager zurückgegeben werden, werden anhand der aktuellen Kosten der Produkte berechnet. Unter Umständen sollen die Kosten der zurückgegebenen Produkte jedoch den Produktkosten zum Zeitpunkt des Verkaufs an den Debitor entsprechen. Sie können dies tun, indem Sie im **Auftragsformular** das Feld **Rücklieferungsloskennung** auf der Registerkarte **Positionsdetails** verwenden.

Betrachten Sie beispielsweise das folgende Szenario. Sie stellen dem Debitoren Produkte in Rechnung. Anschließend gibt der Kunde (Debitor) die gelieferten Produkte zurück. Sie geben die Produkte in den Bestand zurück. Wenn Sie dem Debitor die zurückgegebenen Produkte gutschreiben, werden in diesem Fall die Produktkosten anhand der aktuellen Kosten der Produkte berechnet. Wenn Sie jedoch das Feld **Rücklieferungsloskennung** verwenden, werden die Kosten der zurückgegebenen Produkte auf der Grundlage der Rechnung des ursprünglichen Verkaufs an den Debitor verwendet.

Um andere Kosten als die aktuellen Kosten für Rückgaben von einem Debitor zu verwenden, verwenden Sie eine der folgenden Methoden.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Methode 1: Geben Sie manuell den Rücklieferungseinstandspreis ein.

Wenn Sie Artikel einer Rücklieferung hinzufügen, werden die Artikel standardmäßig zum aktuellen Einstandspreis in den Bestand zurückgegeben. Um einen anderen Rücklieferungseinstandspreis anzugeben, führen Sie die folgenden Schritte aus.

1.  Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.

2.  Klicken Sie im **Aktivitätsbereich** in der Gruppe **Neu** auf **Rücklieferung**.

3.  In der **Rücklieferung erstellen** Formular wählen Sie ein Debitorenkonto aus, und klicken Sie dann **OK**.

4.  Wählen Sie im Formular **Rücklieferung - RMA-Nummer: %1, %2** eine Position aus und geben Sie dann im Feld **Menge** eine negative Menge ein.

5.  Klicken Sie auf das Inforegister "**Positionsdetails**".

6.  Wählen Sie auf der Registerkarte **Allgemeines** im Feld **Rücklieferungseinstandspreis** die gewünschte Option aus. Dieser Wert wird verwendet, wenn die Waren in den Bestand zurückgegeben werden. Wenn Sie keinen Wert eingeben, wird der aktuelle Einstandspreis verwendet, wenn die Waren in den Bestand zurückgegeben werden.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Methode 2: Automatisches Generieren der auf dem Einstandspreis basierenden Debitorenrechnungsposition

Dies ist die bevorzugte Methode zum Erstellen von Rückgabepositionen. Um die Produktkosten zum Zeitpunkt des Verkaufs an den Debitor zu verwenden, erstellen Sie eine Rücklieferung und geben die zurückzugebende Verkaufsposition an.

1.  Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.

2.  Klicken Sie im **Aktivitätsbereich** in der Gruppe **Neu** auf **Rücklieferung**.

3.  In der **Rücklieferung erstellen** Formular wählen Sie ein Debitorenkonto aus, und klicken Sie dann **OK**.

4.  Klicken Sie im Formular **Rücklieferung - RMA-Nummer: %1, %2** im **Aktivitätsbereich** auf **Auftrag suchen**.

5.  Wählen Sie im Formular **Auftrag suchen** die zurückzugebende Rechnungsposition, und klicken Sie anschließend auf **OK**.
    
    Im Inforegister **Positionsdetails** auf der Registerkarte **Allgemein** wird im Feld **Rücklieferungsloskennung** der Wert aus der ursprünglichen Auftragsposition angezeigt. Darüber hinaus wird im Feld **Rücklieferungseinstandspreis** der Einstandswert aus der ursprünglichen Auftragsposition angezeigt.

## <a name="cost-calculation-example"></a>Kostenberechnungsbeispiel

Wenn Sie das Feld **Rücklieferungsloskennung** in einer Rücklieferungsposition verwenden, um den Rücklieferungseinstandspreis anzugeben, werden die Kosten der Rücklieferungsposition verwendet. Wenn Sie die Bestandsabschluss- oder -Neuberechnungsfunktionen ausführen, werden die Kosten der ursprünglichen Auftragsposition reguliert. Die Kosten der Rücklieferungsposition werden automatisch angepasst, um die gleichen Kosten pro Artikel widerzuspiegeln.

1.  Erstellen Sie ein Produkt namens Test, und geben Sie es frei. In der **Details für freigegebene Produkte** Formular geben Sie folgende Informationen an:
    
    1.  Wählen Sie auf dem Inforegister **Kosten verwalten** die standardmäßige **Artikelgruppe** im Feld **Teile** aus.
    
    2.  Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagersteuerungsgruppe** **DEF** aus.
    
    3.  Geben Sie auf dem Inforegister **Einkauf** im Feld **Preis** den Wert 10,00 als Einstandspreis des Artikels ein.
    
    4.  Klicken Sie im **Aktivitätsbereich** auf **Dimensionensgruppen.** Wählen Sie im Feld **Lagerdimensionsgruppe** **Nur Standort und Lagert** aus. Wählen Sie im Feld **Rückverfolgungsangabengruppe** **Keine aktiven Rückverfolgungsangaben** aus.

2.  Erstellen Sie eine Bestellung über 10 Stück des Artikels Test zu 6,00 pro Artikel, und buchen Sie anschließend eine Rechnung für die Bestellung.
    
    Erstellen Sie eine zweite Bestellung über 10 Stück des Artikels Test zu 8,00 pro Artikel, und buchen Sie anschließend eine Rechnung für die Bestellung.

3.  Buchen Sie eine Rechnung für einen Auftrag zum Verkauf von fünf Stück des Artikels Test.
    
    In diesem Fall wird die Auftragsposition mit 35,00 vorkalkuliert (5 Stück \* 7,00 durchschnittlicher Einstandspreis pro Artikel).

4.  Erstellen Sie eine Rücklieferung für den ausgewählten Debitor. Wählen Sie im Formular **Auftrag suchen** die Rechnungsposition, und klicken Sie anschließend auf **OK**.

5.  Vergewissern Sie sich im Formular **Rücklieferung - RMA-Nummer: %1, %2**, dass ein Rücklieferungsauftrag für die Rückgabe des Testartikels generiert wird. Die Menge der Rücklieferung wird auf -5,00 festgelegt.
    
    Die **Rücklieferungsloskennung** zeigt eine Kennung an. Diese Loskennung wird aus dem Originalauftrag des Artikels übernommen, der an den Debitor verkauft wurde. Im Feld **Rücklieferungseinstandspreis** wird der Einstandspreis aus der ursprünglichen Auftragsposition angezeigt.

6.  Erfassen Sie den Empfang zurückgelieferter Artikel.

7.  Buchen Sie einen Lieferschein für die zurückgelieferten Artikel.

8.  Buchen Sie eine Rechnung für die Rücklieferung. Auf der Listenseite **Alle Aufträge** wählen Sie einen Auftrag aus, für den der Auftragstyp **Zurückgegebener Auftrag** ist.

9.  Öffnen Sie das Formular **Lagerbuchungen**. Überprüfen Sie, ob die Rücklieferung mit dem Einstandspreis 7,00 pro Artikel vorkalkuliert wird, indem der Wert im Feld **Rücklieferungseinstandspreis** verwendet wird, sodass sich im Feld **Kostenbetrag** die Summe 35,00 ergibt. Sie können das Formular **Lagerbuchungen** aus dem Formular **Rücklieferung - RMA-Nummer: %1, %2** öffnen. Klicken Sie im Raster **Positionen** auf **Bestand** \> **Transaktion**.

10. In der Bestands- und Lagerortverwaltung verwenden Sie das Formular **Abschluss und Regulierung**, um die Prozedur **3. Schließen** auszuführen.
    
    Hiermit werden die Kosten in der ursprünglichen Auftragsposition, die mit -35,00 vorkalkuliert wurden (5 Stück \* 7,00), in -30,00 (5 Stück \* 6,00) geändert. Dies ist so, weil für die Lagersteuerungsgruppe das FIFO-Prinzip (First in, First out) verwendet wird, und 6,00 pro Artikel sind die FIFO-Kosten aus der ersten Bestellung. Zudem werden mit dieser Aktivität die Kosten in der Rückholverkaufsposition angepasst, sodass die Kosten pro Artikel der ursprünglichen Auftragsposition entsprechen. Daher werden die Kosten der Rückgabeposition von 35,00 in 30,00 geändert.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]