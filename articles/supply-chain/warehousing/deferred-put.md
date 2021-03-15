---
title: Verzögerte Verarbeitung der Lagerarbeit
description: In diesem Thema werden die Funktionen beschrieben, die die verzögerte Verarbeitung von Einlagerungsvorgängen in Dynamics 365 Supply Chain Management verfügbar machen.
author: josaw1
manager: tfehr
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c85dd895e18805da2d1daf5f90f64db82bdc0116
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973784"
---
# <a name="deferred-processing-of-warehouse-work"></a>Verzögerte Verarbeitung der Lagerarbeit

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die die verzögerte Verarbeitung von Lagerarbeiten in Dynamics 365 Supply Chain Management verfügbar machen.

Mit der verzögerten Verarbeitungsfunktion können Lagerarbeiter weiterhin andere Aufgaben erledigen, während im Hintergrund der Einlagerungsvorgang verarbeitet wird. Die verzögerte Verarbeitung ist hilfreich, wenn zahlreiche Arbeitspositionen verarbeitet werden müssen und die Arbeitskraft diese Arbeit asynchron verarbeiten lassen kann. Sie ist außerdem nützlich, wenn es beim Server zu spontanen oder ungeplanten Zunahmen bei der Verarbeitungszeit kommen kann und sich diese erhöhte Verarbeitungszeit auf die Produktivität des Benutzers auswirken kann.

Eine Hintergrundverarbeitung wird durch Verwendung des SysOperations-Frameworks erreicht. Weitere Informationen finden Sie unter [Übersicht über das SysOperation-Framework](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Konfigurieren der Arbeitsverarbeitungsrichtlinien

Um die verzögerte Verarbeitung zu verwenden, müssen Sie eine Arbeitsverarbeitungsrichtlinie konfigurieren.

Richtlinien werden auf der Seite **Arbeitsverarbeitungsrichtlinien** konfiguriert. In der folgenden Tabelle werden die Felder auf dieser Seite beschrieben.

| Feld                           | Beschreibung |
|---------------------------------|-------------|
| Name der Arbeitsverarbeitungsrichtlinien     | Der Name der Arbeitsverarbeitungsrichtlinien. |
| Arbeitsauftragstyp                 | Der Arbeitsauftragstyp, auf den die Richtlinie angewendet wird. |
| Vorgang                       | Der Arbeitsgang, der mithilfe der Richtlinie verarbeitet wird. |
| Arbeitsverarbeitungsmethode          | Die zur Verarbeitung der Arbeitsposition verwendete Methode. Wenn die Methode auf **Sofort** festgelegt wird, ähnelt das Verhalten dem Verhalten, wenn keine Arbeitsverarbeitungsrichtlinien verwendet werden, um die Position zu verarbeiten. Wenn die Methode auf **Verzögert** festgelegt wird, wird die verzögerte Verarbeitung verwendet, die das Batch-Framework verwendet. |
| Verzögerter Verarbeitungsschwellenwert   | Ein Wert von **0** (Null) bedeutet, dass kein Schwellenwert festgelegt ist. In diesem Fall wird die verzögerte Verarbeitung verwendet, wenn sie verwendet werden kann. Wenn die Berechnung des speziellen Schwellenwerts unterhalb des Schwellenwerts liegt, wird die Methode „Sofort“ verwendet. Andernfalls wird die verzögerte Methode verwendet, wenn sie verwendet werden kann. Bei verkaufs- und übertragungsbezogenen Arbeiten wird der Schwellenwert als die Zahl zugeordneter Quellladungspositionen berechnet, die für die Arbeit verarbeitet werden. Für wird der Wiederbeschaffungsarbeiten wird der Schwellenwert als die Anzahl von Arbeitspositionen berechnet, die wiederbeschafft werden. Wenn beispielsweise ein Schwellenwert von **5** für den Verkauf festgelegt wird, wird für kleinere Arbeiten mit weniger als fünf anfänglichen Quellladungspositionen keine verzögerte Verarbeitung verwendet, sondern nur für größere. Der Schwellenwert hat nur Auswirkungen, wenn die Arbeitsverarbeitungsmethode auf **Verzögert** festgelegt wird. |
| Chargengruppe mit verzögerter Verarbeitung |Die Stapelverarbeitungsgruppe, die für die Verarbeitung verwendet wird. |

Für verzögerte Einlagerungsaufgaben werden die folgenden Arbeitsauftragstypen unterstützt: Aufträge, Umlagerungsauftragsprobleme und Wiederbeschaffung.

## <a name="assigning-the-work-creation-policy"></a>Zuweisen der Arbeitserstellungsrichtlinie

Die Arbeitserstellungsrichtlinie kann in den Lagerortverwaltungsparametern zugewiesen werden. Sie kann auch auf der Ebene einzelner Lagerorte zugewiesen werden. Wenn die Richtlinie einem Lagerort zugewiesen wird, wird sie nur auf Arbeiten angewendet, die für diesen Lagerort erstellt werden. Wenn keine Richtlinie auf Lagerortebene zugewiesen wird, wird die Richtlinie aus den Lagerortverwaltungsparametern angewendet.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Anzeigen der verzögerten Einlagerungsaufgaben

Sie können verzögerte Einlagerungsaufgaben auf der Seite **Zurückgestellte Einlagerungsaufgaben** anzeigen.

Standardmäßig werden die **Abgeschlossenen** Aufgaben angezeigt.

| Feld            | Beschreibung |
|------------------|-------------|
| Status           | Der Status der Aufgabe. |
| Status des Batchauftrags | Der Status des verknüpften Stapelverarbeitungsauftrags. Wenn der Stapelverarbeitungsauftrag verarbeitet wurde, enthält die Chargenhistorie das Protokoll und die Informationen aus dem Stapelverarbeitungsauftrag. |

Hier ein Überblick über die möglichen Status:

- **Ausstehend** – Der zugehörige Stapelverarbeitungsauftrag wartet auf die Bearbeitung auf dem Stapelverarbeitungsserver.
- **Fehler** – Das Verarbeiten ist fehlgeschlagen. Die Aufgabe kann erneut verarbeitet werden, indem die Aktion **Verzögerte Einlagerung verarbeiten** verwendet wird, oder sie kann mithilfe der Aktion **Verzögerte Einlagerung abbrechen** storniert werden.
- **Abgeschlossen** – Der Auftrag wurde abgeschlossen.

## <a name="impact-on-closed-work-dates"></a>Auswirkungen auf abgeschlossene Arbeitstermine

Wenn die verzögerte Einlagerungsverarbeitung verwendet wird, wird der abgeschlossene Arbeitstermin als Erstellungsdatum/-uhrzeit der verzögerten Einlagerungsverarbeitungaufgaben festgelegt. Der abgeschlossene Arbeitstermin wird verwendet, weil er die beste Schätzung für den Abschluss des Einlagerungsvorgangs ist.

## <a name="reprocessing-a-failed-task"></a>Erneutes Verarbeiten einer fehlgeschlagenen Aufgabe

Sie können eine fehlgeschlagene Aufgabe erneut verarbeiten, indem Sie sie auf der Seite **Verzögerte Einlagerung verarbeiten** auswählen. Das erneute Verarbeiten entspricht einer Situation, in der der Benutzer das Einlagern über das mobile Gerät abschließt, als wäre es für die sofortige Verarbeitung festgelegt.

## <a name="canceling-failed-tasks"></a>Abbrechen fehlgeschlagener Aufgaben

Nur fehlgeschlagene Aufgaben können storniert werden. Wird eine Aufgabe abgebrochen, kann sie einem neuen Benutzer zugeordnet werden. Alternativ kann die Aufgabe dem Benutzer zugewiesen bleiben, der die Arbeit verarbeitet hat. Das Abbrechen entspricht einer Situation, in der die Arbeit wieder zum mobilen Gerät zurückgebracht wird, als ob der letzte Entnahmeschritt gerade abgeschlossen wurde und die Arbeit eingelagert werden muss. Der Benutzer kann jedoch bestimmen, dass die Arbeit „anders“ ist, da es nur den Einlagerungsschritt gibt, und der Standort entsprich dem Ort, den der erste Benutzer, der die Arbeit verarbeitet hat, als finalen Einlagerungsort hatte.

Wenn eine Aufgabe abgebrochen wird , wird die Arbeit nicht mehr durch den Sperrungsgrund der verzögerten Einlagerungsverarbeitung blockiert. Sie kann erneut mit dem mobilen Gerät verarbeitet werden.

Der Aufgabendatensatz wird gelöscht, wenn die Aufgabe abgebrochen wurde.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfigurieren des Menüs des mobilen Geräts, um die verzögerte Verarbeitungsrichtlinie zu überspringen

Sie können die Menüoption des mobilen Geräts so konfigurieren, sodass die verzögerte Verarbeitungsrichtlinie nicht verwendet wird. Die Arbeit wird dann so verarbeitet, als würde keine verzögerte VerarbeitungsrRichtlinie verwendet werden. Mit dieser Funktion kann ein Vorgesetzter eine bestimmte Menüoption verwenden, wenn keine verzögerte Einlagerung verwendet wird. Legen Sie zum Konfigurieren das Feld **Verzögerte Einlagerungsverarbeitungsrichtlinie** auf **Einstellungen überschreiben und Einlagerung synchron verarbeiten** fest. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Einschränkungen, wenn die verzögerte Einlagerungsverarbeitungsrichtlinie nicht angewendet wird

Es gibt mehrere Szenarios, bei denen die verzögerte Einlagerungsverarbeitungsrichtlinie nicht angewendet wird, obwohl die Richtlinie konfiguriert ist. Nachfolgend finden Sie einige Beispiele:

- Der manuelle Arbeitsabschluss wird verwendet.
- Die Arbeit wird mithilfe der automatische Vervollständigung abgeschlossen.
- Auditvorlagen werden verwendet.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Überwachen der verzögerten Verarbeitungsaufgaben im Arbeitsbereich „Überwachung ausgehender Arbeit“

Der Arbeitsbereich **Überwachung ausgehender Arbeit** hat zwei Kacheln, die Ihnen dabei helfen, verzögerte Einlagerungsaufgaben zu überwachen:

- **Fehlgeschlagene verzögerte Einlagerungsverarbeitungsaufgaben** – Auf dieser Kachel wird die Anzahl fehlgeschlagener Aufgaben angezeigt. Wenn es fehlgeschlagene Aufgaben gibt, muss der Lagerortleiter diese entweder erneut verarbeiten oder abbrechen, da sie nicht automatisch erneut verarbeitet werden.
- **Ausstehende verzögerte Einlagerungsverarbeitungsaufgaben** – Auf dieser Kachel wird die Anzahl von Aufgaben angezeigt, die seit mehr als 10 Minuten den Status **Ausstehend** aufweisen. Wenn auf der Kachel eine Anzahl angezeigt wird, kann dies darauf hinweisen, dass beim Stapelverarbeitungsvorgang ein Problem aufgetreten ist. Sie können die **ausstehenden** Aufgaben manuell verarbeiten. Wenn der Stapelverarbeitungsvorgang für eine Aufgabe später verarbeitet wird, schlägt er einfach fehl, weil er bereits bearbeitet wurde. Es gibt keine Auswirkungen.

## <a name="deleting-completed-tasks"></a>Löschen abgeschlossener Aufgaben

Sie können verzögerte Einlagerungsverarbeitungsaufgaben löschen, die abgeschlossen wurden, indem Sie sie auswählen und sie auf der Seite löschen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]