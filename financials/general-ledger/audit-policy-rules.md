---
title: "Überwachungsrichtlinienregeln"
description: "Mithilfe von Überwachungsrichtlinien kann zur Sicherheit überprüft werden, ob Spesenabrechnungen, Kreditorenrechnungen und Bestellungen den von Ihnen erstellten Richtlinienregeln entsprechen. Alle Regeln, die einer Überwachungsrichtlinie zugeordnet sind, werden nach einem von Ihnen angegeben Zeitplan im Stapelverarbeitungsmodus ausgeführt.  Jede Richtlinienregel ist eine Instanz eines Richtlinienregeltyps. Für jeden Richtlinienregeltyp kann jeweils nur eine Richtlinienregel aktiv sein."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 43d2595a4a80e68ed1c0e5639e5413d732fe6a32
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="audit-policy-rules"></a>Überwachungsrichtlinienregeln

[!include[banner](../includes/banner.md)]


Mithilfe von Überwachungsrichtlinien kann zur Sicherheit überprüft werden, ob Spesenabrechnungen, Kreditorenrechnungen und Bestellungen den von Ihnen erstellten Richtlinienregeln entsprechen. Alle Regeln, die einer Überwachungsrichtlinie zugeordnet sind, werden nach einem von Ihnen angegeben Zeitplan im Stapelverarbeitungsmodus ausgeführt.  Jede Richtlinienregel ist eine Instanz eines Richtlinienregeltyps. Für jeden Richtlinienregeltyp kann jeweils nur eine Richtlinienregel aktiv sein. 

<a name="queries-and-query-types"></a>Abfragen und Abfragetypen
-----------------------

Beim Erstellen einer Überwachungsrichtlinie wird zuerst ein Richtlinienregeltyp ausgewählt. Mit dem Richtlinienregeltyp wird die Entwicklungsumgebungsabfrage angegeben, die als Ausgangspunkt für die Erstellung der Richtlinienregel verwendet wird. Zudem wird der Abfragetyp für die Richtlinienregel angegeben. Mit der Abfrage wird das Quelldokument bestimmt, das die Richtlinienregel überprüft. Außerdem werden die Felder im Quelldokument angegeben, das die juristische Person identifiziert, sowie das Feld mit dem Datum, das bei der Auswahl der zu überwachenden Dokumente verwendet werden soll. Der Abfragetyp steuert die Standardfelder auf der Abfrageseite und der Seite "Überwachungsrichtlinienregel". In der folgenden Tabelle werden die für Überwachungsrichtlinien verfügbaren Abfragetypen aufgeführt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Abfragetyp</th>
<th>Verwendungszweck</th>
<th>Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bedingt</td>
<td>Überprüfen der Attribute des Quelldokuments auf angegebene Werte.</td>
<td></td>
</tr>
<tr class="even">
<td>Zusammenführen</td>
<td>Überprüfen mehrerer Quelldokumente oder Quelldokumentpositionen auf eine Richtlinienregel durch Aggregieren numerischer Werte.</td>
<td></td>
</tr>
<tr class="odd">
<td>Musteraufnahme</td>
<td>Zufällige Auswahl eines angegebenen Prozentsatzes an Quelldokumenten zur Überprüfung auf Richtlinienverletzungen.</td>
<td>Wenn Sie diese Option auswählen, verwenden Sie die Seite "Überwachungsrichtlinienregel", mit der Sie den Prozentsatz der Dokumente für die zufällige Auswahl zur Überwachung angeben können.</td>
</tr>
<tr class="even">
<td>Duplizieren</td>
<td>Überprüfen der Quelldokumente auf doppelte Einträge in angegebenen Feldern.</td>
<td>Wenn Sie diese Option auswählen, verwenden Sie die Seite "Überwachungsrichtlinienregel", mit der Sie die Anzahl der Tage angeben können, die dem Startdatum des Datumsbereichs für die Dokumentauswahl bei der Überprüfung auf doppelte Einträge hinzugefügt werden sollen.</td>
</tr>
<tr class="odd">
<td>Listensuche</td>
<td>Überprüfen der Quelldokumente auf bestimmte Entitäten.</td>
<td>Das überwachte Dokument wird durch das Stammdokument der Abfrage definiert. Die Abfrage muss eine Listenabfrage sein, die eine Referenz zur dirpartytable-Tabelle enthält. Diese Option kann nur mit den folgenden Entwicklungsumgebungsabfragen verwendet werden:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Spesenabrechnung - überwachte Mitarbeiter)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Bestellung - überwachte Kreditoren)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Kreditorenrechnung - überwachte Kreditoren)</li>
</ul>
Geben Sie bei Auswahl dieser Option die überwachten Entitäten auf der Seite "Überwachungsrichtlinienregel" an.</td>
</tr>
<tr class="even">
<td>Schlüsselwortsuche</td>
<td>Überprüfen von Quelldokumenten auf bestimmte Wörter.</td>
<td>Geben Sie bei Auswahl dieser Option die zu suchenden Wörter auf der Seite "Überwachungsrichtlinienregel" ein. Die Seite "Überwachungsrichtlinienregel" enthält auch Optionen, mit denen Sie die Tabellen und Felder angeben können, die auf die eingegebenen Wörter überprüft werden sollen.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Allgemeine Parameter
Alle Richtlinienregeln für eine bestimmte Überwachungsrichtlinie besitzen dieselben Stapelverarbeitungsparameter und denselben Datumsbereich für die Dokumentauswahl. Diese Parameter werden auf der Seite "Zusätzliche Optionen" für die Richtlinie angegeben.



<a name="see-also"></a>Siehe auch
--------

[Überwachungsrichtlinienverletzungen und -anfragen](audit-policy-violations-cases.md)




