---
title: Verfügbare Budgetmittel
description: In diesem Thema werden die Funktion „Budgetmittel“ verfügbar vorgestellt und Informationen bereitgestellt, die Sie bei der Konfiguration der Budgetsteuerung unterstützen, um die Verwaltung der Finanzressourcen Ihres Unternehmens zu optimieren.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891314"
---
# <a name="budget-funds-available"></a>Verfügbare Budgetmittel

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema werden die Funktion „Budgetmittel“ verfügbar vorgestellt und Informationen bereitgestellt, die Sie bei der Konfiguration der Budgetsteuerung unterstützen, um die Verwaltung der Finanzressourcen Ihres Unternehmens zu optimieren.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Verbesserte Berechnungsfunktion für „Budgetmittel verfügbar“

Mit der **Nur Beträge in der Berechnung der verfügbaren Haushaltsmittel verfolgen**-Funktion können Sie die zugrunde liegenden Budgetkontrolltabellen für Dokumenttypen und -Status basierend auf den Einstellungen auf der Seite **Budgetkontrollparameter definieren** protokollieren.

Einige Konfigurationsoptionen für die Budgetkontrolle müssen über bestimmte Einstellungen verfügen, damit die Funktion ordnungsgemäß funktioniert. Diese Optionen werden auf der Registerkarte **Budgetmittel verfügbar** der Seite **Budgetkontrollparameter definieren** ausgewählt oder gelöscht. Die folgende Tabelle zeigt die Einstellungen, die für die Funktion „Budgetmittel verfügbar“ erforderlich sind.

| Bei Auswahl dieser Option | Diese Option muss auch ausgewählt werden |
| ------------------------- | -------------------------------- |
| Budgetreservierungen für Vorabbelastungen | Budgetreservierungen für Belastungen *und* Tatsächliche Ausgaben |
| Budgetreservierungen für Belastungen | Tatsächliche Aufwendungen |
| Budgetreservierungen für Belastungen mit Belegen vom Typ Bestellanforderung | Budgetreservierungen für Vorabbelastungen |

Diese Funktion betrifft nur neue Belege. Beträge für vorhandene Belege werden weiterhin verfolgt und in der Budgetkontroll-Statistikabfrage angezeigt, bis eine Einstellung der verfügbaren Budgetmittel geändert und die neue Budgetkontrollkonfiguration aktiviert wird. An diesem Punkt werden die Budgetverfolgungsdaten für Dokumente entfernt, die aus der Berechnung der verfügbaren Budgetmittel entfernt wurden.

Wir empfehlen Ihnen, die Option **Nicht gebuchte tatsächliche Ausgaben** gelöscht lassen. Wenn sie ausgewählt ist, wird eine zeitaufwändige Budgetkontrollberechnung für noch nicht gebuchte Belege wie ausstehende Kreditorenrechnungen durchgeführt.
