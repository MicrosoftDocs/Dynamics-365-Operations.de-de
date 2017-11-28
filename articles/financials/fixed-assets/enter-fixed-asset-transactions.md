---
title: Anlagenbudgetbuchungsoptione
description: "In diesem Artikel werden die unterschiedlichen, verfügbaren Methoden beschrieben, um Transaktionen für Anlagen zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18352ad921c2e2d110a7535f979272685105662f
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-transaction-options"></a>Anlagenbudgetbuchungsoptione

[!include[banner](../includes/banner.md)]


In diesem Artikel werden die unterschiedlichen, verfügbaren Methoden beschrieben, um Transaktionen für Anlagen zu erstellen.

Sie können Anlagen für die Integration in Kreditoren, Debitoren, Beschaffung und Hauptbuch einrichten. Sie können außerdem Artikel in der Lagerverwaltung in Anlagen übertragen, wenn Sie diese Artikel intern verwenden möchten.

## <a name="accounts-payable"></a>Kreditorenkonten
Sie können Anlagenbuchungen auf der Seite "Alle Journale" eingeben. Diese Seite kann über die Seite "Rechnungserfassung" geöffnet werden. Sie können die Erfassungsbelegseite aus der Rechnungsgenehmigungserfassungsseite öffnen. Wählen Sie im Feld "Gegenkontenart" "Anlagen" aus. Wählen Sie dann im Feld "Gegenkonto" eine Anlagennummer aus. Geben Sie auf der Registerkarte "Anlagen" die Werte in den Feldern "Transaktionstyp" und "Buch" ein.

## <a name="accounts-receivable"></a>Debitorenkonten
Sie können Anlagenbuchungen auf der Seite "Freitextrechung" eingeben.  In der Freitextrechnungsseite im Rechnungspositionsraster, wählen Sie eine Position aus. Klicken Sie auf das Inforegister "Positionsdetails". Geben Sie die Anlagennummer das Buch für die Abgangsbuchung ein. Bei Freitextrechnungen lautet die Anlagenbuchungsart stets "Veräußerung".

## <a name="procurement-and-sourcing"></a>Beschaffung
Sie können Anlagenbuchungen auf der Seite "Bestellung" eingeben. Geben Sie die erforderlichen Informationen zum Erstellen einer Bestellung ein, und klicken Sie anschließend auf OK. In der Bestellungsseite klicken Sie auf das Positionsdetail-Inforegister. Geben Sie danach auf der Registerkarte "Anlagen" Informationen zur Anlage ein. 

Um eine Anschaffungsbuchung für eine vorhandene Anlage zu buchen, geben Sie die Anlagennummer, das Wertmodell und die Buchungsart an. Die Anlage kann nicht gebucht werden, wenn diese Informationen nicht vollständig sind. Um eine Anschaffungsbuchung für eine neue Anlage zu buchen, aktivieren Sie das Kontrollkästchen "Neue Anlage?", und wählen Sie dann die Anlagengruppe aus, der die neue Anlage zugewiesen werden soll. Für eine Position stehen jedoch keine Anlagenfelder zur Verfügung, wenn die Position in einer Lagersteuerungsgruppe enthalten ist, die ein Lagermodell für Standardkosten verwendet. Darüber hinaus bestimmen die Optionen, die auf der Seite "Anlagenparameter" definiert werden, ob Sie Anschaffungsbuchungen in den Einkaufsmodulen buchen können. 

Wird für die Anschaffung von Anlagen die Bestellungserfassung oder die Erfassung "Lager an Anlagen" verwendet, wirkt sich dies auf den Lagerwert aus.

## <a name="general-ledger"></a>Hauptbuch
Jede Anlagenbuchungsart kann auf der Seite "Allgemeine Erfassung" gebucht werden. Sie können auch Erfassungen in Anlagen verwenden, um Anlagenbuchungen vorzunehmen.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Eingabeoptionen für Anlagenbuchungsarten


| Transaktionstyp                    | Modul                   | Optionen                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Anschaffung, Anschaffungsregulierung | Feststehende Inhaltsteile             | Anlagen, Bestand für Anlagen   |
|                                     | Hauptbuch           | Allgemeine Erfassung                           |
|                                     | Kreditorenkonten         | Rechnungserfassung und Rechnungsgenehmigungserfassung |
|                                     | Beschaffung | Bestellung                            |
| Abschreibung                        | Feststehende Inhaltsteile             | Feststehende Inhaltsteile                              |
|                                     | Hauptbuch           | Allgemeine Erfassung                           |
| Abgang                            | Anlagevermögen             | Anlagevermögen                              |
| ** **                               | Hauptbuch           | Allgemeine Erfassung                           |
| ** **                               | Debitorenkonten      | Freitextrechnung                         |



Weitere Informationen finden Sie unter [Anlage-Integration](fixed-asset-integration.md).




