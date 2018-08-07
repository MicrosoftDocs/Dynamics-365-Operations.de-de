--- 
title: "Angebotsanforderungsangebote eingeben und vergleichen und Verträge vergeben"
description: "Diese Prozedur zeigt Ihnen an, wie Sie Antworten auf eine Angebotsanforderung eingeben, Angebote bewerten und vergleichen und dann einem der Händler das Angebot erteilen."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Angebotsanforderungsangebote eingeben und vergleichen und Verträge vergeben

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen an, wie Sie Antworten auf eine Angebotsanforderung eingeben, Angebote bewerten und vergleichen und dann einem der Händler das Angebot erteilen. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. Bevor Sie beginnen, müssen Sie eine Angebotsanforderung mit zwei Positionen haben, die mindestens zwei Händlern gesendet wurde. Sie können die Prozedur "Erstellen einer Angebotsanforderung" als Voraussetzung ausführen, um diese zu erstellen. Sie müssen Bewertungskriterien eingerichtet haben, bevor Sie diese Prozedur ausführen können.


## <a name="enter-a-reply-from-a-vendor"></a>Geben Sie eine Antwort von einem Händler ein
1. Wechseln Sie zu "Beschaffung" > "Angebotsanforderungen" > "Alle Angebotsanforderungen".
2. Wählen Sie eine Angebotsanforderung aus, die den Status " Versendet" hat und klicken Sie auf den Link auf der "Angebotsanforderungs-Anfragenummer".
    * Die Angebotsanforderung sollte zu mindestens 2 Händlern gesendet worden sein.  
3. Klicken Sie auf "Kopfzeile", um zur Liste von Händlern zu wechseln.
4. Wählen Sie den Händler aus, für den Sie eine Antwort auf die Angebotsanforderung eingeben möchten.
5. Klicken Sie auf "Antwort eingeben".
6. Klicken Sie im Aktivitätsbereich auf "Antworten".
7. Klicken Sie auf "Daten in Antwort kopieren".
    * Diese Aktivität kopiert ausgewählte Daten beispielsweise die Menge aus der Angebotsanforderungsanfrage in die Antwort auf die Angebotsanforderung. Alternativ können Sie diese Aktivität überspringen und alle Antwortfelder manuell ausfüllen, wenn Sie die Antwort bearbeiten.  
8. Klicken Sie auf "Bearbeiten".
9. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
10. Wählen Sie die andere Angebotsposition aus.
11. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.

## <a name="score-the-bid"></a>Bewerten Sie das Angebot
1. Klicken Sie auf "Kopfzeile", um zur Bewertung des Angebots zu wechseln.
2. Erweitern Sie den Abschnitt "Angebotsbewertung".
3. Geben Sie im Feld "Bewertung" eine Zahl für eines der Bewertungskriterien ein.
    * Wenn Sie auf einen der Bewertungskriterien zeigen, zeigt eine QuickInfo den Bereich an, innerhalb dem Sie bewerten müssen. In dieser Demo können Sie eine Zahl zwischen 1 und 5 jedem beliebigen der Kriterien hinzufügen.  
4. Wählen Sie ein anderes Bewertungskriterium aus.
5. Geben Sie im Feld "Bewertung" eine Zahl ein.
6. Erweitern Sie den Abschnitt "Fragebögen".
    * Wenn die Angebotsanforderungsanfrage einen Fragebogen hat, der an die Händler gesendet wurde, können Sie deren Antworten im Bereich "Fragebogen" eingeben.  
7. Schließen Sie die Seite.

## <a name="enter-a-reply-for-another-vendor"></a>Geben Sie eine Antwort für einen anderen Händler ein
1. Wählen Sie den nächsten Händler aus, indem Sie den Händler deaktivieren, für den Sie soeben die Antwort eingegeben haben, und wählen Sie dann die Zeile für den nächsten Händler aus.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie auf "Antwort eingeben".
4. Klicken Sie auf "Daten in Antwort kopieren".
5. Klicken Sie auf "Bearbeiten".
6. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
7. Wählen Sie die andere Angebotsposition aus.
8. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.

## <a name="score-the-second-bid"></a>Bewerten Sie das zweite Angebot
1. Klicken Sie auf "Kopfzeile", um zur Bewertung des Angebots zu wechseln.
2. Geben Sie im Feld "Bewertung" eine Zahl ein.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Geben Sie im Feld "Bewertung" eine Zahl ein.

## <a name="compare-the-replies"></a>Vergleichen Sie die Angebote
1. Klicken Sie im Aktivitätsbereich auf "Allgemein".
2. Klicken Sie auf "Antworten vergleichen".
3. Geben Sie im Feld "Rang" eine Zahl ein.
    * Auf dieser Seite werden die Angebote mit dem Kopf und den Positionen angezeigt sowie die Gesamtbewertung auf Kopfzeilenebene. Sie können die Positionen vergleichen, indem Sie im Raster sortieren, damit vergleichbare Positionen nebeneinander sind. Die Informationen enthalten außerdem: Menge: Die vom Händler angegebene Menge. Dies muss nicht mit der Menge, die in der Angebotsanforderung angegeben ist, übereinstimmen.   Nettobetrag: Der von einem Händler angegebene Preis für die Artikel in der Position, nach Abzug aller Rabatte.   Abweichung: Die Anzahl der Tage, um die das Lieferdatum im Angebotskopf oder der Angebotsposition vom angeforderten Lieferdatum im Angebotsanforderungskopf oder der Angebotsanforderungsposition abweicht.   Sie können einen Rang für jedes Angebot eingeben.  
4. Wählen Sie die Kopfzeilenposition für das andere Angebot aus, dem Sie einen Rang zuweisen möchten.
5. Geben Sie im Feld "Rang" eine Zahl ein.
6. Klicken Sie auf "Speichern".

## <a name="reject-a-bid"></a>Lehnen Sie ein Angebot ab
1. Wählen Sie die Kopfzeilenposition für das Angebot aus, das Sie ablehnen möchten.
    * Sie können ein Angebot oder Positionen innerhalb eines Angebots auf einmal annehmen, ablehnen oder zurückgeben.  
2. Wählen Sie das Kontrollkästchen "Markieren" aus.
    * Wenn Sie das Kontrollkästchen "Markieren" im Kopf des Angebots aktivieren, dann werden alle Positionen ebenfalls markiert. Sie können auch wählen, eine Untergruppe der Positionen innerhalb des Angebots zu markieren, um diese abzulehnen oder anzunehmen. Es ist möglich, das Angebot eines Händlers für manche Positionen einer Angebotsanforderung anzunehmen und dann andere Angebotsanforderungspositionen einem anderen Händler zu erteilen. Sie müssen dies jedoch in zwei Schritten ausführen, mit einem Schritt auf einmal. Wenn alternative Positionen vorhanden sind, können Sie entweder die Original-Angebotsposition oder deren Alternative, aber nicht beides akzeptieren.  
3. Klicken Sie auf "Ablehnen".
4. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".
5. Geben Sie im Feld "Ablehnungsgrund" einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Grund für die Ablehnung wird auf der Antwort gespeichert.  
6. Klicken Sie auf "OK".
7. Klicken Sie auf "OK".
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Aktualisieren Sie die Seite.

## <a name="accept-a-bid"></a>Nehmen Sie ein Angebot an
1. Wählen Sie das Angebot aus, das Sie annehmen möchten aus und klicken Sie dann auf den Link im Feld "Angebotsanforderung".
2. Klicken Sie im Aktivitätsbereich auf "Antworten".
3. Klicken Sie auf "Annehmen".
    * Wenn Sie bestimmte Positionen markiert haben und nicht andere, dann wird die Annahmeaktivität nur die markierten Positionen umfassen. Wenn Sie alle Positionen zum Angebot annehmen möchten, dann müssen Sie die Positionen nicht markieren.  
4. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".
    * Dies ermöglicht es Ihnen, einen Grund für die Annahme des Angebots zu erfassen. Der Grund wird im Angebot gespeichert.  
5. Geben Sie im Feld "Annahmegrund" einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie auf "OK".
7. Klicken Sie auf "OK".
    * Wenn Sie auf "OK" klicken, wird dadurch eine Bestellung auf Grundlage der Positionen generiert, die in der Angebotsanforderungsannahme enthalten sind. Wenn es weitere Angebote gibt, die nicht verarbeitet wurden (angenommen, abgelehnt oder zurückgegeben), wird das System Sie dazu auffordern, die verbleibenden Angebote abzulehnen.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Zeigen Sie die Bestellung an, die erstellt wurde
1. Klicken Sie im Aktivitätsbereich auf "Allgemein".
2. Klicken Sie auf "Bestellung".
    * Hier können Sie die Bestellung anzeigen, die generiert wurde, als Sie das Angebot angenommen haben.  
3. Schließen Sie die Seite.
4. Schließen Sie die Seite.
5. Schließen Sie die Seite.
6. Schließen Sie die Seite.


