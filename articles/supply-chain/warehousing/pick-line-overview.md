---
title: Richten Sie einen Menüpunkt für mobile Geräte ein, um eine Übersicht über die Entnahmepositionen bereitzustellen
description: In diesem Thema wird erläutert, wie Sie festlegen, wann eine Liste aller Arbeitspositionen für Lagerarbeiter angezeigt wird, die Lagerarbeit auf einem mobilen Gerät verarbeiten. Diese Funktion kann für Lagerarbeiter nützlich sein, die häufig eine Übersicht über die Entnahmepositionen in einem Arbeitsauftrag benötigen, um ihre Entnahmereihenfolge zu optimieren.
author: Mirzaab
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d3a8972c5d2f4c52dddef458ebd6079118cadfe
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901921"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Richten Sie einen Menüpunkt für mobile Geräte ein, um eine Übersicht über die Entnahmepositionen bereitzustellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Optionen konfigurieren, die sich auf die Übersicht von Entnahmepositionen für Menüelemente für Mobilgeräte beziehen, die zur Verarbeitung der Entnahmepositionen verwendet werden. In der Übersicht über die Entnahmepositionen können Lagerarbeiter alle Arbeitspositionen anzeigen und aus einer Liste auswählen, die sich auf ihre aktuelle Aufgabe beziehen. Diese Funktion kann den Mitarbeitern helfen, ihre Entnahmereihenfolge zu optimieren. Die Funktion bietet Optionen, die die standardmäßige **Überspringen**-Schaltfläche ersetzen, mit der die Mitarbeiter nacheinander in fester Reihenfolge durch die Positionen blättern können. (Die Option zur Verwendung dieser Schaltfläche ist jedoch weiterhin verfügbar.)

Administratoren können jeden Menüpunkt einzeln konfigurieren, um zu steuern, wie, wann und wo die Warehouse Management Mobile App die Entnahmepositionsübersicht anzeigt.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Einschalten der Funktion Arbeitsentnahmepositionen

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** _Lagerortverwaltung_
- **Funktionsname:** _Übersicht über Arbeitsentnahmepositionen_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Konfigurieren Sie Menüelemente so, dass eine Liste aller Arbeitspositionen angezeigt wird

Um einen Menüpunkt für mobile Geräte einzurichten, um eine Übersicht über die Entnahmepositionen bereitzustellen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie einen Menüpunkt oder erstellen Sie ihn, der sich auf die Entnahmearbeit bezieht, und legen Sie die folgenden Werte fest:

    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Ja*
    - **Geleitet von:** *Benutzergeleitet* oder *Systemgesteuert*

    Weitere Informationen zum Erstellen von Menüelementen und zum Verwenden der verschiedenen Einstellungen, die auf der Seite **Menüpunkte für mobile Geräte** verfügbar sind, finden Sie unter [Mobile Geräte für Lagerarbeiten einrichten](configure-mobile-devices-warehouse.md).

1. Im **Allgemeines**-Inforegister konfigurieren Sie die Funktion durch Einstellen des Feldes **Liste der Arbeitspositionen anzeigen** auf einen der folgenden Werte:

    - **Nur auf Anfrage anzeigen** – Arbeitskräfte können die Liste der Entnahmeposition anzeigen, indem sie die **Überspringen zu**-Schaltfläche in der Warehouse Management Mobile App auswählen.
    - **Zu Beginn jeder Entnahme anzeigen** – Arbeitskräfte sehen die Liste jedes Mal, wenn sie eine Entnahmeposition beginnen oder beenden. Sie können die Liste auch erneut anzeigen, indem Sie die **Überspringen zu**-Schaltfläche in der Warehouse Management Mobile App auswählen.
    - **Nur am Anfang der ersten Auswahl anzeigen**: Die Arbeitskräfte sehen die Liste jedes Mal, wenn sie mit der neuen Auswahl beginnen, jedoch nicht nach jeder Zeile. Sie können die Liste auch erneut anzeigen, indem Sie die **Überspringen zu**-Schaltfläche in der Warehouse Management Mobile App auswählen.
    - **Niemals zeigen** – Die standardmäßige **Überspringen**-Schaltfläche wird in der Warehouse Management Mobile App angezeigt und die Anzeige der Liste der Arbeitspositionen ist deaktiviert. Mit der **Überspringen**-Schaltfläche können die Arbeitskräfte nacheinander in einer festgelegten Reihenfolge durch die Positionen blättern. Sie können die Liste auch so oft durchlaufen, wie sie benötigen, bis alle Positionen verarbeitet wurden.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

    Wenn Sie das **Liste der Arbeitspositionen anzeigen**-Feld auf einen beliebigen Wert außer *Niemals zeigen* einstellen,wird die **Feldliste**-Schaltfläche im Aktionsbereich verfügbar.

1. Wählen Sie im Aktivitätsbereich **Feldliste** aus.
1. Konfigurieren Sie auf der **Feldliste**-Seite die Informationen, die die Warehouse Management Mobile App für jede Position in der Liste anzeigt.

    - Das **Primärkontrolle**-Feld ist immer auf *LineNum* festgelegt. Daher beginnt jede Position in der Liste mit einer Positionsnummer.
    - Verwenden Sie die restlichen **Anzeigefeld**-Felder, um je nach Bedarf bis zu sieben zusätzliche Anzeigefelder hinzuzufügen. Wählen Sie in jedem **Anzeigefeld**-Feld den Namen eines Arbeitszeilenfelds aus. In jeder Position wird dann ein Wert für dieses Feld angezeigt. Die Werte werden in der Reihenfolge angezeigt, die Sie hier auswählen. Sie können einige der **Anzeigefeld**-Felder leer lassen, wenn Sie nicht alle sieben Werte benötigen.

1. Wählen Sie im Aktionsbereich **Speichern** aus und schließen Sie die Seite **Feldliste**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]