---
title: Kennzeichenempfang über die Warehousing Mobile App
description: In diesem Thema wird erläutert, wie Sie die Warehousing-App so einrichten, dass die Verwendung eines Kennzeichenempfangsprozesses zum Empfangen von Inventar unterstützt wird.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261334"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a>Kennzeichenempfang über die Warehousing Mobile App

In diesem Thema wird erläutert, wie Sie die Warehousing-Mobile-App einrichten, so dass sie die Verwendung eines Kennzeichenempfangsprozesses zum Empfangen von Bestand unterstützt.

Mit dieser Funktion können Sie schnell den Eingang des eingehenden Bestands aufzeichnen, der sich auf eine Vorabmitteilung (ASN) bezieht. Das System erstellt automatisch einen Lieferavis, wenn Lagerverwaltungsprozesse zum Versenden eines Transportauftrags verwendet werden. Für den Bestellvorgang kann ein ASNs manuell erfasst oder mithilfe eines eingehenden ASN-Datenentitätsprozesses automatisch importiert werden.

Die ANS-Daten werden mit Ladungen und Sendungen über die *Verpackungsstrukturen* verknüpft, wo Paletten (übergeordnete Kennzeichen) Fälle enthalten können (verschachtelte Kennzeichen).

> [!NOTE]
> Um die Anzahl der Bestandtransaktionen zu verringern, wenn Verpackungsstrukturen mit verschachtelten Kennzeichen verwendet werden, zeichnet das System das physische Inventar auf dem übergeordneten Kennzeichen auf. Um die Verschiebung des physischen Bestands vom übergeordneten Kennzeichen zu den verschachtelten Kennzeichen basierend auf den Daten der Verpackungsstruktur auszulösen, muss das mobile Gerät einen Menüpunkt bereitstellen, der auf dem Arbeitserstellungsprozess *auf verschachtelte Kennzeichen packen* basiert.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Zeigen Sie die empfangende Zusammenfassungsseite an oder überspringen Sie sie

Sie können die Funktion *Steuern Sie, ob auf Mobilgeräten eine Empfangsübersichtsseite angezeigt werden soll* verwenden, um einen zusätzlichen detaillierten Warehouse-App-Ablauf als Teil des Kennzeichenempfangsprozesses zu nutzen.

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist diese Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Steuern Sie, ob auf Mobilgeräten eine Empfangsübersichtsseite angezeigt werden soll*

Wenn diese Funktion aktiviert ist, bieten Menüelemente für mobile Geräte zum Empfangen von Kennzeichen oder zum Empfangen und Einlagerungen eine Einstellung **Empfangsübersichtsseite anzeigen** an. Diese Einstellung bietet folgende Optionen:

- **Eine detaillierte Zusammenfassung anzeigen** – Während des Empfangs des Kennzeichens wird den Mitarbeitern eine zusätzliche Seite mit den vollständigen ASN-Informationen angezeigt.
- **Überspringen Sie die Zusammenfassung** – Die Mitarbeiter sehen nicht die vollständigen ASN-Informationen. Lagerarbeiter können während des Empfangsprozesses auch keinen Dispositionscode festlegen oder Ausnahmen hinzufügen.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Verhindern Sie, dass Kennzeichen mit Transportauftragsversand in anderen Lagern als dem Ziellager verwendet werden

Ein Kennzeichenempfangsprozess kann nicht verwendet werden, wenn ein ASN eine Kennzeichen-ID enthält, die bereits vorhanden ist und physische Daten an einem anderen Lagerort als dem Lagerort enthält, an dem die Kennzeichenregistrierung erfolgt.

Für Transportauftragsszenarien, in denen das Transitlager keine Kennzeichen erfasst (und daher auch keinen physischen Lagerbestand pro Kennzeichen erfasst), können Sie die Funktion *Verhindern Sie, dass Versandkennzeichen für Transportaufträge in anderen Lagern als dem Ziellager verwendet werden* verwenden, um physische Aktualisierungen von unterwegs befindlichen Kennzeichen zu verhindern.

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist diese Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Verhindern Sie, dass Kennzeichen mit Transportauftragsversand in anderen Lagern als dem Ziellager verwendet werden*

Führen Sie die folgenden Schritte aus, um die Funktionalität zu verwalten, wenn diese Funktion verfügbar ist.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Auf der Registerkarte **Allgemeines** im Inforegister **Kennzeichnung** legen Sie das Feld **Kennzeichenrichtlinie für Transitlager** auf einen der folgenden Werte fest:

    - **Wiederverwendung von nicht verfolgtem Kennzeichen zulassen** – Das System funktioniert genauso wie wenn die Funktion *Verhindern Sie, dass Versandkennzeichen für Transportaufträge in anderen Lagern als dem Ziellager verwendet werden* nicht verfügbar ist. Dieser Wert ist die Standardeinstellung, wenn Sie die Funktion zum ersten Mal aktivieren.
    - **Verhindern Sie die Wiederverwendung von nicht verfolgten Kennzeichen** – Bis zum Eingang des Überweisungsauftrags sind im Ziellager nur Aktualisierungen zulässig, die sich auf ein versendetes Kennzeichen beziehen.

## <a name="more-information"></a>Weitere Informationen

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Weitere Informationen zu Menüelementen für Mobilgeräte finden Sie unter [Richten Sie mobile Geräte für die Lagerarbeit ein](configure-mobile-devices-warehouse.md).
