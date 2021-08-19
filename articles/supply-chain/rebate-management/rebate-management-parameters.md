---
title: Rückvergütungsverwaltungsparameter
description: In diesem Thema wird die Seite mit den Rückvergütungsverwaltungsparametern beschrieben. Diese Seite enthält Einstellungen, die sich auf Buchungen, Statusaktualisierungen, Nummernkreise und anderes Verhalten auswirken.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9afff67d043d00ade83a522cf801f2b0af7929f512c83040a37f3de0cf0e2579
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780003"
---
# <a name="rebate-management-parameters"></a>Rückvergütungsverwaltungsparameter

[!include [banner](../includes/banner.md)]

Die Seite **Rückvergütungsverwaltungsparameter** wird verwendet, um Einstellungen zu definieren, die im ganzen Modul **Rückvergütungsverwaltung** gelten. Diese Einstellungen wirken sich auf Buchungen, Statusaktualisierungen, Nummernkreise und anderes Verhalten aus. Die Einstellungen auf dieser Seite werden von verschiedenen juristischen Personen gemeinsam genutzt und kann von Benutzern mit den entsprechenden Sicherheitsberechtigungen geändert werden.

Um die Seite **Parameter der Rabattverwaltung** zu öffnen, gehen Sie zu **Rabattverwaltung \> Einrichten \> Parameter der Rabattverwaltung**. Legen Sie dann die Felder wie beschrieben in den folgenden Unterkapiteln beschrieben fest.

## <a name="rebate-management-tab"></a>Registerkarte „Rückvergütungsverwaltung“

Die folgende Tabelle beschreibt die Felder, die auf der Registerkarte **Rückvergütungsverwaltung** der Seite **Rückvergütungsverwaltungsparameter** verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Standardstatus | Wählen Sie den Standardstatus für alle neuen Deals. Benutzen Sie, um die zur Auswahl verfügbaren Statuswerte zu definieren, die [Seite **Rückvergütungsstatus**](rebate-statuses.md). |
| Prozess nach Dimension | Wählen Sie aus, ob Rückstellungs-, Rückvergütungs- und Abschreibungstransaktionen nach Finanzdimension verarbeitet werden sollen. Wenn diese Option aktiviert ist, verwendet das System finanzielle Dimensionen aus den Quelltransaktionen in den Zieltransaktionen. |
| Überprüfen, ob zuvor gebucht | <p>Wählen Sie das Systemverhalten aus, wenn nicht gebuchte Rückvergütungstransaktionen im selben Zeitraum mehrmals verarbeitet werden:</p><ul><li>**Warnung** – Das System ermöglicht es Benutzern, die ursprünglichen Transaktionspositionen zu überschreiben, es wird jedoch eine Warnung angezeigt.</li><li>**Fehler** – Das System verhindert, dass Benutzer die ursprünglichen Transaktionspositionen überschreiben, und es wird eine Fehlermeldung angezeigt. |
| Erfassungen automatisch buchen | Wählen Sie aus, ob das System vorgeschlagene Erfassungen automatisch buchen soll. Dazu gehören tägliche Erfassungen, die für Rückstellungen und Debitorenabzüge verwendet werden, sowie Erfassungen für Kreditorensteuerrechnungen. |
| Freitextrechnungen automatisch buchen | Wählen Sie aus, ob das System Freitextrechnungen automatisch buchen soll. Diese Option gilt nur für Freitextrechnungen, für die der Zahlungstyp *Steuerrechnungs-Debitorabzüge* festgelegt ist. |
| Auftragsreferenz für Rückvergütungsartikel | Wählen Sie die Rabattreferenz, die auf Verkaufsaufträgen und Bestellungen verwendet werden soll, die aus dem Rabattprozess generiert werden (*Keine*, *Rabattverwaltungsgeschäft*, *Rabattverwaltungsnummer*, *Rabatttransaktionsnummer* oder *Beleghinweise*). |
| Anspruchsprozess nutzen | <p>Legen Sie diese Option auf *Ja* fest, um einen Anspruchsprozess zu nutzen. So können Sie Transaktionen, die von der Rückvergütungsverwaltung erstellt werden, als beansprucht oder nicht beansprucht markieren und dann nur die beanspruchten Transaktionen buchen.</p><p>Sie berechnen beispielsweise Rückvergütungen für Transaktionen eines Monats, der Debitor hat jedoch zwei Tage nichts beansprucht. In diesem Fall werden die nicht beanspruchten Transaktionen neu erstellt, wenn Sie das nächste Mal die Funktion *Verarbeiten* für die nächste Periode ausführen.</p><p>Wenn Sie diese Option auf *Nein* setzen, werden alle Anspruchstransaktionen gebucht.</p> |
| Auftragstyp Erfassung einschließen | Für Deals oder Dealpositionen, für die der Transaktionstyp *Auftrag* festgelegt wird mit dieser Option gesteuert, ob ein Auftrag vom Typ *Erfassung* enthalten sein sollte. Es erhöht die Flexibilität, wenn diese Auftragstypen in Szenarien verwendet werden, in denen eine Rückvergütung noch nicht gelten sollte. |

## <a name="number-sequences-tab"></a>Registerkarte Nummernkreise

Verwenden Sie die Registerkarte **Nummernkreise** auf der Seite **Rückvergütungsverwaltungsparameter** zum Zuweisen von Codes zu den verschiedenen Nummernkreisen, die von der Rückvergütungsverwaltung verwendet werden. Die folgende Tabelle beschreibt den Zweck dieser einzelnen Nummernkreise. Weitere Informationen zu Nummernkreisen finden Sie unter [Nummernkreise – Übersicht](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) und den dazugehörigen Themen.

| Referenz | Beschreibung |
|---|---|
| Rabattverwaltungsgeschäft | Der Nummernkreis weist jedem Rückvergütungsdeal einen eindeutigen Schlüsselwert zu. Dieser Schlüssel wird verwendet, wenn Deals erstellt werden. |
| Rabattverwaltungsnummer | Der Nummernkreis weist jeder Rückvergütung einen eindeutigen Schlüsselwert zu. Dieser Schlüssel wird verwendet, um Rückvergütungsbeziehungen zu identifizieren. |
| Rückvergütungstransaktionsnummer | Der Nummernkreis weist jeder Rückvergütungstransaktion einen eindeutigen Schlüsselwert zu. Dieser Schlüssel wird verwendet, um Rückvergütungstransaktionen zu identifizieren. |
| Steuerrechnung | Der Nummernkreis weist jeder Rückvergütungsrechnung einen eindeutigen Schlüsselwert zu. Dieser Schlüssel wird verwendet, wenn Rückvergütungserfassungen automatisch gebucht werden. |

## <a name="feature-visibility-tab"></a>Registerkarte Sichtbarkeit der Funktionen

Die Rückvergütungsverwaltung fügt Funktionen (Felder und Funktionen) zu mehreren häufig verwendeten Seiten in Microsoft Dynamics 365 Supply Chain Management hinzu. Dazu gehören Seiten, die sich auf Aufträge und Verkaufsdeals beziehen. Wenn Sie die Rückvergütungsverwaltung verwenden, müssen Sie diese Funktionen überall sichtbar machen, bevor Sie sie nutzen können. Wenn Sie die Rückvergütungsverwaltung nicht benutzen, können Sie die Funktionen ausblenden, damit sie Sie nicht stören.

Legen Sie auf der Registerkarte **Sichtbarkeit der Funktionen** der Seite **Rückvergütungsverwaltungsparameter** die Option **Aktivieren** auf *Ja* fest, um Funktionen für die Rückvergütungsverwaltung überall sichtbar zu machen, wo sie verfügbar sind. Legen Sie sie auf *Nein* fest, um die Funktionen auf allgemeinen Seiten außerhalb des Moduls **Rückvergütungsverwaltung** auszublenden. Aber auch wenn die Option auf *Nein* festgelegt ist, bleibt das Modul selbst, einschließlich der Seite **Rückvergütungsverwaltungsparameter**, für Benutzer verfügbar, die die entsprechenden Berechtigungen für den Zugriff darauf haben.
