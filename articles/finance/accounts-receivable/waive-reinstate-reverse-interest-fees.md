---
title: Aufheben, Wiedererheben oder Stornieren von Zinsgebühren
description: In diesem Artikel wird beschrieben, wie Belastungen für Zinsen und Gebühren erlassen, erfasst und umgekehrt werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b5c92d6f3bb0bdc3fbadc9708350b5107e6cf37
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443592"
---
# <a name="waive-reinstate-or-reverse-interest-fees"></a>Aufheben, Wiedererheben oder Stornieren von Zinsgebühren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Belastungen für Zinsen und Gebühren erlassen, erfasst und umgekehrt werden.

Sie können durch Klicken auf die Schaltflächen der Registerkarte **Mahnen** auf der Listenseite **Alle Debitoren** Gebühren aufheben, stornieren oder wiedererheben:

-   Aufgehobene Gebühren werden erlassen. Sie können z. B. eine Gebühr aufheben, wenn ein Debitor Widerspruch gegen die Gebühr einlegt und Sie eine gute Geschäftsbeziehung mit dem Debitor aufrecht erhalten möchten.
-   Wieder erhobene Gebühren werden wieder fällig. Sie können Gebühren wieder erheben, die zuvor aufgehoben wurden. Möglicherweise müssen Sie Gebühren wiedererheben, wenn Sie feststellen, dass sie nicht hätten aufgehoben werden sollen.
-   Stornierte Gebühren werden aus dem Konto eines Debitors entfernt und sind nicht mehr fällig. Gebühren können storniert werden, wenn zum Beispiel der falsche Zinssatz ausgewählt wurde, um den Betrag zu berechnen, den ein Debitor schuldig ist. Sie können die Zinsen in einem separaten Prozess neu berechnen und eine Zinsrechnung mit neuen Gebühren für den Debitor erstellen.

Mit all diesen Aktivitäten werden Zinsrechnungen geändert. Dabei handelt es sich um das Geschäftsdokument, das Debitoren davon in Kenntnis setzt, wann das Konto mit den Zinsen bzw. Gebühren belastet wurde. Wenn Zinsen oder Gebühren aufgehoben oder storniert werden, wird automatisch eine Gutschrift oder Anpassungsrechnung erstellt, um die Gebühren zu begleichen. Wenn aufgehobene Gebühren erneut erhoben werden, wird automatisch eine Rechnung mit einem Sollbetrag erstellt, um die Gebühren, die von einem Debitor zu begleichen sind, erneut zu erheben. Die folgende Tabelle beschreibt die Ergebnisse jeder Aktion.

| Aktion                                                                                                                                                                                                            | Ergebnis für den Debitor                                                                                             | Verarbeiten                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufheben der vollständigen Zinsrechnungen mit sämtlichen Zinsen und Gebühren, die sie beinhalten. – Oder – Auswählen und Aufheben von Gebühren oder Zinsbuchungen, die Teil von Zinsrechnungen sind.                                        | Die Gebühren werden erlassen.                                                                                           | Eine Gutschrift oder eine Anpassungsrechnung wird für den Debitor erstellt. Eine Gutschrift wird verwendet, damit die Zinsrechnung oder die ausgewählten Zinsbuchungen oder Gebühren automatisch beglichen werden. Der beglichene Betrag entspricht der Summe der Gebühren abzüglich aller vorherigen Zahlungen seitens des Debitors und abzüglich aller Beträge, die zuvor erlassen oder abgeschrieben wurden. Wenn die Summe der Gutschrift den vom Debitor geschuldeten Betrag überschreitet, kann die Gutschrift in eine Kreditorenrechnung konvertiert werden. An den Debitor kann dann eine Rückerstattung geleistet werden.                                                       |
| Erneute Aktivierung vollständiger Zinsrechnungen einschließlich aller enthaltenen Zinsen und Gebühren. – Oder – Auswählen und erneutes Erheben von Gebühren oder Zinsbuchungen, die Teil von Zinsrechnungen sind.                                | Der aufgehobene Betrag ist wieder fällig.                                                                                     | Eine Rechnung mit einem Sollbetrag wird erstellt, und der Betrag wird automatisch anhand der zuvor aufgehobenen Gebühren ausgeglichen. Die tatsächlichen Zinsrechnungen werden nicht erneut aktiviert. Stattdessen wird eine Rechnung erstellt, die zeigt, dass der Betrag vom Debitor zu begleichen ist. Die Gutschriften oder Anpassungsrechnungen, die erstellt wurden, um aufgehobene Zinsrechnungen zu begleichen, können weiterhin vorhanden sein, wenn damit keine Zinsrechnungen beglichen wurden. Wenn dies der Fall ist, werden die ausstehenden Gutschriften storniert. Ausstehende Gutschriften werden normalerweise automatisch beglichen, wenn Zinsrechnungen aufgehoben werden. Allerdings kann eine ausstehende Gutschrift vorhanden sein, wenn ein Debitor eine Zinsrechnung bezahlt hat, auch wenn der Debitor gegen die Gebühren Einspruch eingelegt hat. |
| Stornieren vollständiger Zinsrechnungen. – Oder – Stornieren von ausgewählten Zinsbuchungen, die Teil von Zinsrechnungen sind. **Hinweis:** Sie können eine Gebühr nicht stornieren. Sie können jedoch eine ganze Zinsrechnung stornieren, die eine Gebühr umfasst. | Die Gebühren sind seitens des Debitors nicht mehr fällig. Allerdings werden die Gebühren wieder fällig, wenn die Zinsen neu berechnet werden. | Der Prozess ist identisch mit der Aufhebung von Zinsrechnungen oder von ausgewählten Zinsbuchungen. Eine Gutschrift oder eine Anpassungsrechnung wird für den Debitor erstellt. Diese Gutschrift wird zum automatischen Ausgleich der Zinsrechnung verwendet. Sie können Zinsen in einem separaten Prozess neu berechnen und eine neue Zinsrechnung erstellen.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Sie können auch einen separaten Prozess verwenden, um uneinbringliche Außenstände abzuschreiben. Durch diesen Prozess werden alle Debitorenbuchungen für den Ausgleich markiert, anstatt nur die Gebühren als Teil von Zinsrechnungen aufzuheben.

## <a name="adjust-interest-for-invoices"></a>Zinsanpassung für Rechnungen
Neben der Anpassung von Zinsrechnungen können mit einem der folgenden Prozesse auch Zinskosten in Rechnungen entfernt werden. In beiden Prozessen können auch Anpassungen an den zugehörigen Zinsrechnungen vorgenommen werden.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Korrigieren einer Rechnung mit zugehörigen Zinsen

Sie können eine gebuchte Rechnung korrigieren, die in einer Zinsrechnung enthalten ist. In diesem Prozess werden die Details aus der vorhandenen Rechnung in eine neue Rechnung kopiert, um nur die gewünschten Korrekturen vorzunehmen. Die Rechnung wird storniert, und eine neue Rechnung wird erstellt. Zinsen für die Buchung werden in der Zinsrechnung ebenfalls storniert, wenn die Zinsrechnung gebucht wurde. 

Sie können die Korrektur vornehmen, indem Sie die Schaltfläche **Rechnung berichtigen** im Aktivitätsbereich der Freitextrechnung verwenden. Diese Schaltfläche ist nur verfügbar, wenn der **Berichtigung für Freitextrechnung**-Konfigurationsschlüssel ausgewählt wurde.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Stornieren einer Debitorenbuchung mit zugehörigen Zinsen

Sie können eine Debitorenbuchung für eine Rechnung stornieren, wenn eine Rechnung falsch erstellt wurde. Wenn die stornierte Debitorenbuchung für eine Zinsrechnung Zinsen enthält und die Zinsrechnung gebucht wurde, werden Zinsen für die Buchung für die Zinsrechnung ebenfalls storniert. Die Zinsrechnung wird storniert, sofern sie nicht gebucht wurde. 

Sie können Debitorenbuchungen stornieren, indem Sie die Schaltfläche **Stornieren** auf der Seite **Debitorenbuchungen** verwenden.

## <a name="waive-or-reinstate-interest-notes"></a>Aufheben oder erneutes Erheben von Zinsrechnungen
Sie können alle Gebühren für die ausgewählten Zinsrechnungen aufheben oder erneut erheben. Wenn Sie Gebühren aufheben, darf der aufzuhebende Gesamtbetrag keine festgelegten maximalen Beträge überschreiten. Eine Zinsrechnung kann nur erneut aktiviert werden, wenn sie zuvor deaktiviert wurde. 

Sie können Zinsrechnungen aufheben oder wieder erheben, indem Sie die Schaltfläche **Zinsrechnung** auf der Registerkarte **Mahnen** der Seite **Debitor** verwenden.

## <a name="waive-or-reinstate-interest-transactions"></a>Aufheben oder erneutes Erheben von Zinsbuchungen
Sie können bestimmte Zinsbuchungen für eine Zinsrechnung aufheben oder wieder erheben, anstatt alle Gebühren für eine Zinsrechnung anzupassen. Wenn Sie Gebühren aufheben, darf der aufzuhebende Gesamtbetrag keine festgelegten maximalen Beträge überschreiten. Eine Zinsbuchung kann nur wieder erhoben werden, wenn sie zuvor aufgehoben (bzw. deaktiviert) wurde. 

Sie können Zinsrechnungen aufheben oder wieder erheben, indem Sie die Schaltfläche **Buchungszinsen** auf der Registerkarte **Mahnen** der Seite **Debitor** verwenden.

## <a name="waive-or-reinstate-fees"></a>Aufhebung oder Wiedererhebung von Gebühren
Sie können bestimmte Gebühren für eine Zinsrechnung aufheben oder wieder erheben, anstatt alle Gebühren für diese Zinsrechnung anzupassen. Wenn Sie Gebühren aufheben, darf der aufzuhebende Gesamtbetrag keine festgelegten maximalen Beträge überschreiten. Eine Gebühr kann nur wieder erhoben werden, wenn sie zuvor aufgehoben wurde. 

Sie können Zinsrechnungen aufheben oder wieder erheben, indem Sie die Schaltfläche **Gebühr** auf der Registerkarte **Mahnen** der Seite **Debitor** verwenden.

## <a name="reverse-interest-notes"></a>Zinsrechnungen stornieren
Sie können alle Gebühren für die ausgewählten Zinsrechnungen stornieren. Stornierte Gebühren werden aus dem Konto eines Debitors entfernt und sind nicht mehr fällig. Nach dem Stornieren der Zinsrechnung können Sie die Zinsen neu berechnen und eine neue Zinsrechnung erstellen. 

Sie können Zinsrechnungen stornieren, indem Sie die Schaltfläche **Zinsrechnung** auf der Registerkarte **Mahnen** der Seite **Debitor** verwenden.

## <a name="reverse-interest-transactions"></a>Stornieren von Zinsbuchungen
Sie können alle ausgewählten Zinsbuchungen stornieren. Stornierte Gebühren werden aus dem Konto eines Debitors entfernt und sind nicht mehr fällig. Nach dem Stornieren der Buchungen können Sie die Zinsen neu berechnen und eine neue Zinsrechnung erstellen.

Sie können Zinsbuchungen stornieren, indem Sie die Schaltfläche **Buchungszinsen** auf der Registerkarte **Mahnen** der Seite **Debitor** verwenden.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Anzeigen des Verlaufs der Anpassungen für Gebühren, die aufgehoben, wieder erhoben oder storniert wurden
Sie können den detaillierten Verlauf der Anpassungen anzeigen, die für Zinsrechnungen vorgenommen wurden, zum Beispiel den Benutzer, von dem die Anpassung eingegeben wurde, den Typ der Anpassung, den Betrag und den Zeitpunkt, zu dem die Anpassung eingegeben wurde. Zum Beispiel möchten Sie vor dem Erstellen einer neuen Zinsrechnung die vorherigen Anpassungen anzeigen, die für eine Zinsrechnung eingegeben wurden. 

Sie können Zinsbuchungen stornieren, indem Sie die Schaltfläche **Verlauf** auf der Registerkarte **Mahnen** der Seite **Debitor** verwenden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]