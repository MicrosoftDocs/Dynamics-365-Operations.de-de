---
title: Angebotsanforderungsangebote eingeben und vergleichen und Verträge vergeben
description: In diesem Thema wird erklärt, wie Sie Antworten auf eine Angebotsanforderung (RFQ) eingeben, Angebote bewerten und vergleichen und dann mit einem der Händler einen Vertrag machen.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7c43516fc90224439f6f7cfd5fd0a6058e8b39
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429132"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Angebotsanforderungsangebote eingeben und vergleichen und Verträge vergeben

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie Antworten auf eine Angebotsanforderung (RFQ) eingeben, Angebote bewerten und vergleichen und dann mit einem der Händler einen Vertrag machen. Sie können diese Prozedur im Demodatunternehmen **USMF** verwenden.

Bevor Sie diese Prozedur beginnen, müssen Sie eine Angebotsanforderung (RFQ) mit zwei Positionen haben, die mindestens zwei Händlern gesendet wurde. Um diese Angebotsanforderung zu erstellen, führen Sie die Prozedur [Erstellen einer Angebotsanforderung](create-request-quotation.md) aus. Die Bewertungskriterien müssen ebenfalls eingerichtet sein, bevor Sie diese Prozedur ausführen können.

Sie können das Angebot entweder als Lieferant oder als Beschaffungsspezialist eingeben. Weitere Informationen finden Sie unter [Kreditorenzusammenarbeit einrichten und verwalten](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Geben Sie eine Antwort als Lieferant ein

1. Wählen Sie auf dem Dashboard **Bieten als Lieferant** aus.
2. In der **Neue Angebotseinladungen** Liste finden Sie Angebotsanforderung, die soeben übermittelt wurde. Wählen Sie die Angebotsanforderung aus, um zu prüfen, was angefordert wurde.
3. Wählen Sie **Angebotsanforderungsanhänge** aus, um alle Anhänge zu überprüfen, die hinzugefügt wurden.
4. Wählen Sie **Angebot**, um die Felder zu bearbeiten. Beachten Sie, dass das Feld **Angebotsfortschritt** auf **Kreditor aktualisiert** festgelegt ist.
5. Im Kopf und den Positionen geben Sie die entsprechenden Werte von der Angebotsantwort ein.
6. Wenn irgendwelche Anhänge dem Angebot hinzugefügt werden sollen, wählen Sie **Anhänge für Angebote**.
7. Wählen Sie die Registerkarte **Führende Artikel für Angebote**, um anzuzeigen, ob alle Dokumente erforderlich sind.
8. Wählen Sie das Inforegister **Ergänzungen**, um anzuzeigen, ob die Angebotsanforderung ergänzt wurde.
9. Wählen Sie im Inforegister **Fragebogen** aus. Sämtliche Fragebögen, die hier angezeigt werden, müssen beantwortet werden.
10. Wählen Sie das Inforegister **Positionsdetails** aus, um ausführlichere Informationen zur Position anzuzeigen.
11. Wählen Sie **Angebotsanforderung zurücksetzen** nur, wenn Sie die Werte zurücksetzen müssen, die in den ursprünglichen Angebotsanforderungswerten eingegeben wurden.
12. Sie können das Angebot jederzeit speichern und später weiter verarbeiten, vorausgesetzt, dass das Ablaufdatum und die Zeit noch  nicht überschritten wurde. In diesem Fall fiden Sie das Angebot in der Liste **Angebot in Bearbeitung** im Arbeitsbereich **Lieferantenangebot**.
13. Wenn das Angebot sum Senden bereit ist, wählen sie **Übermitteln** aus. Wenn Sie kein Angebot unterbreiten möchten, wählen Sie **Ablehnen** aus. Gesendete Angebote sind in der Liste **Gesendete Angebote** im Arbeitsbereich **Lieferantenangebote** verfügbar.  
14. Nachdem das Angebot gesendet ist, können Sie es jederzeit vor dem Ablaufdatum und der Zeit jederzeit erneut aufrufen. Beachten Sie, dass, wenn ein Angebot erneut aufgerufen wird, eas als nicht übermittelt betrachtet wird. Wenn das Angebot von der Beschaffungsabteilung angenommen oder abgelehnt wird, erscheint es entweder als **Zugesprochene Angebote** oder **Verlorene Angebote** im Arbeitsbereich **Lieferantenangebote**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Geben Sie eine Antwort eines Lieferanten als Beschaffungsspezialist ein

1. Überprüfen Sie, ob die Berechtigung, Lieferantenangebote zu bearbeiten eingerichtet ist. Gehen Sie zu **Beschaffung und Ursproung\> Einstellungen \> Beschaffungs- und Ursprungsparameter**. Auf der Registerkarte **Angebotsanforderungen** legen Sie die Option **Einkäufer kann Liederantenangebot bearbeiten** auf **Ja** fest.
2. Wechseln Sie zu **Beschaffung und Ursprung \>Angebotsanforderungen \> Alle Angebotsanforderungen**.
3. Wählen Sie eine Angebotsanforderung aus, die den Status **Versendet** hat und klicken Sie auf den Link im Feld **Angebotsanforderungs-Anfragenummer**.
4. Wählen Sie **Antworten verwalten**. Die Seite, die erscheint, zeigt eine Angebotsanforderung für jeden Lieferanten, der eingeladen wurde, ein Angebot abzugeben.
5. Wählen Sie eine Angebotsanforderung aus, auf die nicht geantwortet wurde. (Das Feld **Antwortsfortschritt** muss auf **Nicht gestartet** festgelegt werden.)
6. Wählen Sie **Bearbeiten \> Angebotsanforderung bearbeiten** aus. Die Seite **Angebotsanforderungsantwort** wird angezeigt. Als Beschaffungsspezialist können Sie nun im Namen des Lieferanten die Antwort eingeben. Beachten Sie, dass das Feld **Angebotsfortschritt** auf **Lieferant aktualisiert** festgelegt ist.  
7. Angebotsdaten eingeben. Klicken Sie abschließend auf **übermitteln**.

## <a name="score-the-bids"></a>Bewerten Sie die Angebote

1. Auf der Seite **Alle Angebotsanforderungen** wählen Sie die Angebotsanforderungsfall aus, für den Sie Antwortpunkte geben  wollen.
2. Wählen Sie **Antworten verwalten**.
3. Wählen Sie die Antwort für die Bewertung aus.
4. Wählen Sie **Kopfzeile**, damit Sie die Auswertung für das Angebot sehen.
5. Geben Sie im Inforegister **Angebotsbwertung** eine Zahl im Feld **Bewertung** für die Bewertungskriterien ein. Wenn Sie mit der Maus über ein Bewertungskriterium fahren, zeigt die QuickInfo den Bereich an, innerhalb dem Sie bewerten müssen. In dieser Demo können Sie eine Zahl zwischen 1 und 5 für jedes beliebige Bewertungskriterium einfügen.  
6. Wiederholen Sie Schritt 5 für ein anderes Auswertungskriterium.
7. Wenn die Angebotsanforderungsanfrage einen Fragebogen hat, der an die Lieferanten gesendet wurde, können Sie deren Antworten im Bereich **Fragebogen** eingeben.
8. Schließen Sie die Seite.
9. Wiederholen Sie die Schritte 1 bis 8 für alle anderen Angebote.

## <a name="compare-the-replies"></a>Vergleichen Sie die Angebote

1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Antworten vergleichen** aus.
2. Geben Sie im Feld **Rang** eine Zahl ein.  
    - Auf dieser Seite werden die Angebote mit dem Kopf und den Positionen angezeigt und auch die Gesamtbewertung auf Kopfzeilenebene. Sie können die Positionen vergleichen, indem Sie sie im Raster sortieren, damit vergleichbare Positionen nebeneinander angezeigt werden. In diesem Thema sind die folgenden Infromationen ebenfalls enthalten:
    - **Menge** – Die von einem Lieferanten angegebene Menge. Diese Menge muss nicht mit der Menge übereinstimmen, die in der Angebotsanforderung angegeben ist.
    - **Nettobetrag** – Der Preis, der ein Lieferant für den Arkel in der Position angibt, abzüglich allfällige Rabatte.
    - **Abweichung** – Die Anzahl der Tage, um die das Lieferdatum im Angebotskopf oder der Angebotsposition vom angeforderten Lieferdatum im Angebotsanforderungskopf oder der Angebotsanforderungsposition abweicht. Sie können einen Rang für jedes Angebot eingeben.  
3. Wählen Sie die Kopfzeilenposition für das andere Angebot aus, dem Sie einen Rang zuweisen möchten.
4. Geben Sie im Feld **Rang** eine Zahl ein.
5. Wählen Sie **Speichern**.

## <a name="reject-a-bid"></a>Lehnen Sie ein Angebot ab

1. Wählen Sie die Kopfzeilenposition für das Angebot aus, das Sie ablehnen möchten. Sie können ein Angebot oder die Positionen innerhalb eines Angebots nur einmal annehmen, ablehnen oder zurückgeben.
2. Wählen Sie das Kontrollkästchen **Markieren** aus.  
    - Wenn Sie das Kontrollkästchen **Markieren** im Kopf des Angebots aktivieren, dann werden alle Positionen ebenfalls markiert. Um nur einige der Positionen im Angebot abzulehnen oder zu akzeptieren, können Sie einfach nur diese Positionen markieren. Zusätzlich können Sie ein Angebot des Lieferanten für einige Positionen einer Angebotsanforderung akzeptieren, und dann andere Angebotsanforderungspositionen an einen anderen Lieferanten vergeben. Allerdings müssen Sie ein Angebot nach dem andern ausführen.  
    - Wenn alternative Positionen vorhanden sind, können Sie entweder die Original-Angebotsposition oder deren Alternative, aber nicht beide akzeptieren.  
3. Wählen Sie **Ablehnen** aus.
4. Wählen Sie **Parameter**, und dann **Ablehnungsgrund** im Feld und geben Sie den Grund für die Ablehnung des Angebots aus oder wählen Sie diesen aus. Der Grund wird in der Antwort gespeichert.  
5. Wählen Sie **OK**.
6. Wählen Sie **OK**.

## <a name="accept-a-bid"></a>Nehmen Sie ein Angebot an

1. Wählen Sie das Angebot aus, das Sie annehmen möchten und klicken Sie dann auf den Link im Feld **Angebotsanforderung**. Wenn Sie auf der Seite **Antworten auf Angebotsanforderung vergleichen** sind, dannist das markierte Angebot im Fokus das Angebot, das das System während der Akzeptierungsaktivität in Erwägung zieht. Sie können Positionen nur von einem Angeobt gleichzeitig akzeptieren.  
2. Klicken Sie im Aktivitätsbereich auf **Antworten**.
3. Wählen Sie **Akzeptieren** aus. Wenn Sie nur bestimmte Positionen markieren, enthält die Angenommeneaktivität nur die Positionen. Wenn Sie alle Positionen zum Angebot annehmen möchten, dann müssen Sie die Positionen nicht markieren.  
4. Wählen Sie **Parameter**, und dann **Akzeptierungsgrund** im Feld und geben Sie den Grund für die Akzeptierung des Angebots aus oder wählen Sie diesen aus. Der Grund wird im Angebot gespeichert.  
5. Wählen Sie **OK**.
6. Wählen Sie **OK**. Wenn Sie auf **OK** klicken, wird dadurch eine Bestellung auf Grundlage der Positionen generiert, die in der Angebotsanforderungsannahme enthalten sind. Wenn es weitere Angebote gibt, die nicht verarbeitet wurden (angenommen, abgelehnt oder zurückgegeben), wird das System Sie dazu auffordern, alle verbleibenden Angebote abzulehnen.  

## <a name="view-the-purchase-order-that-is-generated"></a>Zeigen Sie die Bestellung an, die dazu erstellt wurde

Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Bestellung** aus. Die Seite, die angezeigt wird, zeigt die Bestellung an, die generiert wurde, als Sie das Angebot angenommen haben.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]