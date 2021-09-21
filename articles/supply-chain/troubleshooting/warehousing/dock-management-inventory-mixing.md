---
title: Bestandstypen werden vermischt, wenn ein Rampenverwaltungsprofil verwendet wird.
description: Damit ein Rampenverwaltungsprofil die Vermischung von Beständen effektiv verwalten kann, muss zuerst eine Arbeitskopfunterbrechung festgelegt werden. Auf dieser Seite wird erklärt, wie das geht.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476428"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Bestandstypen werden vermischt, wenn ein Rampenverwaltungsprofil verwendet wird.

## <a name="symptoms"></a>Symptome

Sie verwenden *Sendungskonsolidierungsrichtlinien*. Sie haben zwar ein *Rampenverwaltungsprofil* für ein *Lagerplatzprofil* festgelegt, aber wenn Arbeit erstellt wird, werden die Bestandstypen am endgültigen Lagerplatz vermischt.

## <a name="resolution"></a>Lösung

Dock-Verwaltungsprofile erfordern, dass die Arbeit im Voraus aufgeteilt wird. Mit anderen Worten, das Dock-Verwaltungsprofil erwartet, dass ein Arbeitskopf nicht mehrere Lagerplätze einlagert.

Damit das Dock-Verwaltungsprofil die Vermischung von Beständen effektiv verwalten kann, muss eine Arbeitskopfunterbrechung festgelegt werden.

In diesem Beispiel ist unser Rampenverwaltungsprofil so konfiguriert, dass **Bestandstypen, die nicht vermischt werden sollen** auf *Lieferungs-ID* festgelegt ist, und wir werden eine Arbeitskopfunterbrechung dafür einrichten:

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Wählen Sie die **Arbeitsauftragsart**, die Sie bearbeiten wollen (z.B. *Einkaufsbestellungen*).
1. Wählen Sie die zu bearbeitende Arbeitsvorlage.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Öffnen Sie die Registerkarte **Sortierung** und fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:
    - **Tabelle** - *Vorläufige Arbeitstransaktionen*
    - **Abgeleitete Tabelle** - *Zeitweilige Arbeitstransaktionen*
    - **Feld** - *Sendungs-ID*
1. Wählen Sie **OK**.
1. Sie kehren auf die Seite **Arbeitsvorlagen** zurück. Wählen Sie im Aktivitätsbereich **Arbeitskopfzeilenumbrüche** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Aktivieren Sie das Kontrollkästchen, das mit dem **Feldname** *Shipment ID* verbunden ist.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
