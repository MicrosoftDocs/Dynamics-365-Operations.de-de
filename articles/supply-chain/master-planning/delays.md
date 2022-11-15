---
title: Verzögerungen
description: Dieser Artikel enthält Informationen zu verzögerten Daten in der Masterplanung. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum.
author: t-benebo
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e7e0150e40193f2f799677ad19cae2ea589afc0
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740629"
---
# <a name="delays"></a>Verzögerungen

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu verzögerten Daten in der Masterplanung. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum.

Der Produktprogrammplan kann das früheste Erfüllungsdatum für eine Buchung, für den Lieferzeiten, Materialverfügbarkeit, Kapazitätsverfügbarkeit und verschiedene Planungsparameter berechnen. 

Wenn Produktprogrammplan ein Auftragsdatum berechnet, das vor dem aktuellen Datum liegt, kann der Auftrag nicht rechtzeitig erfüllt werden. Daher wird der Auftrag verzögert. In diesem Fall plant der Produktprogrammplan den Auftrag im Voraus, ausgehend vom aktuellen Datum und einschließlich Lieferzeiten. Diese Lieferzeiten beginnen mit Komponentenartikeln auf niedrigerer Ebene. Der Auftrag empfängt dann ein verzögertes Datum. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum basierend auf den aktuellen Daten. Produktprogrammplan berechnet auch die Anzahl der Verzögerungstagen. 

In bestimmten Situationen möchten Sie möglicherweise Verzögerungen nicht berechnen, z. B. wenn Benutzer wissen, dass sie Durchlaufzeiten beschleunigen können, indem sie Alternativmodi der Lieferung auswählen. 

Sie können konfigurieren, wie Verzögerungen für eine Dispositionssteuerungsgruppe berechnet werden. Sie können die Dispositionssteuerungsgruppe dann später einem Artikel zuordnen. 

Auf der Seite **Parameter für Produktprogrammplanung** können Sie die Startzeit für die Berechnung von Verzögerungen festlegen. Wenn ein Auftrag nach dieser Zeit erfüllt wird, addiert das System einen Tag Verzögerung zum Verzögerungsdatum des Auftrags hinzu. 

> [!NOTE]
> In früheren Versionen waren berechnete Verzögerungen als *Verfügbarkeitsmeldungen* bekannt, das verzögerte Datum als *Verfügbarkeitsdatum*, und eine verzögerte Buchung war als eine *Transaktio mit Erfüllung in der Zukunft* bekannt.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Begrenzte Verzögerungen bei der Einrichtung der Produktion mit mehreren Stücklistenebenen
Wenn Sie mit Verzögerungen in einem Produktionssetup mit mehreren Stücklistenstufen arbeiten, ist es wichtig zu beachten, dass nur die Artikel direkt über dem Artikel (in der Stücklistenstruktur), die die Verzögerung verursachen, im Rahmen der Masterplanung mit einer Verzögerung aktualisiert werden. Bei anderen Elementen in der Stücklistenstruktur wird die Verzögerung erst beim ersten Masterplanungslauf angewendet, wenn der geplante Auftrag für die oberste Ebene genehmigt oder bestätigt wird. 

Um diese bekannte Einschränkung zu umgehen, können die Fertigungsaufträge oben in der Stücklistenstruktur mit Verzögerungen vor dem nächsten Masterplanungslauf genehmigt (oder bestätigt) werden. Auf diese Weise bleibt die Verzögerung des verspäteten genehmigten geplanten Fertigungsauftrags erhalten und alle zugrunde liegenden Komponenten werden entsprechend aktualisiert.
Aktionsnachrichten können auch verwendet werden, um Planaufträge zu identifizieren, die aufgrund anderer Verzögerungen in der Stücklistenstruktur zu einem späteren Zeitpunkt verschoben werden können.

## <a name="desired-date"></a>Gewünschtes Datum

Auf der Seite **Bestellvorschlag** unter der Registerkarte **Verzögerungen** ist das **Gewünschtes Datum** für den Bestellvorschlag. Das gewünschte Datum eines Bestellvorschlags ist das Basisdatum für Verzögerungen, was ein berechnetes Datum ist, dass dem **Angefordertes Datum** entspricht, das anhand des **Bedarfsverlauf** berechnet wird. Wenn der Bestellvorschlag eine Stücklistenposition, eine Produktionsauftragsposition oder eine Kanbanposition ist, basiert das gewünschte Datum auf dem **Bedarfsdatum** und das gewünschte Datum wird auf nicht auf der Seite **Bestellvorschlag** angezeigt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Deckungseinstellungen](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]