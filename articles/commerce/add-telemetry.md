---
title: Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie
description: In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154085"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.

## <a name="overview"></a>Übersicht

Internet-Analyse ist ein wichtiges Tool, wenn Sie verstehen möchten, wie Ihre Debitoren mit der Site interagieren und Entscheidungen treffen, die Ihnen helfen, die Erfahrung für maximale Umrechnung zu optimieren. Viele Internet-Analysepakete sind verfügbar, um zu helfen, diese Ziele zu erreichen wie Google Analytics, Clicky, Moz-Analyse und KISSMetrics. Die meisten Internet-Analysepakete erfordern, dass Sie clientseitige Scriptcode im **\<Kopf\>** Element des HTML für alle Seiten Ihrer Site hinzufügen.

> [!NOTE]
> Die Anweisungen in diesem Thema gelten auch für benutzerdefinierte clientseitige andere Funktionen, die Microsoft Dynamics 365 Commerce System intern nicht bereitstellt.

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a>Erstellen Sie ein wiederverwendbares Seitenfragment für Ihren Skriptcode

Mit einem Seitenfragment können Sie Inline- oder externen Skriptcode auf allen Seiten Ihrer Site wiederverwenden, unabhängig von der verwendeten Vorlage.

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a>Erstellen Sie ein wiederverwendbares Seitenfragment für Ihren Inline-Skriptcode

Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Seitenfragment für Ihren Inline-Skriptcode im Site Builder zu erstellen.

1. Wechseln Sie zu **Seitenfragmente**, und wählen Sie dann **Neu** aus.
1. In dem **Neues Seitenfragment** Dialogfeld wählen Sie **Inline-Skript**.
1. Unter **Name des Seitenfragments** geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK**.
1. Wählen Sie unter dem von Ihnen erstellten Seitenfragment die Option aus **Standard-Inline-Skript** Modul.
1. Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein. Konfigurieren Sie dann andere Optionen nach Bedarf.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a>Erstellen Sie ein wiederverwendbares Seitenfragment für Ihren externen Skriptcode

Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Seitenfragment für Ihren externen Skriptcode im Site Builder zu erstellen.

1. Wechseln Sie zu **Seitenfragmente**, und wählen Sie dann **Neu** aus.
1. In dem **Neues Seitenfragment** Dialogfeld wählen Sie **Externes Skript**.
1. Unter **Name des Seitenfragments** geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK**.
1. Wählen Sie unter dem von Ihnen erstellten Seitenfragment die Option aus **Externes Standard-Skript** Modul.
1. Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu. Konfigurieren Sie dann andere Optionen nach Bedarf.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a>Fügen Sie einer Vorlage ein Seitenfragment hinzu, das Skriptcode enthält

Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Seitenfragment mit Skriptcode einer Vorlage im Site Builder hinzuzufügen.

1. Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.
1. Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.
1. Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Seitenfragment hinzufügen**.
1. Wählen Sie das Fragment aus, das Sie für den Skriptcode erstellt haben.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Fügen Sie einer Vorlage ein externes Skript oder ein Inline-Skript direkt hinzu

Wenn Sie ein Inline- oder externes Skript direkt in eine Reihe von Seiten einfügen möchten, die von einer einzelnen Vorlage gesteuert werden, müssen Sie nicht zuerst ein Seitenfragment erstellen.

### <a name="add-an-inline-script-directly-to-a-template"></a>Fügen Sie einer Vorlage ein Inline-Skript direkt hinzu

Führen Sie die folgenden Schritte aus, um ein Inline-Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.

1. Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.
1. Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.
1. Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.
1. In dem **Modul hinzufügen** Dialogfeld wählen Sie **Inline-Skript**.
1. Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein. Konfigurieren Sie dann andere Optionen nach Bedarf.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

### <a name="add-an-external-script-directly-to-a-template"></a>Fügen Sie einer Vorlage ein externes Skript direkt hinzu

Führen Sie die folgenden Schritte aus, um ein externes Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.

1. Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.
1. Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.
1. Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.
1. In dem **Modul hinzufügen** Dialogfeld wählen Sie **Externes Skript**.
1. Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu. Konfigurieren Sie dann andere Optionen nach Bedarf.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)
