---
title: Wartungsarbeiter und Arbeitskräftegruppen
description: In diesem Artikel werden Wartungsarbeiter und Arbeitskräftegruppen in Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a24c880ee76af1490824aef07976b998d9225d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860898"
---
# <a name="maintenance-workers-and-worker-groups"></a>Wartungsarbeiter und Arbeitskräftegruppen

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel werden Wartungsarbeiter und Arbeitskräftegruppen in Anlagenverwaltung erläutert. In Asset Management können Sie Wartungsarbeiter mit funktionalen Standorten verbinden. (Weitere Informationen zu funktionalen Standorten finden Sie unter [Funktionale Standorte erstellen](../functional-locations/create-functional-locations.md).) Diese Funktionen sind möglicherweise hilfreich, wenn Sie beispielsweise einen Wartungsauftrag für eine Maschine planen, die sich am funktionalen Standort 01 befindet, und Sie Wartungsarbeiter vom gleichen funktionalen Standort zuordnen möchten, um den Auftrag auszuführen.

Sie können auch Wartungsarbeitergruppen erstellen und diesen Wartungsarbeiter zuordnen. Diese Funktionalität ist hilfreich, wenn Sie eine einfache Arbeitsauftragsplanung durchführen und eine Gruppe von Wartungsarbeitern für einen Arbeitsauftrag einplanen möchten. Sie können Wartungsarbeiter und Wartungsarbeitergruppen verwenden, um bevorzugte Wartungsarbeiter und zuständige Wartungsarbeiter einzurichten. 


## <a name="create-workers"></a>Arbeitskräfte erstellen

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Arbeitskräfte** \> **Arbeitskräfte** aus.
2. Wählen Sie **Neu** aus, um der Liste eine Arbeitskraft hinzuzufügen.
3. Wählen Sie im Feld **Arbeitskraft** die gewünschte Arbeitskraft aus.
4. Legen Sie die Option **Aktiv** auf **Ja** fest, um die Arbeitskraft für Arbeitsaufträge einzuplanen.

    Auf dem Inforegister **Allgemein** werden die Felder **Ressource** und **Beschreibung** automatisch ausgefüllt, wenn eine Ressource für die Arbeitskraft ausgewählt wurde. Das Feld **Kalender** wird ebenfalls automatisch ausgefüllt, vorausgesetzt, dass Sie die Arbeitskraft als Ressource eingerichtet und dieser Ressource auf der Seite **Ressourcen** (**Organisationsverwaltung** \> **Ressourcen** \> **Ressourcen**) einen Kalender zugewiesen haben.

5. Wählen Sie auf dem Inforegister **Gruppen** die Option **Hinzufügen** aus, und wählen Sie dann eine Wartungsarbeitergruppe für die Arbeitskraft aus. Eine Arbeitskraft kann mehreren Gruppen angehören.
6. In der Standardeinstellung ist die Zugehörigkeit einer Arbeitskraft zu einer Gruppe ab dem Datum wirksam, an dem Sie die Gruppe hinzuzufügen, und läuft nie ab. Dieses Datum wird im Feld **Gültig** angezeigt. Um das Feld **Gültig** anzuzeigen, wählen Sie **Anzeigen** \> **Alle** aus. Wenn die Zugehörigkeit der Arbeitskraft zu einer Gruppe auf einen bestimmten Zeitraum beschränkt sein soll, verwenden Sie die Felder **Gültig** und **Ablauf**, um den Zeitraum zu definieren.
7. Wählen Sie auf dem Inforegister **Funktionale Standorte** die Option **Hinzufügen** aus, und wählen Sie dann einen funktionalen Standort für den Wartungsarbeiter aus. Geben Sie außerdem an, welcher Standort der primäre funktionale Standort für die Arbeitskraft ist.

    > [!NOTE]
    > Wenn Sie funktionale Standorte für eine Arbeitskraft hinzufügen, werden alle aktiven Anlagen, die diesen funktionalen Standorten zugeordnet sind, in verschiedenen Menüoptionen angezeigt, wie z. B. **Meine aktiven Anlagen** und **Meine aktiven funktionalen Standorte**. Sie werden außerdem in den Anlagesuchen angezeigt, die angezeigt werden, wenn eine neue Anlage, eine Wartungsanfrage oder einen Arbeitsauftrag erstellen.

    Die Felder auf dem Inforegister **Details** zeigen die Anzahl der Wartungsarbeitergruppen und funktionalen Standorte, denen der ausgewählte Wartungsarbeiter zugeordnet ist.

## <a name="create-worker-groups"></a>Arbeitskraftgruppen erstellen

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Arbeitskräfte** \> **Wartungsarbeitergruppen** aus.
2. Wählen Sie **Neu** aus, um der Liste eine Arbeitskraftgruppe hinzuzufügen.
3. Geben Sie im Feld **Wartungsarbeitergruppe** eine Gruppenkennung ein.
4. Geben Sie im Feld **Name** einen Namen ein.
5. Wählen Sie auf dem Inforegister **Arbeitskräfte** die Option **Hinzufügen** aus, und wählen Sie dann einen Wartungsarbeiter für die Arbeitskraftgruppe aus. Informationen über die Felder **Gültig** und **Ablauf** finden Sie Schritt 6 der vorherigen Prozedur.
6. Wenn eine Ressourcengruppe der ausgewählten Wartungsarbeitergruppe zugeordnet sein soll, wählen Sie **Aus Ressourcengruppe kopieren** aus. Wählen Sie im Feld **Gruppe** die Ressourcengruppe aus, aus der Kalendereinstellungen kopiert werden sollen. Wählen Sie anschließend im Feld **Arbeitskraftgruppe** die Arbeitskraftgruppe aus, zu der die Kalendereinstellungen der Ressourcengruppe kopiert werden sollen. Dieser Schritt ist nur relevant, wenn Wartungsarbeiter während der Arbeitsauftragsplanung den Kalender verwenden sollen, der einer Ressource zugeordnet ist.

    Das Feld auf dem Inforegister **Details** zeigt die Anzahl der Wartungsarbeiter, die in der ausgewählte Wartungsarbeitergruppe eingerichtet wurden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]