---
title: Ausgabenverwaltung konfigurieren
description: Dieser Artikel beschreibt die Überlegungen und Entscheidungen, die Sie während des Planungsprozesses machen müssen, bevor Sie die Ausgabenverwaltung in Microsoft Dynamics 365 for Finance and Operations konfigurieren.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac9959a4ee66e52ead5050897403602e407ca10
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570620"
---
# <a name="configure-expense-management"></a>Ausgabenverwaltung konfigurieren

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt die Überlegungen und Entscheidungen, die Sie während des Planungsprozesses machen müssen, bevor Sie die Ausgabenverwaltung in Microsoft Dynamics 365 for Finance and Operations konfigurieren. Im Spesenverwaltungsbereich können Sie unter anderem Informationen zu Zahlungsmethoden, Reiseanforderungen, Spesenabrechnungen und Richtlinien speichern.

Da viele der Entscheidungen, die Sie treffen, wenn Sie die Konfiguration für Spesenverwaltung planen, auf der Hierarchie und die Finanzstruktur der Organisation basieren, müssen Sie die Planungsdokumente für diese Bereiche mit einbeziehen.

## <a name="intercompany-expenses"></a>Intercompany-Ausgaben

Wenn Sie Intercompany-Ausgaben aktivieren, gestatten Sie juristischen Personen und Mitarbeitern im Auftrag einer anderen juristischen Person innerhalb der Organisation Zahlungen einzuziehen und Ausgaben zu tätigen. Beispielsweise beendet ein Mitarbeiter in juristischer Person A ein Projekt für juristische Person B und für das Projekt entstandenen Reisespesen im Zusammenhang mit dem Auftrag. Wenn die Intercompany-Ausgaben aktiviert sind, kann der Mitarbeiter einen Arbeitszeitnachweis für die juristische Person B erstellen und wird durch diese bezahlt. Wenn Ihre Organisation nicht mehrere juristische Personen enthält, müssen Sie die Intercompany-Ausgaben nicht aktivieren.

**Entscheidung:** Möchten Sie Intercompany-Ausgaben aktivieren?

## <a name="financial-management"></a>Finanzverwaltung

Die Ausgabenverwaltung ist eng mit der Finanzverwaltung der Organisation verbunden. Ein Großteil der Konfiguration für die Ausgabenverwaltung basiert auf den Entscheidungen, die Sie bezüglich der Finanzen der Organisation getroffen haben. In den folgenden Abschnitten werden die verschiedenen Bereiche beschrieben, deren Planung und Entscheidungen auf Grundlage der Finanzentscheidungen der Organisation und der Anleitung Ihres Führungsteams basieren.

### <a name="per-diems"></a>Tagessätze

Sie müssen die Mitarbeitertagessätze definieren, die Ihre Organisation bereitstellt. Da Tagessätze in der Regel verwendet werden, um Ausgaben wie Mahlzeiten, Unterkunft und andere Nebenkosten abzudecken, können Sie Regeln für die täglichen Vergütungen erstellen, die Ihre Organisation anbietet. Tagessätze können abhängig von der Jahreszeit, dem Reiseziel oder in Abhängigkeit von beidem festgelegt werden. Beim Definieren einer Tagessatzregel können Sie angeben, dass ein prozentualer Anteil des Tagessatzes einbehalten werden soll, wenn eine Arbeitskraft kostenfreie Verpflegung oder andere Leistungen erhält. Darüber hinaus können Sie einen Tagessatz (Ebenen) für die Reise einer Arbeitskraft festlegen, um eine Mindest- und eine Höchstanzahl von Stunden zu bestimmen.

**Entscheidung:**

- Standard-Tagessatzregeln für den ersten und letzten Tag:

    - Was ist die Mindeststundenzahl, die ein Mitarbeiter für einen Tag beanspruchen kann, um noch den Tagessatz zu erhalten?
    - Gibt es eine Verringerung des Betrags, der für Mahlzeiten für den ersten und letzten Tag angeboten wird? Wenn eine Reduktion erfolgt, welches ist der Prozentsatz der Reduktion?
    - Gibt es eine Reduktion des Betrags, der für ein Hotel für den ersten und letzten Tag angeboten wird? Wenn eine Reduktion erfolgt, welches ist der Prozentsatz der Reduktion?
    - Gibt es eine  Reduktion des Betrags, der für andere Ausgaben für den ersten und letzten Tag angeboten wird? Wenn eine Reduktion erfolgt, welches ist der Prozentsatz der Reduktion?

- Standard-Tagessatzregeln:

    - Gibt es eine Prozentsatzreduzierung im Tagessatzanspruch für die Verpflegung, wenn beispielsweise die Verpflegung inbegriffen ist? Wenn eine Reduktion erfolgt, welches ist der Prozentsatz für jede Mahlzeit?
    - Wird die Verpflegungsreduzierung pro Tag, pro Reise oder anhand der Anzahl der Verpflegungen pro Tag berechnet?
    - Müssen Tagessätze auf normale Art gerundet oder aufgerundet werden?
    - Werden Tagessatzberechnungen über einen 24-Stunden-Zeitraum oder einen Kalendertag definiert?

- Tagessatzregeln auf Grundlage des Standorts:

    - Unterscheiden sich die Tagessätze nach Standort? Welche Orte sind eingeschlossen?
    - Wenn Tagessätze nach Standort abweichen, welcher Prozentsatzbetrag wird für die folgenden Ausgabenvergütungen bereitgestellt:

        - Verpflegung
        - Hotel
        - Sonstige Ausgaben

### <a name="expense-management-journals-and-accounts"></a>Spesenverwaltungserfassungen und Konten

Die Spesenverwaltung erfordert, dass Sie mehrere Erfassungen und Konten verwenden. Sie müssen beispielsweise festlegen, ob das gleiche Konto für Barvorschüsse und Kreditkarten-Buchungsstreitigkeiten verwendet wird.

**Entscheidung:**

- In welcher Sachkontenerfassung werden genehmigte Spesenabrechnungen gebucht?
- Welcehs Konto wird für Barvorschüsse verwendet?
- Sollen Barvorschüsse sofort gebucht werden?

### <a name="payment-methods"></a>Zahlungsmethoden

Wenn Sie Mitarbeitern erlauben, Ausgaben im Auftrag Ihres Unternehmens zu übernehmen, müssen Sie die Zahlungsmethoden definieren, die Mitarbeiter verwenden dürfen. Sie möchten beispielsweise Mitarbeitern die Verwendung von Bargeld oder einer Firmenkreditkarte gestatten. Sie möchten möglicherweise Mitarbeitern auch gestatten, persönliche Kreditkarten zu verwenden und dann Rückerstattungen zu erhalten. Sie müssen folgende Entscheidungen für jede von Ihnen gestattete Zahlungsmethode treffen.

**Entscheidung:**

- Welche Zahlungsmethoden sind zulässig?
- Wer ist der Verantwortliche für Ausgaben nach einer Zahlungsmethode?
- Gibt es einen Gegenkontotyp? Wenn ein Gegenkonto vorhanden sind, welches ist das Konto?
- Wenn ein Gegenkonto vorhanden sind, welches ist das Konto?
- Wenn die Zahlungsmethode Kreditkarte ist, soll die Zahlungsmethode ausschließlich für importierten Buchungen verwendet werden?

### <a name="expense-categories-and-shared-categories"></a>Spesen- und gemeinsam genutzte Kategorien

Wenn Mitarbeiter eine Spesenabrechnung erstellen, muss jede Ausgabe, die sie erfassen, einer Ausgabenkategorie zugeordnet werden. Spesenkategorien können aus gemeinsam genutzten Kategorien, die von allen juristischen Personen in der Organisation verwendet werden, abgeleitet werden Diese Kategorien können ebenfalls im Projektverwaltungs- und Buchhaltungsmodul freigegeben werden, abhängig davon, wie die Organisation definiert ist. Sie müssen auf Grundlage der Definition der Organisation und der Anleitung des Implementierungsteams festlegen, ob die Kategorien, die in der Spesenverwaltung verwendet werden, nur Ausgaben verwenden, oder ob sie für Projekt und Ausgaben freigegeben werden. Beachten Sie, dass diese Kategorien zwischen Projekt und Ausgaben oder Projekt und Produktion freigegeben werden können, aber nicht zwischen Ausgaben und Produktion. Sie müssen folgende Entscheidungen für jede Ausgabenkategorie treffen.

**Entscheidung:**

- Was ist die Spesenkategorie? Beispiele beinhalten Kategorien für Flugtickets, Hotel oder Kilometer.
- Können diese Ausgabekategorie auch in der Projektverwaltung und -buchhaltung verwendet werden?
- Was ist der Ausgabentyp?
- Welches ist die Standardzahlungsmethode für die Ausgabenkategorie?
- Müssen Ausgaben in die Ausgabenkategorie aufgeschlüsselt werden?
- Welches ist das Hauptstandardkonto für die Ausgabenkategorie?
- Was ist die standardmäßige Artikel-Mehrwertsteuergruppe für die Ausgabenkategorie?
- Sind zusätzliche Zahlungsmethoden für die Ausgabenkategorie zulässig? Wenn zusätzliche Zahlungsmethoden erlaubt sind, welche sind das?
- Gibt es Unterkategorien innerhalb dieser Ausgabenkategorie? Wenn es Unterkategorien gibt, müssen Sie außerdem folgende Entscheidungen treffen:

    - Werden bestimmte Unterkategorien aus der Steuerbeitreibung ausgeschlossen?
    - Welches ist die Artikel-Mehrwertsteuergruppe der Unterkategorien?

Wenn diese Ausgabenkategorie auch im Projektverwaltungs- und Buchhaltungsmodul verwendet wird, beantworten Sie die folgenden Fragen. Sonst gehen Sie zum nächsten Abschnitt.

- Welche Kostenkonten werden im Folgenden verwendet?

    - Kosten
    - Lohnzuweisung
    - WIP- Kostenwert
    - Kosten - Artikel
    - WIP - Einstandswert - Artikel
    - Antizipierter Verlust
    - WIP - Antizipierter Verlust

- Welche Umsatzerlöskonten werden im Folgenden verwendet?

    - Fakturierter Umsatzerlös
    - Antizipierter Umsatzerlös – Verkaufswert
    - WIP - Verkaufswert
    - Antizipierter Umsatzerlös – Produktion
    - RIF – Produktion
    - Antizipierter Umsatzerlös – Gewinn
    - RIF – Gewinn
    - Antizipierter Umsatz - Dauerauftrag
    - WIP - Dauerauftrag

### <a name="taxes"></a>USt.

Für ausgabenbezogene Steuern müssen Sie bestimmen, was Spesenabrechnungen beinhalten sollen oder wofür sie aktiviert sind.

**Entscheidung:**

- Ist die Mehrwertsteuer in den Ausgabenbeträgen enthalten.
- Soll Steuerbeitreibung für Ausgaben aktiviert werden?

    > [!NOTE]
    > Wenn Sie das Hauptbuch planen, wenn Sie sich entscheiden, US-Mehrwert- und Erwerbssteuerregeln anzuwenden, können Sie die Steuerbeitreibung für Ausgaben nicht aktivieren, (US-Mehrwert- und Erwerbssteuerregeln festzulegen, wählen Sie die Option **Wenden Sie Mehrwertsteuerbesteuerungsregeln an** auf fest. **Ja**.)

## <a name="policies"></a>Richtlinien

Sie können Spesenabrechnungsrichtlinien erstellen, wenn Mitarbeiter Ausgaben im Auftrag der Organisation tätigen, um dieser Zeit und Geld zu speichern. Richtlinien stellen sicher, dass Mitarbeiter innerhalb des Budgets bleiben, alle erforderlichen Informationen bereitstellen und Geld nur nach Bedarf ausgeben. Sie müssen folgende Entscheidungen für jede Spesenabrechnungsrichtlinie und jede zu genehmigende Spesenabrechnungsrichtlinie treffen, die die Sie erstellen.

**Entscheidung:**

- Wie ist der Name der Richtlinie?
- Wofür ist die Ausgabenrichtlinie?
- Wird diese Richtlinie angewendet, wenn Sie sich zuvor entschieden haben, die Intercompany-Ausgaben Ihrer Organisation zu aktivieren?
- Wann wird die Richtlinie wirksam?
- Wann läuft die Richtlinie ab?
- Was ist die Richtlinienregel?
- Was ist das Ergebnis der Richtlinie?
