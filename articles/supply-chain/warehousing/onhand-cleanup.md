---
title: Einzelvorgang zur Eingangsbereinigung in der Lagerortverwaltung
description: In diesem Artikel wird der Bereinigungsjob für vorhandene Einträge beschrieben, mit dem die Systemleistung verbessert werden kann, indem verwandte, aber nicht benötigte Datensätze identifiziert und gelöscht werden.
author: perlynne
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: df20f00a639d237bf8446f24a2ad4cbbfcf36615
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334384"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Einzelvorgang zur Eingangsbereinigung bei der Lagerortverwaltung

[!include [banner](../includes/banner.md)]

Die Leistung von Abfragen, die zur Berechnung des Lagerbestands verwendet werden, wird durch die Anzahl der Datensätze in den beteiligten Tabellen beeinflusst. Eine Möglichkeit zur Verbesserung der Leistung besteht darin, die Anzahl der Datensätze zu verringern, die die Datenbank berücksichtigen muss.

Dieser Artikel beschreibt den Bereinigungsauftrag für Lagerbestände, der nicht benötigte Datensätze in den Tabellen `InventSum` und `WHSInventReserve` löscht. In diesen Tabellen werden Informationen zu Artikeln gespeichert, die für die Lagerverwaltungsverarbeitung aktiviert sind. (Diese Elemente werden als WMS-Elemente bezeichnet.) Das Löschen dieser Datensätze kann die Leistung der vorhandenen Berechnungen erheblich verbessern.

## <a name="what-the-cleanup-job-does"></a>Was macht der Bereinigungsjob

Der Bereinigungsauftrag für Lagerbestände löscht alle Datensätze in den Tabellen `WHSInventReserve` und `InventSum`, bei denen alle Feldwerte *0* (Null) sind. Diese Datensätze können gelöscht werden, da sie nicht zu den verfügbaren Informationen beitragen. Der Job löscht nur Datensätze, die unter der Ebene **Standort** liegen.

Wenn eine negative Inventur zulässig ist, kann der Bereinigungsjob möglicherweise nicht alle relevanten Einträge löschen. Der Grund für diese Einschränkung ist, dass der Job ein spezielles Szenario zulassen muss, in dem eine Kennzeichnung mehrere Seriennummern hat und eine dieser Seriennummern negativ geworden ist. Beispielsweise verfügt das System Null verfügbar auf Kennzeichenebene, wenn ein Kennzeichen +1 Stück der Seriennummer 1 und –1 Stück der Seriennummer 2 enthält. In diesem speziellen Szenario führt der Job eine Löschung mit der Breite zuerst durch, wobei versucht wird, zuerst von den niedrigeren Ebenen zu löschen.

## <a name="schedule-and-configure-the-cleanup-job"></a>Planen und konfigurieren Sie den Bereinigungsjob

Der Bereinigungsjob für vorhandene Einträge ist unter **Lagerverwaltung \> Periodische Aufgaben \> Bereinigen \> Bereinigung der Lagereinträge** verfügbar. Verwenden Sie die Standardjobeinstellungen, um den Umfang und den Zeitplan für die Ausführung des Jobs zu steuern. Darüber hinaus stehen folgenden Einstellungen zur Verfügung:

- **Löschen, wenn für diese vielen Tage nicht aktualisiert** – Geben Sie die Mindestanzahl von Tagen ein, die der Job warten soll, bevor ein vorhandener Eintrag gelöscht wird, der auf Null gesunken ist. Verwenden Sie diese Einstellung, um das Risiko zu verringern, dass noch verwendete Einträge gelöscht werden. Wenn Sie möchten, dass die Bereinigung so schnell wie möglich erfolgt, geben Sie entweder *0* (Null) ein oder lassen Sie das Feld leer.
- **Maximale Ausführungszeit (Stunden)** – Geben Sie die maximale Ausführungszeit des Bereinigungsjobs in Stunden ein. Wenn der Auftrag nicht vor Ablauf dieser Zeit abgeschlossen wird, speichert er die bisher abgeschlossene Arbeit und schließt sich dann selbst. Diese Funktion ist besonders relevant für Implementierungen mit hohem Lagerbestand. In diesen Fällen sollten Sie den Job so planen, dass er zu Zeiten ausgeführt wird, in denen die Systemlast so gering wie möglich ist. Wenn Sie möchten, dass der Stapeljob so lange ausgeführt wird, bis er abgeschlossen ist, geben Sie entweder *0* (Null) ein oder lassen Sie das Feld leer. Diese Einstellung ist nur verfügbar, wenn die zugehörige Funktion [für Ihr System eingeschaltet](#max-execution-time) wurde.

Obwohl Sie den Job während der regulären Geschäftszeiten ausführen können, empfehlen wir, ihn außerhalb der Arbeitszeiten auszuführen. Auf diese Weise können Sie Konflikte vermeiden, die auftreten können, wenn ein Benutzer mit einem Datensatz arbeitet, der ebenfalls bereinigt wird.

Wenn der Einzelvorgang versucht, einen Datensatz für ein Element zu löschen, während dieser Datensatz von einem anderen Benutzer verwendet wird, tritt entweder für den Bereinigungsvorgang oder für den Benutzer ein Deadlock-Fehler auf.

Wenn der Einzelauftrag ausgeführt wird, hat er eine Festschreibungsgröße von 100. Mit anderen Worten, es wird versucht, einmal pro 100 Löschungen eine Bestätigung durchzuführen. Da einige Löschvorgänge jedoch satzbasiert sind, kann es Szenarien geben, in denen mehr als 100 Datensätze in derselben Transaktion gelöscht werden können. Daher können manchmal immer noch Sperreneskalationen auftreten.

## <a name="possible-user-impact"></a>Mögliche Auswirkungen auf den Benutzer

Benutzer sind möglicherweise betroffen, wenn der Bereinigungsjob für vorhandene Einträge alle Datensätze für eine bestimmte Ebene (z. B. die Kennzeichenebene) löscht. In diesem Fall funktioniert die Funktionalität zum Anzeigen, dass bei einer Kennzeichnung zuvor Bestand verfügbar war, möglicherweise nicht wie erwartet, da die entsprechenden verfügbaren Einträge nicht mehr verfügbar sind. Dies kann beispielsweise in den folgenden Situationen auftreten:

- Für die **Bestandsliste**, wenn der Benutzer die Bedingung **Menge \<\> 0** abwählt oder die Bedingung **Abgeschlossene Transaktionen** in den Einstellungen für **Dimensionsanzeige** auswählt.
- In einem Bericht **Physischer Bestand pro Bestandsdimension** für vergangene Perioden, wenn der Benutzer den Parameter **Ab** festlegt.

Die Leistungsverbesserung, die der Einzelvorgang zur Bereinigung bietet, sollte diese geringfügigen Funktionsverluste jedoch ausgleichen.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Stellen Sie die Einstellung maximale Ausführungszeit zur Verfügung

Die Einstellung für die **maximale Ausführungszeit** ist nur verfügbar, wenn die Funktion *Maximale Ausführungszeit für den Einzelvorgang „Bereinigen der Lagerbestandseinträge für die Lagerortverwaltung“* eingeschaltet ist. Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Administratoren können diese Funktion ein- oder ausschalten, indem sie nach der Funktion *Maximale Ausführungszeit für den Einzelvorgang „Bereinigen der Lagerbestandseinträge für die Lagerortverwaltung“* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]