---
title: Zahlungsmethoden
description: Jeder Zahlungstyp, der von einem Einzelhändler akzeptiert wird, muss beim Einrichten des Systems konfiguriert werden. In diesem Artikel wird beschrieben, wie Sie die Zahlungstypen einrichten können und beschreibt den Prozess, um sie einzurichten.
author: rubencdelgado
manager: AnnBe
ms.date: 06/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2b56609de3b2620dcc605c6c6d697cb74c8ed6c1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412576"
---
# <a name="payment-methods"></a>Zahlungsmethoden

[!include [banner](includes/banner.md)]

Jeder Zahlungstyp, der von einem Einzelhändler akzeptiert wird, muss beim Einrichten des Systems konfiguriert werden. In diesem Artikel wird beschrieben, wie Sie die Zahlungstypen einrichten können und beschreibt den Prozess, um sie einzurichten.

Einzelhändler können für die von ihnen verkauften Produkte und angebotenen Dienstleistungen verschiedene Zahlungsformen akzeptieren. Obwohl die Barzahlung am häufigsten ist, können Einzelhändler Zahlungen auch in Form von Schecks, Kredikarten, Gutscheinen usw. entgegennehmen. Jeder vom Einzelhändler akzeptierte Zahlungstyp muss beim Einrichten des Systems in Dynamics 365 Commerce konfiguriert werden. In der folgenden Liste wird jeder Zahlungstyp beschrieben, der eingerichtet werden kann:

- **Bargeld** – Geld in der physischen Form der Währung, z. B. Banknoten und Münzen. Die Währung kann entweder die Unternehmenswährung oder die im Shop gültige lokale Währung sein.
- **Scheck** – Ein übertragbares Wertpapier, das eine Zahlungsanweisung an die angegebene Bank enthält, einen bestimmten Betrag in einer bestimmten Währung zu zahlen. Ein Scheck ist im Allgemeinen entweder für eine unbegrenzte Dauer oder sechs Monate nach dem Ausstellungsdatum gültig, sofern kein anderer Gültigkeitszeitraum angegeben ist. Dieser Zeitraum variiert und hängt von der Bank ab, bei der der Scheck gezogen wird. Es gibt verschiedene Arten von Schecks, z. B. Orderschecks, Blankoschecks, Inhaberschecks und Schecks für Einzahlungen auf das Konto des Begünstigten. Schecks können für jeden Shop als Zahlungsmethode eingerichtet werden. Schecks können in der Währung akzeptiert werden, die entweder auf Unternehmensebene oder Shopebene definiert ist. Damit Schecks in einem Shop als Zahlungsmittel akzeptiert werden können, müssen Schecks als Zahlungsmethode eingerichtet werden.
- **Währung** – Das primäre Zahlungsmittel, bei dem es sich nicht um die Standardwährung des Unternehmens handelt. Münzen und Papiergeld sind jeweils Formen von Währung. Die Währungszahlungsmethode stellt alle verwendeten Währungen dar. Bevor diese Zahlungsmethode verwendet werden kann, müssen Währungen eingerichtet und einzelhandelsbezogene Wechselkursinformationen für die Währungen angegeben werden.
- **Karte** – Alle verwendeten Karten wie Debit- und Kreditkarten. Es ist eine gute Idee, auf Organisationsebene eine Kartenzahlungsmethode einzurichten, die jede Art von Karte darstellt. Auf Shopebene kann dann für jede Karte oder jeden Kartensatz, der mit den gleichen Einstellungen verarbeitet werden soll, eine Zahlungsmethode eingerichtet werden. Die auf dem Markt erhältlichen Herstellerkarten, z. B. Debitkarten und Kreditkarten, müssen eingerichtet werden, bevor die Karten in einem Shop als Zahlungsmittel akzeptiert werden können.
- **Gutschrift** – Gutschriften, die am POS ausgestellt und eingelöst werden. Die Gutschrift kann ein Guthaben oder eine Retourengutschrift sein, die bei einer Retoure ausgestellt wird. Wenn Gutschriften nur teilweise eingelöst werden, wird vom Programm eine neue Gutschrift für den neuen Saldobetrag ausgestellt. Die neue Gutschrift hat eine neue Nummer. Eine Gutschrift kann nur einmal verwendet werden, und alle verwendeten Nummern werden erfasst. Der Datensatz kann auf der Seite **Gutschriftentabelle** angezeigt werden. Ein Debitor kann keinen Betrag einlösen, der den Wert der Gutschrift übersteigt.
- **Geschenkkarte** – Geschenkkarten, die am Point-of-Sale ausgestellt und eingelöst werden. Überzahlungen sind für Geschenkkarten nicht zulässig. Alle Geschenkkarten sollten Kartennummernzuordnungen haben. 
- **Debitorenkonto** – Ein Debitorenkonto kann zum Verkaufszeitpunkt am Register mit dem Zahlungsbetrag belastet werden. Sie können diese Zahlungsmethode auch verwenden, um Verkaufsinformationen oder debitorenspezifische Rabatte zu erfassen, wenn Debitoren eine Zahlung mit einer anderen Zahlungsmethode leisten. In diesem Fall müssen debitorenspezifische Informationen eingerichtet werden.
- **Treuepunkte** – Die Punkte, die Debitoren für Treueprogramme kumulieren. Wenn Sie Treueprogramme erstellen, Punkte können Debitoren erhalten und sie auf verschiedene Weise dann einlösen. In einigen Treueprogrammen können Kunden Treuepunkte beispielsweise in Form eines Rabatts einlösen oder sogar sie als Zahlungsmethode verwenden.

Zum Einrichten von Zahlungsmethoden müssen Sie die folgenden Aufgaben abschließen.

1. Einrichten von Zahlungsmethoden für eine Organisation. Erstellen Sie die Zahlungsmethoden, die in der gesamten Organisation akzeptiert werden.
2. Einrichten von organisationsweiten Kartentypen und Kartennummern Wenn Kredit- oder Debitkarten akzeptiert werden, müssen Sie eine Zahlungsmethode für Karten und anschließend die organisationsweiten Kartentypen und Kartennummern erstellen.
3. Einrichten von Shopzahlungsmethoden Ordnen Sie die Zahlungsmethoden den einzelnen Shops zu, und geben Sie dann für jede Zahlungsmethode shopspezifische Einstellungen ein.
4. Einrichten von Kartenzahlungsmethoden für Shops Schließen Sie für alle Zahlungsmittel vom Typ "Karte", die im Shop akzeptiert werden, die Karteneinrichtung ab.


[!INCLUDE[footer-include](../includes/footer-banner.md)]