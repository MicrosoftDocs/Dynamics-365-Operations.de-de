---
title: Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind
description: In diesem Thema wird beschrieben, wie Sie Shops und dazugehörige Teams in der Dynamics 365 Commerce-Zentralverwaltung zuordnen, wenn Ihre Organisation bereits vor der Commerce-Integration Teams in Microsoft Teams erstellt hat.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c75525749d9015387cc112beda104238a93698e9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346691"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Shops und dazugehörige Teams in der Dynamics 365 Commerce-Zentralverwaltung zuordnen, wenn Ihre Organisation bereits vor der Commerce-Integration Teams in Microsoft Teams erstellt hat.

Ihre Organisation hat vielleicht schon vor der Integration von Dynamics 365 Commerce und Microsoft Teams Teams für einige oder alle Ihre Shops erstellt. Wenn dies der Fall ist, müssen Sie für die Aufgabensynchronisierung zwischen Commerce POS und Microsoft Teams die Zuordnung der Shops und des dazugehörigen Teams in der Commerce-Zentralverwaltung bereitstellen.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Shops und dazugehörige Teams in der Commerce-Zentralverwaltung zuordnen 

Gehen Sie wie folgt vor, um Shops und dazugehörige Teams in der Commerce-Zentralverwaltung zuzuordnen.

1. Gehen Sie zu **Systemverwaltung \> Arbeitsbereich \> Datenverwaltung**.
1. Wählen Sie **Exportieren**. 
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Gehen Sie als **Gruppenname** „Teams-Zuordnung exportieren“ ein.
1. Wählen Sie im Inforegister **Ausgewählte Entitäten** **Entität hinzufügen** aus. Das Dialogfeld **Entität hinzufügen** wird angezeigt.  
1. Wählen Sie aus der Dropdownliste **Entitätsname** **Teams-Zuordnung zwischen Quelle und Team** aus.
1. Wählen Sie in der Dropdownliste **Zieldatenformat** **CSV** aus.
1. Wählen Sie **Hinzufügen** und anschließend **Schließen** aus.
1. Wählen Sie oben links im Aktivitätsbereich **Jetzt exportieren** aus.
1. Wählen Sie unter **Verarbeitungsstatus der Entität** **Datei herunterladen** aus.
1. Geben Sie in der exportierten CSV-Datei Werte für **SOURCETYE**, **SOURCEID** und **TEAMID** wie folgt ein:
    - Geben Sie für **SOURCETYPE** „RetailStore“ ein. 
    - Geben Sie als **SOURCEID** die Shopnummer ein (z. B. „000135“ für den Shop in San Francisco). Geschäftsnummern finden Sie unter **Einzelhandel und Handel \> Kanäle \> Shops**.
    - Geben Sie als **TEAMID** die entsprechende Team-ID aus Microsoft Teams ein (z. B. „5f8bc92b-6aa8-451e-85d1-3949c01ddc6c“). Informationen zur Team-ID finden Sie unter [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Speichern Sie die CSV-Datei auf Ihrem lokalen Computer.
1. Gehen Sie zu **Systemverwaltung \> Arbeitsbereich \> Datenverwaltung** und wählen Sie dann **Importieren**.
1. Wählen Sie im Inforegister **Ausgewählte Entitäten** **Datei hinzufügen** aus. Das Dialogfeld **Datei hinzufügen** wird angezeigt.
1. Wählen Sie aus der Dropdownliste **Entitätsname** **Teams-Zuordnung zwischen Quelle und Team** aus.
1. Wählen Sie in der Dropdownliste **Quelldatenformat** **CSV** aus.
1. Wählen Sie **Hochladen und hinzufügen**. Wählen Sie dann die CSV-Datei aus, die Sie zuvor gespeichert haben, und wählen Sie **Öffnen** aus.
1. Wählen Sie im Dialogfeld **Datei hinzufügen** **Schließen** aus.
1. Wählen Sie im Aktivitätsbereich **Speichern** und dann **Importieren**.

Das folgende Beispielbild zeigt Gruppe **Teams-Zuordnung exportieren** in Commerce. Die Elemente **Entität hinzufügen** und die Kopfzeilen der exportierten CSV-Datei sind hervorgehoben.

![Gruppe „Teams-Zuordnung exportieren“ in Commerce, Elemente „Entität hinzufügen“ und Kopfzeilen der exportierten CSV-Datei hervorgehoben.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Befolgen Sie nach Abschluss der vorherigen Schritte die Schritte in [Aufgabenverwaltung zwischen Microsoft Teams und POS synchronisieren](synchronize-tasks-teams-pos.md), um die Aufgabenverwaltung zu synchronisieren. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick Integration Dynamics 365 Commerce und Microsoft Teams](commerce-teams-integration.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren](enable-teams-integration.md)

[Microsoft Teams aus Dynamics 365 Commerce bereitstellen](provision-teams-from-commerce.md)

[Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren](synchronize-tasks-teams-pos.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ](teams-integration-faq.md)
