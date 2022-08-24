---
title: Einen Kanal zur Verwendung einer Kanalnavigationshierarchie konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce konfigurieren.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: b15e6eee86880f0315f42b34056385f718cc6bf1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280392"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Einen Kanal zur Verwendung einer Kanalnavigationshierarchie konfigurieren


[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce konfigurieren.

## <a name="overview"></a>Übersicht

Kanalnavigationshierarchien organisieren Produkte in Kategorien, sodass die Produkte auf einer E-Commerce-Website oder an Verkaufsstellen (POS) durchsucht werden können. Einzelhandels- und Onlinekanäle müssen mit Kanalnavigationshierarchien konfiguriert werden.

## <a name="configure-the-channel"></a>Den Kanal konfigurieren

Gehen Sie folgendermaßen vor, um einen Kanal für die Verwendung einer Kanalnavigationshierarchie zu konfigurieren.

1. Wechseln Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinstellungen \> Kanalkategorien und Produktattribute**.
1. Wählen Sie den zu konfigurierenden Kanal aus.
1. Wählen Sie im Aktivitätsbereich **Attributmetadaten festlegen**.
1. Wählen Sie in der Dropdownliste **Kategoriehierarchie** die entsprechende Kanalnavigationshierarchie aus.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Fügen Sie unter **Attributgruppe** alle Attributgruppen hinzu, die globale Attribute für alle Knoten sein werden.

Das folgende Bild zeigt, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie konfigurieren.

![Beispiel Kanalkonfiguration.](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Attributmetadaten festlegen

Durch Festlegen der Attributmetadaten können Attribute auf jedem Knoten konfiguriert werden.

Führen Sie die folgenden Schritte aus, um Attributmetadaten festzulegen.

1. Wählen Sie im Aktivitätsbereich **Attributmetadaten festlegen**.
1. Wählen Sie für jeden Knoten **Kanalproduktattribute** aus.
1. Legen Sie **Attribut auf Kanal anzeigen** auf **Ja** und **Kann verfeinert werden** auf **Ja** fest, um die Filter für diesen Kanal zu aktivieren.
1. Nachdem Sie jeden Knoten wie gewünscht konfiguriert haben, wählen Sie im **Aktionsbereich** die Schaltfläche **Speichern** zum Speichern aus.
1. Wählen Sie das **X** in der oberen rechten Ecke, um diesen Bildschirm zu verlassen und zur Seite **Kanalkategorien und Produktattribute** zurückzukehren.

Die folgende Abbildung zeigt ein Beispiel für eine Reihe von Kanalproduktattributen, die auf einem Kanalkategorieknoten konfiguriert sind.

![Kanalattribute auf einem Kanalkategorieknoten.](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Änderungen veröffentlichen

Damit die Änderungen wirksam werden, müssen Sie die Änderungen veröffentlichen.

Führen Sie folgende Schritte aus, um die Änderungen zu veröffentlichen.

1. Wählen Sie im Aktionsbereich **Kanalaktualisierungen veröffentlichen** aus.
1. Wählen Sie im Bereich **Kanalaktualisierungen veröffentlichen** **OK** aus.

Das folgende Bild zeigt, wie Kanalaktualisierungen veröffentlicht werden.

![Kanalupdates veröffentlichen.](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine Kanalnavigationshierarchie erstellen](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
