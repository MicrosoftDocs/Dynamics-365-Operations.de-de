---
title: Übersicht über das Modul zur Rückvergütungsverwaltung
description: Dieses Thema bietet einen Überblick über das Modul zur Rückvergütungsverwaltung für Microsoft Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 136e528093e6e73ffe090cea0c02a4cdbf787c5efc3d9c0664869c995a682daa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720251"
---
# <a name="rebate-management-module-overview"></a>Übersicht über das Modul zur Rückvergütungsverwaltung

[!include [banner](../includes/banner.md)]

Sie können das Modul **Rückvergütungsverwaltung** zum Erstellen von Verträgen, Deals oder Vereinbarungen zwischen Ihrem Unternehmen und seinen Debitoren oder Kreditoren verwenden, damit Sie Rückvergütungen, Abzüge und Lizenzgebühren berechnen können. Die Rückvergütungsverwaltung verfolgt und verwaltet Rückvergütungs- und Abzugstransaktionen an einem zentralen Ort, an dem Benutzer sie effektiv erstellen, überprüfen und verarbeiten können.

Die Rückvergütungsverwaltung unterstützt die Erstellung, Pflege und Verarbeitung von *Rückvergütungen*. Eine Rückvergütung ist die Rückzahlung eines Teils des Einkaufspreises durch einen Verkäufer oder Käufer. Rückvergütungen basieren normalerweise auf dem Kauf einer bestimmten Menge oder eines bestimmten Warenwerts während eines bestimmten Zeitraums. Im Gegensatz zu Rabatten werden Rückvergütungen erst nach vollständiger Rechnungsstellung des Kaufbetrags gewährt.

Die Rückvergütungsverwaltung unterstützt außerdem *Abzüge*. Ein Abzug ist eine Vergütung, eine Gegenleistung oder eine Gebühr, die entweder für eine Lizenz oder das Recht zur Nutzung von geistigem Eigentum wie einer Marke, einem Urheberrecht oder einem Patent oder für das Recht zur Nutzung einer natürlichen Ressource, für einen Zweck wie Angeln, Jagen oder Bergbau, gezahlt wird. Abzüge werden normalerweise als Prozent vom Umsatzes oder Gewinn aus der realisierten Nutzung berechnet. Je mehr geistiges Eigentum oder natürliche Ressourcen genutzt werden, desto höher ist der realisierte Abzug.

Darüber hinaus unterstützt die Rückvergütungsverwaltung *Lizenzgebühren* der Debitoren. Lizenzgebühren sind Zahlungen, die eine Partei an den Lizenznehmer oder Franchisenehmer für das Recht zur Nutzung eines Vermögenswerts leistet.

Mit der Rückvergütungsverwaltung können Sie Buchungsprofile für Rückstellungen, Rückvergütungen und Abschreibungen definieren. Darüber hinaus können die Buchungen für einen bestimmten Debitor oder Kreditor festgelegt werden. Auf diese Weise können Deals, die nicht für alle Debitor- oder Kreditorszenarien gelten, über Buchungen verfolgt werden.

Rückvergütungstransaktionen werden automatisch basierend auf der ausgewählten Berechnungsmethode generiert und in Stapelverarbeitungsaufträgen geplant. Darüber hinaus können Sie Workflows zum Verwalten, Überprüfen und Genehmigen von Vereinbarungen einrichten.

## <a name="basis-calculation"></a>Basisberechnung

Debitorenrückvergütungen, Debitorenlizenzgebühren und Kreditorenrückvergütungen können je nach Ihren geschäftlichen Anforderungen auf einer anderen Basis verwendet werden:

- Debitorenrückvergütungen können auf Aufträgen, Lieferscheinen oder Rechnungen basieren.
- Debitorenlizenzgebühren können auf Aufträgen, Lieferscheinen oder bezahlten Rechnungen basieren.
- Kreditorenrückvergütungen können entweder auf Bestellungen oder auf Aufträgen basieren. Sie können basierend auf Produkten berechnet werden, die vom Rückvergütungskreditor gekauft und über Verkaufsrechnungen an Debitoren verkauft werden.

## <a name="flexible-calculations"></a>Flexible Berechnungen

Rückvergütungsberechnungszeiträume sind sowohl für Debitoren- als auch Kreditorendeals verfügbar. Ein Berechnungszeitraum legt die Länge des Deals, die Berechnungshäufigkeit und den Berechnungszeitraum fest. Die Rückvergütungen können basierend auf den Auftragsmengen oder -beträgen für qualifizierte Produkte während des Rückvergütungszeitraums auflaufen.

Für jede Vereinbarungsberechnung kann einer der folgenden Zeiträume festgelegt werden:

- Rechnung
- Tag
- Woche
- Monat
- Quartal
- Jahr
- Angepasste Periode
- Beliebiges Vielfaches eines der zuvor aufgeführten Zeiträume

Die Berechnung kann auf einzelne Debitoren und Produkte, Gruppen von Debitoren und Produkten oder alle Debitoren und Produkte angewendet werden. Rückvergütungen mit mehreren Detailpositionen können unterschiedliche qualifizierende Datumsbereiche haben. Die Rückstellungs- und Anspruchsfristen können abweichen. Beispielsweise können Rückstellungen jeden Tag verarbeitet werden, Ansprüche dagegen einmal pro Monat.

Rückvergütungen können basierend auf vielen verschiedenen Parametern konfiguriert werden. Sie können beispielsweise als Prozentsatz, Satz oder fester Betrag konfiguriert werden. Es gibt vier Hauptberechnungsmethoden:

- Abgestuft
- Kumulativ
- Rollierend
- Gesamtwert

Die Ergebnisse der Rückvergütungsberechnung können auch durch andere Rückvergütungen reduziert werden, je nachdem, ob die Rückvergütung so eingerichtet ist, dass sie auf der Grundlage des Nettobetrags berechnet wird.

Auf der Seite des Kreditors können Rabatte, die auf Verkaufsaufträgen basieren, den Preis auf der Grundlage einer FIFO-Regel (first in, first out), dem letzten Einkaufspreis, dem durchschnittlichen Einkaufspreis oder dem Verkaufspreis berechnen.

## <a name="rebate-target-transactions"></a>Rückvergütungszielbuchungen

Die Ergebnisse, die durch den Rückvergütungsdeal oder die Rückvergütungsvereinbarung generiert werden, können finanzieller Art oder Artikel sein.

Die finanziellen Ergebnisse werden durch den Zahlungstyp bestimmt, der der Vereinbarung aus dem Buchungsprofil zugeordnet ist. Diese Ergebnisse können Debitorabzugserfassungen, Freitextrechnungen und Kreditorenrechnungen umfassen. Zu Prüfungszwecken enthalten Zieltransaktionen für finanzielle Rückvergütungen einen Verweis auf die ursprüngliche Rückvergütungsvereinbarung.

Artikelausgaben erstellen einen kostenlosen Artikelauftrag für Debitorenrückvergütungen und eine Bestellung für Kreditorenrückvergütungen. Artikelrückerstattungs-Zieltransaktionen enthalten Optionen, um zu bestimmen, welche Rückvergütungsreferenz in den kostenlosen Artikelauftrag oder die Bestellung eingegeben werden soll.

## <a name="accurate-rebate-calculations"></a>Genaue Rückvergütungsberechnungen

Die Kombination der zugehörigen Deals, der Häufigkeit der Berechnungen, der Berechnungsbasis und der ausgewählten Berechnungsmethode bestimmt die Genauigkeit und Präzision der Rückvergütungsberechnungen. Rückvergütungsrückstellungen können verwendet werden, um gebuchte und beanspruchte Werte zu erfassen.

Rückstellungen können täglich, wöchentlich, monatlich oder nach einer angepassten Periode verwaltet werden. Die Funktionalität kann jedoch den Rabatt in einem beliebigen definierten Rhythmus, der gleich lang oder länger als der Rückstellungsrhythmus ist, zuweisen oder auszahlen oder eine Zahlung davon erhalten. Die Abschreibung verwendet denselben Rhythmus wie der Rabatt. Benutzer können jederzeit während der Auszahlung problemlos einen Plan oder Zahlungsbetrag anpassen.

Benutzer müssen Deals oder Rückstellungen nicht mehr in zwei Schritten abwickeln. Rückstellungen und Abschreibungen werden direkt in das Hauptbuch gebucht. Zusätzlich können Gutschriften automatisch erstellt werden. Daher besteht eine vollständige Integration in die Kreditoren- und Debitorenkonten. Während der Verarbeitung können die Berechnungen Abrechnungsrabatte, bezahlte Rechnungen, Handelsrabatte und vorhandene Gutschriften berücksichtigen, um sicherzustellen, dass Beträge und Werte korrekt berechnet werden.

Wenn Rückvergütungen berechnet werden, erstellt der Prozess Transaktionen, die vor der Buchung überprüft werden können. Ein separater Prozess bucht Transaktionen der Bonusverwaltung. Bei der Buchung kann dann eine Erfassung, eine Gutschrift oder eine Lastschrifttransaktion für vorgeschlagene Transaktionen erstellt werden. Berichtserklärungen und Transaktionslisten können abgerufen werden, um Compliance, Effektivität und Transparenz sicherzustellen.

## <a name="guaranteed-royalty-payments"></a>Garantierte Lizenzgebührzahlungen

In der Rückvergütungsverwaltung ermöglicht die automatische Zahlungsgenerierung die schnelle und einfache Abwicklung von Lizenzgebühren, selbst wenn garantierte Mindestbeträge gelten.

## <a name="maximizing-spend-versus-rebates"></a>Maximierung der Ausgaben im Vergleich zu Rückvergütungen

Kreditoren und Produkte können nach Gebiet gruppiert werden, und je nach Land oder Region der Transaktion können unterschiedliche Angebote bereitgestellt werden. Wenn Benutzer Produkte auswählen, können sie die enthaltenen Artikel und die Anzahl der Artikel definieren, die für die Rückvergütungsabrechnung verwendet werden.
