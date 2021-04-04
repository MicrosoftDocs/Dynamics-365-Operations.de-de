---
title: Route mit mehreren Abschnitten einrichten
description: Dieses Thema beschreibt, wie Sie Routen mit mehreren Abschnitten für das Modul Gesamttransportkosten festlegen.
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 88e1d94f7c3a9b624447c5fc000afc3faab395f1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500429"
---
# <a name="multi-leg-journey-setup"></a>Route mit mehreren Abschnitten einrichten

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie Sie Routen mit mehreren Abschnitten für das Modul **Gesamttransportkosten** festlegen.

## <a name="legs"></a>Teilstrecken

Abschnitte werden verwendet, um separate Teile einer Route zu identifizieren. Jeder Abschnitt wird durch die Auswahl der „An“ und „Von“ Häfen und der Transportmethode, die für diesen Abschnitt verwendet wird, aufgebaut. Vorlaufzeiten können mit jedem Abschnitt verknüpft werden. Vorlaufzeiten können helfen, eine Sendung zu verfolgen und können auch verwendet werden, um das geschätzte Lieferdatum der Waren auf einer Fahrt zu berechnen. Wenn ein Abschnitt einer Route abgeschlossen ist, kann der Status der Fahrt, des Transportcontainers und der zugehörigen Zeilen für die Einkaufsbestellung über die Einrichtung der Verfolgungssteuerung aktualisiert werden. Abschnitte können von einer einzelnen Fahrtvorlage verwendet werden, oder sie können von mehreren Routenvorlagen wiederverwendet werden. Container-Ladung, Zoll und lokaler Transport werden allgemein als Abschnitte festgelegt, und es wird ein unspezifischer Lieferhafen für sie verwendet.

Um mit Abschnitten zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Einrichten von Routen mit mehreren Abschnitten \> Abschnitte**. Dort können Sie Datensätze für Abschnitte anzeigen, öffnen, erstellen und löschen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Teilstrecke | Geben Sie einen eindeutigen Identifikationsnamen/eine Nummer für den Abschnitt der Route ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Abschnitt der Route ein. Typischerweise identifiziert diese Beschreibung den „An“- und „Von“-Hafen oder die Etappe der Route. |
| Von-Port | Geben Sie den Ursprungsort der Waren auf dem Abschnitt ein. |
| Bis-Port | Geben Sie den Bestimmungsort der Waren auf dem Abschnitt ein. |
| Liefermethode | Geben Sie die Transportart für den Abschnitt ein. |

## <a name="journey-templates"></a>Reisevorlagen

Eine Fahrtvorlage definiert die Route mit mehreren Abschnitten zwischen zwei Häfen, die die Waren während einer Fahrt durchlaufen. Die Abschnitte der Route werden kombiniert, um die Zeit zu bestimmen, die die Waren für die Fahrt vom Ursprungsort des Lieferanten bis zum endgültigen Lagerort benötigen. Wenn die Abschnitte in einer bestimmten Reihenfolge in die Fahrtvorlage eingelagert werden, identifizieren die Vorlaufzeiten das Datum jedes Abschnitts und den Status der Fahrt, des Containers und der Einkaufsbestellung für die Fahrt. Sie verwenden das [Tracking-Control-Center](delivery-information-setup.md), um die Vorlaufzeiten festzulegen, die mit jedem Abschnitt verbunden sind, aus dem die Route-Vorlage besteht. Die Fahrtenvorlage wird auch verwendet, wenn die automatische Kalkulation einer Fahrt festgelegt wird. Wenn eine Route definiert ist, können die Kosten, die mit dem Transport der Waren verbunden sind, auf der Seite Autokalkulation definiert werden.

Um mit Fahrtenvorlagen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Route mit mehreren Abschnitten einrichten \> Fahrtenvorlagen**. Dort können Sie Fahrtenvorlagen ansehen, öffnen, erstellen und löschen.

Legen Sie für jede Fahrtenvorlage die folgenden Felder in der Kopfzeile fest.

| Feld | Beschreibung |
|---|---|
| Reisevorlage | Geben Sie einen eindeutigen Identifikationsnamen/eine eindeutige Nummer für die Fahrtvorlage ein. Die Fahrtvorlage beschreibt typischerweise den Ausgangs- und Zielpunkt der Route. |
| Beschreibung | Geben Sie eine Beschreibung der Route-Vorlage ein. Die Beschreibung gibt typischerweise den „Nach“- und „Von“-Hafen und die Art der Fahrt an. |

Fügen Sie im Abschnitt **Zeilen** für jeden Abschnitt der Route eine Zeile hinzu und lagern Sie die Zeilen in der richtigen Reihenfolge ein. Verwenden Sie die Pfeile **Auf** und **Ab** in der Symbolleiste, um die Reihenfolge der Zeilen zu ändern. Die folgende Tabelle beschreibt die Felder, die für jede Zeile verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Teilstrecke | Wählen Sie einen Abschnitt aus, der der Route hinzugefügt werden soll. |
| Beschreibung | Die Beschreibung des Abschnitts. |
| Von-Port | Der Hafen, der der Ursprungsort der Waren auf dem Abschnitt ist. An Hafen, der der „bis“-Hafen ist, der zur Bestimmung der Autokalkulation für eine Fahrt verwendet wird. |
| Bis-Port | Der endgültige Zielhafen der Waren auf dem Abschnitt. |
| Lieferart | Die Art der Lieferung, die für den Abschnitt verwendet wird. |
| Reise von Port | Wenn der Hafen, der für den Abschnitt angegeben ist, zur Bestimmung der Autokalkulation verwendet wird, aktivieren Sie dieses Kontrollkästchen, um ihn als Hafen „von“ der Route zu identifizieren. Dieser Hafen wird dann in der Kopfzeile der Fahrt angezeigt. |
| Reise nach Port | Wenn der Hafen, der für den Abschnitt angegeben ist, zur Bestimmung der Autokalkulation verwendet wird, aktivieren Sie dieses Kontrollkästchen, um ihn als „An“-Hafen zu kennzeichnen. Dieser Hafen wird dann in der Kopfzeile der Fahrt angezeigt. |
| Versandunternehmen | Wählen Sie die Reederei, die für den Abschnitt verwendet wird. |

## <a name="activities"></a>Aktivitäten

Die Einstellungen auf der Seite **Aktivitäten** legen die Arten von Aktivitäten fest, die im Zielhafen eines Abschnitts auftreten können. Benutzer, die auf der Seite **Alle Transportcontainer** arbeiten, können zwischen diesen Werten wählen, wenn sie die Dauer der einzelnen Aktivitäten schätzen und die tatsächliche Dauer zu Vergleichszwecken aufzeichnen.

Um Ihre Aktivitäten festzulegen, gehen Sie zu **Gesamttransportkosten \> Gesamttransportkosten einrichten \> Aktivitäten**. Dort können Sie Aktivitäten hinzufügen, entfernen und bearbeiten, indem Sie die Schaltflächen im Aktivitätsbereich verwenden.

Die folgende Tabelle beschreibt die Felder, die für jede Aktivität im Raster verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Aktivität | Der Name der Aktivität. |
| Beschreibung | Eine Beschreibung der Aktivität. |
| Versandunternehmen | Das Lieferantenkonto der Firma, die mit der Aktivität verbunden ist. |
