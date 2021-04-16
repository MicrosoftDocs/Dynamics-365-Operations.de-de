---
title: Fehlermanagement
description: In diesem Thema wird das Fehlermanagement in der Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c87bfa057fd2808551674f2acb9d654ad47e9a42
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825661"
---
# <a name="fault-management"></a>Fehlermanagement

[!include [banner](../../includes/banner.md)]

 

In der Anlagenverwaltung können Sie den Fehlerdesigner verwenden, um Fehlersymptome, Fehlerbereiche und Fehlerarten für Anlagentypen einzurichten. Auf diese Weise können Sie Fehler verwalten, die bei Anlagen erkannt werden. Darüber hinaus können Fehlerursachen und Vorschläge für das Korrigieren von Fehlern für einen Arbeitsauftrag erfasst werden.

Der Prozess für die Fehlererfassung und -verwaltung besteht aus folgenden Schritten.

1. Erstellen einer Liste der Fehlersymptome, Fehlerbereiche und Fehlerarten, die bei Ihren Anlagentypen auftreten könnten.
2. Im Fehlerdesigner das Einrichten von Symptomen, Fehlerbereichen und Fehlerarten.

Unten sind einige Beispiele angegeben, mit deren Hilfe Sie den Unterschied zwischen Fehlersymptomen, Fehlerbereichen und Fehlerarten erkennen können.

**Fehlersymptome:**

- Unausgeglichene Spannungen
- Kurzschluss
- Lärm
- Leck
- Erschütterungen

**Fehlerbereiche:**

- Elektrisch
- Mechanisch
- Hydraulisch
- Pneumatisch

**Fehlertypen:**

- Fehlerhafte Hauptstatorwicklung
- Fehlerhafte Diode
- Geänderte Wicklungen
- Fehlerhafter Generator
- Fehlerhafter Sensor

## <a name="create-fault-symptoms"></a>Erstellen von Fehlersymptomen

Gehen Sie folgendermaßen vor, um eine Liste von Symptomen zu erstellen, die im Fehlerdesigner verwendet werden können.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlersymptome** aus.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Geben Sie im Feld **Fehlersymptom** einen Namen für das Fehlersymptom ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie **Speichern**.

## <a name="create-fault-areas"></a>Erstellen von Fehlerbereichen

Gehen Sie folgendermaßen vor, um eine Liste von Bereichen oder Standorten zu erstellen, die im Fehlerdesigner verwendet werden können.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerbereiche** aus.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Geben Sie im Feld **Fehlerbereich** einen Namen für den Fehlerbereich ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie **Speichern**.

## <a name="create-fault-types"></a>Fehlertypen erstellen

Gehen Sie folgendermaßen vor, um eine Liste von Fehlertypen zu erstellen, die im Fehlerdesigner verwendet werden können.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlertypen** aus.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Geben Sie im Feld **Fehlertyp** einen Namen für den Fehlertyp ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie **Speichern**.

## <a name="set-up-the-fault-designer"></a>Einrichten des Fehlerdesigners

Im Fehlerdesigner richten Sie Fehlerdaten für Anlagentypen ein.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerdesigner** aus.
2. Wählen Sie im linken Bereich den Typ der Anlage aus, für die Sie einen Fehlerdatensatz einrichten möchten.
3. Wählen Sie im Inforegister **Fehlersymptom** **Position hinzufügen** und dann im Feld **Fehlersymptom** ein Fehlersymptom aus.
4. Wählen Sie im Inforegister **Fehlerbereich** **Position hinzufügen** und dann im Feld **Fehlerbereich** einen Fehlerbereich aus.
5. Wählen Sie im Inforegister **Fehlertyp** **Position hinzufügen** und dann im Feld **Fehlertyp** einen Fehlertyp aus.
6. Um schnell Kombinationen aller vorhandenen Fehlersymptome, -bereiche und -typen für den ausgewählten Anlagetyp erstellen zu können, wählen Sie **Fehlerkombinationen erstellen** aus. Diese Funktion ist hilfreich, wenn Sie viele Fehlersymptome, -bereiche und -typen hinzugefügt haben. Es ist einfacher, die Positionen für beliebige Kombinationen zu löschen, die nicht für den Anlagentyp relevant sind, als neue Positionen manuell zu erstellen.

    > [!NOTE]
    > Um die Einstellungen von Fehlersymptomen, -bereichen und -typen von einem Anlagentyp in den ausgewählten Anlagentyp zu kopieren, wählen Sie **Aus Anlagentyp kopieren** aus.

7. Wählen Sie **Speichern** aus, um die Änderungen zu speichern.

![Standarddesignerseite](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Fehlerursachen erstellen

Gehen Sie folgendermaßen vor, um eine Liste bekannter Fehlerursachen zu erstellen, die einem Arbeitsauftrag oder einer Wartungsanforderung hinzugefügt werden können.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerursachen** aus.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Geben Sie im Feld **Fehlerursache** einen Namen für die Fehlerursache ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie **Speichern**.

## <a name="create-fault-remedies"></a>Erstellen von Fehlerlösungen

Gehen Sie folgendermaßen vor, um eine Liste von Lösungs- und Reparaturvorschlägen zu erstellen, die einem Arbeitsauftrag oder einer Wartungsanforderung hinzugefügt werden können.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerlösungen** aus.
2. Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.
3. Geben Sie im Feld **Fehlerlösung** einen Namen für die Fehlerlösung ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie **Speichern**.

> [!NOTE]
> Sie können die Namen der Fehlersymptome, -bereiche, -typen, -ursachen und -lösungen nach Bedarf ändern. Die Namenänderungen werden automatisch in den betreffenden Fehlererfassungen angezeigt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]