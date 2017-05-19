---
title: "Zahlung bei Zahlungsempfang-Lieferantenverträge"
description: "Dieser Artikel erklärt die Pay-When-Paid (PWP) Bestimmungen für Händlervereinbarungen. PWP-Bestimmungen erlauben es, Zahlungen teilweise oder vollständig zurückzustellen, bis Sie vom Kreditor im Projekt bezahlt wurden. Dieser Artikel setzt auch ein aus dem wirklichem Leben Beispiel fest, um anzuzeigen, wie Sie PWP-Begriffe für ein Projekt verwenden können."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23131
ms.assetid: 20bf1d7f-8813-4c69-9cd7-576884a7e169
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ff4e31434da0fa200cc1c563fb53c8650a643443
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="pay-when-paid-vendor-agreements"></a>Zahlung bei Zahlungsempfang-Lieferantenverträge

[!include[banner](../includes/banner.md)]


Dieser Artikel erklärt die Pay-When-Paid (PWP) Bestimmungen für Händlervereinbarungen. PWP-Bestimmungen erlauben es, Zahlungen teilweise oder vollständig zurückzustellen, bis Sie vom Kreditor im Projekt bezahlt wurden. Dieser Artikel setzt auch ein aus dem wirklichem Leben Beispiel fest, um anzuzeigen, wie Sie PWP-Begriffe für ein Projekt verwenden können.

Wenn Sie einen Kreditor als Zulieferer für ein Projekt genehmigen, möchten Sie möglicherweise die Zahlung an den Kreditor oder Zulieferer aussetzen, bis Sie von Ihrem Debitor für das Projekt bezahlt wurden. Um eine Zahlung für einen Kreditor einzubehalten, richten Sie Pay-When-Paid (PWP)-Bedingungen ein, wenn Sie die Bestellung mit dem Kreditor vereinbaren. Wenn Sie eine Bestellung für den Kreditor erstellen und der Bestellung eine Projektkennung zuweisen, werden PWP-Begriffe im Projekt der Bestellung und dem Kreditor zugeordnet. Im Formular **Kreditorenrechnungen mit Zahlung bei Zahlungsempfang** können Sie eine Liste der unbezahlten Kreditorenrechnungen für die Bestellung und die zugehörigen Debitorenrechnungen anzeigen. Verwenden Sie dieses Formular, um zu bestimmen, wie viel Sie einem Kreditor bezahlen möchten. Wenn ein Kunde einen Betrag einer Projektrechnung bezahlt, können Sie einen Teil oder alle zugehörigen Kreditorenrechnungen zur Zahlung freigeben. Sie können PWP-Bedingungen einrichten, um Zahlung durch einen Kreditor festzulegen, nachdem Sie einen bestimmten Prozentsatz der zugehörigen Zahlung von einem Debitor erhalten haben. Wenn Sie Teilzahlungen von einem Debitor erhalten, können Sie einige der zugehörigen Kreditorenrechnungen manuell zur Zahlung freigeben. Das folgende Beispiel veranschaulicht, wie Sie PWP-Begriffe verwenden können, um Zahlungen an einen Kreditor oder Zulieferer einzubehalten, bis Sie vom Debitor bezahlt werden. Ihre Organisation vereinbart mit einem Debitor, 100 Computer bereitzustellen, auf denen Sie eine von diesem gewünschte Software installieren. Der Preis, den Sie und der Debitor vereinbaren, beträgt 150,00 pro Computer. Sie einigen sich mit einem Drittanbieter, der Ihnen die Computer bereitstellen soll. Der Debitor möchte die Qualität der Computer sicherstellen, bevor er an Ihre Organisation zahlt. Die Richtlinie der Organisation besagt, Zahlung an eine dritte Partei zurückzuhalten, bis Sie vom Debitor für ein Projekt bezahlt wurden. Daher richten Sie das Projekt mit einem PWP-Prozentsatz von 100 Prozent ein, damit Sie alle Zahlungen an den Kreditor zurückhalten, bis Sie die vollständige Zahlung für die Debitorenrechnung empfangen. Der Kreditor stellt Ihnen für jeden Computer 100,00 in Rechnung. Wenn der Kreditor Ihnen die Computer sendet, enthält die Lieferung eine Rechnung über 10.000,00 für 100 Computer. Da Sie das Projekt mit PWP-Bedingungen eingerichtet haben, bezahlen Sie den Kreditor jedoch noch nicht. Nachdem Sie die Computer vom Kreditor empfangen haben, installieren Sie zunächst die bestellte Software auf den Computern. Wenn Sie die Computer an den Debitor senden, schicken Sie ihm dazu eine Rechnung in Höhe von 15.000,00. Der Debitor überprüft die Computer und zeigt sich mit der Qualität des Produkts zufrieden. Der Debitor zahlt dann Ihrer Organisation den Gesamtbetrag der Projektrechnung. Nachdem Sie die vollständige Zahlung vom Debitor empfangen haben, bezahlen Sie dem Kreditor 10.000,00, den Gesamtbetrag der Kreditorenrechnung.




