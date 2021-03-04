---
title: Debitorenrückvergütungen generieren und verarbeiten
description: Diese Verfahren zeigt, wie von Debitorenrückvergütungen aus der Anspruchsgenerierung so weit des Übergebens sie als Abgrenzungen zu Debitoren verarbeitet.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage, MCRBrokerWriteOffReason, MRCHierarchyAddCust, PdsItemRebateGroup, PdsRebate, PdsRebateProgramTMATable, PdsRebateTable, PdsRebateTableListPagePreviewPane, PdsRebateTrans, PdsRebateType_CustLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8ebc281036842bdc8965e062990438e1fb466ff
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428830"
---
# <a name="generate-and-process-customer-rebates"></a>Debitorenrückvergütungen generieren und verarbeiten

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie von Debitorenrückvergütungen aus der Anspruchsgenerierung so weit des Übergebens sie als Abgrenzungen zu Debitoren verarbeitet. Sie läuft Sie durch ein besonderes Beispiel seitens, um zu erläutern, wie die verschiedenen Bedingungen auf den Rückvergütungspositionen die Endbetrag auswirken, die den Debitor gutgeschrieben werden. Sie müssen das USMF-Demodatunternehmen verwenden und führen die folgenden Aufgaben von, bevor Sie Handbuch starten: (1) Für die der Debitorenparameterseite und erweitern die Registerkarte Preise und dann die Preisdetailregisterkarte und prüfen, ob die aktivierens-Preisdetailoption auf "Ja" festgelegt ist. (2) Die Seite "Rückvergütungsvereinbarungen" aufrufen und die Debitorenrückvergütungsvereinbarung auswählen: USMF-000001. Wenn das Workflowgenehmigungsstatusfeld nicht zu genehmigtem festgelegt wird, benötigen Sie auf Prüfung im Aktivitätsbereich, um ihn zu genehmigen.


## <a name="review-a-customer-rebate-agreement"></a>Erstellen einer Debitorennachlassvereinbarung
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Debitorenrückvergütungen > Rückvergütungsvereinbarungen**.
    - Die nächsten Schritte berücksichtigen die Bedingungen der Vereinbarung USMF-000001. Dies vereinfacht die, zu veranschaulichen, wie die Debitorenkreditwerte später in der Prozedur berechnet werden.  
    - Die Vereinbarung gilt für einen einzelnen Debitor, in diesem Beispielsdebitor US-009.  
    - Der Debitor Nachlässe von gegeben, wenn Sie ein bestimmtes Produkt erwerben. In diesem Fall hat das Produkt Artikelnummer T0020.   
    - Das Verkaufsleistung des Debitors, für das die Rückvergütung ist, werden vorkalkuliert, wöchentlich kumuliert werden sollen.  
    - Die Einstellungen für den Ursprung des Preises ist „Brutto“, was bedeutet, dass der Umsatzbetrag der Position, auf dessen Grundlage der Anspruch vorkalkuliert wird, nicht durch den Positionsrabatt verringert wird.  
    - Das Rückvergütungszeilenumbruch-Typfeld zeigt die Methode zum Berechnen von Nachlässen. In diesem Fall für die die Umsatzvorgabe für Nachlässe bewertet werden sollen, wird der Menge festgelegt.   
    - Die Positionen der Vereinbarung geben den Nachlassbetrag Typ, den tatsächlichen Nachlasswert und die Schwellenwerte. In diesem Beispiel gemäß Abschnitt der Debitor für eine Rückvergütung von EUR 20 pro die verkaufte Einheit, wenn deren wöchentlichen Einkäufe des Produkts innerhalb von 1 bis 50 Einheiten fallen; und einen Rabatt von 40 EUR pro verkaufte Einheit, wenn sie über 50 Einheiten kaufen.  
2. Schließen Sie die Seite.

## <a name="generate-rebate-claims"></a>Kreditorenrückvergütungsansprüche erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Aufträge > Alle Aufträge**.
2. Klicken Sie auf **Neu**. Um die Methode zu imitieren in der Nachlass nicht eingefordert würde, die nächste Aufgabe ist einen Auftrag zu erstellen generiert, in dem das Produkt und die Menge den Debitor qualifiziert werden, der für eine Rückvergütung betreffende ist.    
3. Geben Sie im Feld **Debitorenkonto** einen Wert ein oder wählen Sie einen Wert aus.
4. Klicken Sie auf **OK**.
5. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
6. Legen Sie **Menge** auf „40“ fest.
7. Unter dem Abschnitt **Auftragspositionen** klicken Sie auf die **Auftragspositionszeile**.
8. Klicken Sie auf **Preisdetails**. Wenn Sie diese Option nicht angezeigt wird, kann sie, da die Option **Preisdetails aktivieren** nicht auf „Ja“ festlegen, bevor Sie Handbuch diese Nummer.     
9. Erweitern Sie den Abschnitt **Rückvergütungen**. Die Registerkarte **Rückvergütungen** listet alle Rückvergütungsvereinbarungen auf, die für die aktuelle Auftragsposition gültig sind und zeigt den vorkalkulierten Rückvergütungbetrag. Beachten Sie, dass die angezeigten Beträge nur Angabe sind dazu, was zukünftige Rückvergütungsansprüche möglicherweise sind. Die tatsächlichen Rückvergütungsbeträge können abhängig von abweichen: das Gesamtumsatzvolumen erzielt vom Debitor unter einer regelmäßigen Nachlassvereinbarung; ob der Debitor alle oder Teilmengen zurückgegeben wurde ein; und ob der entsprechende Auftrag fakturiert wurde.
10. Schließen Sie die Seite.
11. Klicken Sie auf **Position hinzufügen**.
12. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
13. Legen Sie **Menge** auf „60“ fest.
14. Klicken Sie auf **Speichern**.
15. Klicken Sie im **Aktivitätsbereich** auf **Rechnung**.
16. Klicken Sie auf **Rechnung**.
17. Erweitern Sie den Abschnitt **Parameter**.
18. Wählen Sie im Feld **Menge** die Option „Alle“ aus.
19. Klicken Sie auf **OK**.
20. Klicken Sie auf **OK**.

## <a name="process-rebate-claims"></a>Nachlassansprüche verarbeiten
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Debitorenrückvergütungen > Rückvergütungen**.
    - Die Rückvergütungsseite agiert ein Werktisch, in dem Sie prüfen, genehmigen und können Prozeßrückvergütungsansprüche. Verarbeiten Sie nun die Ansprüche, die bei der Fakturierung eines Auftrags für Debitor US-009 erstellt wurden, der der Betreff der Rückvergütungsvereinbarung USMF-000001 ist.   
    - Die erste Zeile stellt einen Rückvergütungsanspruch für 800 EUR, der auf dem Verkauf von 40 Einheiten des Produkts T0020 ist, berechnet bei 20 EUR pro Einheit dar. Dieses entspricht die Bedingungen der ersten Mengenpause in der Nachlassvereinbarung ab.  
    - Der zweite Anspruch liegt bei 2.400 EUR, der auf dem Verkauf von 60 Einheiten des Produkts T0020 ist, berechnet bei 40 EUR pro Einheit, aufgrund der zweiten Mengenpause in der Vereinbarung.  
    - Beide Ansprüche sind im Status „Zu berechnen“. Das bedeutet, dass sie mit einer Vereinbarung zugeordnet sind, die das Verkaufsleistung des Debitors auf Basis regelmäßiger verfolgt und dass sie neu berechnet werden müssen, um das Gesamtumsatzvolumen innerhalb der betreffenden Periode abzulegen.   
2. Klicken Sie auf **Kumulieren**.
3. Geben Sie im Feld **Debitor** einen Wert ein, oder wählen Sie einen Wert aus.
4. Das **Startdatum** darf nicht vor dem heutigen Datum liegen.
5. Klicken Sie auf **OK**. Infolge der Ausführung im Funktion **Kumulieren**, ist der vorkalkulierte Anspruchsbetrag nun reguliert wurden, um die Verwendung zu erläutern, dass das Gesamtumsatzvolumen des Debitors in die zutreffende Periode höher als ist, als erste Nachlass generiert wurde. Im bestimmten Fertigartikel da die Summe eingekaufte Menge 100 Einheiten erreicht hat, gemäß Abschnitt der Debitor nun für 40 EUR pro Einheit (gemäß der zweiten Mengenpause der Vereinbarung) oder 400 EUR des gesamten Rückvergütungsbetrags. Die Differenz wird als neuer Anspruch "Regulierung" für die zusätzlichen 800 EUR erfasst. Der Status der Rückvergütungsansprüche, die in im Aktualisierung einbezogen waren, werden jetzt zu berechnetem festgelegt. 
6. Schalten Sie in der Liste 'Alle Zeilen markieren' ein/aus.
7. Klicken Sie auf **Genehmigen**.
8. Klicken Sie auf **Verarbeiten**.
9. Geben Sie im Feld **Debitor** einen Wert ein, oder wählen Sie einen Wert aus.
10. Klicken Sie auf **OK**. Eine Meldung zeigt an, dass die Rückvergütung erfolgreich verarbeitet wurde, und der Status der Ansprüche wurde geändert, um zu markieren. Das bedeutet, dass als Ergebnis einer Rückvergütung eine Abgrenzungserfassung gebucht wird:
    - Die Ansprüche wurden jetzt als Abzug zum temporären Debitorensaldo übertragen.
    - Die Rückvergütungs-Abgrenzungserfassung wurde gutgeschrieben, um die zukünftigen Verbindlichkeiten für den Debitor darzustellen.
    - Das ist Rückvergütungsausgabenkonto wurde belastet, um die Kosten darzustellen, die in Verbindung mit dem Verkauf angefallen sind.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]