---
title: Beseitigen Sie eine Projektschätzung
description: Dieses Thema enthält Informationen zum Entfernen einer Projektschätzung nach deren Abschluss.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410222"
---
# <a name="eliminate-a-project-estimate"></a>Beseitigen Sie eine Projektschätzung

[!include [banner](../includes/banner.md)]

Projektschätzungen liefern die Finanzansicht für Arbeiten, die für ein Projekt geschätzt und geplant werden. Wenn Sie mit Vorkalkulationen für ein Projekt arbeiten möchten, müssen Sie das Projekt einem Vorkalkulationsprojekt zuordnen. Ein Vorkalkulationsprojekt basiert stets auf einem vorhandenen Projekt, aber mehrere Projekte können sich auf ein einzelnes Vorkalkulationsprojekt beziehen. Nur Festpreis- und Investitionsprojekte können Vorkalkulationsprojekten angehängt werden, und diese Projekte müssen zur gleichen Projektgruppe gehören wie das Vorkalkulationsprojekt.

Ein Vorkalkulationsprojekt kann nur gelöscht werden, wenn es vollständig abgeschlossen ist. In den folgenden Schritten wird erläutert, wie Sie eine Schätzung entfernen.

1. Wechseln Sie zu **Projektverwaltung und -verrechnung** > **Alle Projekte** und öffnen Sie das Projekt. 
2. Auf der Registerkarte **Verwalten** wählen Sie **Schätzungen** und auf der Seite **Schätzung** wählen Sie **Beseitigen**.
3. Auf der **Schätzung eliminieren** Seite auf der Registerkarte **Allgemein** legen Sie die folgenden Optionen fest:

   - **Periodencode**: Wählen Sie den Periodencode zum Auswählen der entsprechenden Vorkalkulationsprojekte aus. 
   - **Geschätztes Datum**: Wählen Sie das entsprechende Vorkalkulationsdatum für den Löschvorgang aus.
   - **Beseitigen mit WIP-Warnungen**: Aktivieren Sie diese Option, um eine Benachrichtigung bereitzustellen, wenn ein Kostenvoranschlag, der mit einer laufenden Arbeit (WIP) verknüpft ist, entfernt wird. Ist das Kontrollkästchen deaktiviert, kann der Löschvorgang nicht fortgesetzt werden, wenn Buchungen ohne Vorkalkulation vorhanden sind. 
   > [!NOTE]
   > Diese Option steht nur zur Verfügung, wenn die Löschung auf ein Vorkalkulationsprojekt angewendet wird. Bei Verwendung periodischer Buchungen ist es nicht verfügbar. Diese Einstellung funktioniert mit den Einstellungen auf der **Schätzen** Registerkarte auf der **Projektparameter** Seite, in der Feldgruppe **Ermöglichen Sie die Eliminierung, wenn nicht geschätzte Transaktionen vorhanden sind**.
   - **Phase auf Beendet stellen**: Aktivieren Sie diese Option, um die Phase des Vorkalkulationsprojektes auf **Beendet** festzusetzen, nachdem Sie die Eliminierung ausgeführt haben.
   - **Vorkalkulationsliste drucken**: Wählen Sie die Informationen aus, die beim Drucken der Vorkalkulationsprojektliste eingeschlossen werden sollen.
   - **Infolog anzeigen**: Aktivieren Sie diese Option, um den Infolog anzuzeigen.
   - **Buchungsdatum** : Wählen Sie das Buchungsdatum des Kostenvoranschlags.

4.  Wählen Sie **OK**.
5. Nach Abschluss des Eliminierungsprozesses wird das eliminierte Schätzprojekt mit einem negativen Wert angezeigt. 

Wenn Sie nicht vorhatten, eine Schätzung zu entfernen, können Sie die eliminierte Schätzung **Schätzung wiederherstellen** wählen.   
