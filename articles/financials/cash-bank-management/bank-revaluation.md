---
title: Bank – Neubewertung der Fremdwährung
description: In diesem Thema erhalten Sie einen Überblick über den Prozess der Neubewertung der Fremdwährung – Bank. Es umfasst Informationen zum Setup, dem Ausführen des Prozesses, der Berechnung für den Prozess und von Rückbuchungen von Neubewertungsbuchungen.
author: mikefalkner
manager: AnnBe
ms.date: 04/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4ec9814a4a35a1b3ba7ba05a04b53e5b150f4a04
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538631"
---
# <a name="bank-foreign-currency-revaluation"></a>Bank – Neubewertung der Fremdwährung

[!include [banner](../includes/banner.md)]
[!include [preview-banner](../includes/preview-banner.md)]

In diesem Thema erhalten Sie einen Überblick über den Prozess der Neubewertung der Fremdwährung – Bank. Es wird erläutert, wie Sie den Prozess einrichten und ausführen und es bietet Informationen über die Berechnung für den Prozess. Es wird auch erklärt, wie Neubewertungsbuchungen rückgebucht werden, wenn eine Rückbuchung erforderlich ist.

Als Teil eines Periodenendes ist für Buchhaltungskonventionen erforderlich, dass Bankkontosalden in Fremdwährungen mithilfe verschiedener Wechselkurstypen (aktuell, historisch, durchschnittlich usw.) neu bewertet werden. Die Funktion „Neubewertung der Fremdwährung – Bank” kann verwendet werden, um eine oder mehrere Bankkonten neu zu bewerten. Die Funktion ist auch eine globale Funktion. Daher können Sie von einer einzelnen Seite aus Banken bei allen juristischen Personen neu bewerten, auf die Sie Zugriff haben.

> [!NOTE]
> Wird der Neubewertungsprozess ausgeführt, wird der Saldo für jedes Bankkonto, das in einer Fremdwährung gebucht wird, neu bewertet. Die unrealisierten Gewinn- oder Verlusttransaktionen, die während des Neubewertungsprozesses erstellt werden, werden vom System generiert. Zwei Buchungen werden möglicherweise erstellt, eine für die Buchhaltungswährung und eine für die Berichtswährung, wenn eine Berichtswährung relevant ist. Jeder Buchhaltungseintrag wird zum unrealisierten Gewinn oder Verlust gebucht oder zum Hauptkonto, das gerade neu bewertet wird.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Vorbereitungen, um die Neubewertung der Fremdwährung auszuführen

Bevor Sie den Neubewertungsprozess ausführen können, sind folgende Einstellungen erforderlich.

- Geben Sie auf der **Sachkonto**-Seite den Wechselkurstyp an. Wenn ein Wechselkurstyp nicht für das Hauptkonto definiert ist, wird dieser Wechselkurstyp während der Neubewertung der Fremdwährung verwendet.
- Geben Sie auf der **Sachkonto**-Seite die Konten für realisierten Gewinn, realisierten Verlust, nicht realisierten Gewinn und den nicht realisierten Verlust für die Neubewertung der Währung an. Konten für realisierte Gewinne und realisierte Verluste werden verwendet, wenn Debitor- und Kreditorbuchungen ausgeglichen werden. Konten für unrealisierten Gewinn und unrealisierten Verlust werden verwendet, um offene Buchungen und Hauptbuch-Hauptkonten neu zu bewerten.
- Auf der Seite **Währungsneubewertungskonten** wählen Sie verschiedene Währungsneubewertungskonten für jede Währung und jedes Unternehmen aus. Wenn keine Konten definiert werden, werden die Konten der **Sachkonto**-Seite verwendet.

## <a name="enable-foreign-currency-revaluation"></a>Neubewertung der Fremdwährung aktivieren

Sie müssen die Funktion „Neubewertung der Fremdwährung – Bank” aktivieren, bevor Sie Neubewertungen der Fremdwährung verarbeiten können.

1. Wechseln Sie zu **Bargeld- und Bankverwaltung \> Einstellungen \> Parameter für die Bargeld- und Bankverwaltung**.
2. Legen Sie auf der Registerkarte **Allgemein** unter **Neubewertung der Fremdwährung** die Option **Bankneubewertung aktivieren** auf **Ja** fest, um die Funktion für die aktuelle juristische Person zu aktivieren. 
3. Auf der Registerkarte **Nummernkreise** fügen Sie einen Nummernkreis für die Neubewertung der Fremdwährung hinzu.
4. Aktualisieren Sie den Browser, um **Neubewertung der Fremdwährung** im Abschnitt **Periodische Aufgaben** auf der Bereichsseite anzuzeigen.

Sie müssen die Funktion für jede juristische Person aktivieren, die die Neubewertung der Fremdwährung verwendet. Wenn Sie der Rolle Systemadministrator oder Funktionsrolle zugewiesen werden, können Sie diesen Schritt entfernen, indem Sie die Funktion **Aktivieren der Bankneubewertung ohne einen Parameter** im Arbeitsbereich **Funktionsverwaltung** aktivieren.

> [!NOTE]
> Wenn Ihre juristische Person einen russischen, polnischen oder ungarischen Länder-/Regionscode verwendet, können Sie bereits „Neubewertung der Fremdwährung – Bank” vornehmen. Sie können die Neubewertung der Fremdwährung nicht verwenden, die von anderen Ländern oder Regionen verwendet wird.

## <a name="process-foreign-currency-revaluation"></a>Eine Neubewertung der Fremdwährung verarbeiten

Nachdem das Setup abgeschlossen ist, verwenden Sie die Seite **Neubewertung der Fremdwährung** in „Bargeld- und Bankverwaltung”, um die Salden einer oder mehrerer Bankkonten für alle juristischen Personen neu zu bewerten. Sie können den Prozess in Echtzeit ausführen oder ihn planen, damit er als Stapelverarbeitungsvorgang ausgeführt wird.

Die Seite **Neubewertung der Fremdwährung** zeigt die Historie jedes Neubewertungsprozesses an. Sie zeigt an, wann der Prozess ausgeführt wurde und welche Kriterien definiert wurden und bietet einen Link zum Beleg, der für die Neubewertung erstellt wurde. Sie zeigt auch an, ob eine vorherige Neubewertung rückgängig gemacht wurde. Um den Neubewertungsprozess auszuführen, aktivieren Sie **Neubewertung der Fremdwährung** im Aktivitätsbereich, um das Dialogfeld **Bank – Neubewertung der Fremdwährung** zu öffnen.

Das Feld **Neubewertungsdatum** definiert den Abschluss-Stichtag für die Berechnung des Fremdwährungssaldos, der neu bewertet wird. Die Summe aller Bankbuchungen, die bis zu diesem Datum erfolgten, wird neu bewertet.

Das Feld **Wechselkursdatum** definiert das Datum des Wechselkurses, der verwendet wird, um die Währungssalden neu zu bewerten. So können Sie beispielsweise die Salden ab 31. Januar neu bewerten, aber den Wechselkurs verwenden, der für den 1. Februar definiert ist.

Die Neubewertung kann für eine oder mehrere juristischen Personen ausgeführt werden. Die Suche zeigt nur die juristischen Personen, auf die Sie Zugriff haben. Wählen Sie die juristischen Personen aus, für die Sie die Bankkonten auswählen möchten, die für eine Neubewertung der Fremdwährung freigegeben sind. Alle Bankkonten für diese juristischen Personen werden im Raster angezeigt.

Legen Sie die Option **Vorschau vor dem Buchen** auf **Ja** fest, wenn Sie die Ergebnisse der Neubewertung prüfen möchten vor dem Buchen. Die Neubewertung der Fremdwährung hat eine Vorschau, die gebucht werden kann. Sie müssen den Neubewertungsprozess nicht erneut ausführen. Sie können die Ergebnisse in der Vorschau nach Microsoft Excel exportieren, um einen Verlauf über die Berechnung der Beträge aufzubewahren. Sie können die Stapelverarbeitung nicht verwenden, wenn Sie die Ergebnisse der Neubewertung in der Vorschau anzeigen möchten.

Wählen Sie **OK** aus, um die Neubewertungen der Fremdwährung zu verarbeiten. Ein Datensatz wird erstellt, um den Verlauf von jeder Ausführung nachzuverfolgen. Ein separater Datensatz wird für jede juristische Person und Buchungsebene erstellt.

## <a name="calculate-unrealized-gainloss"></a>Berechnen von unrealisierten Gewinnen/Verlusten

In „Bargeld- und Bankveraltung” wird die Bankwährung als Basiswährung betrachtet und nicht neu bewertet. Der Saldo des Bankkontos in der Buchhaltungswährung wird unter Verwendung der Wechselkurse zwischen der Bankwährung und der Buchhaltungswährung am **Wechselkursdatum** neu bewertet. Der Saldo des Bankkontos in der Berichtswährung wird ebenfalls unter Verwendung der Wechselkurse zwischen der Bankwährung und der Berichtswährung am **Wechselkursdatum** neu bewertet.

Eine Buchung wird für die Differenz zwischen dem Saldo des Bankkontos und dem neuen Saldo erstellt, der für die Buchhaltungswährung berechnet wird. Eine weitere Buchung wird für die Differenz zwischen dem Saldo des Bankkontos und dem neuen Saldo erstellt, der für die Berichtswährung berechnet wird. Die Einträge für diese Buchungen werden als abgestimmt markiert. 

Kein Eintrag für die Buchhaltungswährung wird vorgenommen, wenn die Bankwährung mit der Buchhaltungswährung übereinstimmt. Gleichsam wird kein Eintrag für die Berichtswährung vorgenommen, wenn die Bankwährung mit der Berichtswährung übereinstimmt.

Die Buchung zur Neubewertung der Fremdwährung wird ebenfalls über die Dimensionen aufgeteilt, die in den Bankbuchungen gefunden werden. Die Teilung basiert auf dem Saldo für jede Dimension. Beispielsweise ist der gesamte Banksaldo 10.000, aber der Saldo für Unternehmenseinheit 001 beträgt 4.000, während der Saldo für Unternehmenseinheit 002 der Betrag 6.000 ist. In diesem Fall werden 40 Prozent des Neubewertungsbetrags zum Neubewertungskonto gebucht, das Unternehmenseinheit 001 hat, und 60 Prozent werden zum Neubewertungskonto gebucht, das Unternehmenseinheit 002 hat. Wenn die Kontostruktur keine Unternehmenseinheit enthält, wird der Gesamtbetrag zum Neubewertungskonto gebucht.

## <a name="reverse-foreign-currency-revaluation"></a>Neubewertung der Fremdwährung stornieren

Wenn Sie die Neubewertungsbuchung rückbuchen müssen, wählen Sie die Schaltfläche **Buchung stornieren** im Aktivitätsbereich auf der Seite **Neubewertung der Fremdwährung** aus. Es wird eine neue Neubewertung der Fremdwährung des historischen Datensatzes erstellt, um den historischen Audit-Trail zum Zeitpunkt der Ausführung oder Rückbuchung der Neubewertung zu erhalten.

Um mehrere Neubewertungen rückzubuchen, müssen Sie die neueste Neubewertung zuerst zurückbuchen. Fahren Sie dann fort, um ältere Neubewertungen in Datumsreihenfolge umzukehren. Sie können dann neue Neubewertungen für die von Ihnen rückgebuchten Zeiträume verarbeiten.
