---
title: Umsatzerlöszuteilung für mehrere Elemente einrichten
description: In diesem Thema wird beschrieben, wie Sie die Parameter für die Umsatzerlöszuteilung für mehrere Elemente in der Abonnementabrechnung einrichten.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e422b16d1c4505b2837bb282918ecada902b806e
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566360"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Umsatzerlöszuteilung für mehrere Elemente einrichten

Mit der Umsatzerlöszuteilung für mehrere Elemente können Sie verschiedene Vorlagen einrichten, die zum Berechnen und Zuweisen von Umsatzerlösen über mehrere Elemente hinweg verwendet werden. Diese Funktion kann Ihnen dabei helfen, Vorschriften wie Accounting Standards Codification Topic 606 (ASC 606) und/oder International Financial Reporting Standard 15 (IFRS 15) einzuhalten.

## <a name="multiple-element-revenue-allocation-parameters"></a>Parameter für die Umsatzerlöszuteilung für mehrere Elemente

Verwenden Sie die Seite **Parameter für die Umsatzerlöszuteilung für mehrere Elemente**, um die Parameter für die Umsatzerlöszuteilung für mehrere Elemente einzurichten.

### <a name="standalone-selling-price-origin"></a>Ursprung des eigenständigen Artikelverkaufspreises

Das Feld **Ursprung des eigenständigen Artikelverkaufspreises** bestimmt, woher der eigenständige Artikelverkaufspreis stammt. Sie können den Wert auf der Seite **Eigenständiger Artikelverkaufspreis** und in der Transaktion aktualisieren. Die folgenden Optionen sind verfügbar.

| Option | Description |
|--------|-------------|
| Betrag | Der eigenständige Artikelverkaufspreis ist ein von Ihnen festgelegter Betrag, der größer als 0 (null) ist. Der Betrag wird nach Bedarf zwischen der funktionalen Währung und der Ursprungswährung umgerechnet. |
| Basisverkaufspreis | Der eigenständige Artikelverkaufspreis entspricht dem Basisverkaufspreis des Artikels. |
| Rechnungspreis | Der eigenständige Artikelverkaufspreis entspricht dem Rechnungspreis des Artikels. |
| Prozent des Artikels | Der eigenständige Artikelverkaufspreis wird als Prozentwert angegeben und errechnet sich aus dem Artikelpreis. Wenn Sie diese Option auswählen, geben Sie den Standardprozentsatz ein. |
| Restbetrag zuteilen | <p>Der Ursprung des eigenständigen Verkaufspreises wird wie folgt berechnet: *Gesamtvertragswert des übergeordneten Artikels* – *Eigenständiger Verkaufsgesamtpreis der untergeordneten Artikel*:</p><ul><li>Der *Gesamtvertragswert des übergeordneten Artikels* ist der Netto- oder fakturierte Betrag.</li><li>*Eigenständiger Verkaufsgesamtpreis der untergeordneten Artikel* ist die Summe des erweiterten oder vertraglichen eigenständigen Verkaufspreises aller untergeordneten Artikel, mit Ausnahme des untergeordneten Artikels, der diesen Ursprung des eigenständigen Artikelverkaufspreises verwendet.</li></ul><p>Wenn der berechnete Betrag ein negativer Wert ist, wird der Betrag auf 0 (null) gesetzt.</p><p>**Hinweis:** Diese Option kann nur für einen untergeordneten Artikel in der Umsatzerlösverteilung ausgewählt werden.</p> |
| Kein | Der Ursprung des eigenständigen Verkaufspreises basiert auf den untergeordneten Artikeln. Diese Option gilt für Artikel, die in einer Umsatzerlösverteilungsvorlage als übergeordnete Artikel definiert sind. Wenn das Kontrollkästchen **Umsatzerlösverteilung** aktiviert ist, wird diese Option automatisch ausgewählt und die Einstellung kann nicht geändert werden. |
| Prozent des übergeordneten Rechnungspreises | Der Ursprung des eigenständigen Verkaufspreises ist ein Prozentsatz des Rechnungspreises des übergeordneten Artikels. Sie können den Standardwert ändern. Diese Option ist nur für untergeordnete Artikel in einer Umsatzerlösverteilungsvorlage verfügbar. |
| Prozent des übergeordneten Standardpreises | Der Ursprung des eigenständigen Verkaufspreises ist ein Prozentsatz des Standardpreises des übergeordneten Artikels. Sie können den Standardwert ändern. Diese Option ist nur für untergeordnete Artikel in einer Umsatzerlösverteilungsvorlage verfügbar. Dies ist die Standardoption für untergeordnete Artikel. Wenn die Option für einen untergeordneten Artikel von **Prozent des übergeordneten Standardpreises** in **Prozent des übergeordneten Rechnungspreises** oder von **Prozent des übergeordneten Rechnungspreises** in **Prozent des übergeordneten Standardpreises** geändert wird, werden auch die berechneten Werte aktualisiert. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Konto für Rundungsdifferenzen bei der Umsatzerlöszuteilung

Das Feld **Konto für Rundungsdifferenzen bei der Umsatzerlöszuteilung** gibt das Konto an, das verwendet wird, um alle Rundungsanpassungen an einem Vertragsumsatzerlös zu erfassen. Es ist verfügbar, wenn die wiederkehrende Vertragsabrechnung verwendet wird.

## <a name="item-standalone-selling-price"></a>Eigenständiger Artikelverkaufspreis

Verwenden Sie die Seite **Eigenständiger Artikelverkaufspreis**, um die Herkunft und den eigenständigen Verkaufspreis eines Artikels anzugeben. Die auf dieser Seite angegebenen Werte werden als Standardwerte auf der Seite **Umsatzerlöszuteilung** in der Umsatzerlöszuteilung für mehrere Elemente und in der wiederkehrenden Vertragsabrechnung verwendet.

### <a name="specify-item-standalone-selling-price"></a>Eigenständigen Artikelverkaufspreis angeben

Gehen Sie wie folgt vor, um den eigenständigen Preis für einen Artikel anzugeben.

1. Wählen Sie auf der Seite **Eigenständiger Artikelverkaufspreis** im Feld **Ursprung des eigenständigen Artikelverkaufspreises** den Ursprung des eigenständigen Artikelverkaufspreises aus.
2. Führen Sie einen dieser Schritte aus, je nach dem Wert, den Sie im Feld **Ursprung des eigenständigen Artikelverkaufspreises** ausgewählt haben:

    * Wenn Sie **Prozent des Artikels** ausgewählt haben, geben Sie den Prozentsatz im Feld **Prozent** an.
    * Wenn Sie **Betrag** ausgewählt haben, geben Sie den Betrag im Feld **Eigenständiger Verkaufspreis** an.

2. Wählen Sie für alle Artikel, die Sie der Liste hinzufügen möchten, **Hinzufügen** aus.
3. Wählen Sie im Feld **Artikelcode** den Artikelcode aus. Wählen Sie im Feld **Artikelrelation** die Artikelrelation aus. Für Artikel, für die das Kontrollkästchen **Umsatzerlösverteilung** deaktiviert ist, muss die ausgewählte Kombination aus Artikelcode und Artikelrelation eindeutig sein.
4. Ändern Sie den Standardwert des Felds **Ursprung des eigenständigen Artikelverkaufspreises**, **Eigenständiger Verkaufspreis** oder **Prozent** nach Bedarf.
5. Wählen Sie für alle übergeordneten Artikel, die Sie der Liste hinzufügen möchten, **Hinzufügen** aus.
6. Wählen Sie im Feld **Artikelcode** den Artikelcode aus. Wählen Sie im Feld **Artikelrelation** die Artikelrelation aus.
7. Aktivieren Sie das Kontrollkästchen **Umsatzerlösverteilung**.
8. Wählen Sie im Feld **Artikelrelation** die Artikelrelation aus. Die Liste wird mit dem übergeordneten Artikel und allen untergeordneten Artikeln aktualisiert.
9. Ändern Sie für den untergeordneten Artikel den Standardwert des Felds **Ursprung des eigenständigen Artikelverkaufspreises**, **Prozent des übergeordneten Standardpreises**, **Prozent des übergeordneten Rechnungspreises** oder **Restbetrag zuteilen** je nach Bedarf.
10. Um mehrere Artikel gleichzeitig hinzuzufügen, wählen Sie **Artikel hinzufügen** aus.
11. Aktualisieren Sie die Abfrage so, dass der Bereich von Artikeln ausgewählt wird, die Sie hinzufügen möchten.
12. Wählen Sie **OK**, überprüfen Sie die Liste der hinzugefügten Artikel, und wählen Sie dann **OK** aus.

### <a name="fields"></a>Felder

Die Seite **Eigenständiger Artikelverkaufspreis** enthält die folgenden Felder.

| Feld | Description |
|-------|-------------|
| Ursprung des eigenständigen Artikelverkaufspreises | <p>Wählen Sie den Ursprung des eigenständigen Verkaufspreises aus:</p><ul><li>**Betrag** – Der eigenständige Artikelverkaufspreis ist ein von Ihnen festgelegter Betrag, der größer als 0 (null) ist. Der Betrag wird nach Bedarf zwischen der funktionalen Währung und der Ursprungswährung umgerechnet.</li><li>**Basisverkaufspreis** – Der eigenständige Artikelverkaufspreis entspricht dem Basisverkaufspreis des Artikels.</li><li>**Rechnungspreis** – Der eigenständige Artikelverkaufspreis entspricht dem Rechnungspreis des Artikels.</li><li>**Prozent des Artikels** – Der eigenständige Artikelverkaufspreis wird als Prozentwert angegeben und errechnet sich aus dem Artikelpreis. Wenn Sie diese Option auswählen, geben Sie den Standardprozentsatz ein.</li></ul>**Restbetrag zuteilen** – Der Ursprung des eigenständigen Verkaufspreises wird wie folgt berechnet: *Gesamtvertragswert des übergeordneten Artikels* – *Eigenständiger Verkaufsgesamtpreis der untergeordneten Artikel*:</p><ul><li>Der *Gesamtvertragswert des übergeordneten Artikels* ist der Netto- oder fakturierte Betrag.</li><li>*Eigenständiger Verkaufsgesamtpreis der untergeordneten Artikel* ist die Summe des erweiterten oder vertraglichen eigenständigen Verkaufspreises aller untergeordneten Artikel, mit Ausnahme des untergeordneten Artikels, der diesen Ursprung des eigenständigen Artikelverkaufspreises verwendet.</li></ul><p>Wenn der berechnete Betrag ein negativer Wert ist, wird der Betrag auf 0 (null) gesetzt.</p><p>**Hinweis:** Diese Option kann nur für einen untergeordneten Artikel in der Umsatzerlösverteilung ausgewählt werden.</p></li><li>**Keine** – Der Ursprung des eigenständigen Verkaufspreises basiert auf den untergeordneten Artikeln. Diese Option gilt für Artikel, die in einer Umsatzerlösverteilungsvorlage als übergeordnete Artikel definiert sind. Wenn das Kontrollkästchen **Umsatzerlösverteilung** aktiviert ist, wird diese Option automatisch ausgewählt und die Einstellung kann nicht geändert werden.</li><li>**Prozent des übergeordneten Rechnungspreises** – Der Ursprung des eigenständigen Verkaufspreises ist ein Prozentsatz des Rechnungspreises des übergeordneten Artikels. Sie können den Standardwert ändern. Diese Option ist nur für untergeordnete Artikel in einer Umsatzerlösverteilungsvorlage verfügbar.</li><li>**Prozent des übergeordneten Standardpreises** – Der Ursprung des eigenständigen Verkaufspreises ist ein Prozentsatz des Standardpreises des übergeordneten Artikels. Sie können den Standardwert ändern. Diese Option ist nur für untergeordnete Artikel in einer Umsatzerlösverteilungsvorlage verfügbar. Dies ist die Standardoption für untergeordnete Artikel. Wenn die Option für einen untergeordneten Artikel von **Prozent des übergeordneten Standardpreises** in **Prozent des übergeordneten Rechnungspreises** oder von **Prozent des übergeordneten Rechnungspreises** in **Prozent des übergeordneten Standardpreises** geändert wird, werden auch die berechneten Werte aktualisiert.</li></ul> |
| Eigenständiger Verkaufspreis | Geben Sie den eigenständigen Verkaufspreis des Artikels an. Dieses Feld ist verfügbar, wenn das Feld **Ursprung des eigenständigen Artikelverkaufspreises** auf **Betrag** festgelegt ist. |
| Prozent | Geben Sie den Prozentsatz des eigenständigen Verkaufspreises an. Dieses Feld ist verfügbar, wenn das Feld **Ursprung des eigenständigen Artikelverkaufspreises** auf **Prozent des Artikels**, **Prozent des übergeordneten Rechnungspreises** oder **Prozent des übergeordneten Standardpreises** festgelegt ist. |
| Umsatzerlösverteilung | <p>Geben Sie an, ob eine Position die Umsatzerlösverteilung verwendet:</p><ul><li>**Aktiviert** – Im Feld **Artikelrelation** können nur Artikel ausgewählt werden, für die eine Umsatzerlösverteilungsvorlage eingerichtet ist. Sie können dieses Kontrollkästchen nur für übergeordnete Artikel einer Umsatzerlösverteilungsvorlage aktivieren.</li><li>**Deaktiviert** – Der Artikel ist ein Standardartikel, der keine Umsatzerlösverteilung verwendet.</li></ul> |
| Beziehung | Ein Symbol gibt an, ob es sich bei dem Artikel um einen übergeordneten oder untergeordneten Artikel in einer Umsatzerlösverteilung handelt. |
| Artikelcode | <p>Wählen Sie den Artikelcode aus: **Tabelle** oder **Gruppe**.</p><p>Wenn das Kontrollkästchen **Umsatzerlösverteilung** aktiviert ist, ist dieses Feld auf **Tabelle** eingestellt und der Wert kann nicht geändert werden.</p> |
| Artikelrelation | <p>Wählen Sie eine Artikelnummer aus.</p><p>Wenn das Kontrollkästchen **Umsatzerlösverteilung** aktiviert ist, stehen nur Artikel zur Auswahl, die übergeordnete Artikel sind, für die eine Umsatzerlösverteilungsvorlage eingerichtet ist. Wenn der übergeordnete Artikel ausgewählt wird, wird die Liste automatisch mit den untergeordneten Artikeln dieses übergeordneten Artikels aktualisiert.</p> |
| Übergeordneter Artikel | Für den übergeordneten Artikel zeigt dieses Feld die Artikelnummer an. Für untergeordnete Artikel in einer Umsatzerlösverteilung wird die Artikelnummer des übergeordneten Artikels angezeigt. |

## <a name="mea-templates"></a>MEA-Vorlagen

Verwenden Sie die Seite **MEA-Vorlagen** zum Erstellen und Bearbeiten von MEA-Vorlagen-IDs (Multiple Element Arrangement). Diese IDs werden auf der Seite **Umsatzerlöszuteilung** verwendet, um Elemente zu gruppieren.

### <a name="create-a-template"></a>Vorlage erstellen

Gehen Sie zum Einrichten einer MEA-Vorlage folgendermaßen vor.

1. Wählen Sie auf der Seite **MEA-Vorlagen** die Option **Neu** aus.
1. Geben Sie im Feld **MEA-Vorlagenkennung** eine eindeutige ID ein.
1. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
1. Wählen Sie im Feld **Konto für verzögerte Vertragsumsatzerlöse** das Konto aus, das Sie für Erfassungseinträge verwenden möchten, wenn eine MEA-Vertragsrechnung erstellt wird. Dieses Feld ist verfügbar, wenn die wiederkehrende Vertragsabrechnung aktiviert ist und verwendet wird.
1. Wählen Sie **Speichern** aus.
