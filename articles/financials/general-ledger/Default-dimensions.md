---
title: Finanzdimensionen und Buchungen
description: Wenn Sie Ihren Kontenplan und die Planung einrichten, müssen Sie entscheiden, wie die verschiedenen Komponenten zusammenarbeiten, wenn Sie ein Dokument oder eine Erfassung buchen. Diese Komponenten schließen Kontostrukturen, erweiterte Regeln und Ausgleichen und feste Dimensionen ein. In diesem Thema wird erläutert, was jede Komponente ist und wie die Komponenten zusammenarbeiten.
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2e218351f2462ca135ef6e453fb127c3e111fc40
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839664"
---
# <a name="financial-dimensions-and-posting"></a>Finanzdimensionen und Buchungen 

[!include [banner](../includes/banner.md)]

Wenn Sie Ihren Kontenplan und die Planung einrichten, müssen Sie entscheiden, wie die verschiedenen Komponenten zusammenarbeiten, wenn Sie ein Dokument oder eine Erfassung buchen. Diese Komponenten schließen Kontostrukturen, erweiterte Regeln und Ausgleichen und feste Dimensionen ein. In diesem Thema wird erläutert, was jede Komponente ist und wie die Komponenten zusammenarbeiten.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Kontenplan und Komponenten von Finanzdimensionen

Microsoft Dynamics 365 for Finance and Operations hat eine großes, regelbasiertes System zum Definieren der zulässigen Kombinationen von Hauptkonten und von Finanzdimensionswerten. Dieser Abschnitt gibt einen kurzen Überblick über die Funktionen jeder Komponente und beschreibt, wo Sie die Komponente suchen können.

### <a name="account-structures"></a>Kontostrukturen

Eine Kontostruktur ist erforderlich, wenn Sie das Sachkonto einrichten. Sie müssen mindestens eine Kontostruktur definieren und aktivieren, die Sie dem Sachkonto zuweisen. Das Hauptkonto muss die Kontostruktur enthalten. Sie können die Reihenfolge der Segmente definieren, die für das Unternehmen am besten sind. Nachdem das Hauptkonto definiert wird, kann das System die Kontostruktur, die verwendet wird, bestimmen. Wenn Sie zuerst das Hauptkonto vor oder in der Nähe einer Struktur stellen, können Sie die Werte einschränken und das System auch unterstützen, den letzten bekannten gültigen Wert als Standardwert zu übernehmen. Sie können bis 10 um zusätzliche Finanzdimensionen in der Kontostruktur sind. Die Kontostruktur definiert, welche Dimensionswerte in Verbindung mit anderen Werten gültig sind. sie definiert auch, dass die Dimensionswerte eingegeben werden müssen.

### <a name="advanced-rules"></a>Erweiterte Regeln

Erweiterte Regeln sind eine beliebige Komponente, wenn der Kontenplan einrichten. Sie können beliebig viele erweiterte Regeln hinzufügen, die Sie der Kontostruktur zuführen möchten. Erweiterte Regeln werden häufig verwendet, Szenarien zu behandeln, bei denen zusätzliche Finanzdimensionen verfolgt werden müssen, wenn bestimmte Kriterien erfüllt werden. Wenn Sie beispielsweise ein Reisekostenkonto verwenden, möchten Sie möglicherweise zusätzliche Informationen nachverfolgen, wie beispielsweise das Ereignis für das der Mitarbeiter reist. Sind mehrere erweiterte Regeln vorhanden sind, werden sie in alphabetischer Reihenfolge, basierend auf den Namen der Regeln, angewendet. Die Segmente, bei denen eine Regel hinzufüg wird, können erst angewendet werden, nachdem die Segmente der Kontostruktur angewendet werden.

### <a name="balancing-dimension"></a>Dimension ausgleichen

Sie können eine Ausgleichsfinanzdimension optional definieren. Auf der Seite **Sachkonto** können Sie die Finanzdimension definieren, die gebucht werden soll. Anschließend sobald Buchungen für diese Finanzdimension gebucht werden, erstellt und bucht das System automatisch Einträge, um die ausgeglichenen Finanzdimension zu erstellen.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Die Standard-/Feste finanzdimensionen für das Hauptkonto.

Standarddimensionen stammen aus verschiedenen Orten, wie Hauptdatensätzen, Debitor oder Kreditorendatensätze und Dokumentköpfen des Hauptkontos. Dieses Thema bezieht sich auf Standarddimensionen im Hauptkonto nach juristischer Person. Sie können definieren, ob ein Hauptkonto den Wert **Nicht Fest** oder **Fest** für die einzelnen Finanzdimensionen hat, die von allen Kontostrukturen für das Sachkonto verwendet wird. Wenn eine Finanzdimension **Nicht fixiert** ist, wird sie den Standardwert nutzen, dieser Wert kann jedoch überschrieben werden. Dieses Verhalten gilt für alle Standardwerte im System, selbst für Standardwerte, die von den Hauptdatensätzen stammen. Wenn eine Finanzdimension auf einen Wert **Fest** festgelegt ist, wird dieser Wert immer, unabhängig davon, ob er von irgendwoher als Standardwert kommt oder der Benutzer ihn eingegeben hat.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Auftrag, in dem Standarddimensionen für die Buchungen verwendet werden

Personen haben häufig Fragen über den Auftrag, den die verschiedenen Komponenten ausführen. Es ist außerordentlich wichtig, dass Sie den Auftrag kennen, der Standarddimensionen verwendet, da sich dieses Verhalten auf den Ansatz auswirkt, den Sie akzeptieren, um einzurichten.

> [!NOTE]
> Diese Informationen beziehen sich nur auf die Anwendung von Standarddimensionen in der Anwendung. Wenn Sie Daten importieren, indem Sie das Microsoft Excel- oder Datenverwaltungs-Framework verwenden, variiert das Verhalten.

### <a name="example-1"></a>Beispiel 1

**Kontostruktur**

| Hauptkonto            | Unternehmenseinheit           | Abteilung              | Kostenstelle             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Alle Werte sind zulässig. | Alle Werte sind zulässig. | Alle Werte sind zulässig. | Alle Werte sind zulässig. |

**Hauptkonto**

| Hauptkonto | Name          | Juristische Person | Abteilung                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Produktverkäufe | USMF         | Fest - 022 Abteilung Marketing und Vertrieb |

In der folgenden Abbildung wird die feste Standarddimension angezeigt, die im Hauptkonto 401100 festgelegt wird.

[![Standardfinanzdimensionen](./media/default-dimensions.png)](./media/default-dimensions.png)

Für dieses sehr grundlegende Beispiel geben Sie eine allgemeine Erfassung ein, in der die Abteilungsdimension auf den Standardwert **023** (Arbeitsgänge) festgelegt wird. Wir geben das  Sachkonto ein und buchen es. Die folgende Abbildung zeigt die Standardfinanzdimension im Feld Hauptbuchkopf.

[![Allgemeine Erfassungen](./media/general-journal.png)](./media/general-journal.png)

Die Standarddimension im Erfassungskopf hat zur Folge, dass Abteilung 023 Abteilung, als Standard für die Verkaufskontoposition verwendet wird. Die folgende Abbildung stellt die allgemeine Erfassungsposition an, in dem der **023** Standarddimensionswert vom Kopf angewendet wird.

[![Alle Journale](./media/journal-voucher.png)](./media/journal-voucher.png)

Wenn die Position gebucht wird, wird die feste Dimension angewendet, und die Position wird in Abteilung 022 gebucht. Die folgende Abbildung zeigt den gebuchten Beleg an, in der die feste Dimension für das Verkaufskonto verwendet wird.

[![Belegbuchungen](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Beispiel 2

Dieses Beispiel verwendet die gleiche Einstellung wie das erste Beispiel. Allerdings können wir eine zweite Komponente hinzufügen und  die Abteilungsdimension als Ausgleichsdimension verwenden. In der folgenden Abbildung wird **Abteilung** als Ausgleichsfinanzdimension für das USMF-Sachkonto festgelegt.

[![Sachkonto](./media/ledger.png)](./media/ledger.png)

Wenn eine Erfassungskopfeinstellung verwendet wird und die gleiche Buchung gebucht ist, wird zuerst die feste Dimension angewendet. Danach wird die Ausgleichslogik angewendet, die sicherstellt, dass jede Abteilung einen Eintrag ausgeglichenen hat. Die folgende Abbildung zeigt Belegbuchungen an, die die Gegenbuchung enthalten, nachdem die feste Dimension angewendet wurde.

[![Belegbuchungen](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Beispiel 3

In diesem Beispiel werden wir eine erweiterte Regel hinzufügen. Die erweiterte Regel legt zudem fest, dass wenn Verkaufskonto 401100 und 022 Abteilung (Vertrieb und Marketing) verwendet werden, vom System ein zusätzliches Segment verfolgt werden soll, das "Kunde" heißt.

Dieses Beispiel ist wegen dem  Auftrag wichtig. Die Kontostruktur wird bestimmt, wenn das Hauptkonto eingegeben wurde. Wenn Sie die Kontostruktureinstellung beziehen, kann das System erkennen, dass das Hauptkonto, Geschäftseinheit, die Abteilung und die Kostenstelle relevant sind. An diesem Punkt wurde die erweiterte Regel nicht gestartet, da feste Dimensionen nicht angewendet werden, bis für den Erfassungsbeleg Standarddimensionen für die Buchung angewendet wurden. In der folgenden Abbildung ist das Debitorensegment nicht vorhanden, da die Kriterien für die erweiterte Regel nicht ausgeführt wurden.

[![Sachkonto](./media/drop-down.png)](./media/drop-down.png)

Die Buchung ist nicht erfolgreich, da die feste Dimension am Ende des Prozesses angewendet wurde. Die Dimensionsprüfungen bestimmt, dass das Debitorensegment erforderlich ist, wenn das Hauptkonto 401100 ist und die Abteilung 022 ist. Buchung kann aufgrund des Prüfungsfehlers nicht erfolgen. Die folgende Abbildung zeigt die Meldung an, die angezeigt wird, nachdem Dimensionsprüfungen bestimmt, dass ein Debitor ein Pflichtsegment ist.

[![Meldungsdetails](./media/message.png)](./media/message.png)

In diesem Beispiel müssen Sie den Standardwert überschreiben, sodass die erweiterte Regel ausgelöst wurde und Sie das Debitorensegment eingeben können. Diese Lösung ist jedoch nicht immer möglich, und einige Benutzer kennen diese Buchungsregeln nicht einmal. Daher ist es wichtig, dass Sie den Auftrag verstehen, dass Standarddimensionen angewendet werden, wenn Sie den Kontenplan einrichten.

Um zu gewährleisten, was Sie möchten in diesem Beispiel, können Sie die Konfiguration auf verschiedene Weise ändern. Sie können beispielsweise einen neuen Kontostruktur für Verkaufskonten erstellen und das Debitorensegment in der Struktur einfügen. So können mehr Zeilen in eine vorhandene Kontostruktur hinzugefügt werden und das Hauptkonto und den gültigen Abteilungswerten angezeigt werden. In der zusätzlichen Debitorenstruktur ist es möglicherweise sinnvoll, eine separate Kontostruktur von Verkaufskonten zu haben, bei denen das Debitorensegment vorhanden ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen 

Einige der folgenden Ressourcen beziehen sich auf eine ältere Versionen der erhaltenen Finanzierung und Arbeitsgänge. Sie sind jedoch Teil der Informationen zur Bewerbung von Standarddimensionen und viele der Konzepte sind  identisch in der Vorgängerversion, und die Referenzen sind noch gültig.

[Ausgeglichene Erfassungen für einheitenbezogene Buchhaltung](example-balanced-journals-interunit-accounting.md)

[Ihren Kontenplan planen](plan-chart-of-accounts.md) 

[Planung Ihres Kontenplans in AX 2012 (Blog)](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – Dieser Link geht zu Teil 1 einer siebenteiligen Reihe.

[Dimension, die in den Buchhaltungsverteilungen den Standardwert akzeptiert](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Dimension, die das Dimensionsframework standardmäßig akzeptiert](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2014/09/)
