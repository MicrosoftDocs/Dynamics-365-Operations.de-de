---
title: Auslastungsnutzung planen
description: In diesem Thema wird erläutert, wie die Auslastung für einen Lagerort eingerichtet und und geplant wird.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15f3735f79671ac41789d39a5473722a5f35fde0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "332034"
---
# <a name="schedule-load-utilization"></a>Auslastungsnutzung planen

[!include[banner](../includes/banner.md)]

Sie können Auslastungsnutzung für ausgewählte Lagerplatztypen planen und auch die aktuellen und künftige Auslastungsnutzung projizieren. Sie können die Auslastung für einen oder mehrere Standorte, für die Ladeeinheiten des Lagerorts oder für eine Kombination von Zone und Lagerort projizieren.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Planen und Anzeigen der Auslastung für einen Lagerort oder einen Standort

Um die Auslastung für Standorte, Lagerorte oder Zonen zu planen, erstellen Sie eine Platznutzungseinrichtung und ordnen diese einem Produktprogrammplan zu.

In den Einstellungen für die Platzauslastung verwenden Sie Lagerplatztypen wie **Sammellagerplatz** und **Entnahmeort**, um anzugeben, wie die Platznutzung projektiert werden soll. Darüber hinaus geben Sie einen Speicherlademodus, wie **Zone** an.

Die Projektion der zukünftigen Platznutzung basiert auf Informationen, die auf Grundlage des zugeordneten Produktprogrammplans berechnet werden. Produktprogrammpläne dienen zur Voraussage der Ressourcenplanung für ein- und ausgehende Aufträge für Produktion und Arbeitsgänge. Die Projizierung der verfügbaren Fläche basiert auf der Beziehung zwischen der Platznutzungseinrichtung und dem ausgewählten Produktprogrammplan.

Mithilfe des Einheitslademodus, den Sie in der Platznutzungseinstellung ausgewählt haben, geben Sie an, ob die Auslastung für jeden Lagerort oder Zone projiziert werden soll, oder ob die Prognosen Informationen zu Lagerort und Zone enthalten. Darüber hinaus geben Sie an, ob gesperrte Lagerplätze von der Berechnung der Auslastungsnutzung ausgeschlossen werden sollen.

Sie können die Platznutzung projizieren, indem Sie den Bericht **Lagerort-Auslastungsnutzung** generieren. Wenn Sie den Bericht generieren, können Sie festlegen, ob die Auslastungsnutzung für jeden Standort oder standortübergreifend oder für die ausgewählte Ladeeinheit, wie Zone oder Lagerort projiziert werden soll.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Erstellen einer Platznutzungseinrichtung für einen Lagerort

1. Wählen Sie **Lagerverwaltung** \> **Einrichten** \> **Lagerortüberwachung** \> **Platzauslastung**.
2. Klicken Sie auf **Neu**, um eine Platzauslastungseinrichtung zu erstellen. Geben Sie eine Kennung und einen Namen für die neue Einrichtung an.
3. Wählen Sie im Feld **Lagerauslastungsmodus** aus, ob die Übersicht über Platznutzung nach Lagerort, Zone oder Lagerort und Zone vorgehen soll.
4. Hier können Sie die Option **Blockierte Lagerplätze ausschließen** auf **Ja** festlegen, um gesperrte Lagerplätzen in die Berechnung des verfügbaren Platzes auszuschließen. Sie können einen Lagerplatz für Lagerbestand für Zugangs- und Ausgabe sperren, indem Sie einen Sperrungsgrund für den Lagerplatz im Feld **Zugang gesperrt** oder **Abgang gesperrt** auf der Registerkarte **Sonstiges** der Seite **Lagerplätze** angeben.
5. Wählen Sie im Inforegister **Lagerplatztyp** die Lagerplatztypen aus, die in der Platznutzungsberechnung einzubeziehen sind. Sie müssen mindestens einen Lagerplatztyp für die Projizierung auswählen.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Zuordnen einer Platznutzungseinrichtung zu einem Produktprogrammplan

1. Wählen Sie **Lagerverwaltung** \> **Periodisch** \> **Auslastungsnutzung planen**.
2. Wählen Sie im Feld **Masterplan** einen Produktprogrammplan aus.
3. Geben Sie im Feld **Anzahl an Tagen:** die Anzahl von Tagen ein, die in der Projizierung der aktuellen und zukünftigen Arbeitsauslastungen einzubeziehen sind.
4. Wählen Sie im Feld **Platzauslastung** die Platznutzungseinrichtung aus, die in der Projizierung der aktuellen und zukünftigen Arbeitsauslastungen zu verwenden ist.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Angeben der Auslastungsnutzungsprojektion und Anzeigen von Informationen

1. Wählen Sie **Lagerverwaltung** \> **Anfragen und Berichte** \> **Physische Bestandsberichte** \> **Lagerort-Auslastungsnutzung**.
2. Wählen Sie im Feld **Anzeigen nach** aus, um die Stufe der Platznutzungsprojektion zu identifizieren:

    - **Standort** - Platznutzung für jeden Standort projizieren. Diese Projektion ist hilfreich, wenn Sie beispielsweise alle Lagerorte für einen Standort anzeigen möchten, damit Sie die Platznutzung zwischen den Lagerorten ausgleichen können.
    - **Auslastungseinheit** - Platznutzung für Zonen oder Lagerorte projizieren. Der verfügbare Platz wird dann entsprechend dem Wert projiziert, das im Feld **Lagerauslastungsmodus** auf der Seite **Platzauslastung** aktiviert haben, als Sie die Platznutzungseinstellung erstellt haben.

3. Führen Sie einen dieser Schritte aus, abhängig vom Wert, die Sie im vorherigen Schritt ausgewählten:

    - Wenn Sie **Standort** im **Anzeigen nach**-Feld ausgefügt haben, ist das Feld **Standort** verfügbar. Wählen eine oder mehrere Standorte aus, die in der Projektion einzubeziehen sind.
    - Wenn Sie **Auslastungseinheit** im **Anzeigen nach**-Feld ausgefügt haben, ist das Feld **Auslastungseinheit** verfügbar. Wählen Sie Auslastungseinheit.

4. Geben Sie im Feld **Auslastungstyp** **Volumen** oder **Gewicht** an, um die Lagerortorganisationseinheit anzugeben, für die Platz projiziert werden soll.
5. Wählen Sie im Feld **Platzauslastungseinstellungen** die Einstellungen für die Platznutzung aus, auf denen die Projektion basiert.
