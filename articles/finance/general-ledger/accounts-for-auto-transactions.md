---
title: Konten für automatische Buchungen
description: In diesem Thema wird erläutert, wie Konten für automatische Transaktionen verwendet werden, um über Microsoft Dynamics 365 zu buchen und bietet Beispiele für automatische Transaktionen bei wichtigen Konten.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275c74d673d1ba2468e23c5fa443c9272d13a184
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735259"
---
# <a name="accounts-for-automatic-transactions"></a>Konten für automatische Buchungen

Die Seite **Konten für automatische Transaktionen** (**Hauptbuch &gt; Buchungseinstellungen &gt; Konten für automatische Transaktionen**) wird verwendet, um das Standardhauptkonto zu definieren, das für jeden Buchungstyp im System zu buchen. Obwohl die meisten Buchungstypen auf einer modulspezifischen oder funktionsspezifischen Seite konfiguriert werden können, können einige Buchungstypen nur auf der Seite **Konten für automatische Transaktionen** konfiguriert werden.

Sie können beispielsweise das Hauptkonto angeben, das für den **Debitorensaldo** Buchungstyp im **Zusammenfassung**-Feld auf der **Debitorenbuchungsprofil**-Seite verwendet wird und verwenden eina anderes Hauptkonto für jedes Kundenprofil. Auf diese Weise haben Sie genauere Kontrolle über die Buchungen. Andererseits können Sie das Fehlerkonten nur auf der Seite **Konten für automatische Buchungen** angeben.

Beim Öffnen der **Konten für automatische Transaktionen**-Seite in einer neuen juristischen Person, ist die Liste der Konten leer. Sie können die gängigsten Buchungstypen hinzufügen, die auf der Seite konfiguriert werden sollten, indem Sie **Standardtypen erstellen**-Schaltfläche auswählen. Dann können Sie für jede Zeile das Hauptkonto im **Hauptkonto**-Feld in auswählen. Wenn Sie das **Hauptkonto**-Feld für ein Buchungstyp leer gelassen haben und Sie kein Hauptkonto auf der einer modulspezifischen oder funktionsspezifischen Seite konfiguriert haben, erhalten Sie eine Fehlermeldung, wenn Sie eine Transaktion buchen, die den Buchungstyp verwendet. Normalerweise lautet die Nachricht: „Das Konto für \[Buchungstyp\] kann nicht gefunden werden.“

## <a name="default-posting-types"></a>Standardbuchungstypen

Die folgende Tabelle zeigt Beispiele für die Standardbuchungstypen, die erstellt werden, wenn Sie **Standardtypen erstellen** auf der **Konten für automatische Transaktionen**-Seite auswählen. Es zeigt beispielhafte Hauptkonten und Beschreibungen. Die „Soll/Haben?“ Spalte zeigt an, ob die Transaktion typischerweise eine Soll oder Haben bucht. In einigen Fällen kann eine Transaktion entweder ein Soll oder ein Haben buchen. Die Spalte „Clearingkonto“ gibt an, ob es sich bei dem Buchungstyp um ein Verrechnungskonto handelt. Wenn der Buchungstyp ein Clearingkonto ist, wird der auf diesem Konto gebuchte Betrag automatisch storniert, wenn eine spätere Transaktion gebucht wird.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Centdifferenz in Berichtswährung | 618160 | Sonstige Ausgaben | Ausgaben | Beides | Nein | Dieser Buchungstyp wird verwendet, wenn eine Centdifferenz auftritt, wenn ein Transaktionsbetrag in einer Fremdwährung in die Berichtswährung umgerechnet wird. |
| Centdifferenz in Buchhaltungswährung | 618160 | Sonstige Ausgaben | Ausgaben | Beides | Nein | Dieser Buchungstyp wird verwendet, wenn eine Centdifferenz auftritt, wenn ein Transaktionsbetrag in einer Fremdwährung in die Buchhaltungswährung umgerechnet wird. |
| Fehlerkonto | 999999 | Fehlerkonto | Ausgaben | Beides | Nein | Dieser Buchungstyp wird verwendet, wenn ein Fehler im System auftritt. Das Konto sollte in jedem Zeitraum validiert und alle Fehler behoben werden. |
| Jahresendergebnis | 300160 | Nicht ausgeschüttete Gewinne | Eigenkapital | Beides | Nein | Dieser Buchungstyp wird verwendet, wenn der Jahresabschlussprozess ausgeführt wird, um den Kontensaldo des **Gewinn- und Verlust**-Typs in das für das Jahresergebnis ausgewählte Hauptkonto zu verschieben. |
| Debitorenskonto | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein | Der Buchungstyp, die auf **Konten für automatische Transaktionen**-Seite der definiert ist, wird nicht verwendet. Ein Hauptkonto ist erforderlich, wenn Skonti in der Debitorenbuchhaltung konfiguriert werden.|
| Kreditorenskonto | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Nein | Der Buchungstyp, die auf **Konten für automatische Transaktionen**-Seite der definiert ist, wird nicht verwendet. Ein Hauptkonto ist erforderlich, wenn Skonti in der Kreditorenkonten konfiguriert werden. |

## <a name="additional-posting-types"></a>Zusätzliche Buchungstypen

Die folgende Tabelle zeigt Beispiele für zusätzliche Buchungstypen, die konfiguriert werden müssen, wenn Sie die zugehörigen Funktionen verwenden möchten. Für diese Buchungstypen ist keine Buchungsprofilkonfiguration in einem anderen Modul verfügbar. Die „Soll/Haben?“ Spalte zeigt an, ob die Transaktion typischerweise eine Soll oder Haben bucht. In einigen Fällen kann eine Transaktion entweder ein Soll oder ein Haben buchen. Die Spalte „Clearingkonto“ gibt an, ob es sich bei dem Buchungstyp um ein Verrechnungskonto handelt. Wenn der Buchungstyp ein Clearingkonto ist, wird der auf diesem Konto gebuchte Betrag automatisch storniert, wenn eine spätere Transaktion gebucht wird.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Saldokonto für Konsolidierungsdifferenz | 801200 | Gewinn und Verlust – Neubewertung | Ausgaben | Beides | Nein | Dieser Buchungstyp wird verwendet, wenn Sie eine Konsolidierung durchführen, die eine Währungsneubewertung beinhaltet, und während der Neubewertung Centdifferenzen auftreten. |
| GuV-Konto für Konsolidierungsdifferenzen | 801200 | Gewinn und Verlust – Neubewertung | Ausgaben | Beides | Nein | Dieser Buchungstyp wird verwendet, wenn Sie eine Konsolidierung durchführen, die eine Währungsneubewertung beinhaltet, und während der Neubewertung Centdifferenzen auftreten. |
| Einheitenbezogen – Soll | 133500 | Einheitsbezogene Forderungen | Anlage | Belastung | Nein | Dieser Buchungstyp wird verwendet, wenn Sie auf der **Sachkonto**-Seite eine Ausgleichsdimension auswählen, und die Dimension wird in einer gebuchten Transaktion nicht ausgeglichen. |
| Einheitenbezogen - Haben | 233500 | Einheitsbezogen Fällig | Passivposten | Gutschrift | Nein | Dieser Buchungstyp wird verwendet, wenn Sie auf der **Sachkonto**-Seite eine Ausgleichsdimension auswählen, und die Dimension wird in einer gebuchten Transaktion nicht ausgeglichen. |
