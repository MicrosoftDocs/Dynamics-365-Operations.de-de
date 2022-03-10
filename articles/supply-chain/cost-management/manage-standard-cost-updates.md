---
title: Standardkostenaktualisierungen verwalten
description: Die Aktualisierung von Standardkostendaten kann auf zwei unterschiedliche Arten verwaltet werden - durch den Einzelversionsansatz oder durch den Zwei-Versionen-Ansatz.
author: AndersGirke
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3485f0722b8b99d7dc2d6dab470fdcc465b1da3d
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678664"
---
# <a name="manage-standard-cost-updates"></a>Standardkostenaktualisierungen verwalten

[!include [banner](../includes/banner.md)]

Die Aktualisierung von Standardkostendaten kann auf zwei unterschiedliche Arten verwaltet werden - durch den Einzelversionsansatz oder durch den Zwei-Versionen-Ansatz.

Beim Einzelversionsansatz wird eine Nachkalkulationsversion mit sämtlichen Kostendatensätzen verwendet. Diese Datensätze beinhalten die anfänglich definierten Kosten sowie allen Kostenaktualisierungen.

Beim Zwei-Versionen-Ansatz enthält eine Version die Datensätze der anfänglich definierten Kosten und eine zweite Version alle Datensätze der Kostenaktualisierungen. Einer der wichtigsten Vorteile des Zwei-Versionen-Ansatzes besteht in der übersichtlichen Darstellung sowie in der Nachverfolgung von Kostenaktualisierungen in einer eigenen Nachkalkulationsversion, ohne dass sich dies auf die ursprüngliche Nachkalkulationsversion auswirkt. Der Zwei-Versionen-Ansatz kann zur Erkennung mehrerer stufenweiser Aktualisierungen verwendet werden, bei denen jede einzelne stufenweise Aktualisierung eine eigene Nachkalkulationsversion mit den stufenweisen Kostendatensätzen besitzt.

## <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht, wie der Einzelversions- und der Zwei-Versionen-Ansatz bei der Aktualisierung von Standardkosten in einer Produktionsumgebung verwendet werden kann. Aktualisierungen geben beispielsweise neue Artikel oder Korrekturen wieder. Angenommen, eine einzelne Nachkalkulationsversion stellt die Standardkosten des aktuellen Jahres dar. Die Kennung für diese Version lautet "2020-STD". Version "2020-STD" enthält die derzeit aktiven Kosten für alle Artikel. Darüber hinaus enthält diese Version alle arbeitsgangsteuerungsbezogenen Kostenkategorien und Berechnungsformeln für Gemeinkosten, die zu Beginn des Jahres 2020 bekannt waren. "2020-STD" ist die ursprüngliche Nachkalkulationsversion.

- **Einzelversionsansatz für die Aktualisierung von Kostendaten** − Beim Einzelversionsansatz enthält die ursprüngliche Nachkalkulationsversion "2020-STD" sämtliche Kostendatensätze. Kostenaktualisierungen werden in "2020-STD" erfasst und auf den Status "Ausstehend" festgelegt. Die ausstehenden Kosten können manuell für neue eingekaufte Artikel eingegeben oder als Folge einer Korrektur für einen produzierten Artikel berechnet werden. Beim Einzelversionsansatz wird für die Herstellkostenkalkulation keine Fallback-Datenquelle benötigt, da in der Nachkalkulationsversion alle aktiven Kosten enthalten sind. Nach Aktivierung der ausstehenden Kosten enthält die ursprüngliche Nachkalkulationsversion "2020-STD" auch wieder alle derzeit aktiven Kosten.
- **Zwei-Versionen-Ansatz für die Aktualisierung von Kostendaten** − Für den Zwei-Versionen-Ansatz wird eine zusätzliche Nachkalkulationsversion benötigt, in der ausschließlich die Kostenaktualisierungen enthalten sind. Der Bezeichner für diese Version ist "2020-STD-ÄNDERUNGEN". Kostenaktualisierungen werden in „2020-STD-ÄNDERUNGEN“ erfasst und auf den Status „Ausstehend“ festgelegt. Beim Zwei-Versionen-Ansatz ist für die Herstellkostenkalkulation der ausstehenden Kosten für produzierte Artikel eine Fallback-Datenquelle erforderlich. Denn die zusätzliche Nachkalkulationsversion "2020-STD-ÄNDERUNGEN" enthält lediglich einen Teil der Kostendaten. Das Fallback kann entweder als aktive Kosten oder als Nachkalkulationsversion "2020-STD" ausgedrückt werden, da beide die Quelle der Kostendaten identifizieren, wenn sie nicht in "2020-STD-ÄNDERUNGEN" enthalten sind. Nach Aktivierung der ausstehenden Kosten enthält die Nachkalkulationsversion „2020-STD-ÄNDERUNGEN“ die derzeit aktiven Kosten (also die Aktualisierungen), wohingegen die ursprüngliche Nachkalkulationsversion „2020-STD“ unverändert bleibt. Beim Zwei-Versionen-Ansatz sollten Sperrrichtlinien eingerichtet werden, um eine Aktualisierung der ursprünglichen Nachkalkulationsversion zu verhindern. Für die zusätzliche Nachkalkulationsversion sollten exakt die gleichen Richtlinien eingerichtet werden. Davon ausgenommen sind das angegebene Anfangsdatum sowie die selektive Verwendung von Sperrrichtlinien, um Aktualisierungen zuzulassen. Das angegebene Anfangsdatum muss zur Berücksichtigung des geplanten Aktivierungsdatums bei jeder Änderung geändert werden.

In diesem Beispiel wurde eine zusätzliche Nachkalkulationsversion zum Verwalten von Aktualisierungen im Laufe des Jahres 2020 verwendet. Es können auch mehrere zusätzliche Nachkalkulationsversionen verwendet werden, beispielsweise getrennte Versionen für jede einzelne Änderung. Falls mehrere zusätzliche Nachkalkulationen verwendet werden, muss das Fallback als aktive Kosten ausgedrückt werden, da sie sich über mehrere Nachkalkulationsversionen erstrecken würden.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Finanzdimensionen für die Standardkostenneubewertung

Durch Aktivieren eines neuen Standardpreises wird der verfügbare Lagerbestand in der Regel durch Standardkosten-Neubewertungstransaktionen neu bewertet. Normalerweise werden die Finanzdimensionen des Artikels anschließend in den Transaktionen gebucht. Wenn Sie jedoch steuern möchten, ob und wie die Finanzdimensionen gebucht werden, verwenden Sie die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die Funktion *Optionen für standardmäßige Finanzdimensionen zur Neubewertung der Standardkosten des Bestands* zu aktivieren. Wechseln Sie nach dem Aktivieren dieser Funktion zu **Kostenmanagement > Einrichtung der Bestandsbuchhaltungsrichtlinien> Parameter** und wählen Sie in der neuen Dropdownliste **Ursprung der Finanzdimension** einen der folgenden Werte aus:

- **Kein** – Bei den Transaktionen zur Neubewertung werden keine Finanzdimensionen gebucht. Wenn Ihre Kontostruktur eine erforderliche Finanzdimension umfasst, wird der Neubewertungsprozess zwar weiterhin ausgeführt, aber er erstellt Buchhaltungseinträge, die keine Finanzdimensionen haben. In diesem Fall erhalten Benutzer zuerst eine Warnmeldung, damit sie die Neubewertung bei Bedarf abbrechen können.
- **Tabelle** – Die Finanzdimensionen des Artikels werden bei den Transaktionen zur Neubewertung gebucht. Hierbei handelt es sich um die Standardeinstellung. Sie stimmt mit dem ursprünglichen Systemverhalten überein, bei dem die Funktion *Optionen für standardmäßige Finanzdimensionen zur Neubewertung der Standardkosten des Bestands* nicht aktiviert ist.
- **Buchung** – Die Finanzdimensionen der Transaktion, die neu bewertet wird, werden bei den Transaktionen zur Neubewertung gebucht. Standardmäßig werden die Finanzdimensionen des Bestandskontos der ursprünglichen Transaktion sowohl für das Bestandskonto als auch für das Neubewertungskonto verwendet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]