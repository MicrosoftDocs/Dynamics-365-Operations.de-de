---
title: Standortseiten zur Unterstützung von Telemetrie mit Skriptcode ergänzen
description: In diesem Artikel wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a0a5103d239c7f93ad6888a2eaf56d1cac32bd58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282271"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Standortseiten zur Unterstützung von Telemetrie mit Skriptcode ergänzen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.

Internet-Analyse ist ein wichtiges Tool, wenn Sie verstehen möchten, wie Ihre Debitoren mit der Site interagieren und Entscheidungen treffen, die Ihnen helfen, die Erfahrung für maximale Umrechnung zu optimieren. Viele Internet-Analysepakete sind verfügbar, um zu helfen, diese Ziele zu erreichen wie Google Analytics, Clicky, Moz-Analyse und KISSMetrics. Die meisten Internet-Analysepakete erfordern, dass Sie clientseitigen Scriptcode im **\<head\>**-Element der HTML für alle Seiten Ihrer Website hinzufügen.

> [!NOTE]
> Die Anweisungen in diesem Artikel gelten auch für andere benutzerdefinierte clientseitige Funktionen, die Microsoft Dynamics 365 Commerce intern nicht bereitstellt.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Erstellen Sie ein wiederverwendbares Fragment für Ihren Skriptcode

Mit einem Fragment können Sie Inline- oder externen Skriptcode auf allen Seiten Ihrer Site wiederverwenden, unabhängig von der verwendeten Vorlage.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Erstellen Sie ein wiederverwendbares Fragment für Ihren Inline-Skriptcode

Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment für Ihren Inline-Skriptcode im Site Builder zu erstellen.

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Neues Fragment** die Option **Inline-Skript** aus.
1. Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.
1. Wählen Sie unter dem von Ihnen erstellten Fragment die Option aus **Standard-Inline-Skript** Modul.
1. Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein. Konfigurieren Sie dann andere Optionen nach Bedarf.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Erstellen Sie ein wiederverwendbares Fragment für Ihren externen Skriptcode

Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment für Ihren externen Skriptcode im Site Builder zu erstellen.

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Neues Fragment** die Option **Externes Skript** aus.
1. Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.
1. Wählen Sie unter dem von Ihnen erstellten Fragment die Option aus **Externes Standard-Skript** Modul.
1. Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu. Konfigurieren Sie dann andere Optionen nach Bedarf.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

> [!NOTE]
> Wenn die Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) für Ihre Site aktiviert ist, stellen Sie sicher, dass alle externen URLs zur Inhaltssicherheitsrichtlinie **script-src** im Commerce Site Builder hinzugefügt werden. Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie (CSP) verwalten](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Fügen Sie einer Vorlage ein Fragment hinzu, das Skriptcode enthält

Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment mit Skriptcode einer Vorlage im Site Builder hinzuzufügen.

1. Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.
1. Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.
1. Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Fragment hinzufügen**.
1. Wählen Sie das Fragment aus, das Sie für den Skriptcode erstellt haben.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Fügen Sie einer Vorlage ein externes Skript oder ein Inline-Skript direkt hinzu

Wenn Sie ein Inline- oder externes Skript direkt in eine Reihe von Seiten einfügen möchten, die von einer einzelnen Vorlage gesteuert werden, müssen Sie nicht zuerst ein Fragment erstellen.

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

[Sitedesign auswählen](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
