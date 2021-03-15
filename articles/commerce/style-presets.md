---
title: Mit Stilvoreinstellungen arbeiten
description: In diesem Thema wird beschrieben, wie Sie mit vordefinierten Stilen in Microsoft Dynamics 365 Commerce Sitebuilder arbeiten.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1bd8f6e31afa300c5e7687a657ae2807995af8d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006309"
---
# <a name="work-with-style-presets"></a>Mit Stilvoreinstellungen arbeiten

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie mit vordefinierten Stilen in Microsoft Dynamics 365 Commerce Sitebuilder arbeiten.

## <a name="overview"></a>Übersicht

Ein voreingestellter Stil ist ein gespeicherter Satz aller autorisierbaren Stilwerte für das Thema einer Site. Es kann verwendet werden, um das Aussehen einer Site sofort vom Site Builder aus zu ändern. Mit Stilvoreinstellungen können Commerce Site Builder-Autoren schnell eine Reihe von Stilwerten auf ihrer Website ändern, in der Vorschau anzeigen und aktivieren, ohne Cascading Style Sheets verwenden zu müssen (CSS) oder Themen bereitstellen. Schriftstile, Schaltflächenstile und Site-Farben sind typische Beispiele für Stilvariablen, die über Stilvoreinstellungen verwaltet werden können.

Der Satz von Stilvariablen, der auf einer Site verfügbar ist, wird durch die Themen- und Modulbibliothek bestimmt, die für den Mandanten einer Site bereitgestellt wird. Mit dem Dynamics 365 Commerce Online Software Development Kit (SDK) können Entwickler so viele (oder so wenige) autorisierbare Stilvariablen implementieren, wie sie für ein bestimmtes Thema benötigen. Durch die Aktivierung weiterer Stilvariablen kann ein Theme-Entwickler den Autoren des Site Builders die endgültige Auswahl der Site-Stile überlassen. Daher können Nichtentwickler mithilfe des Toolset Site-Stile aktualisieren und in der Vorschau anzeigen. Die Funktion ist auch für alle Szenarien nützlich, in denen direkte Änderungen an Themen oder CSS unnötigen Overhead verursacht.

Für Themen, für die autorisierbare Stilvariablen aktiviert sind, ist eine Standardstilvoreinstellung erforderlich. Sie können optional zusätzliche voreingestellte Optionen als Teil eines bereitgestellten Themenpakets enthalten. Beispielsweise kann ein Thema bereitgestellt werden, für das eine einzige Standardvoreinstellung im Stil modern light festgelegt ist. Alternativ können neben der Standardvoreinstellung auch zusätzliche Stilvoreinstellungsoptionen enthalten sein, z. B. modern dark, vintage light oder vintage dark. Diese integrierten Themenvoreinstellungen werden von Entwicklern erstellt und können als Ausgangspunkt für neue Website-Designs verwendet werden.

Im Site Builder können Autoren unter den integrierten Voreinstellungen eines Themas auswählen oder mithilfe der aktivierten Stilvariablen ihre eigenen Stilvoreinstellungen und Anpassungen erstellen. Eine Stilvoreinstellung kann im Site Builder in der Vorschau angezeigt werden, bevor sie auf der Live-Site aktiviert wird. Nachdem die Stiländerungen eines Autors überprüft wurden, kann die Stilvoreinstellung für die Live-Site auf aktiv gesetzt werden.

## <a name="preview-a-style-preset"></a>Vorschau einer Stilvoreinstellung

Führen Sie die folgenden Schritte aus, um eine Vorschau einer Stilvoreinstellung auf Ihrer Site im Site Builder anzuzeigen.

1. Gehen Sie im linken Navigationsbereich Ihrer Site zu **Seiteneinstellungen \> Design**.
1. Auf der Registerkarte **Stilvoreinstellungen** oben im Design-Editor in der Liste **Verfügbare Voreinstellungen** wählen Sie eine Voreinstellung und wählen Sie dann **Ansicht**, um zum voreingestellten Editor zu gehen.

    Wenn derzeit keine Voreinstellungen in der Liste **Verfügbare Voreinstellungen** vorhanden sind, gehen Sie zu [Erstellen Sie eine benutzerdefinierte Stilvoreinstellung](#create-a-custom-style-preset) für Informationen zum Erstellen einer benutzerdefinierten Stilvoreinstellung.

    > [!NOTE]
    > Voreinstellungen, die im Thema enthalten waren, sind mit einem **eingbauten** Zeichen angegeben. Diese integrierten Voreinstellungen sind schreibgeschützt. Um eine integrierte Voreinstellung als neue anpassbare Voreinstellung zu kopieren, wählen Sie die Schaltfläche mit den Auslassungspunkten (**..**) für die Voreinstellung und wählen Sie dann **Speichern als**.

1. Wählen Sie in der Befehlsleiste **Vorschau** aus.
1. Wählen Sie eine URL von Ihrer Site aus, die zur Vorschau der Stilvoreinstellung verwendet werden soll, und wählen Sie dann aus **OK**.
1. Wählen Sie die kanalspezifische und länderspezifische URL-Variante für die Vorschau aus, indem Sie den Namen der Variante auswählen. Ein neues Vorschau-Browserfenster wird geöffnet, in dem die ausgewählte Stilvoreinstellung auf die angegebene Seite angewendet wird.

> [!NOTE]
> Die Vorschau-URL ist dauerhaft und authentifiziert. Daher können Sie sie kopieren, einfügen und zur Überprüfung an andere authentifizierte Mitarbeiter senden, bevor Sie sie auf Ihrer Live-Site auf aktiv setzen. Die Vorschau-URL ist auch nützlich, um Stile auf verschiedenen Geräten, in verschiedenen Browsern und auf verschiedenen Bildschirmen zu überprüfen.

> [!TIP]
> Während Sie eine Stilvoreinstellung bearbeiten, ist es möglicherweise hilfreich, das Vorschau-Browserfenster in einem separaten Browserfenster geöffnet zu lassen, damit Sie Ihre Änderungen schnell überprüfen können. Nachdem Sie Ihre Änderungen in einer Voreinstellung gespeichert haben, aktualisieren Sie das geöffnete Vorschau-Browserfenster, um die Benutzererfahrung zu überprüfen.

## <a name="create-a-custom-style-preset"></a>Erstellen Sie eine benutzerdefinierte Stilvoreinstellung

Um einen benutzerdfinierten Stil im Site Builder voreinzuzstellen, folgen Sie diesen Schritten.

1. Gehen Sie im linken Navigationsbereich Ihrer Site zu **Seiteneinstellungen \> Design**.
1. Auf der Registerkarte **Stilvoreinstellungen** wählen Sie oben im Design-Editor in der Befehlsleiste die Registerkarte **Neue Voreinstellung**.
1. Geben Sie einen Namen und eine neue Beschreibung für die neue Voreinstellung ein und wählen Sie **Speichern**. Es wird eine neue anpassbare Voreinstellung erstellt, die die Standardwerte des Themas als Ausgangspunkt verwendet.

> [!NOTE]
> Sie können auch eine neue benutzerdefinierte Stilvoreinstellung aus einer vorhandenen Voreinstellung erstellen, indem Sie auf die Schaltfläche mit den Auslassungspunkten (**...**) für diese Voreinstellung klikcne und dann **Speichern als** auswählen. Alternativ wählen Sie **Speichern als** in der Befehlsleiste im voreingestellten Editor.

## <a name="modify-global-and-module-type-style-values"></a>Ändern Sie globalen und Modultyp-Stilwerte

Einige Stilvariablen eines Themas werden von mehreren Modultypen gemeinsam genutzt. Diese Stilvariablen werden als *globale* Stilvariablen bezeichnet. Beispiele hierfür sind primäre Site-Farben, Standard-Schriftstile und Schaltflächenstile. Durch Festlegen globaler Variablen können Sie das Erscheinungsbild für viele verschiedene Modultypen ändern.

Einige Stilwerte können für einen Modultyp eindeutig sein oder müssen optional einen globalen Standardwert überschreiben. Wenn das Design einer Site Modultyp-Stilvariablen implementiert hat, können Site Builder-Autoren den Stil eines Modultyps unabhängig von den globalen Einstellungen anpassen. Modultypvariablen können die globalen Stilvariablen in einem Thema entweder erweitern oder überschreiben.

> [!NOTE]
> Die Hierarchie der Stilwerte in einer Site verhält sich wie folgt. Stilwerte, die weiter rechts angezeigt werden, überschreiben die Stilwerte links davon.
>
> Standardwerte des Themas \< Globale Stilwerte \< Modultyp-Stilwerte \< CSS überschreiben

Führen Sie die folgenden Schritte aus, um die globalen Werte oder die Modultypwerte einer Stilvoreinstellung im Site Builder zu ändern.

1. Gehen Sie im linken Navigationsbereich Ihrer Site zu **Seiteneinstellungen \> Design**.
1. Auf der Registerkarte **Stilvoreinstellungen** wählen Sie oben im Design-Editor die Registerkarte **Anzeige** für jede Stilvoreinstellung an, um zum Voreinstellungseditor zu gehen.
1. Wählen Sie **Vorschau** und befolgen Sie anschließend die Schritte zur URL-Auswahl, um eine Vorschau des vollständigen Browserfensters für Ihre Voreinstellung zu öffnen. Lassen Sie dieses Vorschau-Browserfenster geöffnet.
1. Wählen Sie im voreingestellten Editor oben rechts **Bearbeiten** aus.
1. Verwenden Sie die Steuerelemente für Stilvariablen im Editor, um einige globale Stilwerte zu ändern.
1. Oben im Editor auf der Registerkarte **Module** wählen Sie die Registerkarte **Global** und wählen Sie einen Modultyp, der gestaltet werden muss.
1. Verwenden Sie die Stilsteuerelemente, um einige Werte für den Modultyp zu ändern.
1. Wenn Sie eine Vorschau Ihrer Änderungen anzeigen möchten, wählen Sie **speichern** in der Befehlsleiste.
1. Kehren Sie zum geöffneten Vorschau-Browserfenster zurück und aktualisieren Sie es. Die Vorschau des vollständigen Browserfensters ist nützlich, um Stiländerungen an verschiedenen Ansichts-Haltepunkten, in verschiedenen Browsern und auf verschiedenen Geräteplattformen zu überprüfen.
1. Wenn alle Änderungen abgeschlossen und validiert wurden, wählen Sie **Beenden Sie die Bearbeitung** oben rechts im Editor.

> [!NOTE]
> Wenn Sie die Stilvoreinstellung bearbeiten, die derzeit auf Ihrer Site aktiv ist, sehen Sie ein blaues **aktives** Abzeichen im Editor. Dieses Abzeichen zeigt an, dass die Voreinstellung derzeit auf Ihrer Website aktiv ist. Wenn Sie die aktive Voreinstellung ändern, wählen Sie **Veröffentlichen**, um diese Änderungen auf Ihre Live-Site zu übertragen.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Aktivieren Sie eine neue Stilvoreinstellung auf Ihrer Live-Site

Führen Sie die folgenden Schritte aus, um eine Stilvoreinstellung als neue aktive Voreinstellung auf Ihrer Site festzulegen.

- Wählen Sie **Als aktive Schaltfläche einstellen** an einem dieser Orte:

    - Die Befehlsleiste im Stilvoreinstellungseditor
    - Das Auslassungsmenü (**...**) für alle verfügbaren Voreinstellungen in der Hauptansicht auf der Registerkarte **Stilvoreinstellungen** unter **Seiteneinstellungen \> Design**

Die Stilwerte der Voreinstellung werden auf Ihrer öffentlich zugänglichen Website aktiviert.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]