---
title: Bereitstellen eines neuen E-Commerce-Mandanten
description: In diesem Thema wird beschrieben, wie Sie einen neuen E-Commerce-Mandanten bereitstellen, indem Microsoft Dynamics Lifecycle Services (LCS) verwenden.
author: psimolin
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d7dfcaf244260de5f39a1201ec1ea78e94351e7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001782"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Bereitstellen eines neuen E-Commerce-Mandanten


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine neue E-Commerce-Site bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.

## <a name="overview"></a>Übersicht

Microsoft Dynamics Lifecycle Services (LCS) ist ein Cloud-basierter kooperativer Arbeitsbereich, den Partnern und Kunden verwenden können, um die Projekte und Umgebung zu verwalten, die neuesten Informationen anzuzeigen über die Microsoft Dynamics Produkte und Funktionen und Stützvorfälle zu erstellen, nachzuverfolgen und zu durchsuchen. E-Commerce-Verwaltungsfunktionen sind in LCS integriert.

Weitere Informationen zu LCS finden Sie unter [Lifecycle Services Benutzerhandbuch](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Erste Schritte

Bevor Sie E-Commerce initialisieren können, müssen Sie ein Projekt, eine Umgebung und ein Retail Cloud Scale Unit (RCSU) initialisieren. Um die Initialisierung in LCS zu bewerkstelligen, müssen Sie über Berechtigungen entweder als Projekt-Inhaber oder Umgebungsmanager haben. Die Produktion und Sandboxumgebungstopologien werden unterstützt.

Weitere Informationen über Umgebungen finden Sie unter [Umgebungsplanung](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Weitere Informationen zur RCSU-Compliance finden Sie unter [Retail Cloud Scale Unit initialisieren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>E-Commerce initialisieren

Verwenden Sie diese Prozedur, um die E-Commerce-Funktion in einer vorhandenen Umgebung zu initialisieren.

Bevor Sie beginnen, stellen Sie sicher, dass Sie folgende Informationen enthalten:

- Die RCSU,die verwendet wird.
- Die Microsoft Azure Active Directory Sicherheitsgruppe, die für E-Commerce-Systemadministratoren verwendet wird.
- Die Microsoft Azure Active Directory Sicherheitsgruppe, die für Bewertungen verwendet wird und Moderatoren überprüft.
- Die Domänen, die der Umgebung zugeordnet werden.

Zudem können Sie folgende optionale Informationen erfassen:

- Azure AD Onlinebankenlösung Informationen (B2C):

    - Mandantenname.
    - Kundenkennung.
    - Benutzerdefinierte Domäne für Anmeldung.
    - Antwort auf URL.
    - Richtlinienkennung zur Registrierung anmelden.
    - Richtlinienkennung für „Kennwort zurücksetzen“.
    - Profilrichtlinienkennung bearbeiten.

[!NOTE]
Diese Information kann später über eine Serviceanforderung hinzugefügt werden.

Nachdem Sie die erforderlichen Informationen gesammelt haben, folgen Sie diesen Schritten, um E-Commerce zu initialisieren.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com) an.
1. Öffnet das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.
1. Im Abschnitt **Umgebung** wählen Sie die Umgebung.
1. Wählen Sie unter **Umgebungsfunktionen** den Link **Einzelhandel verwalten** aus.
1. Auf der Registerkarte **E-Commerce** wählen Sie **Einstellungen** aus. Ein Dialogfeld wird angezeigt, in dem Sie die Informationen eingeben müssen, die für die Bereitstellung erforderlich ist.
1. Geben Sie die erforderlichen Informationen ein und wechseln dann zur nächsten Seite.
1. Auf der nächsten Seite geben Sie die erforderlichen Informationen ein und übermitteln das Formular. Sie werden zur Registerkarte **E-Commerce** zurückgeführt, wo Sie die Initialisierung sehen sollten, die begonnen wurde.
1. Um den Initialisierungsstatus später anzuzeigen, **Aktualisieren** Sie oder kehren später zur Registerkarte **E-Commerce** zurück.
    
Wenn E-Commerce von LCS initialisiert wird, erstellt das System mehrere Komponenten, die für E-Commerce erforderlich sind bereit und ordnet sie der Umgebung zu. Nachdem das Bereitstellen abgeschlossen ist, wird die Registerkarte **E-Commerce** auf der Seite **Retailverwaltung** aktualisiert, um der Bereitstellung zu entsprechen. Die Seite zeigt die aktuellsten Anpassungsbereitstellungen und den aktuellen Status aller anderen Bereitstellungen an. Sie schließt auch Links zur E-Commerce-Site und dem E-Commerce-Site-Builder ein, in dem Sites erstellt werden.

## <a name="access-site-builder"></a>Site Builder aufrufen

Um auf den Site Builder zuzugreifen, gehen Sie zur Registerkarte **E-Commerce** auf der Seite **Retail-Verwaltung** in LCS und wählen Sie den Link **E-Commerce-Site-Management-Tool**. Auf der Zielseite des Site Builders wird eine Ansicht auf Mandantenebene angezeigt. Auf dieser Seite können Sie folgende Aktivitäten durchführen:

- Die Einstellungen auf Mandantenebene ändern.
- Zu einer von Ihnen erstellten Site navigieren und die Berechtigung zum Anzeigen haben. 
- Auf Überprüfungsfunktionen wie Moderation und Berichterstattung zugreifen.
- Erstellen einer neuer Site. Weitere Informationen zum Erstellen einer neuen Site finden Sie unter [E-Commerce-Site erstellen](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Konfigurieren Ihres Domänennamens](configure-your-domain-name.md)

[Erstellen einer E-Commerce-Webseite](create-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Verwalten von robots.txt-Dateien](manage-robots-txt-files.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Unterstützung für ein Content Delivery Network (CDN) hinzufügen](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)
