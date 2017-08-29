---
title: Lagerortarbeitsrichtlinien
description: "Lagerortarbeitsrichtlinien steuern, ob Lagerortarbeit nach Lagerortprozesse in der Fertigung auf Grundlage Arbeitsauftragstyp, Lagerplatz für Lagerbestand und Produkt erstellt wird."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 7612003bc20f91f173629893750478b034cff27b
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="warehouse-work-policies"></a>Lagerortarbeitsrichtlinien

[!include[banner](../includes/banner.md)]


Lagerortarbeitsrichtlinien in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition steuern, ob Lagerortarbeit nach Lagerortprozesse in der Fertigung auf Grundlage Arbeitsauftragstyp, Lagerplatz für Lagerbestand und Produkt erstellt wird.

Diese Arbeitsrichtlinie steuert, ob Lagerortarbeit für Lagerortprozesse in der Fertigung erstellt wird. Sie können die Arbeitsrichtlinie einrichten, indem Sie eine Kombination von **Arbeitsauftragstypen**, einen **Bestandslagerbestand** und ein **Produkt** verwenden. Beispielsweise wird Produkt L0101 dem Ausgangslagerplatz 001 als fertig gemeldet. Das Endprodukt wird später in einem anderen Produktionsauftrag an Ausgangslagerplatz 001 verbraucht. In diesem Fall können Sie eine Arbeitsrichtlinie einrichten, um zu verhindern, dass fertige eingelagerte Waren erstellt werden, wenn Sie Produkt L0101 dem Ausgangslagerort 001 als fertig melden. Die Arbeitsrichtlinie ist eine einzelne Entität, die durch die folgenden Informationen beschrieben werden kann:

-   **Arbeitsrichtlinienname**(der eindeutige Bezeichner der Arbeitsrichtlinie)
-   **Arbeitsauftragstypen** und **Arbeitserstellungsmethode**
-   **Lagerplätze für Lagerbestand**
-   **Produkte**

## <a name="work-order-types"></a>Arbeitsauftragstypen
Sie können die folgenden Arbeitsauftragstypen auswählen:

-   Einlagerung von Fertigerzeugnissen
-   Einlagerung von Kuppel- und Nebenprodukten
-   Rohmaterialentnahme

Das Feld **Arbeitserstellungsmethode** hat den Wert **Nie**. Dieser Wert gibt an, dass die Arbeitsrichtlinie verhindert, dass Lagerortarbeit für den ausgewählten Arbeitsauftragstyp erstellt wird.

## <a name="inventory-locations"></a>Lagerplätze für Lagerbestand
Sie können einen Lagerplatz auswählen, für den die Arbeitsrichtlinie gilt. Wenn keinem Lagerplatz eine Arbeitsrichtlinie zugeordnet wird, gilt die Arbeitsrichtlinie für keine Prozesse. Auf der Seite **Lagerplätze** können Sie die Auswahl der Arbeitsrichtlinie für einen bestimmten Lagerplatz auswählen oder stornieren.

## <a name="products"></a>Produkte
Sie können ein Produkt auswählen, für den die Arbeitsrichtlinie gilt. Sie können die Arbeitsrichtlinie entweder auf alle oder auf ausgewählte Produkte anwenden.

## <a name="example"></a>Beispiel
Im folgenden Beispiel gibt es zwei Produktionsaufträge, PRD-001 und PRD-00*2*. Produktionsauftrag PRD-001 hat einen Arbeitsgang, der als **Montage** bezeichnet wird, wo Produkt SC1 an Lagerplatz O1 als fertig gestellt gemeldet ist. Produktionsauftrag PRD-002 hat einen Arbeitsgang, der als **Anstrich** bezeichnet wird und bei dem Produkt SC1 von Lagerplatz O1 verbraucht wird. Produktionsauftrag PRD-002 verbraucht auch Rohmaterial RM1 von Lagerplatz O1. RM1 wird am Lagerort BULK-001 gespeichert und wird an Lagerplatz O1 durch Lagerortarbeit für Rohmaterialentnahme entnommen. Die Entnahmearbeit wird generiert, wenn die Produktion PRD-002 freigegeben wird. 

[![Lagerortarbeitsrichtlinien](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Wenn Sie planen, eine Lagerort-Arbeitsrichtlinie dieses Szenarios zu konfigurieren, sollten Sie die folgenden Informationen berücksichtigen:

-   Lagerortarbeit für die Einlagerung von Fertigerzeugnissen ist nicht erforderlich, wenn Sie Produkt SC1 aus Produktionsauftrag PRD-001 zum Lagerplatz O1 als fertig gestellt melden. Dies liegt daran, dass beim Arbeitsgang **Anstrich** für Produktionsauftrag PRD-002 das Produkt SC1 am selben Lagerplatz benutzt wird.
-   Lagerortarbeit für Rohmaterialentnahme ist erforderlich, um Rohmaterial RM1 vom Lagerort BULK-001 zum Lagerplatz O1 zu verschieben.

Hier ist ein Beispiel der Arbeitsrichtlinie, die Sie einrichten können, basierend auf diesen Überlegungen.

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|**Name für Arbeitsrichtlinien**<br>                 |**Arbeitsauftragstypen**<br>                               |
| Kein Einlagern von 01     `                    |- Einlagerung von Fertigerzeugnissen<br>                           |
|                                         |**Lagerplätze**<br>                                      |
|                                         |- O1   |                                               |
|                                         |**Produkte** <br>                                      |
|                                         |- SC1                                                  |

Die folgenden Prozeduren bieten Schritt-für-Schritt-Anweisungen zum Einrichten der Lagerort-Arbeitsrichtlinie für dieses Szenario. Ein Beispielsetup, das zeigt, wie ein Produktionsauftrag an einen Lagerplatz als fertig gestellt gemeldet wird, der nicht kennzeichengesteuert ist, wird ebenfalls beschrieben.

## <a name="set-up-a-warehouse-work-policy"></a>Eine Lagerort-Arbeitsrichtlinie einrichten
Lagerortprozesse enthalten nicht immer Lagerortarbeit. Wenn Sie eine Arbeitsrichtlinie definieren, können Sie die Erstellung von Arbeit für Rohmaterialentnahme sowie die Einlagerung fertiger Waren für einen Satz von Produkten an bestimmten Lagerplätzen verhindern. Das Demodatenunternehmen USMF wurde verwendet, um diese Prozedur zu erstellen. 

SCHRITTE (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Wechseln Sie zu "Lagerortverwaltung" &gt; "Einstellungen" &gt; "Arbeit" &gt; "Arbeitsrichtlinien".        |
| 2.  | Klicken Sie auf "Neu".                                                                 |
| 3.  | Geben Sie im Feld "Arbeitsrichtlinienname" die Bezeichnung "Keine Einlagerungsarbeit" ein.                    |
| 4.  | Klicken Sie auf Speichern.                                                                |
| 5.  | Klicken Sie auf Hinzufügen.                                                                 |
| 6.  | Markieren Sie in der Liste die ausgewählte Zeile.                                        |
| 7.  | Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung fertiger Waren" aus.            |
| 8.  | Klicken Sie auf Hinzufügen.                                                                 |
| 9.  | Markieren Sie in der Liste die ausgewählte Zeile.                                        |
| 10. | Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung von Co-Produkt und Nebenprodukt" aus. |
| 11. | Erweitern Sie den Abschnitt "Lagerplätze für Lagerbestand".                                    |
| 12. | Klicken Sie auf Hinzufügen.                                                                 |
| 13 | Markieren Sie in der Liste die ausgewählte Zeile.                                        |
| 14. | In der Lagerortliste geben Sie "51" ein.                                         |
| 15. | Geben Sie im Feld "Lagerplatz" den Wert "001" ein oder wählen Sie ihn aus.                              |
| 16. | Erweitern Sie den Abschnitt Produkte.                                               |
| 17. | Wählen Sie im Feld "Produktauswahl" die Option "Ausgewählt" aus.                         |
| 18. | Klicken Sie auf Hinzufügen.                                                                 |
| 19. | Markieren Sie in der Liste die ausgewählte Zeile.                                        |
| 20. | Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein oder wählen Sie ihn aus.                         |
| 21. | Klicken Sie auf Speichern.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Einen Produktionsauftrag an einen Lagerplatz, der nicht kennzeichengesteuert ist, als fertig gestellt melden
Diese Prozedur zeigt ein Beispiel der Berichterstellung als beendet zu einem Lagerplatz an, der nicht kennzeichengesteuert ist. Eine anwendbare Arbeitsrichtlinie ist die Voraussetzung für diese Aufgabe. Die vorherige Prozedur zeigt das Setup der Arbeitsrichtlinie an. 

SCHRITTE (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Unteraufgabe: Richten Sie einen Ausgabelagerplatz ein</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Wechseln Sie zu Organisationsverwaltung &gt; Ressourcen &gt; Ressourcengruppen.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Wählen Sie in der Liste Ressourcengruppe "5102" aus.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klicken Sie auf Bearbeiten.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Geben Sie im Feld "Ausgangslagerort" den Wert "51" ein.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Geben Sie im Feld "Ausgangslagerplatz" den Wert "001" ein.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Lagerplatz 001 ist kein kennzeichengesteuerter Lagerplatz. Sie können einen Ausgabelagerplatz ohne Kennzeichen nur einrichten, wenn eine anwendbare Arbeitsrichtlinie für den Lagerplatz vorhanden ist.</td>
</tr>
<tr>
<td colspan="3"><strong>Unteraufgabe: Erstellen Sie einen Produktionsauftrag und melden Sie ihn als abgeschlossen</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Schließen Sie die Seite.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Wechseln Sie zu "Produktionssteuerung" &gt; "Produktionsaufträge" &gt; "Alle Produktionsaufträge".</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klicken Sie auf "Neuer Produktionsauftrag".</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Klicken Sie auf Erstellen.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Klicken Sie auf "Vorkalkulation".</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Klicken Sie auf "OK".</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Klicken Sie auf "Start".</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Klicken Sie auf die Registerkarte Allgemeines.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Wählen Sie im Feld "Stücklistenverbrauch" die Option "Nie" aus.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Klicken Sie auf "OK".</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Klicken Sie auf Fertigmeldung.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Klicken Sie auf die Registerkarte Allgemeines.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Wählen Sie "Ja" im Feld "Fehler akzeptieren" aus.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Klicken Sie auf "OK".</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Klicken Sie im Aktivitätsbereich auf "Lagerort".</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Klicken Sie auf "Arbeitsdetails".</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Wenn der Produktionsauftrag als fertig gemeldet wurde, wurde keine Arbeit für die Einlagerung generiert. Dies tritt auf, weil eine Arbeitsrichtlinie definiert ist, die verhindert, dass Arbeit generiert wird, wenn Produkt L0101 als fertig nach Lagerplatz 001 gemeldet wird.</td>
</tr>
</tbody>
</table>




