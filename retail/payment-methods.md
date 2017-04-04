---
title: Zahlungsmethoden
description: "Jeder Zahlungstyp, den ein Einzelhändler akzeptiert, muss im Einzelhandel und im Handel in Microsoft Dynamics 365 für Vorgänge konfiguriert werden, wenn das System so eingerichtet ist. In diesem Artikel wird beschrieben, wie Sie die Zahlungstypen einrichten können und beschreibt den Prozess, um sie einzurichten."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: MargoC
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b887fc5d03ea8982515e92725ce98cc416e56f9e
ms.openlocfilehash: 011beec07bf1ab858892ab1c374f1acf3839e877
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods"></a>Zahlungsmethoden

Jeder Zahlungstyp, den ein Einzelhändler akzeptiert, muss im Einzelhandel und im Handel in Microsoft Dynamics 365 für Vorgänge konfiguriert werden, wenn das System so eingerichtet ist. In diesem Artikel wird beschrieben, wie Sie die Zahlungstypen einrichten können und beschreibt den Prozess, um sie einzurichten.

Einzelhändler können für die von ihnen verkauften Produkte und angebotenen Dienstleistungen verschiedene Zahlungsformen akzeptieren. Obwohl die Barzahlung am häufigsten ist, können Einzelhändler Zahlungen auch in Form von Schecks, Kredikarten, Gutscheinen usw. entgegennehmen. Jeder Zahlungstyp den Einzelhändler, der akzeptiert, muss in Dynamics 365 für Vorgänge konfiguriert werden - Einzelhandel, wenn das System so eingerichtet ist. In der folgenden Liste wird jeden Zahlungstyp, der in Dynamics 365 für Arbeitsgänge eingerichtet werden kann - Einzelhandel:

-   **Bargeld** – Geld in der physischen Form der Währung, z. B. Banknoten und Münzen. Die Währung kann entweder die Unternehmenswährung oder die im Shop gültige lokale Währung sein.
-   **Scheck** – Ein übertragbares Wertpapier, das eine Zahlungsanweisung an die angegebene Bank enthält, einen bestimmten Betrag in einer bestimmten Währung zu zahlen. Ein Scheck ist im Allgemeinen entweder für eine unbegrenzte Dauer oder sechs Monate nach dem Ausstellungsdatum gültig, sofern kein anderer Gültigkeitszeitraum angegeben ist. Dieser Zeitraum variiert und hängt von der Bank ab, bei der der Scheck gezogen wird. Es gibt verschiedene Arten von Schecks, z. B. Orderschecks, Blankoschecks, Inhaberschecks und Schecks für Einzahlungen auf das Konto des Begünstigten. Schecks können für jeden Shop als Zahlungsmethode eingerichtet werden. Schecks können in der Währung akzeptiert werden, die entweder auf Unternehmensebene oder Shopebene definiert ist. Damit Schecks in einem Shop als Zahlungsmittel akzeptiert werden können, müssen Schecks als Zahlungsmethode eingerichtet werden.
-   **Währung** – Das primäre Zahlungsmittel, bei dem es sich nicht um die Standardwährung des Unternehmens handelt. Münzen und Papiergeld sind jeweils Formen von Währung. Die Währungszahlungsmethode stellt alle Währungen dar, die in Einzelhandel und Handel verwendet werden. Bevor diese Zahlungsmethode verwendet werden kann, müssen Währungen eingerichtet und einzelhandelsbezogene Wechselkursinformationen für die Währungen angegeben werden.
-   **Karte** – Alle Arten von Karten, die in Einzelhandel und Handel verwendet werden, beispielsweise Debit- und Kreditkarten. Es ist eine gute Idee, auf Organisationsebene eine Kartenzahlungsmethode einzurichten, die jede Art von Karte darstellt. Auf Shopebene kann dann für jede Karte oder jeden Kartensatz, der mit den gleichen Einstellungen verarbeitet werden soll, eine Zahlungsmethode eingerichtet werden. Die auf dem Markt erhältlichen Herstellerkarten, z. B. Debitkarten und Kreditkarten, müssen eingerichtet werden, bevor die Karten in einem Shop als Zahlungsmittel akzeptiert werden können.
-   **Gutschrift** – Gutschriften, die am POS ausgestellt und eingelöst werden. Die Gutschrift kann ein Guthaben oder eine Retourengutschrift sein, die bei einer Retoure ausgestellt wird. Wenn Gutschriften nur teilweise eingelöst werden, wird vom Programm eine neue Gutschrift für den neuen Saldobetrag ausgestellt. Die neue Gutschrift hat eine neue Nummer. Eine Gutschrift kann nur einmal verwendet werden, und alle verwendeten Nummern werden erfasst. Der Datensatz kann auf der Seite **Gutschriftentabelle** angezeigt werden. Ein Debitor kann keinen Betrag einlösen, der den Wert der Gutschrift übersteigt.
-   **Geschenkkarte** – Geschenkkarten, die am Point-of-Sale ausgestellt und eingelöst werden. Überzahlungen sind für Geschenkkarten nicht zulässig.
-   **Debitorenkonto** – Ein Debitorenkonto kann zum Verkaufszeitpunkt am Register mit dem Zahlungsbetrag belastet werden. Sie können diese Zahlungsmethode auch verwenden, um Verkaufsinformationen oder debitorenspezifische Rabatte zu erfassen, wenn Debitoren eine Zahlung mit einer anderen Zahlungsmethode leisten. In diesem Fall müssen debitorenspezifische Informationen eingerichtet werden.
-   ** ** Treuepunkte – Die Punkte, die Debitoren für Treueprogramme kumulieren. Wenn Sie Treueprogramme erstellen, Punkte können Debitoren erhalten und sie auf verschiedene Weise dann einlösen. In einigen Treueprogrammen können Kunden Treuepunkte beispielsweise in Form eines Rabatts einlösen oder sogar sie als Zahlungsmethode verwenden.

Zum Einrichten der Zahlungsmethoden in Einzelhandel und Handel müssen folgende Aufgaben ausgeführt werden.

1.  Einrichten von Zahlungsmethoden für eine Organisation. Erstellen Sie die Zahlungsmethoden, die in der gesamten Organisation akzeptiert werden.
2.  Einrichten von organisationsweiten Kartentypen und Kartennummern. Wenn Kredit- oder Debitkarten akzeptiert werden, müssen Sie die Zahlungsmethode für Karten erstellen und anschließend die organisationsweiten Kartentypen und Kartennummern erstellen.
3.  Einstellungszahlungsart shop. Hier können Sie Zahlungsmethoden den einzelnen Shops zu, und geben Sie dann den shopspezifische Einstellungen für jede Zahlungsmethode ein.
4.  Einrichten von Kartenzahlungsmethoden für Shops. Für alle Kartenzahlungsmethoden, die im Shop akzeptiert wird, schließen die Karteneinrichtung ab.



