---
title: Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie
description: In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914538"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.

## <a name="overview"></a>Übersicht

Internet-Analyse ist ein wichtiges Tool, wenn Sie verstehen möchten, wie Ihre Debitoren mit der Site interagieren und Entscheidungen treffen, die Ihnen helfen, die Erfahrung für maximale Umrechnung zu optimieren. Viele Internet-Analysepakete sind verfügbar, um zu helfen, diese Ziele zu erreichen wie Google Analytics, Clicky, Moz-Analyse und KISSMetrics. Die meisten Internet-Analysepakete erfordern, dass Sie clientseitige Scriptcode im **\<Kopf\>** Element des HTML für alle Seiten Ihrer Site hinzufügen.

> [!NOTE]
> Die Anweisungen in diesem Thema gelten auch für benutzerdefinierte clientseitige andere Funktionen, die Microsoft Dynamics 365 Commerce System intern nicht bereitstellt.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Erstellen Sie ein wiederverwendbares Fragment für Ihren Skriptcode

Nachdem Sie ein Fragment für den Skriptcode erstell haben, kann er über alle Seiten auf dem Standort wiederverwendet werden.

1. Gehen Sie zu **Fragmente \> Neues Seitenfragment**
2. Wählen Sie **Externes Skript** aus, geben Sie einen Namen für das Fragment ein, und wählen Sie dann **OK** aus.
3. In der Fragmenthierarchie wählen Sie das untergeordnete Modul **Skript-Injector** des Fragments aus, das Sie soeben erstellt haben.
4. Im Eigenschaftenbereich auf der rechten Seite fügen Sie das Skript clientseitiges hinzu und legen andere Konfigurationsoptionen fest, wie Sie sie benötigen.

## <a name="add-the-fragment-to-templates"></a>Das Fragment den Vorlagen hinzufügen

1. Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.
2. Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.
3. Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Fragment hinzufügen**.
4. Wählen Sie das Fragment aus, das Sie für den Skriptcode erstellt haben.
5. Speichern Sie die Vorlage und veröffentlichen Sie sie.

> [!NOTE]
> Nachdem Sie fertig sind, müssen Sie das Fragment und die Master-Vorlage veröffentlichen. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

