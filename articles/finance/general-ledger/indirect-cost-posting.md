---
title: Buchung indirekter Kosten
description: In diesem Artikel wird erläutert, wie Sie indirekte Kosten buchen, Kostengruppen erstellen und dem Nachkalkulationsschema Knoten für indirekte Kosten hinzufügen.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868430"
---
# <a name="indirect-cost-posting"></a>Buchung indirekter Kosten

Indirekte Kosten sind Kosten, die nicht direkt mit einer einzelnen Aktivität im Produktionsprozess zusammenhängen. Beispiele hierfür sind Verwaltungskosten wie Mitarbeitergehälter, Kosten der Buchhaltung und Gemeinkosten wie Miete, Nebenkosten und Maschinenkosten.

## <a name="calculating-indirect-costs"></a>Berechnung indirekter Kosten

Microsoft Dynamics 365 Finance bietet keine automatische Methode zur Berechnung des Satzes für indirekte Kosten. Sie müssen Ihre indirekten Kosten ermitteln, indirekte Kostencodes erstellen und den Satz für alle indirekten Kosten im Nachkalkulationsschema pflegen.

Der genaue Prozess, der zur Berechnung der indirekten Kosten verwendet wird, kann von Unternehmen zu Unternehmen leicht variieren. Im Allgemeine besteht der Prozess allerdings aus den folgenden grundlegenden Schritten:

1. Erstellen Sie eine Liste der indirekten Kosten, die in der Produktion anerkannt werden sollen. Diese Liste kann Miete, Verwaltungskosten, Buchhaltungsgebühren und Anwaltskosten enthalten. Sie sollte keine Rohstoffkosten oder Arbeitskosten enthalten, die in Produktionswegen anerkannt werden.
2. Summieren Sie alle indirekten Kosten. Sie können ähnliche Arten von indirekten Kosten gruppieren oder getrennt halten. Alle konfigurierten indirekten Kosten können unterschiedliche Hauptkonten haben, die für die Buchung im Hauptbuch verwendet werden.
3. Vergleichen Sie die indirekten Kosten mit einem Faktor, der auch als Absorptionsbasis bezeichnet wird. Der Faktor kann alles sein, was Sie wählen. Im Folgenden finden Sie einige allgemeine Beispiele hierfür:

    - Umsatzerlös
    - Gesamtmenge, die produziert wird
    - Rüstzeit
    - Bearbeitungszeit

    Sie können den Zeitraum auswählen, für den Sie Ihre indirekten Kosten berechnen möchten, z. B. monatlich, vierteljährlich oder jährlich. Die Summe Ihrer indirekten Kosten und die Summe Ihres Faktors sollten für die gleiche Zeitdauer gelten. Zur Berechnung des indirekten Kostensatzes wird folgende Formel verwendet:

    *Indirekter Kostensatz* = *Gesamte indirekte Kostenaufwendungen* &divide; *Gesamtfaktor*

4. Erstellen Sie indirekte Kostengruppen.
5. Konfigurieren Sie die Nachkalkulationstabelle mit Ihren Tarifen.
6. Pflegen Sie die Kosten für Ihre indirekten Kosten in der Nachkalkulationsversion.

> [!NOTE]
> Du kannst das **Kostenrechnung**-Modul verwenden, um Kosten zu kumulieren und Ihre Gemeinkosten aus verschiedenen Quellen wie Produktion, Projekten und dem Hauptbuch zu ermitteln. Weitere Informationen hierzu finden Sie unter [Kostenbuchhaltung](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Verschiedene Regulierungsbehörden haben Leitlinien zu den Kostenarten veröffentlicht, die als indirekte Kosten oder Gemeinkosten in die Kosten Ihrer Fertigerzeugnisse einbezogen werden können. Bevor Sie mit der Konfiguration der indirekten Kosten beginnen, empfehlen wir Ihnen, sich bei Ihrem Buchhalter und den örtlichen Vorschriften zu erkundigen, um sicherzustellen, dass Sie die Vorschriften einhalten.

## <a name="create-cost-groups-for-indirect-costs"></a>Kostengruppen für indirekte Kosten erstellen

Sie müssen mindestens eine Kostengruppe für indirekte Kosten erstellen. Die Anzahl der Kostengruppen, die Sie verwenden können, ist unbegrenzt. Überlegen Sie, wie Sie Ihre Kosten berechnen und ob es unterschiedliche Sätze für verschiedene Kostenarten gibt. Beispiel: Ihr Unternehmen stellt Lebensmittel her. Einige Rohstoffe und Fertigwaren sind Kurzwaren und haben indirekte Kosten für die Lagerung. Andere Rohstoffe und Fertigwaren werden gekühlt und haben höhere indirekte Kosten. In diesem Fall sollten Sie möglicherweise zwei Kostengruppen erstellen: **Gemeinkosten für trockenes Material** und **Gemeinkosten für gekühltes Material**.

Gehen Sie folgendermaßen vor, um eine Kostengruppe für indirekte Kosten anzulegen.

1. Wechseln Sie zu **Produktionssteuerung &gt; Einrichten &gt; Arbeitspläne &gt; Kostengruppen**.
2. Wählen Sie **Neu** aus, um eine Gruppe zu erstellen.
3. Geben Sie im Feld **Kostengruppe** einen eindeutigen Namen für die Kostengruppe ein, z. B. **MATOVH**.
4. Geben Sie im Feld **Name** eine Beschreibung der Kostengruppe ein, z. B. **Gemeinkosten für Material**.
5. Wählen Sie im Feld **Kostengruppentyp** die Option **Indirekt** aus.
6. Optional: Wählen Sie im **Verhalten**-Feld **Fixkosten** oder **Variable Kosten** aus.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Das Nachkalkulationsschema für indirekte Kosten konfigurieren

Nachdem Sie eine oder mehrere Kostengruppen erstellt haben, können Sie Ihr Nachkalkulationsschema mit indirekten Kosten konfigurieren und Ihre Kalkulation definieren. Möglicherweise möchten Sie indirekte Kosten im Kalkulationsschema gruppieren. Um indirekte Kosten zu gruppieren, können Sie im Kalkulationsschema eine optionale Kopfzeile anlegen. Im Nachkalkulationsschema müssen Sie für jede Kostengruppe mindestens einen Knoten anlegen. Für jede Kostengruppe für indirekte Kosten können Sie eine weitere indirekte Kostenberechnung hinzufügen.

### <a name="indirect-cost-node-types"></a>Knotentypen für indirekte Kosten

In diesem Abschnitt werden die verschiedenen Arten von Knoten für indirekte Kosten beschrieben.

#### <a name="surcharge"></a>Zuschlag

**Aufpreis** ist eine der häufigsten Arten indirekter Kosten. Sie berechnet einen Prozentsatz der Kosten aus einer Absorptionsbasis der Kosten des Produktionsauftrags. Sie definieren die Absorptionsbasis, indem Sie im Nachkalkulationsschema die Kostengruppen auswählen, die mit Ihren Material- oder Zeitkomponenten verknüpft sind.

Beispielsweise kann für alle Rohstoffe eines Produktionsauftrags ein Aufpreis von 3 Prozent auf die Produktionskosten erhoben werden.

#### <a name="rate"></a>Satz

Die indirekten Kosten des **Rate**-Typs werden verwendet, um dem Produktionsauftrag einen festen Kostenbetrag aus einer Kostenübernahmebasis des Produktionsauftrags hinzuzufügen. Die Rate kann auf einem von drei Untertypen basieren:

- **Prozess** – die Rate richtet sich nach der Laufzeit im Arbeitsplan.
- **Einrichtung** – die Rate richtet sich nach der Einrichtungszeit im Arbeitsplan.
- **Menge** – die Rate richtet sich nach der produzierten Menge.

Sie definieren die Absorptionsbasis, indem Sie im Nachkalkulationsschema die Kostengruppen auswählen, die mit den Material- oder Zeitkomponenten verknüpft sind.

Beispielsweise wird jedem Produktionsauftrag ein fester Betrag von 2,00 US-Dollar (USD) hinzugefügt, basierend auf der Laufzeit im Arbeitsplan für die Lohnkostengruppe in Ihrem Nachkalkulationsschema.

#### <a name="output-unit-based"></a>Ausgabeeinheitenbasiert

Die indirekten Kosten des **Ausgabeeinheitenbasiert**-Typs werden berechnet, indem durch der Betrag, der auf dem **Rate**-Inforegister des Kalkulationsschemas angegeben ist mit dem ausgewählten Untertyp multipliziert wird. Als Multiplikator für die indirekten Kosten können Sie die Menge, das Gewicht oder das Volumen des Fertigprodukts auswählen.

Beispielsweise verwenden Sie die Menge, um 1,50 USD der Maschinenabschreibung für jede produzierte Menge zu berechnen. Als weiteres Beispiel verwenden Sie das Volumen, um 2,00 USD der Kühlkosten für das Raumvolumen zu berechnen, das die fertigen Waren in Ihren Kühleinheiten einnehmen.

#### <a name="input-unit-based"></a>Eingabeeinheitenbasiert

Die indirekten Kosten des **Eingabeeinheitsbasiert**-Typs werden berechnet, indem die Menge an Rohstoffen, die für einen Produktionsauftrag verbraucht wird, mit einer Menge multipliziert wird. Sie können das Gewicht oder das Volumen der Eingabe auf dem Produktionsauftrag verwenden, um die Gesamtsumme zu berechnen. Sie können die Berechnung auf eine Teilmenge von Materialien beschränken, indem Sie eine oder mehrere Kostengruppen auf dem Inforegister **Absorptionsbasis** des Nachkalkulationsschemas auswählen.

Beispielsweise verwenden Sie das Volumen der Eingabe für eine bestimmte Kostengruppe, die mit gekühlten Produkten verknüpft ist, um 1,00 USD zum Produktionsauftrag hinzuzufügen.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Im Nachkalkulationsschema einen Summenknoten für indirekte Kosten erstellen

Um im Nachkalkulationsschema einen Summenknoten für indirekte Kosten zu erstellen, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Kostenverwaltung &gt; Einrichtung der Buchhaltungsrichtlinien für indirekte Kosten &gt; Nachkalkulationsbogen**.
2. Wählen Sie in der Baumstruktur einen Knoten aus, der die Herstellungskosten darstellt.
3. Wählen Sie **Neu** aus, um einen Knoten zu erstellen.
4. Wählen Sie im Feld **Knotentyp auswählen** die Option **Gesamt**.
5. In dem **Code**-Feld geben Sie eine eindeutige ID für den Knoten ein, z. B. **Produktionsgemeinkosten**.
6. Aktivieren Sie das **Kopfzeile**-Kontrollkästchen.
7. Aktivieren Sie das **Gesamt**-Kontrollkästchen.
8. Wählen Sie **OK** aus.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Im Nachkalkulationsschema einen Gruppenknoten für indirekte Kosten erstellen

Um im Nachkalkulationsschema einen Gruppenknoten für indirekte Kosten zu erstellen, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Kostenverwaltung &gt; Einrichtung der Buchhaltungsrichtlinien für indirekte Kosten &gt; Nachkalkulationsbogen**.
2. Wählen Sie in der Baumstruktur den Knoten aus, unter dem Sie die indirekten Kosten erstellen möchten. Wählen Sie beispielsweise den Gesamtknoten für **Produktionsgemeinkosten** aus.
3. Wählen Sie **Neu** aus, um einen Knoten zu erstellen.
4. Wählen Sie im Feld **Knotentyp auswählen** die Option **Kostengruppe** aus.
5. In dem **Code**-Feld geben Sie eine eindeutige ID für den Knoten ein, z. B. **TRANSP**.
6. Geben Sie im Feld **Beschreibung** eine kurze Beschreibung ein, wie beispielsweise **Transportgemeinkosten**.
7. Wählen Sie **OK** aus.
8. Wählen Sie im Feld **Kostengruppe** die Kostengruppe aus, z. B. **OVH1: Transportgemeinkosten**.

### <a name="create-a-surcharge-indirect-cost"></a>Einen Aufpreis für indirekte Kosten erstellen

Um in Ihrem Nachkalkulationsschema einen Aufpreis für indirekte Kosten zu erstellen, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Kostenverwaltung &gt; Einrichtung der Buchhaltungsrichtlinien für indirekte Kosten &gt; Nachkalkulationsbogen**.
2. Wählen Sie in der Baumstruktur den Knoten für indirekte Kostengruppe aus, unter dem Sie die indirekten Kosten erstellen möchten. Wählen Sie beispielsweise den Gesamtknoten für **TRANSP - Transportgemeinkosten** aus.
3. Wählen Sie **Neu** aus, um einen Knoten zu erstellen.
4. Wählen Sie im Feld **Knotentyp auswählen** die Option **Aufpreis**.
5. In dem **Code**-Feld geben Sie eine eindeutige ID für den Knoten ein, z. B. **Transportaufpreis**.
6. Wählen Sie **OK** aus.
7. Wählen Sie im Feld **Untertyp** **Gesamt** aus.
8. Wählen Sie im Inforegister **Absorptionsbasis** die Option **Neu** aus, um einen Kostencode zu erstellen.
9. Wählen Sie im Feld **Code** eine Kostengruppe aus, die zur Berechnung des Aufpreises verwendet werden soll.
10. Optional: Wiederholen Sie die Schritte 8 bis 9 für jede zusätzliche Kostengruppe, die Sie für die Berechnung verwenden möchten.
11. Klicken Sie im Inforegister **Aufpreis** auf **Neu**, um eine Rate zu erstellen.
12. In dem **Version**-Feld wählen Sie die Nachkalkulationsversion aus, zu der der Aufpreis hinzugefügt werden soll.
13. Optional: Geben Sie im Feld **Site** eine Site ein, auf die der Aufpreis erhoben werden soll.
14. Geben Sie im Feld **Prozent** den Prozentsatz ein, der für Produktionsaufträge aus den Kostengruppen berechnet werden soll, die im **Absorptionsbasis**-Inforegister definiert sind.
15. Wählen Sie im Inforegister **Hauptbuchbuchungen** das Hauptkonto aus, das für die Felder **Geschätzte absorbierte indirekte Kosten**, **Geschätzte Kosten der verbrauchten indirekten Kosten, WIP**, **Absorbierte, indirekte Kosten** und **Kosten der verbrauchten indirekten Kosten, WIP** verwendet werden soll.
16. Optional: geben Sie im **Finanzdimensionen**-Inforegister alle Finanzdimensionen an, die standardmäßig für Buchungen eingegeben werden sollen, wenn sie in das Hauptbuch gebucht werden.

Das vorstehende Verfahren zeigt, wie indirekte Kosten des **Aufpreis**-Typs erstellt werden. Ähnliche Schritte werden verwendet, um andere Arten von indirekten Kosten zu erstellen. In den folgenden Abschnitten werden die Unterschiede für jeden Typ beschrieben.

#### <a name="rate"></a>Satz

- Wählen Sie in Schritt 4 **Rate** statt **Aufpreis** aus.
- Wählen Sie in Schritt 7 **Prozess**, **Einrichtung** oder **Menge** statt **Gesamt**.
- Verwenden Sie in Schritt 11 das Inforegister **Rate** statt des Inforegisters **Aufpreis** .
- Geben Sie in Schritt 14 einen Betrag in das Feld **Menge** ein, stelle einen Prozentsatz in das Feld **Prozent** einzugeben.

#### <a name="output-unit-based"></a>Ausgabeeinheitenbasiert

- Wählen Sie in Schritt 4 **Ausgabeeinheitsbasiert** statt **Aufpreis** aus.
- Wählen Sie in Schritt 7 **Menge**, **Gewicht** oder **Volumen** statt **Gesamt**.
- Überspringen Sie die Schritte 8 bis 10.
- Verwenden Sie in Schritt 11 das Inforegister **Rate** statt des Inforegisters **Aufpreis** .

#### <a name="input-unit-based"></a>Eingabeeinheitenbasiert

- Wählen Sie in Schritt 4 **Eingabeeinheitsbasiert** statt **Aufpreis** aus.
- Wählen Sie in Schritt 7 **Gewicht** oder **Volumen** statt **Gesamt**.
- Verwenden Sie in Schritt 11 das Inforegister **Rate** statt des Inforegisters **Aufpreis** .
