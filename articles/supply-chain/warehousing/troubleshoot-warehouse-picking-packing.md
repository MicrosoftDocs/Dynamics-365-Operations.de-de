---
title: Fehlerbehebung beim Entnehmen und Verpacken
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die beim Entnehmen und Verpacken in Microsoft Dynamics 365 Supply Chain Management auftreten können.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 74854fa95837dd8a133860e2a017be4c92ff84a3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645476"
---
# <a name="troubleshoot-picking-and-packing"></a>Fehlerbehebung beim Entnehmen und Verpacken

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die beim Entnehmen und Verpacken in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Ich erhalte die folgende Fehlermeldung: „Der Lagerplatz der Dimension kann nicht leer gelassen werden, wenn die Seriennummer der Dimension festgelegt ist.“

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten diese Fehlermeldung, wenn Sie einen Transportauftrag für ein serielles Element erstellen, indem Sie ein Lagerort verwenden, der für die erweiterte Lagerortverwaltung (WMS) aktiviert ist, und dann, nachdem die Arbeit abgeschlossen ist, versuchen, die Sendung zu bestätigen.

### <a name="issue-resolution"></a>Problemlösung

Das Feld **Standard-Eingangsort** ist für ein Transitlager des „von“-Lagers leer. Um dieses Problem zu beheben, geben Sie einen Standard-Empfangsort im Transitlager an. Stellen Sie sicher, dass dieser Lagerplatz über Ladungsträger gesteuert wird.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Ich erhalte die folgende Fehlermeldung: „Ungültiger Ladungsträger“.

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten diese Fehlermeldung in der Lagerort App, wenn Sie einen Ladungsträger ID scannen.

### <a name="issue-resolution"></a>Problemlösung

Vergewissern Sie sich, dass die Kennzeichen-ID in der Kennzeichentabelle vorhanden ist und dass die Elemente und Mengen auf dem Kennzeichen verfügbar sind (d.h. nicht gesperrt sind).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Ich erhalte die folgende Fehlermeldung: „Feld 'Lastgewicht'(=-%1) kann nur positive Zahlen enthalten. Die Aktualisierung wurde abgebrochen.“

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten diese Fehlermeldung, wenn bei der Verarbeitung von Arbeit von Packplätzen zu Lagerplätzen oder von Lagerplätzen zu Andockplätzen offene Arbeit vorhanden ist.

### <a name="issue-resolution"></a>Problemlösung

Um dieses Problem zu beheben, gehen Sie zu **Systemadministration \> Periodische Aufgaben \> Datenbank \> Konsistenzprüfung**, und führen Sie den Prozess für **Konsistenzprüfung für Lagerort-Lastgewicht** aus.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Ich erhalte die folgende Fehlermeldung: „Die Menge ist für die Einheit %1 nicht gültig.“

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten diese Fehlermeldung, wenn Sie versuchen, eine *Gesplittete Entnahme* über mehrere Chargen hinweg durchzuführen.

### <a name="issue-resolution"></a>Problemlösung

Die Arbeitskraft im Lager muss den Prozess *Kurzes Entnehmen* in der Lagerort App verwenden. Wenn Sie versuchen, mehrere Chargen vom selben Lagerplatz zu entnehmen, können Sie auch die Option **Voll** in der Lagerort App verwenden.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Ich kann den Bestand nicht an einen Lagerplatz verschieben, der von Ladungsträgern kontrolliert wird.

### <a name="issue-description"></a>Problembeschreibung

Sie können die entnommenen Mengen einer Ladung nicht reduzieren.

### <a name="issue-resolution"></a>Problemlösung

In früheren Versionen können Sie die entnommenen Mengen auf einer Ladung nicht reduzieren. Jetzt können Sie jedoch die Entnahme rückgängig machen und an einen Lagerplatz verschieben, der von einem Ladungsträger kontrolliert wird. Sie müssen sowohl einen **Ort**-Wert als auch einen **Kennzeichen**-Wert für die Ladezeile auf der Seite **Kommissionierte Menge reduzieren** angeben.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Kann ich einen Lieferschein oder Verpackungsinhalt nach Lagerort drucken?

### <a name="issue-description"></a>Problembeschreibung

Sie möchten einen Lieferschein oder Packungsinhalt nach Lagerort oder Standort auf der Seite **Arbeitsprüfungsvorlage Zeilenaktualisierung** drucken.

### <a name="issue-resolution"></a>Problemlösung

Wenn Sie ein Dokument über die Einstellungen der Druckverwaltung ausdrucken, schränken Sie den Umfang (Standort/Lager) über die Druckverwaltung ein, anstatt durch die Auswahl von **Druckeinstellungen bearbeiten** auf der Seite **Work-Audit-Vorlage Zeilenaktualisierung**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Ich kann einen Lieferschein nicht stornieren, nachdem er aus einem Verkaufsauftrag gebucht wurde.

### <a name="issue-description"></a>Problembeschreibung

Wenn Kommissionier- und Versandprozesse für WMS aktiviert sind, können Sie einen Lieferscheins nicht stornieren, nachdem er aus einem Verkaufsauftrag gebucht wurde.

### <a name="issue-resolution"></a>Problemlösung

Um gebuchte Lieferscheine für Artikel, die für WMS aktiviert sind, zu korrigieren, muss die Buchung aus der Ladung erfolgen, nicht aus dem Auftrag. Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Im Allgemeinen kann ein Verkaufsauftrag, der durch Lagerortverwaltungsprozesse entnommen und versandt wurde, aus der Ladung oder dem Versand und dem Verkaufsauftragsbeleg selbst Lieferscheinaktualisiert werden. Wenn Sie jedoch den Kundenauftrag vom Kundenauftragsbeleg aus Lieferscheinaktualisieren, kann die Stornierung des Lieferscheins immer noch nicht von der Ladung oder dem Kundenauftrag aus erfolgen. Daher empfehlen wir Ihnen, die Lieferscheinbuchung aus der Ladung heraus zu verwenden. In diesem Fall wird die Stornierung, die von der Ladung aus erfolgen muss, aktiviert.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Ich erhalte die folgende Fehlermeldung: „Es kann nicht genügend Arbeit für den Cluster gefunden werden.“

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie den Prozess *Systemgesteuerte Cluster-Kommissionierung* verwenden und ein Cluster-Profil konfigurieren, bei dem z.B. 10 Positionen entnommen werden können, funktioniert der Prozess wie geplant, wenn genügend Arbeit vorhanden ist, um 10 Positionen zu entnehmen. Wenn jedoch nur acht Positionen zu entnehmen sind, erhalten Sie diese Fehlermeldung, weil nicht genug Arbeit für einen Cluster vorhanden ist.

### <a name="issue-resolution"></a>Problemlösung

Um dieses Problem zu beheben, bearbeiten Sie das Clusterprofil und legen Sie die Option **Positionen aktivieren** auf *Nein* fest.
