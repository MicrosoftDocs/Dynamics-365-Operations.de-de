---
title: Einzelvorgang zur Eingangsbereinigung bei der Lagerortverwaltung
description: In diesem Thema wird der Bereinigungsjob für vorhandene Einträge beschrieben, mit dem die Systemleistung verbessert werden kann, indem verwandte, aber nicht benötigte Datensätze identifiziert und gelöscht werden.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 9d01c577fc33564d3517d242e9b01f73cc8e079c
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429088"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Einzelvorgang zur Eingangsbereinigung bei der Lagerortverwaltung

Die Leistung von Abfragen, die zur Berechnung des Lagerbestands verwendet werden, wird durch die Anzahl der Datensätze in den beteiligten Tabellen beeinflusst. Eine Möglichkeit zur Verbesserung der Leistung besteht darin, die Anzahl der Datensätze zu verringern, die die Datenbank berücksichtigen muss.

In diesem Thema wird der Bereinigungsjob für vorhandene Einträge beschrieben, mit dem nicht benötigte Datensätze in den Tabellen InventSum und WHSInventReserve gelöscht werden. In diesen Tabellen werden Informationen zu Artikeln gespeichert, die für die Lagerverwaltungsverarbeitung aktiviert sind. (Diese Elemente werden als WHS-Elemente bezeichnet.) Das Löschen dieser Datensätze kann die Leistung der vorhandenen Berechnungen erheblich verbessern.

## <a name="what-the-cleanup-job-does"></a>Was macht der Bereinigungsjob

Der Bereinigungsjob für vorhandene Einträge löscht alle Datensätze in den Tabellen WHSInventReserve und InventSum, in denen sich alle Feldwerte befinden *0* (Null). Diese Datensätze können gelöscht werden, da sie nicht zu den verfügbaren Informationen beitragen. Der Job löscht nur Datensätze, die unter der Ebene **Standort** liegen.

Wenn eine negative Inventur zulässig ist, kann der Bereinigungsjob möglicherweise nicht alle relevanten Einträge löschen. Der Grund für diese Einschränkung ist, dass der Job ein spezielles Szenario zulassen muss, in dem eine Kennzeichnung mehrere Seriennummern hat und eine dieser Seriennummern negativ geworden ist. Beispielsweise verfügt das System Null verfügbar auf Kennzeichenebene, wenn ein Kennzeichen +1 Stück der Seriennummer 1 und –1 Stück der Seriennummer 2 enthält. In diesem speziellen Szenario führt der Job eine Löschung mit der Breite zuerst durch, wobei versucht wird, zuerst von den niedrigeren Ebenen zu löschen.

## <a name="schedule-and-configure-the-cleanup-job"></a>Planen und konfigurieren Sie den Bereinigungsjob

Der Bereinigungsjob für vorhandene Einträge ist unter **Bestandsverwaltung \> Periodische Aufgaben \> Bereinigen \> Bereinigung der Lagereinträge** verfügbar. Verwenden Sie die Standardjobeinstellungen, um den Umfang und den Zeitplan für die Ausführung des Jobs zu steuern. Darüber hinaus stehen folgenden Einstellungen zur Verfügung:

- **Löschen, wenn für diese vielen Tage nicht aktualisiert** – Geben Sie die Mindestanzahl von Tagen ein, die der Job warten soll, bevor ein vorhandener Eintrag gelöscht wird, der auf Null gesunken ist. Verwenden Sie diese Einstellung, um das Risiko zu verringern, dass noch verwendete Einträge gelöscht werden. Wenn Sie möchten, dass die Bereinigung so schnell wie möglich erfolgt, geben Sie entweder *0* (Null) ein oder lassen Sie das Feld leer.
- **Maximale Ausführungszeit (Stunden)** – Geben Sie die maximale Ausführungszeit des Bereinigungsjobs in Stunden ein. Wenn der Auftrag nicht vor Ablauf dieser Zeit abgeschlossen wird, speichert er die bisher abgeschlossene Arbeit und schließt sich dann selbst. Diese Funktion ist besonders relevant für Implementierungen mit hohem Lagerbestand. In diesen Fällen sollten Sie den Job so planen, dass er zu Zeiten ausgeführt wird, in denen die Systemlast so gering wie möglich ist. Wenn Sie möchten, dass der Stapeljob so lange ausgeführt wird, bis er abgeschlossen ist, geben Sie entweder *0* (Null) ein oder lassen Sie das Feld leer. Diese Einstellung ist nur verfügbar, wenn die zugehörige Funktion [in Ihrem System eingeschaltet](#max-execution-time) wurde.

Obwohl Sie den Job während der regulären Geschäftszeiten ausführen können, empfehlen wir, ihn außerhalb der Arbeitszeiten auszuführen. Auf diese Weise können Sie Konflikte vermeiden, die auftreten können, wenn ein Benutzer mit einem Datensatz arbeitet, der ebenfalls bereinigt wird.

Wenn der Einzelvorgang versucht, einen Datensatz für ein Element zu löschen, während dieser Datensatz von einem anderen Benutzer verwendet wird, tritt entweder für den Bereinigungsvorgang oder für den Benutzer ein Deadlock-Fehler auf.

Wenn der Einzelauftrag ausgeführt wird, hat er eine Festschreibungsgröße von 100. Mit anderen Worten, es wird versucht, einmal pro 100 Löschungen eine Bestätigung durchzuführen. Da einige Löschvorgänge jedoch satzbasiert sind, kann es Szenarien geben, in denen mehr als 100 Datensätze in derselben Transaktion gelöscht werden können. Daher können manchmal immer noch Sperreneskalationen auftreten.

## <a name="possible-user-impact"></a>Mögliche Auswirkungen auf den Benutzer

Benutzer sind möglicherweise betroffen, wenn der Bereinigungsjob für vorhandene Einträge alle Datensätze für eine bestimmte Ebene (z. B. die Kennzeichenebene) löscht. In diesem Fall funktioniert die Funktionalität zum Anzeigen, dass das Inventar zuvor auf einer Kennzeichnung verfügbar war, möglicherweise nicht wie erwartet arbeitet, da die entsprechenden verfügbaren Einträge nicht mehr verfügbar sind. (Diese Funktion überprüft die Bedingung **Menge \<\> 0** in dem die **Dimensionsanzeige** Einstellungen, wenn Benutzer vorhandene Informationen anzeigen.) Die Leistungsverbesserung, die der Bereinigungsvorgang bietet, sollte diesen kleinen Funktionsverlust jedoch ausgleichen.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Stellen Sie die Einstellung maximale Ausführungszeit zur Verfügung

Standardmäßig ist die Einstellung **Maximale Ausführungszeit** nicht verfügbar. Wenn Sie es verwenden möchten, müssen Sie die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um die zugehörige Funktion in Ihrem System zu aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Maximale Ausführungszeit für den Bereinigungsvorgang für Lagereinträge*
