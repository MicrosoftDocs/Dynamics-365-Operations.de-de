---
title: Eingehende Fahrten und Transportcontainer-Routen verfolgen
description: In diesem Thema wird erklärt, wie Sie die Seite Eingangsverfolgung verwenden können, um den Fortschritt Ihrer eingehenden Fahrten und Transportcontainer-Fahrten zu verfolgen.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 678f2b6cda0592e0393bb15f372cb4be84778932
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501245"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Eingehende Fahrten und Transportcontainer-Routen verfolgen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Auf der Seite **Eingehende Verfolgung** können Sie den Fortschritt Ihrer eingehenden Fahrten und Transportcontainer-Fahrtn verfolgen. Jede Fahrt und Route ist in *Aktivitäten* unterteilt, von denen jede ihre eigene Zeile auf der Seite hat. Sie können die Seite verwenden, um geschätzte Termine und tatsächliche Termine pro Aktivität anzuzeigen und einzugeben.

Typischerweise zeigen diese Aktivitäten, abhängig von der Einrichtung im [Tracking-Control-Center](delivery-information-setup.md#tracking-control-center), automatisch das geschätzte Landedatum am endgültigen Zielort an. Ebenfalls abhängig von der Einrichtung aktualisiert das Enddatum in der Regel das Lieferdatum oder das bestätigte Datum auf Einkaufsbestellungszeilen. Für Umlagerungsauftragszeilen können Sie das System so festlegen, dass das Eingangsdatum aktualisiert wird.

Um die Seite **Eingehende Verfolgung** zu öffnen, gehen Sie zu **Gesamttransportkosten \> Verfolgung \> Eingehende Verfolgung**.

## <a name="filter-the-activities-list"></a>Filtern der Aktivitätenliste

Sie können die Felder **Fahrt** und **Transportcontainer** oben auf der Seite **Eingehende Verfolgung** verwenden, um die Seite so zu filtern, dass sie nur Aktivitäten anzeigt, die mit der ausgewählten Fahrt und/oder dem Transportcontainer verbunden sind.

## <a name="update-tracking-information"></a>Tracking-Informationen aktualisieren

Um den Zeitplan für eine Fahrt oder Route zu aktualisieren, geben Sie das Startdatum für die erste Aktivität ein. Das geschätzte Enddatum der letzten Aktivität wird dann aktualisiert. Die Einrichtung für jeden Abschnitt und jede Route-Vorlage im [Tracking-Control-Center](delivery-information-setup.md#tracking-control-center) bestimmt die geschätzten Vorlaufzeiten. Die geschätzten Endtermine verwenden die Vorlaufzeit ab dem Startdatum der Aktivität. Wenn dann das tatsächliche Enddatum erfasst wird, wird das Startdatum der nächsten Aktivität auf das gleiche Datum wie das tatsächliche Enddatum der vorherigen Aktivität aktualisiert. Die tatsächliche Vorlaufzeit wird aktualisiert, so dass Vergleiche und Analysen durchgeführt werden können. Zusätzliche Notizen können in das Feld **Notiz** eingegeben werden.

Die Reihenfolge der Aktivitäten im Raster wird durch die Reihenfolge der Abschnitte in der entsprechenden Route-Vorlage bestimmt. Wenn sich die Reihenfolge der Abschnitte in der angehängten Route ändert, ändert sich auch die Tracking-Steuerung.

Sie können die Termine für alle Container aktualisieren, indem Sie **Startdatum aktualisieren** oder **Ist-Enddatum aktualisieren** im Aktivitätsbereich wählen. Alternativ können Sie die Daten auch pro Container auf der Sendung eingeben. Diese Vorgehensweise erlaubt eine größere Flexibilität, da Container in einer Umgebung mit mehreren Routen aufgeteilt werden können.

## <a name="buttons-on-the-action-pane"></a>Schaltflächen im Aktivitätsbereich

Sie können die Schaltflächen im Aktivitätsbereich der Seite **Eingangsverfolgung** verwenden, um mit eingehenden Fahrtn und Fahrten zu arbeiten. Die folgende Tabelle beschreibt die zur Verfügung stehenden Schaltflächen.

| Schaltfläche | Beschreibung |
|---|---|
| Bearbeiten | Bearbeiten Sie eine Fahrt oder eine Transportcontainer-Route. |
| Neue | Erstellen Sie eine neue Fahrt oder Transportcontainer-Fahrt. |
| Löschen | Löschen einer ausgewählten Fahrt oder Transportcontainer-Fahrt. |
| Aktualisiertes Startdatum | Aktualisieren Sie das Startdatum einer Aktivität für alle Container einer Fahrt. Wenn das Startdatum einer bestimmten Aktivität oder eines Abschnitts einer Route aktualisiert wird, werden die nachfolgenden geschätzten Startdaten basierend auf der angegebenen Vorlaufzeit aktualisiert. |
| Tatsächliches Enddatum aktualisieren | Aktualisieren Sie das Enddatum einer Aktivität für alle Container auf einer Fahrt. Wenn das Enddatum einer bestimmten Aktivität aktualisiert wird, werden die nachfolgenden Aktivitäten auf der Basis der angegebenen Vorlaufzeit aktualisiert. |
| Aktivitäten hinzufügen | Manuelles Hinzufügen einer Aktivität zu einer Fahrt. Sie könnten z. B. eine Begasungsaktivität hinzufügen. Das Hinzufügen kann dazu führen, dass sich das bestätigte Lieferdatum der Waren auf dem Schiff oder der Fahrt ändert. Wenn eine Aktivität zur Route hinzugefügt wird, werden die geschätzten Tage erst eingetragen, wenn das Startdatum eines Abschnitts der Route aktualisiert wird. |

## <a name="information-and-settings-on-the-overview-tab"></a>Informationen und Einstellungen auf der Registerkarte Übersicht

Die Registerkarte **Übersicht** zeigt eine Liste aller Aktivitäten, die zu der Fahrt und/oder dem Transportcontainer gehören, der oben auf der Seite ausgewählt ist. Die folgende Tabelle beschreibt die Felder, die für jede Aktivität verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Teilstrecke | Die ID des Abschnitts für die Aktivität, wie in der Route-Vorlage definiert. |
| Lieferart | Die erwartete Liefermethode für die Aktivität. |
| Aktivität | Dieses Feld identifiziert normalerweise den Auftrag oder die Aufgabe, die mit der Aktivität verbunden ist. Typische Beispiele sind *Fahrt* und *Abfertigung*. |
| Beschreibung | Eine längere Beschreibung der Aktivität. |
| Startdatum | Dieses Feld zeigt zunächst das geschätzte Startdatum der Aktivität an. Nachdem jedoch das tatsächliche Enddatum der vorherigen Aktivität eingegeben wurde, zeigt es das tatsächliche Startdatum an. Dieses Feld wird verwendet, um das geschätzte Enddatum zu bestimmen, basierend auf der Vorlaufzeit. |
| Geschätztes Enddatum | Der Wert dieses Feldes wird auf der Basis des Startdatums und der Vorlaufzeit berechnet. Sie werden den Wert normalerweise nicht direkt bearbeiten. |
| Tatsächliches Abschlussdatum | Ein Benutzer sollte dieses Feld so schnell wie möglich aktualisieren, nachdem die Aktivität stattgefunden hat. Die tatsächliche Vorlaufzeit wird dann aktualisiert. |
| Vorkalkulierte Tagesanzahl | Die geschätzte Zeit (in Tagen), die benötigt wird, um die Aktivität abzuschließen. |
| Tatsächliche Tagesanzahl | Die tatsächliche Zeit (in Tagen), die benötigt wird, um die Aktivität abzuschließen. |
| Notiz | Verwenden Sie dieses Feld, um verschiedene Notizen und Details zur Aktivität hinzuzufügen. |

## <a name="information-and-settings-on-the-general-tab"></a>Informationen und Einstellungen auf der Registerkarte Allgemein

Die Registerkarte **Allgemein** zeigt Informationen über den Abschnitt an, der auf der Registerkarte **Übersicht** ausgewählt ist. Obwohl sie einige der Informationen wiederholt, die auf der Registerkarte **Übersicht** angezeigt werden, enthält sie auch zusätzliche Informationen über den ausgewählten Abschnitt.
