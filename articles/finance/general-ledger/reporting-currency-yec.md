---
title: Berichtswährung aus dem Gleichgewicht, wenn der Jahresabschluss ausgeführt wird
description: In diesem Artikel wird erläutert, wie die Berichtswährung beim Jahresabschluss aus dem Gleichgewicht geraten kann.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850260"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>Berichtswährung aus dem Gleichgewicht, wenn der Jahresabschluss ausgeführt wird

Nachdem Sie die Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** (die Funktion **Unterschied**) aktiviert haben, werden die Hauptbuchtransaktionen, die abgerechnet wurden, werden nicht mehr in die Eröffnungsbilanz des nächsten Geschäftsjahres aufgenommen, wenn der Jahresabschluss des Hauptbuchs ausgeführt wird. Der Ausschluss von abgerechneten Hauptbuchtransaktionen kann für Kunden am Jahresende eine Herausforderung darstellen, wenn für das Hauptbuch eine Berichtswährung definiert ist.

Der Sachkontoausgleich erfolgt nur für die Buchhaltungswährung. Wenn Hauptbuchtransaktionen abgerechnet werden, bestätigt die Validierung nur, dass die Belastungen in der Buchhaltungswährung den Gutschriften in der Buchhaltungswährung entsprechen. Die Berichtswährungsbeträge für diese Sachkontotransaktionen werden nicht validiert, und Belastungen entsprechen möglicherweise nicht den Gutschriften. Darüber hinaus berechnet und verbucht der Hauptbuchausgleich nicht automatisch einen Gewinn/Verlust in der Berichtswährung.

Aufgrund dieser Einschränkungen muss eine Gewinn-/Verlust-Transaktion in der Berichtswährung vorliegen, wenn die Sachkontoabrechnung erfolgt. Wenn kein Gewinn/Verlust in der Hauptbuchabrechnung enthalten ist, wird eine Ungleichgewichtsmeldung angezeigt, wenn der Jahresabschluss ausgeführt wird.

Im folgenden Beispiel werden die Schritte zur Behebung dieses Problems vor dem Jahresabschluss beschrieben.

## <a name="example-setup"></a>Beispiel für die Einrichtung

Um dieses Beispiel einzurichten, aktivieren Sie die Funktion **Unterschied** und richten Sie das Hauptkonto 110180 für die Hauptbuchabrechnung ein. Die folgende Abbildung zeigt die Sachkontobuchungen, die in der juristischen Person DEMF gebucht wurden. Die Rechnungswährung für DEMF ist US-Dollar (USD) und die Berichtswährung ist Euro (EUR).

![Gebuchte Hauptbuchtransaktionen in der Berichtswährung.](./media/reporting-currency-1.png)

Die Seite **Hauptbuchabrechnungen** zeigt die Hauptbuchtransaktionen für das Hauptkonto 110180. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) im Raster und wählen Sie dann **Spalten einfügen**. Fügen Sie die Spalte **Betrag in Berichtswährung** hinzu, sodass die Beträge in Transaktionswährung, Buchhaltungswährung und Berichtswährung angezeigt werden.

![Betrag in der Berichtswährungsspalte, die der Seite „Sachkontoabrechnungen“ hinzugefügt wurde.](./media/Ledger-settlement2.png)

Die ersten beiden Hauptbuchtransaktionen für 100.00 EUR werden als eine Gruppe abgerechnet, und die nächsten beiden Hauptbuchtransaktionen für 100.00 EUR werden als eine andere Gruppe abgerechnet. (Die beiden Transaktionen haben unterschiedliche Abrechnungs-IDs.) Diese Einrichtung zeigt, dass Organisationen mehrere Gruppen von Hauptbuchtransaktionen haben, die zu unterschiedlichen Zeiten abgerechnet werden und unterschiedliche Abrechnungsdaten haben. Nach dem Abschluss des Ausgleichs zeigt die Seite **Sachkontoabrechnungen** die folgenden Informationen an, wenn sie gefiltert wird, um die Transaktionen mit dem Status **Ausgeglichen** anzuzeigen.

![Ausgeglichene Buchungen auf der Sachkontoausgleichseite.](./media/Settled-trans-filtered3.png)

Wählen und halten Sie (oder rechtsklicken) Sie auf der Seite **Sachkontoausgleiche** in der Spalte **Betrag** und wählen Sie dann **Summe dieser Spalte**. Wiederholen Sie diesen Schritt für die Spalten **Betrag in Berichtswährung**. Die Buchhaltungswährung muss eine Differenz von 0 (Null) aufweisen, damit eine Abrechnung erfolgen kann. Es erfolgt jedoch keine Validierung des Abrechnungsbetrags für die Berichtswährung. Die folgende Abbildung zeigt eine Differenz von -27,79 USD für die Berichtswährung.

![Unterschied für die Berichtswährung.](./media/Difference4.png)

## <a name="year-end-close"></a>Jahresabschluss

Wird nun der Jahresabschluss für 2022 durchgeführt, endet der Prozess mit einem Out-of-Balance-Error. Dieser Fehler wird direkt durch die Tatsache verursacht, dass die Berichtswährung keinen Sachkontoausgleichsbetrag hat, der sich auf 0 (Null) saldiert.

![Fehlermeldung, die angibt, dass der Abrechnungsbetrag des Sachkontos nicht 0 (Null) ist.](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>Gewinn/Verlust in Berichtswährung buchen

Damit der Jahresabschluss erfolgreich durchgeführt werden kann, muss die Differenz des Betrags in der Berichtswährung verbucht werden, typischerweise als Gewinn oder Verlust, und in die Hauptbuchabrechnung aufgenommen werden. Der Berichtswährungsgewinn/-verlust kann auf mehrere Arten gebucht werden:

- Wenn es sich bei dem Hauptkonto um Verbindlichkeiten oder Forderungen handelt, wird die AR/AP-Abrechnung dieser Dokumente den erforderlichen Gewinn/Verlust generieren. Dieser Buchhaltungseintrag muss in den Hauptbuchausgleich aufgenommen werden, wenn die entsprechenden Hauptbuchtransaktionen aus der Rechnung, Zahlungen, Gutschriften usw. ausgeglichen werden.
- Handelt es sich bei dem Hauptkonto um ein anderes Konto als Kreditoren- oder Debitorenkonten, muss der Gewinn/Verlust manuell eingegeben werden. Wenn der Gewinn/Verlust gebucht wird, wird der Detaillierungsgrad für den Buchhaltungseintrag von Ihrer Organisation bestimmt.
- Identifizieren Sie für jedes Hauptkonto den zu verbuchenden Währungsgewinn/-verlustbetrag.

Wie zuvor beschrieben, kann diese Buchung auf der Seite **Hauptbuchabrechnungen** durchgeführt werden.

1. Filtern Sie nach dem Datumsbereich, für den Sie den Gewinn/Verlust buchen möchten. Wenn Sie planen, einen Gewinn/Verlust pro Monat zu veröffentlichen, filtern Sie nach jedem Monat. Wenn Sie planen, einen Gewinn/Verlust pro Geschäftsjahr zu buchen, filtern Sie nach dem ganzen Jahr.
2. Filtern Sie nach dem Hauptkonto.
3. Filtern Sie nach dem Status, sodass nur **Abgewickelte** Transaktionen angezeigt werden.
4. Fügen Sie in der Spalte **Betrag in Berichtswährung** einen Gesamtbetrag hinzu.
5. Wenn Sie den Gewinn/Verlust auf einer detaillierteren Ebene buchen möchten, können Sie eine zusätzliche Filterung nach Abrechnungs-ID, Finanzdimensionen usw. vornehmen. Der Gesamtbetrag für die Spalte **Betrag in Berichtswährung** stellt den Betrag dar, für den der Gewinn/Verlust gebucht wird.
6. Wechseln Sie zu **Hauptbuch \> Erfassungseinträge \> Erfassungen der Berichtswährungsregulierung**.
7. Geben Sie die Transaktion für Gewinn/Verlust ein. Dieses Journal bucht eine Anpassung nur in der Berichtswährung. Die gebuchten Beträge in Transaktionswährung und Buchhaltungswährung sind immer 0 (Null). Wenn dieses Journal noch nicht verwendet wurde, müssen Sie möglicherweise einen Journalnamen mit dem Journaltyp **Währungsanpassung melden** unter **Allgemein erstellen Ledger \> Journaleinrichtung \> Journalnamen**.
8. Wenn das Hauptkonto keine manuelle Eingabe zulässt, wir diese Anpassung nicht gebucht. Möglicherweise müssen Sie daher den Parameter **Manuelle Eingabe nicht zulassen** auf der Seite **Hauptkonto** vorübergehend deaktivieren.

![Manuelle Eingabe auf der Journalbelegseite.](./media/Manual-entry6.png)

Nachdem Sie das Ausgleichsjournal gebucht haben, kehren Sie zur Seite **Hauptbuchabrechnungen** zurück und wählen Sie das Hauptkonto aus, für das Sie den Gewinn/Verlust gebucht haben. Die Gewinn-/Verlustanpassung muss in einer Hauptbuchabrechnung enthalten sein. Da der Berichtswährungsbetrag nicht mit 0 (null) verrechnet werden muss, können Sie alle vorherigen Transaktionen rückgängig machen und dann erneut ausgleichen, aber diesmal den Gewinn/Verlust einbeziehen. Wie genau Sie bei der Buchung des Gewinns/Verlusts und der Abrechnung dieses Gewinns/Verlusts in Hauptbuchabrechnungen vorgehen möchten, hängt von Ihrer Organisation ab.

Die folgende Abbildung zeigt, dass die Transaktionen für 200 EUR nicht abgewickelt und dann wieder zur Abwicklung markiert wurden. Diesmal enthalten sie die Gewinn-/Verlustanpassung.

![Gewinn-/Verlustanpassung auf der Seite Hauptbuchabrechnungen.](./media/gain-loss7.png)

Nachdem die Transaktionen abgerechnet wurden, ändern Sie den Filter **Status** so, dass auf der Seite **Abgerechnete** Transaktionen angezeigt werden. Die Summe für die Spalte **Betrag in Berichtswährung** ist jetzt 0 (Null). Der Jahresabschluss kann nun erfolgreich durchgeführt werden.

![Erfolgreicher Jahresabschluß.](./media/Zero-settled8.png)
