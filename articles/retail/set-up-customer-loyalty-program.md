---
title: "Überblick über die Loyalität"
description: "In diesem Thema werden die Loyalitätsfunktionen innerhalb von Microsoft Dynamics 365 for Retail und die damit verbundenen entsprechenden Einrichtungsschritte behandelt, damit Einzelhändler einfach mit ihrem Treueprogramm anfangen können."
author: scott-tucker
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 09d4e46694e89b648981352f64da4a43ab1522e1
ms.contentlocale: de-de
ms.lasthandoff: 01/04/2019

---

# <a name="loyalty-overview"></a>Überblick über die Loyalität

[!include [banner](includes/banner.md)]

Ein Treueprogramm kann dazu beitragen, die Debitorenloyalität durch die Belohnung der Debitoren für das Kaufen von Produkte in den Einzelhandelsgeschäften zu erhöhen. In Microsoft Dynamics 365 for Retail können Sie einfache oder komplexe Treueprogramme einrichten, die für alle juristischen Personen in einem beliebigen Einzelhandelskanal gelten. In diesem Thema werden die Loyalitätsfunktionen innerhalb von Microsoft Dynamics 365 for Retail und die damit verbundenen entsprechenden Einrichtungsschritte behandelt, damit Einzelhändler einfach mit ihrem Treueprogramm anfangen können.

Sie können Ihr Treueprogramm so einrichten, dass es die folgenden Optionen enthält.

- Richten Sie die mehrere Arten von Belohnungen ein, die Sie in den Treueprogrammen anbieten, und verfolgen Sie Teilnahme an den Treueprogrammen.
- Richten Sie Treueprogramme ein, das die verschiedenen Belohnungsanreize abbildet, die Sie anbieten. Sie können Treueprogrammstufen einrichten, um den Debitoren größere Anreize und Belohnungen anzubieten, die häufig einkaufen oder mehr Geld in Ihren Shops ausgeben.
- Definieren Sie Einnahmenregeln, um die Aktivitäten zu identifizieren, die ein Debitor ausführen muss, um Belohnungen zu erhalten. Sie können auch Tilgungsregeln festlegen, um zu identifizieren, wann und wie ein Debitor Belohnungen einlösen kann.
- Geben Sie Treuekarten von einem beliebigen Einzelhandelskanal, der für den Treueprogrammen teilnimmt, und Treuekarten einer oder mehreren Treueprogrammen aus, aus, für die der Debitor teilnehmen kann angezeigt. Sie können eines Debitorendatensatzes für eine Treuekarte auch verknüpfen, sodass der Debitor Treuepunkte von mehreren Karten zusammenlegen und sie einlösen kann.
- Passen Sie Treuekarten manuell an oder übertragen Sie den Treuebelohnungssaldo von einer Karte auf eine andere, um einem Debitor entgegenzukommen oder um ihn zu belohnen.

## <a name="setting-up-loyalty-programs"></a>Einrichten von Treueprogrammen

Sie müssen mehrere Komponenten einrichten, um die Treuefunktion in Dynamics 365 for Retail zu aktivieren. Das folgende Diagramm zeigt die Treuekomponenten und wie diese zueinander in Beziehung stehen.

![Treuprogramm Einrichtungsprozessfluss](./media/loyaltyprocess.gif "Treueprogramm-Komponenten und wie sie zueinander zugeordnet sind")

## <a name="loyalty-components"></a>Treuekomponenten

In der folgenden Tabelle werden die einzelnen Komponenten beschrieben und wo sie in der Treueeinrichtung verwendet werden.

| Bestandteil                                        | Beschreibung | Wo sie verwendet werden |
|--------------------------------------------------|-------------|-----------------|
| Einrichten von Rabatten (Komponente)                  | Richten Sie die Rabatte ein, die Sie den Debitoren mit Kundentreue anbieten. Beispielsweise können Sie 5 Prozent auf alle Bekleidungsprodukte anbieten. | Rabatte müssen zu den Preisgruppen hinzugefügt werden, bevor Sie in ein Treueprogramm einbezogen werden. Preisgruppen werden den Treueprogrammen und Treuestufen zugewiesen. |
| Einrichten von Preisgruppen (Komponente)               | Preisgruppen werden verwendet, um Preise und Rabatte für Einzelhandelsprodukte zu erstellen und zu verwalten. Richten Sie die Preisgruppen ein, die die Rabatte umfassen, die für Treueprogramme gelten. | Preisgruppen werden Ihren Treueprogrammen und Treuestufen zugewiesen. |
| Einrichten von Kanälen (Komponente)                   | Einzelhandelskanäle sind Shops, die an Ihren Treueprogrammen teilnehmen, wie physische Shops, Onlineshops oder Callcenter. Sie müssen die Einzelhandelskanäle einrichten, bevor Sie ihnen Treueprogramme zuweisen können. | Sie weisen Einzelhandelskanäle einem Treueprogramm zu, wenn der Einzelhandelskanal am Treueprogramm teilnimmt. |
| Einrichten von Treuezahlungsmethoden (Komponente) | Sie müssen eine Zahlungsmethode einrichten, bevor eine Treuekarte an einem Register verwendet werden kann und Treuepunkte im Rahmen eines Treueprogramms eingelöst werden können. Sie müssen auch die Treuezahlungsmethode dem Einzelhandelskanal hinzufügen, bevor Debitoren in der Lage sind, ihre Treuepunkte als Zahlungsmittel für Produkte einzulösen. | Richten Sie eine Treuezahlungsmethode ein, und weisen Sie anschließend die Treuezahlungsmethode zu den Einzelhandelskanälen hinzu, die am Treueprogramm teilnehmen. |
| Einrichten von Datumsintervallen                            | Datumsintervalle bieten eine flexible Methode, um die Dauer festzulegen, die für Treuestufen gilt. Verwenden Sie Datumsintervalle, um anzugeben, wie lange ein Debitor auf einer Stufe bleiben kann, oder wie lange ein Debitor eine Aktivität ausführen muss, um sich für eine Stufe zu qualifizieren. | Datumsintervalle gelten nur, wenn Sie Stufen in Ihren Treueprogrammen verwenden. Sie wählen das Datumsintervall aus, das für Programmstufen gilt, und auch die Datumsintervalle, die auf Programmstufenregeln zutreffen. |
| Einrichten von Belohnungspunkten                             | Belohnungspunkte sind die Arten von Belohnung, die Sie den Debitoren anbieten. Belohnungspunkte können einlösbar oder nicht einlösbar sein. Einlösbare Belohnungspunkte können gegen Produkte eingetauscht werden. Nicht einlösbare Belohnungspunkte werden für Nachverfolgungszwecke verwendet oder um einen Debitor in die nächste Stufe in einem Treueprogramm anzuheben. | Belohnungspunkte werden in Stufenregeln referenziert und werden verwendet, um einen Debitor für eine bestimmte Stufe zu qualifizieren. Belohnungspunkte werden auch in Treueschemas in den Einnahme- und Tilgungsregeln referenziert. In den Einnahmeregeln geben Sie die Belohnungen an, die ein Debitor für eine bestimmte Aktivität erhalten kann. In den Tilgungsregeln geben Sie die Belohnung an, die der Debitor einlösen kann. |
| Einrichten von Treueprogrammen                          | Treueprogramme sind die Kerntreueentität, die Sie anbieten. Jedes Treueprogramm kann Treuestufen haben, die ihm zugewiesen sind. Rabatte und Preisgruppen werden den Treueprogrammen entweder auf Programmebene oder auf Treuestufenebene zugeordnet. | Sie erstellen Treueschemas für Ihre Treueprogramme. Sie weisen Treuekarten Ihren Treueprogrammen zu, und Treuekarten können einem Debitor zugewiesen werden. Einzelhandelskanäle nehmen an den Treueprogrammen teil, die den Treueschemas zugewiesen sind. Jeder Debitor, der eine Treuekarte besitzt, kann an den Treueprogrammen teilnehmen, die der Karte zugewiesen sind. |
| Einrichten von Treuestufen und Stufenregeln              | Treuestufen sind optionale Ebenen, die Sie für Ihre Treueprogramme definieren können. Sie können Basisrabatte und Belohnungen für alle Debitoren einrichten, die am Treueprogramm teilnehmen, und Sie können zusätzliche Rabatte und Belohnungen für Debitoren einrichten, die die verschiedenen Stufen im Programm erklimmen. Für jede Treuestufe, die Sie definieren, können Sie die Regeln einrichten, die einen Debitor für jede Stufe qualifizieren. Sie können auch festlegen, wie lange Debitoren in dieser Stufe bleiben können, nachdem sie erreicht wurde. | Treuestufen und Treuestufenregeln werden in den Treueprogrammen definiert. Wenn Sie keine Treuestufen definieren, qualifizieren sich alle Debitoren, die am Treueprogramm teilnehmen, für die Rabatte, die Sie in der Treueprogrammpreisgruppe zuweisen. Wenn Sie Treuestufen definieren, können Sie Einnahmeregeln und Tilgungsregeln für die Treuestufen im Treueschema einrichten. |
| Einrichten von Treueschemas                           | Treueschemas geben die Einnahmeregeln und Tilgungsregeln an, die für ein ausgewähltes Treueprogramm gelten. Sie weisen Einzelhandelskanäle zu einem Treueschema zu, um zu identifizieren, welches Treueprogramm und welche Einnahmeregeln und Tilgungsregeln für einen Einzelhandelsshop gelten. | Ein Treueschema wird zu einem Treueprogramm und Einzelhandelskanälen zugewiesen. Sie können viele Treueschemas dem gleichen Treueprogramm zuweisen, und Sie können viele Treueschemas zu vielen Einzelhandelskanälen zuweisen. |
| Einrichten von Treuekarten                             | Eine Treuekarte berechtigt den Karteninhaber zur Teilnahme an den Treueprogrammen, die der Karte zugewiesen sind. Treuekarten können anonym ausgestellt werden, oder sie können einem bestimmten Debitor zugewiesen werden. Sie können die Treuebuchungen für eine bestimmte Karte anzeigen, und Sie können eine Zusammenfassung von Treuepunkten anzeigen, die auf der Karte angesammelt wurden. Sie können Treuekarten von einem beliebigen Einzelhandelskanal ausgeben. Sie können eine Treuekarte auch manuell anpassen, um den Debitor in eine andere Stufe hochzustufen, Treuepunkte hinzufügen oder den Treuepunktsaldo von einer Karte auf eine andere übertragen. | Sie weisen Treueprogramme zu einer Treuekarte zu. |

## <a name="loyalty-processes"></a>Treueprozesse

In der folgenden Tabelle werden die Prozesse beschreiben, die ausgeführt werden müssen, um die Loyalitätskonfigurationen und -Daten an Ihre Shops zu senden, und die Treuebuchungen von Ihren Shops abzurufen.

| Prozessname                         | Beschreibung | Seitenname |
|--------------------------------------|-------------|-----------|
| 1050 (Treueinformationen)           | Führen Sie diesen Prozess aus, um die Treuedaten von Microsoft Dynamics 365 for Retail an die Einzelhandelsshops zu senden. Es wird empfohlen, diesen Vorgang für eine regelmäßige Ausführung zu planen, damit Loyalitätsdaten an allen Filialen gesendet werden. | Vertriebsplan |
| Treueschemas verarbeiten              | Führen Sie diesen Prozess aus, um Treueschemas den Einzelhandelskanälen zuzuordnen, denen das Treueschema zugewiesen ist. Dieser Vorgang kann so geplant werden, dass er als Stapelverarbeitungsvorgang ausgeführt wird. Sie müssen diesen Prozess ausführen, wenn Sie die Loyalitätskonfigurationsdaten (z. B. Treueschemas, Treueprogramme oder Treuebelohnungspunkte) ändern. | Treueschemas verarbeiten |
| Offlinetreuebuchungen verarbeiten | Führen Sie diesen Prozess aus, um Treuekarten zu aktualisieren, damit sie Transaktionen einbeziehen, die offline verarbeitet wurden. Dieser Prozess gilt nur, wenn das **Offline verdienen**-Kontrollkästchen auf der Seite **Freigegebene Einzelhandelsparameter** aktiviert ist, damit Belohnungen offline erworben werden können. | Offlinetreuebuchungen verarbeiten |
| Treuekartenebenen aktualisieren            | Führen Sie diesen Prozess aus, um die Einnahmenaktivität des Debitors mit den Stufenregeln für ein Treueprogramm zu vergleichen und um den Stufenstatus des Debitors zu aktualisieren. Dieser Prozess ist nur erforderlich, wenn Sie die Stufenregeln in den Treueprogrammen ändern und wenn Sie die aktualisierten Regeln rückwirkend auf die Treuekarten anwenden möchten, die bereits ausgestellt wurden. Dieser Prozess kann für einzelne Karten als Stapelverarbeitungsvorgang ausgeführt werden. | Treuekartenebenen aktualisieren |

## <a name="loyalty-enhancements"></a>Loyalitätserweiterungen

Einzelhandel hat neue Loyalitätsfunktionen als Teil der Freigabe vom Oktober 2018. Jede der neuen Erweiterungen wird nachstehend erläutert.

- Im Rahmen eines Treueschemas in früheren Versionen können Einzelhändler verschiedene Einnahme- und Tilgungsregeln definieren, um die Belohnungen für Debitoren auf verschiedenen Ebenen zu unterscheiden. Einzelhändler können nun "Zuordnungen" als Teil der Einnahme- und Einlösungsregeln einbeziehen, damit bestimmte Debitorengruppen Teil der vorhandenen Ebenen werden, jedoch unterschiedlich  vergütet werden. Dies verhindert die Anforderung, zusätzliche Ebenen erstellen zu müssen.
    
    > [!NOTE]
    > Die Einnahmeregeln innerhalb eines Treueschemas sind zusätzlich. Wenn Sie beispielsweise eine Regel erstellen, einem Mitglied der Stufe Gold 10 Punkte für jeden US-Dollar zu geben und Sie auch eine Regel für einen Debitor mit Zugehörigkeit "Veteran" erstellen, bei dem er 5 Punkte für jeden US-Dollar erhält, dann würde ein Veteran, der gleichzeitig den Status Gold hat, für 1 US-Dollar 15 Punkte erhalten, da sich der Debitor für beide Positionen qualifiziert. Wenn der Veteran-Debitor kein Mitglied mit Gold-Status ist, dann würde er 5 Punkte für jeden US-Dollar erhalten. Wenn Sie die Änderungen in den Kanälen widerzuspiegeln, aktivieren Sie die **Prozesstreueschemen** und **1050** (Loyalitätsinformationen) Einzelvorgänge.
    
    ![Erträge basieren auf Zugehörigkeit](./media/Affiliation%20based%20earning.png "Ertärge basierend auf Zugehörigkeit")

- Einzelhändler habeb oftmals Sonderpreise für eine bestimmte Debitorengruppe, für die sie die  Treueprogramme nicht anwenden möchten. Beispielsweise Großhändler oder Mitarbeiter, die speziellen Preise und keine Treuepunkte erhalten. Allgemein werden "Zuordnungen" verwendet, um besondere Preise für diese Kundengruppen bereitzustellen. Um bestimmte Debitorengruppen vom Erwerb von Treuepunkten auszuschliessen. kann der Einzelhändler mindestens eine Zuordnungen unter **Ausgeschlossene Zuordnungen** im Bereich Treueschemas angeben. So können Debitoren, die von einer Zuordnung ausgeschlossenen und bestehende Treuprogrammmitglieder sind, keine Treuepunkte für Ihre Einkäufe verdienen. Wenn Sie die Änderungen in den Kanälen widerzuspiegeln, aktivieren Sie die **Prozesstreueschemen** und **1050** (Loyalitätsinformationen) Einzelvorgänge.

    ![Ausgeschlossene Zuordnungen](./media/Excluded%20affiliations.png "Zuordnungen vom Erwerben von Treuepunkten ausschliessen")
    
- Einzelhändler können Treuekartennummern in den Kanälen generieren. Vor der Aktualisierung im Oktober 2018 konnten Einzelhändler physische Treuekarten verwenden oder eine Treuekarte mithilfe einiger eindeutiger Debitoreninformationen wie Telefonnummer generieren. Zum Aktivieren der automatischen Erstellung von Treuekarten in den Ladengeschäften aktivieren Sie **Generieren Sie Treuekartennummer** im Funktionsprofil, das dem Shop zugeordnet ist. Für Online Kanäle können Einzelhändler das IssueLoyaltyCard API verwenden, um Treuekarten für Debitoren zu verwenden. Einzelhändler können entweder eine Treuekartennummer zu diesem API eingeben, das verwendet wird, um die Treuekarte zu generieren, oder das System verwendet den Treuekartenummernkreis in Dynamics 365 for Retail. Wenn der Nummernkreis nicht vorhanden ist, und der Einzelhändler keine Treuekartennummer beim Anrufe des API bereitstellt, wird ein Fehler angezeigt.

    ![Treuekarte erstellen](./media/Generate%20loyalty%20card.png "Erstellt automatisch Treuekartennummer")

- Erworbene und eingelöste Treuepunkte werden nun für jede Buchung und alle Aufträge für die Verkaufsposition gespeichert, sodass der gleiche Betrag rückerstattet oder zurückgenommen werden kann bei vollständigen oder teilweisen Rücklieferungen Darüber hinaus bietet die Sichtbarkeit für Punkte auf der Verkaufspositionsebene die Funktion für Callcenterbenutzer, Debitorenfragen zu der Anzahl gewonnenen oder ausgegebenen Punkten pro Position zu beantworten. Vor dieser Änderung wurden Belohnungspunkte immer bei Rücklieferungen neu berechnet, was zu einem anderen als der ursprüngliche Betrag ergab, wenn die Einnahme- oder Einlösungsregeln geändert wurden, und auch die Callcenterbenutzer hatten  auf der Punktaufschlüsselung nicht die Sichtbarkeit. Die Punkte können mit dem Formular **Kartenbuchungen** für jede Treuekarte angezeigt werden.    
- Einzelhändler können die betreffende Periode für jeden Belohnungspunkt nun definieren. Eine betreffende Periodenkonfiguration definiert die Dauer vom Erwerbungsdatum, nachdem die Treuepunkte für die Debitoren zur Verfügung stehen. Nicht übertragene Punkte können in der Spalte **Nicht übertragene Punkte** auf der Seite **Treuekarten** angezeigt werden. Darüber hinaus können Einzelhändler die maximalen Treuepunkte pro Treuekarte definieren. Dieses Feld kann verwendet werden, um die Auswirkung des Treuepunktebetrugs zu reduzieren. Wenn die maximalen Prämienpunkte erreicht wurden, kann der Benutzer keine Punkte mehr erwerben. Der Einzelhändler kann entscheiden, solche Karten zu sperren, bis der potenzielle Betrug untersucht wurde. Wenn der Einzelhändler den Betrug bestätigt, kann der Einzelhändler die Treuekarte für den Debitor sperren und den Debitor auch als gesperrt markieren. Klicken Sie hierfür auf die Eigenschft**Debitor für Treuepunkteregistrierung sperren** und wählen Sie **Ja** unter **Alle Debitoren** auf dem Inforegister **Einzelhandel**. Den gesperrten Debitoren kann nun keine Treuekarte mehr in einem der Kanäle ausgestellt werden.

    ![Übertragen und maximal vergebende Punkte](./media/Vesting%20and%20maximum%20reward%20points.png "Definieren Sie die Übertragung und die maximale Anzahl Punkte")

- Zuordnungen werden verwendet, um bestimmte Preise und Rabatte bereitzustellen, aber es gibt gewisse Zuordnungen, die der Einzelhändler seinen Kunden nicht anzeigen möchten. Beispielsweise wird eine Zugehörigkeit mit dem Titel "Debitor mit hohen Ausgaben" nicht von allen Kunden gut aufgenommen. Darüber hinaus gibt es bestimmte Zuordnungen, die nicht im Shop verwaltet werden sollen, beispielsweise Mitarbeiter, weil Sie nicht möchten, dass die Kassierer entscheiden, wer ein Mitarbeiter ist und so Mitarbeiter-basierte Rabatte gewährt. Einzelhändler können die Zuordnungen nun auswählen, die in den Einzelhandelskanälen ausgeblendet werden sollen. Die Zuordnungen, die als **Ausblenden in den Kanälen** markiert sind, können nicht am POS angezeigt, hinzugefügt oder entfernt werden. Allerdings werden die Preise und Rabatte, die der Zugehörigkeit zugeordnet werden, noch zu den Produkten zugeordnet.

    ![Zugehörigkeit verbergen](./media/Hide%20affiliations.png "Zugehörigkeit in Kanälen verbergen")
    
- Callcenterbenutzer können die Aktivitäten nun für einen Debitor mithilfe der Treuekarteinformationen einfacher suchen und zu den Treuekarten- und Treuekartenbuchungsseiten des Debitors von der Seite **Kundendienst** aus navigieren.

    ![Kundendienst](./media/Customer%20service.png "Treuekarteninformationen für den Kunden finden")
    
- Wenn eine Treuekarte beeinträchtigt wird, muss eine Ersatzkarte generiert werden und die vorhandenen Punkte in die neue Karte übertragen werden. Der Ersetzungskartenfluss ist in dieser Version vereinfacht worden. Darüber hinaus können Debitoren einen Teil oder alle Treuepunkte Freunden oder Familie schenken. Wenn Punkte übertragen werden, werden Punkte-Regulierungseinträge für jede Treuekarte erstellt. Die Ersetzungskarte und die Saldoübertragungsfunktionen können über die Seite **Treuekarten** aufgerufen werden.

    ![Punkte ersetzen und übertragen](./media/Replace%20and%20transfer%20points.png "Treuekarte ersetze oder Saldo übertragen")
    
- Einzelhändler können die Effizienz eines Kanals erfassen, um bestimmten Debitoren in einem Treueprogramm zu registrieren. Die Registrierungsquelle für die Treuekarten wird nun gespeichert, sodass dieser Einzelhändler Berichte zu diesen Daten ausführen kann. Die Registrierungsquelle wird automatisch für alle ausgegebenen Treuekarten von MPOS/CPOS oder von den E-Commerce-Kanälen aufgezeichnet. Bei den Treuekarten, die von der Backofficebewerbung ausgestellt werden, kann der Callcenterbenutzer entsprechend einen Kanal auswählen.
- In den früheren Versionen konnten Einzelhänder MPOS/CPOS nutzen, um Treuepunkte für Debitoren in einem Shop als Zahlung zu leisten. Allerdings konnte in diesen Programmen der Kassier den Währungswertbetrag nicht anzeigen, der für die aktuelle Buchung angewendet werden kannm weil der Treusaldo in Treupunkten angezeigt wird. Der Kassierer musste die Punkte mit der Währungskonvertierung umrechnen, bevor er die Punkte als Zahlung annehmen konnte. In der aktuellen Version nachdem Positionen der Transaktion hinzugefügt wurden, kann der Kassierer den Betrag sehen, den die Treuepunkte für die aktuelle Transaktion abdecken. Dadurch können gewisse oder alle Treuepunkte einfacher für die Transaktion angewendet werden. Darüber hinaus kann der Kassierer die Punkte anzeigen, die in die nächste 30 Tage ablaufen werden, sodass er den Debitor motivieren kann, die verfallenden Punkte fürr diese Transaktion zu verwenden.

    ![Punkte, die vom Treusaldo abgedeckt werden](./media/Points%20covered%20by%20loyalty%20balance.png "Zeigt Saldo, der von Treupunkten abgedeckt ist")

    ![Verfallende Punkte](./media/Expiring%20points.png "Verfallende Punkte anzeigen")
    
## <a name="upcoming-enhancements"></a>Anstehende Verbesserungen

Die folgenden Funktionen werden in den künftigen monatlichen Aktualisierungen von Dynamics 365 for  Retail verfügbar sein.
    
- Debitoren wollen die Möglichkeit, die Treusaldodetails auf den Verbraucherseiten ansehen zu können. Desgleichen ist es wichtig, dass der Kassierer den Debitorenverlauf der Treupunkte in MPOS/CPOS anzeigen kann, um rasch auf Anfragen von Kunden zu antworten. In einer geplanten monatlischen Aktualisierung können Kunden un d Kassierer die Details des Loyalitätsverlaufs sehen.
- Viele Einzelhändler können Treuepunkte nur auf Basis der Verkaufstransaktionen vornehmen, aber die  die Debitor-orientierteren Einzelhändler möchten ihre Kunden für alle Engagementaktivität mit ihrer Marke vergüten. Beispielsweise möchten sie eine Belohnung für das Ausfüllen einer Onlineumfrage, für den Besuch im Geschäft, für das Liken des Einzelhändlers auf Facebook, für das Tweeten und mehr ausgeben. In der Zukunft werden wir die Möglichkeit hinzufügen, für jede Debitorenaktivität Treuepunkte auszugeben. Um dies zu tun, kann der Einzelhändler einen "anderen Aktivitätstyp" definieren und die Einnahmen für diese Aktivitäten definieren. Wir werden auch eine Retail Server API bereitstellen, die aufgerufen werden kann, wenn eine Aktivität angezeigt wird, die die Einnahmeregel verwendet, um die erforderlichen Treuepunkte zu vergeben).
- Um eine echte OmniKanals Retail Experience zu aktivieren, erlauben wir Debitoren, Treuepunkte über alle Kanäle zu erwerben und einzulösen.
- Kostenloser Versand oder vergünstigter Versand ist einer der erwiesenen Motivationsfaktoren, damit Kunden online kaufen. Um Einzelhändler zu ermöglichen, Versandpromotionen einzurichten, stellen wir eine neue Promotionsart bereit, in der Einzelhändler den Schwellenwerte definieren können, bei dem Debitoren nach Erreichen von vergünstigtem oder kostenlosem Versand profitieren können.

