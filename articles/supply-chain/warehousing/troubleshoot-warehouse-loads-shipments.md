---
title: Fehlerbehebung bei Ladungserstellung und Sendungen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit der Ladungserstellung und den Sendungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994028"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Fehlerbehebung bei Ladungserstellung und Sendungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit der Ladungserstellung und den Sendungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Ich erhalte die folgende Fehlermeldung: „Sie können für diese Zeile keine Ladung erstellen, da sie Bestandsdimensionen enthält, die ungültig sind.“

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten die folgende Fehlermeldung, wenn Sie versuchen, einen Rücklieferungs-Verkaufsauftrag an das Lagerort freizugeben:

> Sie können keine Ladezeile für diese Auftragszeile erstellen, da sie Bestandsdimensionen enthält, die ungültig sind. Sie können sich nicht auf Bestandsdimensionen beziehen, die sich in der Reservierungshierarchie unterhalb der Dimension Lagerplatz befinden. Entfernen Sie die ungültigen Dimensionen aus der Auftragszeile.

### <a name="issue-resolution"></a>Problemlösung

Leider unterstützt das Produkt keine Ladungsverarbeitung für einen Rückgabeprozess. Daher können Sie den Verkaufsauftrag für die Rücklieferung nicht an das Lagerort freigeben.

Bei Verkaufsauftragstransaktionen können Sie nicht auf Bestandsdimensionen verweisen, die sich in der Reservierungshierarchie unterhalb der Dimension **Ort** befinden. Die Lösung ist, die ungültigen Dimensionen aus der Auftragszeile zu entfernen.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Ich erhalte die folgende Fehlermeldung: „Eine der Zeilen befindet sich bereits in einer Ladung. Kann nicht an das Lagerort freigegeben werden.“

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie Ladungen manuell erstellen oder den Prozess so festlegen, dass Ladungen bereits vor der Eingabe von Verkaufsauftragszeilen erstellt werden, wird davon ausgegangen, dass die anschließende Freigabe manuell erfolgt und dass der Arbeitsplan und die Einstufung aus der Ladung verwendet werden.

In einem anderen möglichen Szenario versuchen Sie, eine automatische Freigabe an das Lager durchzuführen, aber der Wellenprozess konnte keine Arbeit erstellen. Daher wird noch eine offene Sendung oder Ladung erstellt. Diese offene Sendung oder Ladung blockiert dann nachfolgende Versuche, den Auftrag automatisch freizugeben, bis Sie entweder die offene Sendung oder Ladung löschen oder die Welle manuell neu verarbeiten.

### <a name="issue-resolution"></a>Problemlösung

Sie können die Freigabe über die Seite Verkaufsauftrag oder die automatische Freigabe über die Seite Freigabe Verkaufsauftrag nur dann durchführen, wenn vor der Freigabe an das Lager keine Ladung vorhanden ist. Die Ladung wird automatisch erstellt, nachdem die Welle verarbeitet wurde.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Ich erhalte die folgende Fehlermeldung: „Die Lieferscheinkorrektur kann nicht verarbeitet werden. Der Lieferschein enthält nur Elemente, die den Prozessen der Lagerortverwaltung unterliegen, da diese von der Lieferscheinkorrektur nicht unterstützt werden.“

### <a name="issue-description"></a>Problembeschreibung

Nachdem Sie einen Lieferschein gebucht haben, können Sie ihn nicht stornieren, da die Schaltfläche **Stornieren** nicht verfügbar ist. Sie können den Lieferschein auch nicht korrigieren. Wenn Sie es versuchen, erhalten Sie diese Fehlermeldung.

### <a name="issue-resolution"></a>Problemlösung

Um gebuchte Lieferscheine für Elemente zu korrigieren, die für die erweiterte Lagerortverwaltung (WMS) aktiviert sind, müssen Sie die Buchung aus der Ladung heraus vornehmen, nicht direkt aus dem Auftrag.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Wie kann ich Arbeit aus ausgehenden Ladungen statt aus Wellen erstellen?

### <a name="issue-description"></a>Problembeschreibung

Hier ist eine Möglichkeit, dieses Problem zu reproduzieren.

1. Erstellen Sie eine ausgehende Ladung mit Hilfe eines Verkaufsauftrags oder eines Transportauftrags.
2. Geben Sie die Ladung für den Lagerort frei.
3. Beachten Sie, dass noch keine Entnahmearbeiten erzeugt wurden.

### <a name="issue-resolution"></a>Problemlösung

Wenn bei der Freigabe der Ladung sofort Arbeit erzeugt werden muss, müssen Sie die Wellenvorlage entsprechend konfigurieren. Legen Sie in der Wellenvorlage die folgenden Optionen auf *Ja* fest:

- Wellenerstellung automatisieren
- Welle bei Freigabe für Lagerort verarbeiten
- Wellenfreigabe automatisieren

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Ich kann eine teilweise ausgelieferte Ladung nicht wieder freigeben.

### <a name="issue-description"></a>Problembeschreibung

Sie können eine teilweise ausgelieferte Ladung nicht an das Lagerort freigeben. Wenn Sie die Freigabe an das Lagerort durchführen, erscheint die Meldung „Vorgang abgeschlossen“, aber es passiert nichts, und es wird keine Arbeit für die verbleibende Menge erstellt. Dieses Problem tritt auf, wenn Sie die Transportladungsfunktionalität verwenden und es eine unvollständige Reservierung gibt.

### <a name="issue-resolution"></a>Problemlösung

[KB-Problem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Teilweise versendete Ladungen können erneut versendet und verarbeitet werden“) ist in [Version 10.0.15](../get-started/whats-new-scm-10-0-15.md) behoben.
