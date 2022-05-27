---
title: Umsatzerlöszuteilung
description: In diesem Thema wird erklärt, wie Sie Umsatzerlöszuteilung in der Abonnementabrechnung verwenden.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 09d3e9295f1fb753156aa603b00372316173721e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695245"
---
# <a name="revenue-allocation"></a>Umsatzerlöszuteilung

In diesem Thema wird erklärt, wie Sie Parameter für die Umsatzerlöszuteilung für einen Abrechnungszeitplan einrichten. Sie können die Umsatzerlöszuteilung einrichten oder bearbeiten, wenn Sie den Abrechnungszeitplan erstellen. Beim Öffnen der Seite **Umsatzerlöszuteilung** für einen aktiven oder beendeten Abrechnungszeitplan sind die Felder schreibgeschützt.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Umsatzerlöszuteilung für einen Abrechnungszeitplan angeben

So geben Sie die Umsatzerlöszuteilung für einen Abrechnungszeitplan an.

1. Wählen Sie auf der Listenseite **Alle/Aktive Abrechnungspläne** einen Abrechnungszeitplan oder eine Abrechnungszeitplanposition aus.
2. Wählen Sie oben auf der Seite in der Registerkarte **Umsatzerlöszuteilung** die Option **Umsatzerlöszuteilung**.
3. Wählen Sie im Feld **Anordnungstyp für mehrere Elemente** die Art der Anordnung mehrerer Elemente (MEA) aus.
4. Geben Sie im Feld **Anordnungsnummer für mehrere Elemente** die MEA-Nummer an. Geben Sie dann im Feld **Konto für verzögerte Vertragsumsatzerlöse** das Konto für verzögerte Vertragsumsatzerlöse an.

    Wenn Sie das Feld **Anordnungstyp für mehrere Elemente** auf **Einzeln** festlegen, gelten dieselben Werte **Anordnungsnummer für mehrere Elemente** und **Konto für verzögerte Vertragsumsatzerlöse** für jede Position. Wenn Sie das Feld **Anordnungstyp für mehrere Elemente** auf **Mehrere** festlegen, können Sie verschiedene Werte **Anordnungsnummer für mehrere Elemente** und **Konto für verzögerte Vertragsumsatzerlöse** für jede Position angeben.
    
    Eine MEA-Nummer kann nur zwei oder mehr Artikeln zugeordnet werden. Eine einzelne Position kann keine eigene MEA-Nummer haben.

5. Wählen Sie **Speichern** aus.

### <a name="fields"></a>Felder

Die Seite **Anordnung für mehrere Elemente** enthält die folgenden Felder.

| Feld | Description |
|---|---| 
| Anordnungstyp für mehrere Elemente | <p>Wählen Sie den MEA-Typ für die Transaktion:</p><ul><li>**Mehrere** – Die Positionsartikel der Transaktion sind Teil der MEA oder es besteht mehr als eine Vereinbarung.</li><li>**Keiner** – Die Transaktion ist eine Standardtransaktion ohne Umsatzerlöszuteilung.</li><li>**Einzeln** – Alle Artikel der Transaktion sind Teil einer einzigen MEA.</li></ul> |
| Anordnungsnummer für mehrere Elemente | <p>Die MEA-Nummer für die Position. Dieses Feld ist nur verfügbar, wenn das Feld **Anordnungstyp für mehrere Elemente** auf **Mehrere** festgelegt ist.</p><p>Wenn dieses Feld leer ist und Sie eine MEA-Nummer zuweisen, werden die Felder **Ursprung des eigenständigen Artikelverkaufspreises** und **Eigenständiger Verkaufspreis** automatisch basierend auf den Werten der Seite **Eigenständiger Artikelverkaufspreis** aktualisiert. Es sind nur die MEA-Nummern verfügbar, die anderen Positionen im Auftrag zugeordnet sind.</p> |
| Konto für verzögerte Vertragsumsatzerlöse | Geben Sie das Konto an, das für Erfassungseinträge verwendet werden soll, wenn eine MEA-Vertragsrechnung erstellt wird. Dieses Feld ist nur verfügbar, wenn die wiederkehrende Vertragsabrechnung verwendet wird. |
| **Positionen** | |
| Variantennummer | Die Variantennummer des Auftrags. |
| Artikelnummer | Die Artikelnummer des Auftrags. |
| Abrechnungsfrequenz | Die Frequenz der Umsatzerlöszuteilung: **Täglich**, **Monatlich**, **Vierteljährlich**, **Halbjährlich** oder **Jährlich**. |
| Menge | Der Wert des Auftrags. |
| Vertragswert | Der Vertragswert. |
| Anordnungsnummer für mehrere Elemente | <p>Die MEA-Nummer für die Position. Dieses Feld ist nur verfügbar, wenn das Feld **Anordnungstyp für mehrere Elemente** auf **Mehrere** festgelegt ist.</p><p>Wenn dieses Feld leer ist und Sie eine MEA-Nummer zuweisen, werden die Felder **Ursprung des eigenständigen Artikelverkaufspreises** und **Eigenständiger Verkaufspreis** automatisch basierend auf den Werten der Seite **Eigenständiger Artikelverkaufspreis** aktualisiert. Es sind nur die MEA-Nummern verfügbar, die anderen Positionen im Auftrag zugeordnet sind. Wenn diese Werte nicht für den Artikel eingerichtet sind, werden die Werte der Seite **Parameter für die Umsatzerlöszuteilung für mehrere Elemente** verwendet.</p> | 
| Ursprung des eigenständigen Artikelverkaufspreises | <p>Der Ursprung des eigenständigen Verkaufspreises:</p><ul><li>**Betrag** – Der eigenständige Artikelverkaufspreis ist ein von Ihnen festgelegter Betrag, der größer als 0 (null) ist. Der Betrag wird nach Bedarf zwischen der funktionalen Währung und der Ursprungswährung umgerechnet.</li><li>**Basisverkaufspreis** – Der eigenständige Artikelverkaufspreis entspricht dem Basisverkaufspreis des Artikels.</li><li>**Rechnungspreis** – Der eigenständige Artikelverkaufspreis entspricht dem Rechnungspreis des Artikels.</li><li>**Prozent des Artikels** – Der eigenständige Artikelverkaufspreis wird als Prozentwert angegeben und errechnet sich aus dem Artikelpreis. Wenn diese Option ausgewählt ist, geben Sie den Standardprozentsatz ein.</li><li>**Restbetrag zuteilen** – Der Ursprung des eigenständigen Verkaufspreises wird wie folgt berechnet: *Gesamtvertragswert des übergeordneten Artikels* – *Eigenständiger Verkaufsgesamtpreis der untergeordneten Artikel*:</p><ul><li>Der *Gesamtvertragswert des übergeordneten Artikels* ist der Netto- oder fakturierte Betrag.</li><li>*Eigenständiger Verkaufsgesamtpreis der untergeordneten Artikel* ist die Summe des erweiterten oder vertraglichen eigenständigen Verkaufspreises aller untergeordneten Artikel, mit Ausnahme des untergeordneten Artikels, der diesen Ursprung des eigenständigen Artikelverkaufspreises verwendet.</li></ul><p>Wenn der berechnete Betrag ein negativer Wert ist, wird der Betrag auf 0 (null) gesetzt.</p><p>**Hinweis:** Diese Option kann nur für einen untergeordneten Artikel in der Umsatzerlösverteilung ausgewählt werden.</p></li><li>**Keine** – Der Ursprung des eigenständigen Verkaufspreises basiert auf den untergeordneten Artikeln. Diese Option gilt für Artikel, die in einer Umsatzerlösverteilungsvorlage als übergeordnete Artikel definiert sind. Wenn das Kontrollkästchen **Umsatzerlösverteilung** aktiviert ist, wird diese Option automatisch ausgewählt und die Einstellung kann nicht geändert werden.</li><li>**Prozent des übergeordneten Rechnungspreises** – Der Ursprung des eigenständigen Verkaufspreises ist ein Prozentsatz des Rechnungspreises des übergeordneten Artikels. Diese Option ist nur für untergeordnete Artikel in einer Umsatzerlösverteilungsvorlage verfügbar.</li><li>**Prozent des übergeordneten Standardpreises** – Der Ursprung des eigenständigen Verkaufspreises ist ein Prozentsatz des Standardpreises des übergeordneten Artikels. Diese Option ist nur für untergeordnete Artikel in einer Umsatzerlösverteilungsvorlage verfügbar. Wenn die Option für einen untergeordneten Artikel von **Prozent des übergeordneten Standardpreises** in **Prozent des übergeordneten Rechnungspreises** oder von **Prozent des übergeordneten Rechnungspreises** in **Prozent des übergeordneten Standardpreises** geändert wird, werden auch die berechneten Werte aktualisiert.</li></ul> |
| Eigenständiger Verkaufspreis | <p>Der eigenständige Verkaufspreis für die Position in der Transaktionswährung.</p><p>Der Wert im Feld **Betrag** wird entweder eingegeben oder berechnet.</p> |
| Eigenständiger Verkaufspreis für Vertrag | Der eigenständige Verkaufspreis für den Vertrag. |
| Restumsatzerlös des Vertrags | Der verbleibende Umsatzerlös für den Vertrag. Dieser Betrag ist die Summe aller Positionen, für die noch keine Rechnungen erstellt wurden. |
| Gesamter Vertragsumsatzerlös | Der Gesamtbetrag des Vertragsumsatzerlöses für die Position. Dieser Betrag ist die Summe aller Positionen, unabhängig davon, ob schon Rechnungen dafür erstellt wurden. |
| Konto für verzögerte Vertragsumsatzerlöse | <p>Geben Sie das Konto an, das für Erfassungseinträge verwendet werden soll, wenn eine MEA-Vertragsrechnung erstellt wird.</p><p>Dieses Feld ist nur verfügbar, wenn die wiederkehrende Vertragsabrechnung verwendet wird.</p> |
| Fehler | Alle Fehler, die bei der Umsatzerlöszuteilung aufgetreten sind. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Umsatzerlöszuteilung für einen Auftrag verwenden

Führen Sie die folgenden Schritte aus, um die Umsatzerlöszuteilungsfunktion für einen Auftrag zu verwenden.

1. Erstellen Sie auf der Seite **Alle Aufträge** einen Auftrag mit Artikeln.
2. Wählen Sie in der Registerkarte **Rechnung** unter **Umsatzerlöszuteilung** **Umsatzerlöszuteilung** aus.
3. Wählen Sie im Feld **Anordnungstyp für mehrere Elemente** den MEA-Typ aus.
4. Geben Sie im Feld **Anordnungsnummer für mehrere Elemente** die MEA-Nummer an.
5. Wenn das Feld **Anordnungstyp für mehrere Elemente** auf **Mehrere** eingestellt ist, wählen Sie die gewünschten Positionen aus, und wählen Sie dann **Für Auswahl anwenden** aus.
6. Wählen Sie **Speichern** aus.

Wenn Sie Umsatzerlös- und Ausgabenstundungen verwenden, wird der Stundungszeitplan automatisch erstellt. Sie können ihn auf der Seite **Alle Stundungszeitpläne** anzeigen.
