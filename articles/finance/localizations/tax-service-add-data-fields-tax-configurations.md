---
title: Datenfelder in Steuerkonfigurationen hinzufügen
description: In diesem Thema wird erläutert, wie Sie Steuerkonfigurationen durch Hinzufügen von Datenfeldern anpassen.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921188"
---
# <a name="add-data-fields-in-tax-configurations"></a>Datenfelder in Steuerkonfigurationen hinzufügen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Steuerkonfigurationen anpassen, indem Sie [Datenfelder, die in der Steuerintegration hinzugefügt werden](tax-service-add-data-fields-tax-integration-by-extension.md) verwenden.

## <a name="customize-the-tax-data-model"></a>Steuerdatenmodell anpassen

1. Wechseln Sie in Microsoft Dynamics 365 Finance zu **Elektronische Berichterstellung** \> **Steuerkonfigurationen**.
2. Wählen Sie im Konfigurationsbaum **Steuerdatenmodell – Europa** aus. Wählen Sie dann im Aktivitätsbereich **Konfiguration erstellen** aus.
3. Wählen Sie im Dropdown-Dialogfeld die Option **Modell des steuerpflichtigen Dokuments abgeleitet von Name: Steuerdatenmodell – Europa, Microsoft**. Geben Sie bei dieser Option einen Namen für das neue Steuerdatenmodell ein und wählen Sie dann **Konfiguration erstellen**.
4. Wählen Sie das Steuerdatenmodell aus, das Sie gerade erstellt haben, und wählen Sie dann im Aktionsbereich **Designer** aus.
5. Erweitern Sie den Datenmodellbaum und wählen Sie **Positionen** und dann **Neu** aus.
6. Geben Sie im Dialogfeld **Knoten erstellen** einen Namen ein, geben Sie den Elementtyp an und wählen Sie dann **Hinzufügen** aus.
7. Fügen Sie alle erforderlichen Spalten hinzu.
8. Wählen Sie im Aktivitätsbereich **Speichern** und dann **Abschließen**.
9. Schließen Sie die Seite und zeigen Sie die fertige Version Ihres Steuerdatenmodells an.

## <a name="customize-the-tax-configuration"></a>Anpassen der Steuerkonfiguration

1. Wechseln Sie in Finance zu **Elektronische Berichterstellung** \> **Steuerkonfigurationen**.
2. Wählen Sie im Konfigurationsbaum **Steuerkonfiguration – Europa** aus. Wählen Sie dann im Aktivitätsbereich **Konfiguration erstellen** aus.
3. Wählen Sie im Dropdown-Dialogfeld die Option **Steuerdienstkonfiguration abgeleitet von Name: Steuerkonfiguration – Europa, Microsoft**. Geben Sie bei dieser Option einen Namen für die neue Steuerkonfiguration ein und wählen Sie dann **Konfiguration erstellen**.
4. Wählen Sie die Steuerkonfiguration aus, das Sie gerade erstellt haben, und wählen Sie dann im Aktionsbereich **Designer** aus.
5. Wählen Sie im Abschnitt **Eigenschaften** im Feld **Datenmodell** das zuvor erstellte benutzerdefinierte Steuerdatenmodell aus.
6. Wählen Sie im Feld **Datenmodellversion** die fertige Version des Steuerdatenmodells aus.
7. Wählen Sie **Hinzufügen** und fügen Sie die erforderlichen Steuermaßnahmen hinzu.
8. Wählen Sie im Aktivitätsbereich **Speichern** und dann **Abschließen**.
9. Schließen Sie die Seite und zeigen Sie die fertige Version Ihrer Steuerkonfiguration an.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Implementieren von Steuerfunktionen in der benutzerdefinierten Steuerkonfiguration

1. Wechseln Sie in Regulatory Configuration Services (RCS) zu **Globalisierungsfunktionen** \> **Steuern**.
2. Wählen Sie **Hinzufügen**, geben Sie Informationen zur neuen Funktion ein und wählen Sie dann **Funktion erstellen** aus.
3. Wählen Sie auf der Registerkarte **Versionen** die Funktion aus und wählen Sie dann **Bearbeiten**.
4. Wählen Sie auf der Registerkarte **Allgemein** im Feld **Konfigurationsversion** die angepasste Steuerkonfiguration und -version aus.
5. Wählen Sie im Dialogfeld **Spalten verwalten** die Kopf- und Positionsspalten aus, die Sie in Ihre benutzerdefinierte Steuermaßnahme aufnehmen möchten, und klicken Sie dann auf die Schaltfläche mit dem Rechtspfeil, um sie der **Ausgewählte Spalten**-Liste hinzuzufügen.
