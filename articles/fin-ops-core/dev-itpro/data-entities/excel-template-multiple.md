---
title: Datenvorlagen mit mehreren Arbeitsblättern
description: Dieser Artikel beschreibt, wie Sie Daten mithilfe von Excel-Vorlagen für Entitäten in Finanzen und Betrieb importieren können.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: f0845b111afb18205677b885c91fe1585b24ab14
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108805"
---
# <a name="data-templates-with-multiple-worksheets"></a>Datenvorlagen mit mehreren Arbeitsblättern

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Die Datenverwaltung in der Anwendung unterstützt Microsoft Excel-basierte Vorlagen für Datenentitäten. Diese Vorlagen können eines oder mehrere Arbeitsblätter enthalten. Vorlagen mit mehreren Arbeitsblättern werden häufig verwendet, wenn es von Vorteil ist, Daten in einer einzigen Datei zu verwalten und diese in mehrere Datenentitäten zu importieren. Ein Beispiel wären Standorte und Lagerorte.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Einmaliges Hochladen einer Datei und deren Zuweisung zu allen Entitäten
Nehmen wir als Beispiel eine Excel-Datei mit Arbeitsblättern, die **Standorte** und **Lagerorte** heißen. Um das Datenimportprojekt einzurichten, würden Sie die erste Datenentität hinzufügen, nämlich **Standorte**. Dann würden Sie die Datei hochladen. Sie können dann **Standorte** als das Arbeitsblatt auswählen, das für diese Entität verwendet werden soll.

Wenn Sie die zweite Entität **Lagerorte** hinzufügen, ohne das Formular **Datei hinzufügen** zu verlassen, können Sie mithilfe der Arbeitsblattsuche das Arbeitsblatt **Lagerorte** auswählen, ohne die Datei erneut hochzuladen. Der einzige Grund, eine neue Datei hochzuladen, wäre gegeben, wenn die Daten zu **Lagerorte** sich in einer anderen Datei befänden.

![Mehrere Arbeitsblätter.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Zuordnung von Arbeitsblatt zu Entität korrigieren

Die Zuordnung des Arbeitsblatts zu einer Datenentität im Importeinzelvorgang kann vom Raster aus korrigiert werden. Die Spalte **Arbeitsblatt** im Raster zeigt die Arbeitsblätter der Datei an, die zugeordnet wurde. Sie können ein anderes Arbeitsblatt über das Dropdownmenü auswählen. Wenn das ausgewählte Arbeitsblatt bereits einer Entität im Datenprojekt zugeordnet ist, fordert das System Sie dazu auf, die Änderung zu bestätigen. Es wird empfohlen, alle Zuordnungen im Raster zu korrigieren.

![Arbeitsblattzuordnung aktualisieren.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Einer neuen Datei erneut zuordnen

In Fällen, in denen eine neue Version derselben Datei oder eine völlig neue Datei für vorhandene Entitäten in einem Datenprojekt hochgeladen werden müssen, müssen Sie die Benutzeroberfläche für **Datei hinzufügen** verwenden, und die Entitäten erneut hinzufügen, so als ob Sie zum ersten Mal hinzugefügt würden. Das System bestätigt, dass Sie die vorhandenen Entitäten im Datenprojekt überschreiben möchten, bevor Sie fortfahren. Entitäten, die nicht erneut hinzugefügt werden (oder überschrieben werden), werden weiterhin die vorherigen Zuordnungen aus der vorherigen Datei aufweisen.

## <a name="upload-a-file-using-run-project"></a>Eine Datei mithilfe von „Projekt ausführen” hochladen

Sie können eine Excel-Datei hochladen, während Sie die Option **Projekt ausführen** verwenden, um ein Importprojekt auszuführen. Sie müssen darauf achten, dass Sie nur Dateien hochladen, die dieselben Arbeitsblätter wie die vorhandenen Zuordnungen zu den Datenentitäten im Datenprojekt haben. Wenn ein Arbeitsblatt in der neu hochgeladenen Datei nicht gefunden wird, zeigt das System eine Fehlermeldung an und der Importvorgang wird beendet. Wenn die Zuordnung zum Arbeitsblatt für eine Entität geändert werden muss, dann müssen die Zuordnungen im Datenprojekt zuerst vom Datenprojekt selbst aus aktualisiert werden, bevor die Datei in der Benutzeroberfläche **Projekt ausführen** verwendet wird.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

