---
title: Qualitätsmanagementprozesse
description: Dieser Artikel enthält Informationen zum Qualitätssicherungsprozess für fehlerhafte Produkte. Es beschreibt, wie Sie Qualitätskontrollfunktionen verwenden können, wie Sie Qualitätsmängel definieren und verwalten und wie Korrekturen behandelt werden.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ab3b886b9d5237e96e193d7369c6060f19516e5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214066"
---
# <a name="quality-management-processes"></a>Qualitätsmanagementprozesse

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zum Qualitätssicherungsprozess für fehlerhafte Produkte. Es beschreibt, wie Sie Qualitätskontrollfunktionen verwenden können, wie Sie Qualitätsmängel definieren und verwalten und wie Korrekturen behandelt werden.

Die Qualitätssicherung umfasst das Testen von Produkten sowie die Verwaltung von Material, das die Qualitätsanforderungen nicht erfüllt. Qualitätssicherungsprozesse helfen, ein hohes Maß an Produktqualität in der Lieferkette sicherzustellen. Diese Prozesse erleichtern außerdem, Lieferkettenprozesse zu optimieren und die Kundenzufriedenheit zu steigern. Qualitätsmanagement können Ihnen dabei helfen, Abfertigungszeiten, wenn Sie fehlerhafte Produkte zu tun haben, unabhängig von Bezugspunkt dieser Produkte zu verwalten. Sie können Diagnoseergebnisse zu den Korrekturaufgaben verknüpfen. Das System kann Aufgaben planen, Probleme korrigiert und damit von Wiederholungen, dieser Probleme zukünftig zu verhindern. Qualitätsmanagement kann auch Probleme (einschließlich) durch interne Probleme Problemtyp, nachverfolgen und Lösungen Sie können ermitteln, wie entweder kurzzeitig oder langfristig. Die Statistiken zu Key Performance Indicators (KPIs) geben Einblick in Qualitätsmangelprobleme, die zuvor aufgetreten sind, sowie in die Lösungen, die angewendet wurden, um sie zu korrigieren. Sie können Vergangenheitsdaten verwenden, um die Effizienz der Qualitätsmaßnahmen besser zu prüfen, die zuvor ausgeführt wurden und geeignete Maßnahmen in der Zukunft zu bestimmen.

## <a name="controlling-the-quality-management-process"></a>Steuern des Qualitätssicherungsprozesses
Nachfolgend einige der Methoden, mit denen Sie den Qualitätssicherungsprozess steuern können:

-   Erstellen von Qualitätsprüfungsaufträgen, die auf Grundlage von Triggerpunkten wie z. B. "am Produktzugang" für eingehende Arbeitsgänge oder "an der Produktaufnahme" für ausgehende Arbeitsgänge basieren.
-   Dokumentieren Sie Testergebnisse und entscheiden Sie, ob die Ergebnisse den eingerichteten Testkriterien und akzeptable Qualitätsstufen entsprechen.
-   Verwenden Sie Dokumentverwaltung für ausführliche Produktbeschreibungen und benutzerspezifische Hinweise als Teil der Berichterstellung während des Inspektionsprozesses.
-   Verwalten Sie Produkte mit Qualitätsmangel, und statten Sie diese Produkte mit zusätzlichen Qualitätsmangelinformationen aus, um die ursprüngliche Ursache eines Problems ausfindig zu machen.
-   Dokumentieren Sie die Kosten der Verwaltung eines Qualitätsmangels. Die Kosten beinhalten die Artikel (z. B. Ersatzteile), sonstigen Zuschläge und benötigten Arbeitsstunden, die im Zusammenhang mit der Korrektur des Qualitätsmangels nötig sind.
-   Planen Sie Prozesse zur Fehlerkorrektur mithilfe der Korrekturbehandlung, die mit Qualitätsprüfungsaufträgen verknüpft ist.

[![Qualitätsmanagementprozesse](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Produkttests und Qualitätsprüfungsaufträgen
Das Testen von Produkten wird üblicherweise als Qualitätskontrolle bezeichnet und nutzt Qualitätsprüfungsaufträge. Mit der Qualitätssteuerungsfunktion besitzen Sie folgende Möglichkeiten:

-   Sie können Tests definieren, die für Material ausgeführt werden müssen. Diese Tests enthalten die Qualitätsangaben, das geeignete Testinstrument, Dokumente mit einer Beschreibung des Tests, einen Musteraufnahmeplan und das akzeptable Qualitätsniveau.
-   Sie können einen Qualitätsprüfungsauftrag mit Informationen zu den auszuführenden Tests für einen bestimmten Auftrag (beispielsweise eine Bestellung oder ein Produktionsauftrag) oder Informationen zu einer bestimmten Lagermenge. Qualitätsprüfungsaufträge können manuell oder automatisch auf der Grundlage von Qualitätsrichtlinien erstellt werden.
-   Sie können in jedem Geschäftsprozess die Qualitätsrichtlinien in Bezug auf Aufträge, Bestellungen, Quarantäneaufträge oder Produktionsaufträge für die automatische Generierung eines Qualitätsauftrags mit den Testanforderungen für ein- oder ausgehendes Material definieren.
-   Sie können die Testergebnisse eines Qualitätsprüfungsauftrags erfassen, die Testergebnisse anhand des akzeptablen Qualitätsniveaus prüfen und eine Analysebescheinigung mit den Testergebnissen drucken.

## <a name="nonconformance"></a>Nichtübereinstimmung
Ein Qualitätsmangel beschreibt einen Artikel, der ein Qualitätsproblem hat. Sie können einen Qualitätsmangelprozess erstellen, der für die Menge des Materials mit Qualitätsmängeln eine Beschreibung der Problemursache, die Art des Problems sowie erläuternde Hinweise enthält. Zur Vereinfachung der Analyse von Material mit Qualitätsmängeln besteht die Möglichkeit zum Definieren einer Klassifizierung für Problemtypen. Sie können eine Qualitätsmangelmarkierung und einen Qualitätsmangelbericht auch drucken, um die Disposition des Materials mit Qualitätsmängeln zu verwalten. Beispielsweise können die Markierung und der Bericht eine Bedingung von **Nicht verwendbar** oder **Eingeschränkte Verwendung** anzeigen.

In der folgenden Tabelle werden die sechs Standard Qualitätsmangeltypen angegeben und die Informationen beschrieben, die für jeden Typ erfasst werden müssen.

| Nichtübereinstimmungstyp   | Quellinformationen                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kunde              | Die Debitorenkontonummer, die Auftragsnummer oder Losnummer einer Auftragsbuchung. Der Qualitätsmangel könnte sich beispielsweise auf eine bestimmte Auftragslieferung oder auf Debitorenfeedback zur Produktqualität beziehen.       |
| Serviceanforderung       | Die Debitorenkontonummer, die Auftragsnummer oder Losnummer einer Auftragsbuchung. Der Qualitätsmangel könnte sich beispielsweise auf eine bestimmte Auftragslieferung oder auf eine Debitorenbeschwerde zur Artikelqualität beziehen.     |
| Händler                | Die Kreditorenkontonummer, die Bestellnummer oder Losnummer einer Bestellbuchung. Der Qualitätsmangel könnte sich beispielsweise auf einen Bestelleingang oder auf die Bedenken eines Kreditors hinsichtlich eines gelieferten Teils beziehen. |
| Produktion            | Die Produktionsauftragsnummer oder Losnummer einer Produktionsauftragsbuchung. Der Qualitätsmangel könnte sich beispielsweise auf eine bestimmte produzierte Charge beziehen.                                                                      |
| Intern              | Die Nummer des Qualitätsprüfungsauftrags oder Losnummer einer Buchung für einen Qualitätsprüfungsauftrag. Der Qualitätsmangel könnte sich beispielsweise auf die Tests beziehen, die im Rahmen des Qualitätsprüfungsauftrags ausgeführt wurden, oder auf die Bedenken eines Mitarbeiters hinsichtlich der Produktqualität.     |
| Kuppelprodukt - Produktion | Ein Co-Produkt-Produktionsauftragsqualitätsmangel, der Chargenproduktionsaufträgen zugeordnet ist.                                                                                                                                                    |

Qualitätsmängel werden mit einem Problemtyp zugeordnet. Problemtypen werden auf der Seite **Problemtypen** definiert, in der Sie angeben, welche Problemtypen mit jedem Nichtübereinstimmungstyp zugeordnet werden können. Zum Beispiel können die Problemtypen für Qualitätsmängel des Typs **Serviceanforderung** eine Klassifizierung von Debitorenbeschwerden darstellen, wohingegen die Problemtypen für einen **internen** Qualitätsmangel eine Klassifizierung von Fehlercodes darstellen können.

Beim Erstellen eines neuen Qualitätsmangels wählen Sie die Art des Qualitätsmangels und den Problemtyp aus. Der erste Genehmigungsstatus ist **Neu**, der eine Handlungsaufforderung darstellt. Der nächste Schritt darin, den Genehmigungsstatus zu **Genehmigt** oder **Abgelehnt** zu ändern, um anzugeben, dass Sie wegen des Qualitätsmangels (keine) Maßnahmen ergreifen werden. Sie können einen Qualitätsmangel auch schließen (durch Auswahl eines gesonderten Kontrollkästchens), um anzugeben, dass Sie den Mangel fertig bearbeitet haben, oder ihn öffnen, um anzugeben, dass eine weitere Prüfung erforderlich ist.

Sie können Kommentare für einen Qualitätsmangel eingeben, indem Sie ein Dokument zuordnen. Es wird empfohlen, einen eindeutigen Dokumenttyp für Qualitätsmängel zu definieren, indem die Seite **Dokumenttyp** verwendet. Anschließend können Sie auf der Seite **Berichtseinstellungen** definieren, ob Kommentare für diesen Dokumenttyp gedruckt werden sollen bezüglich der Nichtübereinstimmungsbericht- und Qualitätsmangelmarkierung. Der Qualitätsmangelbericht und eine entsprechende Markierung können bei der Disposition von Material helfen. Berichte und Markierungen können auf Basis von Auswahlkriterien generiert werden, die einem Qualitätsmangel zugeordnet sind. Diese Kriterien umfassen die Qualitätsmangelnummer, Artikel-, -Debitor, -Kreditor und Statusangaben.

Der Qualitätsmangelbericht enthält die Qualitätsmangelnummer, Artikel- und -Problemtyp. Abhängig von Ihrer Berichtseinstellungsrichtlinie kann der Bericht möglicherweise auch zugehörige Hinweise zum Qualitätsmangel enthalten. Die Qualitätsmangelmarkierung zeigt ähnliche Informationen an und zeigt zudem Quarantänezone und -typ an (zum Beispiel **Eingeschränkt verwendbar** im Vergleich zu **Nicht verwendbar**), die dem Qualitätsmangel zugeordnet wurden, um die Disposition des fehlerhaften Materials zu regeln.

## <a name="approved-nonconformance"></a>Genehmigter Qualitätsmangel
Optional lassen sich zugehörige Arbeitsgänge für einen genehmigten Qualitätsmangel definieren. Ein zugehöriger Arbeitsgang beschreibt die Arbeit, die ausgeführt werden soll, und enthält eine Liste der Qualitätsarbeitsgänge, die Sie definiert haben, und beschreibenden Text zur Ursache für die Arbeit. Nach dem Definieren eines Arbeitsgangs können optional die sonstigen Zuschläge, Artikel und die Arbeitszeitnachweise definiert werden, die für die Arbeitsschritte erforderlich sind. Die berechneten Kosten werden für den zugehörigen Arbeitsgang angezeigt, und die gesamten berechneten Kosten werden für den Qualitätsmangel angezeigt. Die berechneten Kosten und die zu Grunde liegenden Details (zu Artikeln, Arbeitsstunden und sonstigen Zuschlägen) stellen Referenzinformationen dar. Sie werden nur in der Qualitätsmanagementfunktion verwendet.

Sie können aufgrund eines Qualitätsmangels optional einen Qualitätsprüfungsauftrag erstellen. Führen Sie dazu zunächst eine Abfrage nach Qualitätsprüfungsaufträgen aus, und erstellen Sie anschließend den neuen Qualitätsprüfungsauftrag. Zum Beispiel kann ein Qualitätsprüfungsauftrag ergeben, dass das fehlerhafte Material getestet bzw. erneut getestet werden muss. Im neu erstellten Qualitätsprüfungsauftrag wird die Verbindung zum ursprünglichen Qualitätsmangel angezeigt.

Optional besteht die Möglichkeit zum Verknüpfen von Qualitätsmängeln sowie zum Erstellen eines Qualitätsmangeleintrags auf Basis eines bereits vorhandenen Qualitätsmangels. So kann es sich bei einer Verknüpfung beispielsweise um die Kopplung von Qualitätsproblemen handeln.

## <a name="correction-handling"></a>Korrekturbehandlung
Die Seite **Korrekturen** können Sie eine Liste von Qualitätsmängeln erstellen, die korrigiert werden müssen. Jeder Korrekturartikel wird dem Diagnosetyp zugeordnet, der bewirkte, dass das Problem entdeckt wurde. Die **Korrekturen** Seite enthält außerdem Informationen darüber, wer Korrekturaktivität ausführen muss, wenn und. Sie können die Details der Quelle sowie und Korrektur beschreiben, die erforderlich ist, indem ein Dokument der Korrektur Kunden. Nachdem der Qualitätsmangel adressiert oder korrigiert wurde, "schließen" Sie den Korrekturartikel, indem Sie die Option **Abgeschlossen** auswählen. Sie können auch angeben, dass die Lösung eine kurzfristige Lösung war.

Es wird empfohlen, einen eindeutigen Dokumenttyp für Korrekturen zu definieren, indem die Seite **Dokumenttyp** verwendet wird. Anschließend können Sie auf der Seite **Berichtseinstellungen** definieren, ob Kommentare für diesen Dokumenttyp gedruckt werden sollen bezüglich des Korrekturreports. Ein gedruckter Korrekturbericht enthält Informationen zur Nichtübereinstimmung und die zugehörigen Hinweise. Der Bericht umfasst auch Korrekturinformationen, wie der Diagnosetyp und die zugehörigen Korrekturhinweise.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Qualitätsmanagement – Übersicht](enable-quality-management.md)

[Qualitätsmangelverwaltung](enable-nonconformance-management.md)

[Sperrung von Lagerbestand](inventory-blocking.md)

[Quarantäneaufträge](quarantine-orders.md)

[Testbestellungen einrichten](tasks/set-up-quality-orders.md)

[Überprüfen Sie die Qualität von Waren](tasks/inspect-quality-goods.md)
