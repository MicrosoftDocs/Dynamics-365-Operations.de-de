---
title: Einrichten von Steuercodes
description: In diesem Artikel wird erläutert, wie Sie Steuercodes im Steuerberechnungsdienst einrichten.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 1bc250716763ce9d8e25c8850c8a3676bf65fb0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862927"
---
# <a name="set-up-tax-codes"></a>Einrichten von Steuercodes

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Steuercodes im Steuerberechnungsdienst einrichten. Er enthält die Einrichtung für ein einfaches Szenario, damit der Steuercode funktioniert, und Informationen zu einigen erweiterten Steuercodefunktionen für komplexe Szenarien.

> [!IMPORTANT]
> Die Einrichtung von Steuercodes im Steuerberechnungsdienst ist unabhängig von juristischen Personen. Sie können diese Einrichtung im Regulatory Configuration Service (RCS) nur einmal abschließen. Steuercodes werden automatisch mit Microsoft Microsoft Dynamics 365 Finance synchronisiert, wenn Sie den Steuerberechnungsdienst für eine ausgewählte juristische Person in Finance aktivieren.

## <a name="simple-setup"></a>Einfache Einrichtung

Führen Sie diese Schritte aus, um einen Steuercode in einem einfachen Szenario zu verwenden, beispielsweise in einem Szenario, in dem es nur einen Steuersatz gibt.

1. Melden Sie sich beim [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) an.
2. Gehen Sie zu **Arbeitsbereiche** \> **Globalisierungsfunktionen** \> **Steuerberechnung**.
3. Wählen Sie die Funktion und Version aus, die Sie einrichten möchten, und wählen Sie **Bearbeiten**.
4. Wählen Sie auf der Registerkarte **Allgemein** die Option **Konfigurationsversion**.
5. Wählen Sie auf der **Steuercode**-Registerkarte **Hinzufügen** aus, und geben Sie den Steuercode und eine Beschreibung ein.
6. Wählen Sie **Berechnungsherkunft**. Die Berechnungsherkunft ist eine Gruppe von Methoden, die in der ausgewählten Version der Steuerkonfiguration definiert wurden. Wählen Sie für dieses einfache Szenario **Nach Nettobetrag**.
7. Wählen Sie **Speichern** aus. Je nach ausgewählter Berechnungsherkunft werden weitere Felder verfügbar.
8. Wählen Sie im Inforegister **Sätze** die Option **Hinzufügen** aus, um einen Steuersatz für diesen Steuercode hinzuzufügen.
9. Wählen Sie **Speichern** aus.

## <a name="calculation-origin"></a>Berechnungsursprung

Die Berechnungsherkunft legt fest, wie der Steuerbasisbetrag und der Steuerbetrag berechnet werden. Es wird nach Steuerkonfiguration im Arbeitsbereich **Elektronische Berichterstattung** konfiguriert. Die folgenden Werte stehen im Feld **Berechnungsherkunft** zur Verfügung:

- Nach Nettobetrag
- Nach Bruttobetrag
- Nach Menge
- Nach Marge
- Steuer auf Steuern

### <a name="by-net-amount"></a>Nach Nettobetrag

Wenn Sie **Nach Nettobetrag** im Feld **Berechnungsherkunft** auswählen, wird der Steuerbetrag als Prozentsatz der Einkaufs- oder Verkaufssumme ohne andere Steuercodes berechnet.

Der Steuersatz beträgt beispielsweise 25 Prozent, die Rechnungsposition zeigt eine Menge von 10 Artikeln zu je 1,00 und dem Kunden wird ein Positionsrabatt von 10 Prozent gewährt. Die Beträge werden hier folgendermaßen berechnet:

- **Nettobetrag:** (10 × 1,00) – 10 Prozent = 9,00 
- **Mehrwertsteuer:** 9,00 × 25 Prozent = 2,25 
- **Rechnungsgesamtbetrag:** 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Nach Bruttobetrag

Wenn Sie **Nach Bruttobetrag** im Feld **Berechnungsherkunft** auswählen, wird der Steuerbetrag als Prozentanteil der Bruttoverkaufssumme berechnet. Der Bruttobetrag ist der Positionsnettobetrag einschließlich aller Steuern und Gebühren für die Position mit Ausnahme der Steuer, wo das Feld **Berechnungsherkunft** auf **Nach Bruttobetrag** festgelegt ist.

Die Steuerbehörde sieht z. B. für einen Artikel die Zahlung spezieller Abgaben vor. Der Abgabenbetrag wird zum Nettobetrag hinzuaddiert, bevor die Steuer berechnet wird. Folgende Steuercodes werden verwendet:

- **Abgabe 1** – Der Satz beträgt 10 Prozent, und die Berechnungsmethode **Nach Nettobetrag** wird verwendet.
- **Abgabe 2** – Der Satz beträgt 20 Prozent, und die Berechnungsmethode **Nach Nettobetrag** wird verwendet.
- **Steuersatz** – Der Satz beträgt 25 Prozent, und die Berechnungsmethode **Nach Bruttobetrag** wird verwendet.

Wenn der Nettobetrag 10,00 ist, beträgt der Betrag von Abgabe 1 1,00 (10.00 × 10 Prozent) und der Betrag von Abgabe 2 2,00 (10.00 × 20 Prozent). Die Beträge werden hier folgendermaßen berechnet: 

- **Bruttobetrag:** Nettobetrag + Betrag Abgabe 1 + Betrag Abgabe 2 = 10,00 + 1,00 + 2,00 = 13,00 
- **Steuerbetrag:** 13,00 × 25 Prozent = 3,25 
- **Abgaben und Steuer gesamt:** 1,00 + 2,00 + 3,25 = 6,25 
- **Rechnungsgesamtbetrag:** 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Nach Menge

Wenn Sie **Nach Menge** im Feld **Berechnungsherkunft** auswählen, wird der Steuerbetrag als fester Betrag pro Einheit berechnet und mit der Menge multipliziert, die für die Dokumentposition eingegeben wurde. Der Betrag pro Einheit ist im Inforegister **Sätze** angegeben.

Der Steuercode ist beispielsweise auf 1,20 pro Einheit festgelegt. In einer Verkaufsrechnungsposition werden 25 Einheiten eines Artikels verkauft. In diesem Fall wird der Steuerbetrag als 25 × 1,20 = 30,00 berechnet.

### <a name="by-margin"></a>Nach Marge

Wenn Sie **Nach Marge** im Feld **Berechnungsherkunft** auswählen, wird der Steuerbetrag als Prozentanteil der Verkaufsspanne berechnet. Die Verkaufsspanne ist der Umsatzbetrag abzüglich des Einstandsbetrags. Diese Berechnungsmethode gilt nur für Verkaufstransaktionen.

Der Steuersatz beträgt beispielsweise 25 Prozent, die Rechnungsposition zeigt eine Menge von 10 Artikeln zu je 10,00 und die Gesamtkosten pro Artikel sind 6. Die Beträge werden hier folgendermaßen berechnet:

- **Verkaufsspanne** 10 × (10,00 – 6,00) = 40,00
- **Steuerbetrag:** 40,00 × 25 Prozent = 10,00
- **Rechnungsgesamtbetrag:** 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Steuer auf Steuern

Wenn Sie **Steuer auf Steuer** im Feld **Berechnungsherkunft** auswählen, wird die Mehrwertsteuer als Prozentsatz aller anderen Steuerbeträge in derselben Dokumentposition berechnet.

Folgende Steuercodes werden beispielsweise verwendet:

- **Abgabe 1** – Der Satz beträgt 10 Prozent, und die Berechnungsmethode **Nach Nettobetrag** wird verwendet.
- **Abgabe 2** – Der Satz beträgt 20 Prozent, und die Berechnungsmethode **Nach Nettobetrag** wird verwendet.
- **Steuer auf Abgabe** – Der Satz beträgt 25 Prozent, und die Berechnungsmethode **Steuer auf Steuer** wird verwendet.

Die Beträge werden hier folgendermaßen berechnet:

- **Nettobetrag:** 10,00 
- **Abgabe 1:** 10,00 × 10 Prozent = 1,00 
- **Abgabe 2:** 10,00 × 20 Prozent = 2,00 
- **Steuer auf Abgabe:** 3,00 × 25 Prozent = 0,75
- **Gesamtsteuer:** 1,00 + 2,00 + 0,75 = 3,75 
- **Rechnungsgesamtbetrag:** 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Erweiterte Funktionalität

In diesem Abschnitt werden einige erweiterte Funktionen der Steuercode-Einrichtung für komplexe Szenarien erläutert.

### <a name="tax-exemption"></a>Steuerbefreiung

Wenn Sie die Option **Ist befreit** im Inforegister **Allgemein** auf **Ja** setzen, wird der Steuerbetrag unabhängig vom tatsächlichen Steuersatz immer auf 0 (Null) überschrieben.

Sie können das Feld **Befreiungscode** festlegen, um den Grund für die Befreiung anzugeben. 

Sie können die Masterdatensuche für das Feld **Befreiungscode** aktivieren. Auf diese Weise können Sie unter den Befreiungscodewerten auswählen, die in Finance definiert sind. Informationen zum Aktivieren der Masterdatensuche finden Sie unter [Masterdatensuche für die Steuerberechnungskonfiguration aktivieren](tax-service-set-up-environment-master-data-lookup.md).

Der Steuersatz beträgt beispielsweise 25 Prozent, und die Option **Ist befreit** ist eingestellt auf **Ja** auf dem Steuercode. Unter der Rechnungsposition wird eine Menge von 10 Artikeln zu je 1,00 angezeigt, und der Debitor erhält einen Positionsrabatt von 10 Prozent. Die Beträge werden hier folgendermaßen berechnet:

- **Nettobetrag:** (10 × 1,00) – 10 Prozent = 9,00 
- **Mehrwertsteuer:** 0,00 
- **Rechnungsgesamtbetrag:** 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Erwerbsteuer (USA)

Wenn Sie die Option **Ist Verbrauchssteuer** im Inforegister **Allgemein** auf **Ja** festlegen, wird der Steuerbetrag auf das Konto **Gegenkonto Erwerbsteuerabgaben** statt **Kreditorsammlung** gebucht.

Der Steuersatz beträgt beispielsweise 25 Prozent, und die Option **Ist Verbrauchssteuer** ist eingestellt auf **Ja** auf dem Steuercode. Unter der Rechnungsposition wird eine Menge von 10 Artikeln zu je 1,00 angezeigt, und der Debitor erhält einen Positionsrabatt von 10 Prozent. Die Beträge werden hier folgendermaßen berechnet:

- **Nettobetrag:** (10 × 1,00) – 10 Prozent = 9,00 
- **Verbrauchssteuer :** 9,00 × 25 Prozent = 2,25
- **Rechnungsgesamtbetrag:** 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Wenn beides die Optionen **Ist befreit** und **Ist Verbrauchssteuer** auf einem Steuercode auf **Ja** eingestellt sind, wird der Code für Verkaufstransaktionen als steuerfrei und für Kauftransaktionen als Verbrauchssteuer anerkannt.

### <a name="reverse-charges"></a>Verlagerung der Steuerschuld

Wenn die Option **Ist Verlagerung der Steuerschuld** im Inforegister **Allgemein** auf **Ja** festgelegt ist, kann der Steuersatz als negativ konfiguriert werden. Für ein Steuerschuldumkehr-Szenario wird empfohlen, zwei Steuercodes einzurichten: eines mit positivem Steuersatz und das andere mit negativem Steuersatz. Beide Steuercodes sollten denselben Satzwert haben, und die Option **Ist Verlagerung der Steuerschuld** sollte auf **Ja** gesetzt werden auf dem Steuercode, der einen negativen Steuersatz hat. Weitere Informationen zur Steuerschuldumkehr-Lösung in Finance finden Sie unter [Mechanismus zur Verlagerung der Steuerschuld für USt./GST-Regelung](emea-reverse-charge.md).

Beispielsweise werden in einer Rechnungsposition zwei Steuercodes festgelegt. Ein Steuersatz beträgt 25 Prozent. Der andere Steuersatz beträgt ‑25 Prozent, und die Option **Ist Verlagerung der Steuerschuld** ist eingestellt auf **Ja** auf dem zweiten Steuercode. Die Rechnungsposition zeigt eine Menge von 10 Artikeln zu je 1,00. Die Beträge werden hier folgendermaßen berechnet:

- **Nettobetrag:** (10 × 1,00) = 10,00 
- **Steuercode 1:** 10,00 × 25 Prozent = 2,50
- **Steuercode 2:** 10 × ‑25 Prozent = ‑2,50
- **Rechnungsgesamtbetrag:** 10,00 + 2,50 ‑2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Ausschluss von Basisbetragsberechnungen

Wenn Sie die Option **Von der Basisbetragsberechnung ausschließen** Im Inforegister **Allgemein** auf **Ja** setzen, wird der berechnete Steuerbetrag des Steuercodes für andere Steuercodeberechnungen im Preis-Inklusive-Szenario vom Steuergrundlagenbetrag ausgeschlossen.

Weitere Informationen finden Sie unter [Steuer auf Preise berechnen, wenn die Option „Preise inkl. Steuer“ aktiviert ist](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Sätze

Im Inforegister **Satz** können Sie unterschiedliche Steuersätze für verschiedene Bereiche von Steuergrundlagebeträgen definieren. Zur Berechnung des Steuerbetrags verwendet der Steuerberechnungsdienst immer den Satz, der dem Steuergrundlagenbetrag entspricht.

Steuersätze können beispielsweise wie in der folgenden Tabelle gezeigt konfiguriert werden.

| Mindestbetrag | Höchstbetrag | Steuersatz   |
| -------------- | -------------- | ---------- |
| 0              | 1.000          | 10 Prozent |
| 1.000          | 5.000          | 15 Prozent |
| 5.000          | 10,000         | 20 Prozent |
| 10,000         | 0              | 30 Prozent |

Der Steuerbetrag wird hier folgendermaßen berechnet:

- Wenn der Steuergrundlagenbetrag 300,00 beträgt, beträgt der Steuersatz 10 Prozent und der Steuerbetrag ist 300,00 × 10 Prozent = 30,00.
- Wenn der Steuergrundlagenbetrag 3.000,00 beträgt, beträgt der Steuersatz 15 Prozent und der Steuerbetrag ist 3.000,00 × 15 Prozent = 450,00.
- Wenn der Steuergrundlagenbetrag 6.000,00 beträgt, beträgt der Steuersatz 20 Prozent und der Steuerbetrag ist 6.000,00 × 10 Prozent = 1.200,00.
- Wenn der Steuergrundlagenbetrag 20.000,00 beträgt, beträgt der Steuersatz 30 Prozent und der Steuerbetrag ist 20.000,00 × 30 Prozent = 6.000,00.

> [!NOTE]
> Wenn der Steuergrundlagenbetrag sowohl dem Höchstbetrag in einer Position als auch dem Mindestbetrag in der anderen Position entsprechen kann, verwendet die Basis den Steuersatz, der dem Mindestgrundbetrag entspricht. Wenn z. B. der Steuergrundlagenbetrag 1000,00 beträgt, beträgt der Steuersatz 15 Prozent und der Steuerbetrag ist 1.000,00 × 15 Prozent = 150,00.

### <a name="limits"></a>Begrenzungen

Im Inforegister **Grenzwerte** können Sie Steuergrenzen definieren, um den berechneten Steuerbetrag zu überschreiben, wenn der Steuerbetrag in den Mindest-/Höchstbereich fällt.

- Wenn der berechnete Steuerbetrag größer oder gleich dem maximalen Steuerbetrag ist, der im Inforegister **Grenzwerte** konfiguriert ist, entspricht der endgültige Steuerbetrag dem maximalen Steuerbetrag.
- Wenn der berechnete Steuerbetrag geringer ist als der Mindeststeuerbetrag, der im Inforegister **Grenzwerte** konfiguriert ist, ist der endgültige Steuerbetrag 0 (Null).

Die Steuergrenzen werden beispielsweise wie folgt konfiguriert:

- **Mindeststeuerbetrag:** 100 
- **Höchststeuerbetrag:** 1.000

Wenn der berechnete Steuerbetrag 2.000 beträgt, beträgt der endgültige Steuerbetrag 1.000.

Wenn der berechnete Steuerbetrag 500 beträgt, beträgt der endgültige Steuerbetrag 500.

Wenn der berechnete Steuerbetrag 80 beträgt, beträgt der endgültige Steuerbetrag 0 (Null).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
