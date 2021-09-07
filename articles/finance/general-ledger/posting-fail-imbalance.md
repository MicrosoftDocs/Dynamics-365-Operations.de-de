---
title: Fehler bei der Erfassung von Erfassungen aufgrund eines Ungleichgewichts
description: Dieses Thema erklärt, warum Soll- und Habenbeträge in Belegtransaktionen möglicherweise nicht ausgeglichen sind, so dass die Transaktionen nicht gebucht werden können. Das Thema enthält auch Schritte zur Behebung des Problems.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385722"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Fehler bei der Erfassung von Erfassungen aufgrund eines Ungleichgewichts

[!include [banner](../includes/banner.md)]

Dieses Thema erklärt, warum Soll- und Habenbeträge in Belegtransaktionen möglicherweise nicht ausgeglichen sind, so dass die Transaktionen nicht gebucht werden können. Das Thema enthält auch Schritte zur Behebung des Problems.

## <a name="symptom"></a>Symptom

In manchen Fällen kann eine Erfassung nicht gebucht werden, und es wird die folgende Nachricht angezeigt: "Die Transaktionen auf einem bestimmten Beleg sind ab einem bestimmten Datum nicht ausgeglichen (Buchhaltungswährung: 0,01 - Berichtswährung: 0,06)." Warum kann die Erfassung nicht gebucht werden?

## <a name="resolution"></a>Lösung

Beim Buchen im Hauptbuch muss jeder Beleg in der Transaktionswährung, der Buchhaltungswährung und der Berichtswährung ausgeglichen werden, wenn diese Währungen auf der Seite **Einrichtung des Hauptbuchs** definiert sind. (Belege sind ausgeglichen, wenn die Summe der Belastungen gleich der Summe der Gutschriften ist).

Unten auf der Seite mit den Buchungsblattzeilen werden die Summen in der Buchungswährung und der Berichtswährung angezeigt. Sie werden **nicht** in der Transaktionswährung für Fremdwährungstransaktionen angezeigt. Außerdem zeigt die Fehlermeldung, die Benutzer während der Simulation oder Buchung erhalten, die Differenzen nur in der Buchhaltungswährung und der Berichtswährung an. Sie werden nicht in der Transaktionswährung angezeigt, da ein einzelner Beleg mehr als eine Transaktionswährung haben kann und das Journal Belege in verschiedenen Transaktionswährungen enthalten kann. Daher ist es wichtig, dass Sie überprüfen, ob die Beträge in Transaktionswährung für jeden Beleg ausgeglichen sind.

### <a name="transaction-currency"></a>Buchungswährung

Während der Simulation und Buchung prüft das System, dass jeder Beleg in der Transaktionswährung ausgeglichen ist. Für jeden eingegebenen Beleg kann es eine oder mehrere Währungen als Transaktionswährung geben. Ein Beleg, der im Allgemeinen Erfassungen eingegeben wird, kann z.B. zwei Transaktionswährungen haben, wenn Bargeld von einem Bankkonto, das Euro (EUR) verwendet, auf ein Bankkonto, das kanadische Dollar (CAD) verwendet, übertragen wird.

Wenn ein Beleg nur eine Transaktionswährung hat, muss die Summe der Belastungen der Summe der Gutschriften für diesen Beleg entsprechen. Kunden sind auf die folgenden Szenarien gestoßen, in denen die Buchung korrekt fehlgeschlagen ist, weil die Beträge der Transaktionswährungen nicht ausgeglichen waren:

- Die Gesamtbelastungen und Gesamtgutschriften waren **nicht** in der Transaktionswährung ausgeglichen, aber sie waren für die Buchhaltungswährung und die Berichtswährung ausgeglichen. Ein Debitor nahm an, dass der Beleg trotzdem gebucht werden würde. Diese Annahme war jedoch falsch. **Die Beträge in Transaktionswährung auf einem Beleg müssen immer ausgeglichen sein, wenn alle Zeilen des Belegs die gleiche Währung haben.**
- Der Beleg wurde über Microsoft Excel importiert, und der Benutzer dachte, dass die Beträge der Transaktionswährung ausgeglichen seien. In der Excel-Arbeitsmappe wurden die Beträge, die importiert wurden, als **Numerische** Werte festgelegt, nicht als **Währung** Werte. In diesem Szenario hatten die numerischen Beträge in der Arbeitsmappe mehr als zwei Dezimalstellen, und beim Importieren der Beträge wurden mehr als zwei Dezimalstellen einbezogen. Daher stimmten die Belastungen nicht mit den Gutschriften überein, da sie um den Bruchteil eines Pennys abwichen. Die Erfassung spiegelte diese Differenz in den Zeilen des Belegs nicht wider, da die angezeigten Beträge nur zwei Dezimalstellen haben.
- Der Beleg wurde über Excel importiert, und der Benutzer war der Meinung, dass die Beträge der Transaktionswährungen ausgeglichen waren. Obwohl der Beleg ausgeglichen war, hatten einige Zeilen des Belegs unterschiedliche Transaktionsdaten. Wenn Sie die Gesamtsoll- und Gesamthabenbeträge pro Beleg und Transaktionsdatum addierten, waren sie nicht ausgeglichen. Das System verhindert nun dieses Szenario. Ein Beleg kann nur ein Transaktionsdatum haben. Diese Anforderung wird erzwungen, wenn Sie einen Beleg über das Allgemeine Buch.-Blatt im System erfassen. Ursprünglich wurde sie jedoch nicht erzwungen, wenn ein Beleg über Excel importiert wurde.

In einem unterstützten Szenario kann ein Beleg mehr als eine Transaktionswährung haben. In diesem Fall prüft das System **nicht**, ob die Belastungen gleich den Gutschriften in der Transaktionswährung sind, da die Währungen nicht übereinstimmen. Stattdessen prüft das System, dass die Beträge in der Buchungswährung ausgeglichen sind.

### <a name="accounting-currency"></a>Buchhaltungswährung

Wenn alle Zeilen eines Belegs die gleiche Transaktionswährung haben und die Beträge in der Transaktionswährung ausgeglichen sind, prüft das System, dass die Beträge in der Buchhaltungswährung ausgeglichen sind. Wenn der Beleg in einer Fremdwährung eingegeben wurde, wird der Wechselkurs in den Belegzeilen verwendet, um die Beträge in Transaktionswährung in die Buchhaltungswährung umzurechnen. Zuerst wird jede Zeile des Belegs umgerechnet. Dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamtsollbeträge zu ermitteln. Da jede Zeile umgerechnet wird, kann es sein, dass die Gesamtsoll- und Gesamtsollbeträge nicht ausgeglichen sind. Wenn die Differenz jedoch innerhalb des Wertes **Maximale Pfennigdifferenz** liegt, der auf der Seite **Hauptbuch-Parameter** definiert ist, wird der Beleg gebucht und die Differenz wird automatisch auf das Pfennigdifferenz-Konto gebucht.

Wenn der Beleg mehr als eine Transaktionswährung hat, wird jede Zeile des Belegs in die Buchhaltungswährung umgerechnet und dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamthabenbeträge zu ermitteln. Um als ausgeglichen zu gelten, müssen die Soll- und Habenbeträge ausgeglichen sein und es darf keine Rundungsdifferenz im Centbereich bestehen.

### <a name="reporting-currency"></a>Berichtswährung

Wenn alle Zeilen eines Beleges die gleiche Transaktionswährung haben und die Beträge in der Transaktionswährung ausgeglichen sind, prüft das System, ob die Beträge in der Berichtswährung ausgeglichen sind. Wenn der Beleg in einer Fremdwährung eingegeben wurde, wird der Exchange-Satz in den Belegzeilen verwendet, um die Beträge in Transaktionswährung in die Berichtswährung umzurechnen. Zuerst wird jede Zeile des Belegs umgerechnet. Dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamtsollbeträge zu ermitteln. Da jede Zeile umgerechnet wird, kann es sein, dass die Gesamtsoll- und Gesamtsollbeträge nicht ausgeglichen sind. Wenn die Differenz jedoch innerhalb des Wertes **Maximale Pfennigrundung in der Berichtswährung** liegt, der auf der Seite **Hauptbuch-Parameter** definiert ist, wird der Beleg gebucht und die Differenz wird automatisch auf das Pfennig-Differenzkonto gebucht.

Wenn der Beleg mehr als eine Transaktionswährung hat, wird jede Zeile des Beleges in die Berichtswährung umgerechnet und dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamtsollbeträge zu ermitteln. Um als ausgeglichen zu gelten, müssen die Soll- und Habenbeträge ausgeglichen sein und es darf keine Rundungsdifferenz im Centbereich bestehen.
