---
title: Finanzberichterstellung
description: Die Finanzberichterstellung ermöglicht Finanz- und Geschäftsexperten Finanzaufstellungen zu erstellen, zu verwalten, bereitzustellen und anzuzeigen.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b1db953165bd745a00f68048767a2b19fcc2f38
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093950"
---
# <a name="financial-reporting"></a>Finanzberichterstellung

[!include [banner](../includes/banner.md)]

Die Finanzberichterstellung für die Anwendung ermöglicht Finanz- und Geschäftsexperten Finanzaufstellungen zu erstellen, verwalten, bereitzustellen und anzuzeigen. Es bewegt sich über die traditionellen Berichtseinschränkungen hinaus, um effizient verschiedene Arten von Berichten zu entwerfen.

Die Finanzberichterstellung umfasst Dimensionsunterstützung. Daher sind Kontosegmente oder Dimensionen sofort verfügbar. Es sind keine zusätzlichen Tools oder Konfigurationsschritte erforderlich.

## <a name="financial-reporting-setup"></a>Finanzberichterstellungseinrichtung
Die Seite **Rechnungslegungseinstellung** enthält eine Liste aller Finanzdimensionen im System. **Hauptbuch**\>**Sachkontoeinstellung**\>**Rechnungslegungseinstellung**.

Die Seite **Rechnungslegungseinstellung** enthält zwei Abschnitte, die die Daten bestimmen, die Sie in der Finanzberichterstellung melden:

- **Dimensionsregisterkarte** - Weil verschiedene Unternehmen verschiedene Dimensionen und Kontostrukturen verwenden, besteht keine Möglichkeit, den Auftrag zu bestimmen, in dem Benutzer alle enthaltenen Finanzdimensionen auf Berichten angezeigt werden sollen. Mit dieser Seite können Sie den Auftrag festlegen, in dem Sie Finanzdimensionen anzeigen möchten, wenn Sie einen Bericht in der Finanzberichterstellung erstellen und anzeigen.
- **Attributregisterkarte**, in dem Sie auswählen können, ob die Fähigkeit wünschen, **Kreditoren** und **Debitoren** als Attribut für das Filtern und Erstellen von Berichten zu verwenden. Das Erstellen einer Fertigmeldung in "Kreditoren" und in " Debitoren ist nur wertvoll, wenn Sie nicht mehrere Kreditoren oder Debitoren in einem einzelnen Dokument eingeben, wenn Sie Posten buchen. Kreditor und/oder Debitors werden zusätzliche Zeit der Integration hinzufügen.

## <a name="financial-reporting-components"></a>Finanzberichterstellungskomponenten
Die folgenden Komponenten der Finanzberichterstellung erleichtern das Erstellen, Anzeigen und Planen von Berichten.

| Komponente        | Funktionen | Weitere Informationen: |
|------------------|-----------|------------------------|
| Berichts-Designer  | Erstellen Sie Berichtsbausteine, die kombiniert werden können, um einen Bericht zu definieren und zu generieren. Der Berichts-Assistent führt weniger erfahrene Benutzer durch den Designprozess. Erfahrene Benutzer können neue Berichtsbausteine erstellen oder vorhandene Bausteine den Anforderungen entsprechend ändern. | |
| Berichtszeitpläne | Planen Sie einen einzelnen Bericht oder eine Gruppe von Berichten so, dass sie regelmäßig generiert werden. | [Finanzberichte generieren](generate-financial-report.md) |

## <a name="features"></a>Funktionen
<table>
<thead>
<tr>
<th>Funktion</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Berichtsdesignflexibilität</td>
<td>Der Berichts-Designer stellt folgende Berichtsoptionen bereit, wenn Sie einen Bericht entwerfen:
<ul>
<li>Speichern Sie Dimensionskombinationen, und verwenden Sie die Dimensionen für weitere Berichte erneut.</li>
<li>Steuern Sie, wie Dimensionsbeschreibungen formatiert und angezeigt werden.</li>
<li>Erkennen Sie Konten oder Dimensionen, die in den Berichtsbausteinen ausgelassen wurden.</li>
<li>Überschriften für rollende Prognosen formatieren.</li>
</ul>
</td>
</tr>
<tr>
<td>Zusammenarbeit an Finanzberichten</td>
<td>Die folgenden Funktionen helfen Ihnen, die Generierung und Verteilung von Berichten zu vereinfachen:
<ul>
<li>Planen Sie Berichte, sodass sie täglich, wöchentlich, monatlich oder jährlich automatisch generiert werden.</li>
<li>Exportieren Sie ins schreibgeschützte XPS-Format, das eine bessere Dokumentensicherheit durch digitale Signaturen bietet.</li>
<li>Exportieren Sie in ein Microsoft Excel-Arbeitsblatt.</li>
<li>Um Berichte freizugeben, können Sie E-Mails erstellen, die Links auf die Berichte enthalten.</li>
</ul>
</td>
</tr>
<tr>
<td>Interaktive Berichtsanzeige</td>
<td>Mit interaktiven Funktionen können Sie die folgenden Aufgaben ausführen:
<ul>
<li>Ändern Sie das Berichtsdatum des Berichts, den Sie anzeigen möchten.</li>
<li>Ändern Sie die Währung des Berichts, den Sie anzeigen möchten.</li>
<li>Zeigen Sie den Berichts in einer Übersichts- oder detaillierten Ansicht an.</li>
<li>Fügen Sie Dimensionsfilter hinzu, um Berichtsinhalte auf eine bestimmte Dimension oder eine Kombination aus Dimensionen zu begrenzen.</li>
<li>Fügen Sie Attributfilter hinzu, um Berichtsinhalte auf ein bestimmtes Attribut oder eine Kombination aus Attributen zu begrenzen.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Zusätzliche Ressourcen
[Finanzberichte generieren](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]