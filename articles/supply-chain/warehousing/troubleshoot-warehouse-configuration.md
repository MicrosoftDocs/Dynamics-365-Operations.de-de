---
title: Fehlerbehebung bei der Lagerort-Konfiguration
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Konfiguration von Microsoft Dynamics 365 Supply Chain Management auftreten können.
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
ms.openlocfilehash: 1fe285f05e5f1ddcb7bd206290b9954cbdaffc75
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487096"
---
# <a name="troubleshoot-warehouse-configuration"></a>Fehlerbehebung bei der Lagerort-Konfiguration

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Konfiguration von Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Ich erhalte die folgende Fehlermeldung: „Der Ladungsträger oder Lagerplatz ist nicht gültig.“

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten diese Fehlermeldung, wenn Sie einen Ladungsträger oder einen Lagerplatz scannen.

### <a name="issue-resolution"></a>Problemlösung

Stellen Sie sicher, dass die Ladungsträger-ID nicht durch etwas anderes reserviert ist. Dieses Problem trat früher auf, wenn der Wert, den ein Benutzer in der Lagerort App gescannt hat, sowohl ein gültiger Lagerplatz als auch eine gültige Ladungsträger-ID war. Dieses Problem wurde jedoch in Version 10.0.11 behoben.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Ich erhalte die folgende Fehlermeldung: „Der Ladungsträger muss für diesen Lagerplatz angegeben werden.“

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten diese Fehlermeldung, wenn Sie einen Transportauftrag unter Verwendung eines Lagers erstellen, das für die erweiterte Lagerortverwaltung (WMS) aktiviert ist, und dann nach Abschluss der Arbeit versuchen, die Sendung zu bestätigen.

### <a name="issue-resolution"></a>Problemlösung

Das Feld **Standard-Eingangsort** ist für ein Transitlager des „von“-Lagers leer. Um dieses Problem zu beheben, geben Sie einen Standard-Empfangsort im Transitlager an. Stellen Sie sicher, dass dieser Lagerplatz über Ladungsträger gesteuert wird.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Ich erhalte die folgende Fehlermeldung: „Sie können keine Arbeitsvorlagenzeile für Bestandsstatusänderung erstellen, da der Arbeitstyp nicht gültig ist. Wählen Sie einen anderen Arbeitstyp.“

### <a name="issue-description"></a>Problembeschreibung

Für eine Arbeitsvorlage können Sie in der Spalte **Arbeitstyp** des Abschnitts **Arbeitsvorlagendetails** nicht *Bestandsstatusänderung* auswählen.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Der Arbeitstyp *Bestandsstatusänderung* wird nur von Systemprozessen verwendet. Er kann nicht konfiguriert werden. Da die Liste der Arbeitstypen als Aufzählung festgelegt ist, können die zusätzlichen Einträge nicht aus dem Dropdown-Menü **Arbeitstyp** herausgefiltert werden.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Ich erhalte die folgende Fehlermeldung: „Die Menge ist für die Einheit 1% nicht gültig.“

### <a name="issue-description"></a>Problembeschreibung

Die Menge ist für die Einheit *ea* nicht gültig, wenn es Entnahmearbeiten gibt, die mehrere Ladungsträger an einem Lagerplatz haben.

### <a name="issue-resolution"></a>Problemlösung

Stellen Sie sicher, dass die Felder **Einheit Sequenz Gruppen-ID** und **Einheit Umrechnungen** auf dem freigegebenen Produkt oder der Produktvariante korrekt festgelegt sind.

Beachten Sie, dass die Fehlermeldung in Version 10.0.15 verbessert wurde (siehe [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Die neue Fehlermeldung lautet: „Die Menge ist nicht gültig. Erwartet wird %1 %2.“

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>In Lagerplatzrichtlinien für das Einlagern von Verkaufsaufträgen wertet die Option „Mehrere SKU“ nicht mehrere Lagerplatzrichtlinien-Aktionen aus.

### <a name="issue-description"></a>Problembeschreibung

Lagerplatzrichtlinien der Arbeitsauftragsart *Verkaufsaufträge* und der Arbeitsauftragsart *Einlagern* werten nicht mehrere Lagerplatzrichtlinien-Aktionen aus, wenn die Option **Mehrere SKU** ausgewählt ist. Es wird nur die erste Aktion der Lagerplatzrichtlinie ausgewertet.

### <a name="issue-resolution"></a>Problemlösung

Eine neue Funktion, *Alle Aktionen für Multi SKU Lagerplatzrichtlinien auswerten*, wurde in Version 10.0.15 hinzugefügt (siehe [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Diese Funktion wertet alle Aktionen für Multi-SKU Lagerplatzrichtlinien aus. Wenn Sie diese Funktion benötigen, verwenden Sie [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um sie zu aktivieren.

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>Ich kann mit der Lagerort App keine Teilkommissionierung durchführen.

### <a name="issue-description"></a>Problembeschreibung

Bei Verkaufs- und Transportaufträgen können Sie keine Elemente überspringen und eine Teilkommissionierung vornehmen.

### <a name="issue-resolution"></a>Problemlösung

Legen Sie auf der Seite **Mobilgeräte-Menüelemente** für jeden Menüpunkt, der für die Bearbeitung von Verkaufsaufträgen oder Transportaufträgen eingerichtet ist, die Option **Arbeitsteilung zulassen** auf dem Inforegister **Allgemein** auf *Ja* fest.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Wie kann ich eine Bestandsstatusänderung für Teilmengenarbeiten durchführen?

### <a name="issue-description"></a>Problembeschreibung

Sie möchten eine Bestandsstatusänderung für eine Teilmenge einer Charge durchführen.

### <a name="issue-resolution"></a>Problemlösung

Um den Arbeitskräften diese Änderung zu ermöglichen, können Sie einen Menüpunkt für die Lagerort App erstellen. Erstellen (oder bearbeiten) Sie auf der Seite **Mobilgeräte-Menüpunkte** einen Menüpunkt, der die folgenden Einstellungen hat:

- **Modus:** *Arbeit*
- **Vorhandene Arbeit verwenden:** *Nein*
- **Arbeitserstellungsprozess:** *Bewegung*
- **Status des Bestands anzeigen:** *Ja*

Sie können weitere Felder auf der Seite nach Bedarf festlegen.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Das Dock-Verwaltungsprofil eines Lagerplatz-Profils verhindert nicht, dass Bestandstypen gemischt werden.

### <a name="issue-description"></a>Problembeschreibung

Sie verwenden *Sendungskonsolidierungsrichtlinien*. Sie haben ein *Dock-Verwaltungsprofil* für ein *Standortprofil* festgelegt, aber wenn Arbeit erstellt wird, werden die Bestandstypen am endgültigen Lagerplatz gemischt.

### <a name="issue-resolution"></a>Problemlösung

Dock-Verwaltungsprofile erfordern, dass die Arbeit im Voraus aufgeteilt wird. Mit anderen Worten, das Dock-Verwaltungsprofil erwartet, dass ein Arbeitskopf nicht mehrere Lagerplätze einlagert.

Damit das Dock-Verwaltungsprofil die Vermischung von Beständen effektiv verwalten kann, muss eine Arbeitskopfunterbrechung festgelegt werden.

In diesem Beispiel ist unser Dock-Verwaltungsprofil so konfiguriert, dass **Bestandstypen, die nicht gemischt werden sollen** auf *Sendungs-ID* festgelegt ist, und wir werden eine Arbeitskopfunterbrechung dafür einrichten:

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
