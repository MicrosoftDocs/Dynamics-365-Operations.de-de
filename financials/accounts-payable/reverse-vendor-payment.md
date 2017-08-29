---
title: Kreditorenzahlung stornieren
description: "In diesem Artikel beschriebt die Unterschiede zwischen dem Rückbuchen, Löschen, Stornieren und Ablehnen einer Zahlung. Desweiteren werden die zwei Methoden zur Rückbuchung eines Kreditorenschecks erläutert."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4f8b77efabe0c002654dac0b80d721a79dc42003
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="reverse-a-vendor-payment"></a>Kreditorenzahlung stornieren

[!include[banner](../includes/banner.md)]


In diesem Artikel beschriebt die Unterschiede zwischen dem Rückbuchen, Löschen, Stornieren und Ablehnen einer Zahlung. Desweiteren werden die zwei Methoden zur Rückbuchung eines Kreditorenschecks erläutert. 

Gelegentlich kann es erforderlich sein, eine Zahlung zurückzubuchen, nachdem eine Kreditorenzahlung gebucht wurde. Die Rückbuchung unterscheidet sich vom Löschen, vom Stornieren oder der Ablehnung einer Zahlung. Sie können eine Zahlung nur löschen, wenn der Status **Erstellt** ist. Dieser Status besagt, dass die Zahlung erstellt wurde, jedoch noch nicht berücksichtigt wurde generiert. Diese Einschränkung gilt immer, unabhängig von der Zahlungsmethode verwendet. Sie können noch nicht gebuchte Schecks für storniert erklärt, nachdem die Periode erzeugt wurden, jedoch bevor sie gebucht wurden. Wenn die Zahlung generiert wurde als elektronischen Zahlungsverkehr (EFT) erfolgt, können Sie die Zahlung abgelehnt, bevor sie gebucht wurde. Wenn Sie eine Zahlung ablehnen, ändern Sie den **Zahlungsstatus** Wert. Eine Zahlung, die storniert gekennzeichnet oder abgelehnt wurde, kann erneut generiert werden, wenn der **Zahlungsstatus** Wert zurück zu **Keiner** geändert wurde. 

Nachdem eine Zahlung gebucht wurde, werden Rückbuchungen verwendet. Zahlungen, die elektronisch vorgenommen werden, können nicht storniert werden, nachdem sie gebucht wurden. Stattdessen muss eine neue Transaktion für den Betrag der Zahlung erstellt werden, um die Verbindlichkeiten auf das Bankkonto des Kreditors zurückzubuchen. Es gibt zwei Methoden zur Rückbuchung von gebuchten Schecks. In einer Methode werden Rückbuchungen umgehend gebucht, wenn Sie auf **Zahlungsrückbuchung** auf der Seite **Scheck** klicken. Bei der anderen Methode wird die Rückbuchung nach dem Klicken auf die Schaltfläche **Zahlungsrückbuchung** im Feld **Scheck** zunächst an die Scheckrückbuchungserfassung in der Bargeld- und Bankverwaltung gesendet, in der sie dann von einem Prüfer entweder gebucht oder abgelehnt werden kann. 

Um ermitteln, welche Methode Ihre Organisation verwendet, sehen Sie sich die Seite **Bargeld- und Bankverwaltungsparameter** an. Wenn die **Überprüfungsprozess für Zahlungsrückbuchungen verwenden** Option auf **Ja** festgelegt ist, werden Rückbuchungen an die Scheckrückbuchungserfassung zur Prüfung gesendet. In der folgenden Tabelle wird beschrieben, wie sich die Scheckumrückbuchungsverfahren unterscheiden.

| Wenn Ihre Organisation Scheckrückbuchungen nicht prüft, bevor sie gebucht werden                                                                                                                                  | Wenn Ihre Organisation Scheckrückbuchungen prüft, bevor sie gebucht werden                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Scheck wird sofort storniert, wenn Sie auf **OK** auf der Seite **Scheck** klicken.                                                                                                                      | Der Scheck wird nicht sofort zurückgebucht. Eine Erfassung für Scheckrückbuchungen wird zur Prüfung erstellt. Wenn die die Erfassung für Scheckrückbuchungen gelöscht wird, kann der Scheck erneut storniert werden.                                                                                                                                                                                                                                                                |
| Die Buchhaltungseinträge für den Scheck werden storniert.                                                                                                                                         | Das Sachkonto aus dem Buchhaltungseintrag des ursprünglichen Schecks wurde möglicher Weise nicht gebucht. Die Finanzdimensionen aus der Erfassung des ursprünglichen Schecks wurden als Standardfinanzdimensionen in der Scheckrückbuchungserfassung verwendet. Diese Standardwert können geändert werden. Wenn die Scheckrückbuchungserfassung gebucht wird, werden die Hauptkonten der Kreditoren automatisch aus den Buchungsprofilen eingegeben, die möglicherweise geändert wurden. |
| Die Buchhaltungsstrukturen, die verwendet wurden, als der ursprüngliche Scheck gebucht wurde, werden verwendet, um den Scheck zu stornieren, auch wenn die Kontostruktur geändert wurde. Die Sachkontokombination ist nicht validiert. | Wenn eine Kontostruktur sich geändert hat, nachdem der Scheck gebucht wurde, kann eine neue Finanzdimension möglicherweise für die Rückbuchung des Schecks erforderlich sein. Diese Finanzdimension wird möglicherweise nicht automatisch aus der ursprünglichen Zahlungserfassung eingegeben. Die Kontokombination wird geprüft, wenn die Schecrückbuchung gebucht wird.                                                                                                        |
| Feste Dimensionen werden nicht auf Rückbuchungen angewendet, um sicherzustellen, dass die gleichen Sachkonten rückgebucht werden.                                                                                      | Feste Dimensionen werden auf die Erfassung für Scheckrückbuchungen während der Buchung angewendet. Der Finanzdimensionswert ist möglicherweise nicht im Buchhaltungseintrag für den Origionalscheck enthalten, je nachdem, wann die feste Dimension definiert wurde.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Gebuchte Schecks rückbuchen, ohne sie zu prüfen
Wenn Ihre Organisation Scheckrückbuchungen sofort buchen möchte, wenn Sie auf **Zahlungsrückbuchung** auf der Seite **Schecks** klicken. Legen Sie auf der Seite **Bargeld- und Bankverwaltungsparameter** die Option **Überprüfungsprozess für Zahlungsrückbuchungen verwenden** auf **Nein** fest. Auf der Seite **Schecks** können Sie den Scheck zur Rückbuchung auswählen und **Zahlungsrückbuchung**wählen. Geben Sie dann das Datum ein, und wählen Sie einen Grund für die Rückbuchung aus.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Gebuchte Schecks nach Überprüfung in der Scheckrückbuchungserfassung rückbuchen
Wenn Ihre Organisation Scheckrückbuchungen prüfen möchte, bevor sie gebucht werden, erstellen Sie eine Scheckrückbuchungserfassung zur Prüfung und legen Sie auf der Seite **Bargeld- und Bankverwaltungsparameter** die Option **Überprüfungsprozess für Zahlungsrückbuchungen verwenden** auf **Ja** fest. Auf der Seite **Schecks** können Sie den Scheck zur Rückbuchung auswählen und **Zahlungsrückbuchung**wählen. Geben Sie dann das Datum ein, und wählen Sie einen Grund für die Rückbuchung aus. Sie müssen auch einen Erfassungsnamen auswählen, um eine Erfassung in der Scheckrückbuchungserfassung zu erstellen.

### <a name="review-a-reversal"></a>Überprüfen einer Rückbuchung

Als Benutzer, der mit der Überprüfung von Rückbuchungen betraut ist, können Sie entweder die Erfassung genehmigen und buchen, oder die Rückbuchung ablehnen, indem Sie die Erfassung löschen. Auf der Seite **Scheckrückbuchungserfassung** Seite können Sie die Rückbuchungserfassung auswählen, um sie zu prüfen und klicken dann auf **Positionen**. Sie können die Rückbuchung überprüfen und anschließend eine der folgenden Genehmigungsoptionen auswählen:

-   Um eine Rückbuchungserfassung zu genehmigen und zu buchen, klicken Sie auf **Buchen** oder auf **Buchen und übertragen**.
-   Zum Ablehnen einer Rückbuchung löschen Sie die Scheckrückbuchungserfassung.

> [!NOTE]
> Durch das Löschen der Erfassung wird lediglich die Rückbuchung aus dem System entfernt; der ursprüngliche Scheck verbleibt jedoch auf der Seite **Scheck**. Der Status des Schecks lautet dann nicht mehr **Storno ausstehend**.

## <a name="results-of-posting-a-reversal"></a>Ergebnis einer ausgeführten Rückbuchung
Beim Buchen einer Scheckrückbuchung geschieht Folgendes:

-   Der Status des Schecks wird zu **Stornierung** aktualisiert.
-   Wenn die **Abstimmen** Option auf der Rückbuchungsseite bei der Rückbuchung aktiviert ist, wird der Scheck abgestimmt (die Option **Abgestimmt** ist aktiviert) und wird nicht auf der Seite **Kontoabstimmung** angezeigt.
-   Für den Rückbuchungsbeleg erfolgt eine entsprechende Buchung auf dem Bankkonto, für das der Scheck ausgestellt war, wodurch sich der Saldo des Bankkontos erhöht.
-   Der Beleg wird im Hauptbuch gebucht.
-   Die Änderungsdetails werden in der Feldgruppe **Historie** auf der Seite **Scheck** aktualisiert.

> [!NOTE] 
> Beim Stornieren eines Schecks für eine Intercompany-Handelsbuchung stammen die Gegenbuchungen nicht aus der ursprünglichen Buchung, sondern aus den Verrechnungseinstellungen für Intercompanyhandel. Wurde der rückgebuchte Scheck für eine Kreditorenzahlung ausgestellt, gilt außerdem Folgendes:

-   Die Zuordnung der ursprüngliche Zahlung aus der Rechnung, mit der die Zahlung ausgeglichen wurde, wird rückgängig gemacht (der Ausgleich wird storniert).
-   Für das Kreditorenkonto der Zahlungsstornierung erfolgt eine entsprechende Buchung, und die stornierte Zahlung wird mit der ursprünglichen Zahlung ausgeglichen. Das Feld **Letzter Ausgleichsbeleg** auf der Seite **Kreditorenbuchungen** für die ursprüngliche Kreditorenzahlung wird mit der Belegnummer der stornierten Buchung aktualisiert.

Wurde der rückgeholte Scheck für eine Debitorenrückerstattung ausgestellt, gilt außerdem Folgendes:

-   Für das Debitorenkonto der Zahlungsstornierung erfolgt eine entsprechende Buchung, und der Ausgleich zwischen der ursprünglichen Zahlung und dem Dokument, mit dem die Zahlung ursprünglich ausgeglichen wurde, wird rückgängig gemacht (eine negative Zahlung wird erstellt).
-   Auf die ursprüngliche Zahlung wird eine Zahlungsstornierung angewendet. Das Feld **Letzter Ausgleichsbeleg** auf der Seite **Debitorenbuchungen** für die ursprüngliche Debitorenzahlung wird mit der Belegnummer der stornierten Buchung aktualisiert.





