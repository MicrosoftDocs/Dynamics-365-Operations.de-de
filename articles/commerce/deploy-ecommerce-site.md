---
title: Neuen E-Commerce-Mandanten bereitstellen
description: In diesem Thema wird beschrieben, wie Sie eine neue Dynamics 365 Commerce-E-Commerce-Website bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4b54e10cb4bd897b4c0706a13eeaf32f8892a05f7a09f3b27dbdd3dcdad1606
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750713"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Neuen E-Commerce-Mandanten bereitstellen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine neue Dynamics 365 Commerce-E-Commerce-Website bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.

Microsoft Dynamics Lifecycle Services (LCS) ist ein Cloud-basierter kooperativer Arbeitsbereich, den Partnern und Kunden verwenden können, um die Projekte und Umgebung zu verwalten, die neuesten Informationen anzuzeigen über die Microsoft Dynamics Produkte und Funktionen und Stützvorfälle zu erstellen, nachzuverfolgen und zu durchsuchen. E-Commerce-Verwaltungsfunktionen sind in LCS integriert.

Weitere Informationen zu LCS finden Sie unter [Lifecycle Services Benutzerhandbuch](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Erste Schritte

Bevor Sie E-Commerce initialisieren können, müssen Sie ein Projekt, eine Umgebung und eine Retail Cloud Scale Unit (RCSU) initialisieren. Um die Initialisierung in LCS zu bewerkstelligen, müssen Sie über Berechtigungen entweder als Projekt-Inhaber oder Umgebungsmanager haben. Die Produktion und Sandboxumgebungstopologien werden unterstützt.

Weitere Informationen über Umgebungen finden Sie unter [Umgebungsplanung](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Weitere Informationen zur RCSU-Compliance finden Sie unter [Retail Cloud Scale Unit initialisieren](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>E-Commerce initialisieren

Verwenden Sie diese Prozedur, um die E-Commerce-Funktion in einer vorhandenen Umgebung zu initialisieren.

Bevor Sie beginnen, stellen Sie sicher, dass Sie folgende Informationen enthalten:

- Die RCSU,die verwendet wird.
- Die Microsoft Azure Active Directory-Sicherheitsgruppe, die für E-Commerce-Systemadministratoren verwendet wird.
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

> [!NOTE]
> Diese Information kann später über eine Serviceanforderung hinzugefügt werden.

Nachdem Sie die erforderlichen Informationen gesammelt haben, folgen Sie diesen Schritten, um E-Commerce zu initialisieren.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com) an.
1. Öffnen Sie das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.
1. Im Abschnitt **Umgebung** wählen Sie die Umgebung.
1. Wählen Sie unter **Umgebungsfunktionen** den Link **Einzelhandel verwalten** aus.
1. Auf der Registerkarte **E-Commerce** wählen Sie **Einstellungen** aus. Ein Dialogfeld wird angezeigt, in dem Sie die Informationen eingeben müssen, die für die Bereitstellung erforderlich ist.
1. Geben Sie die erforderlichen Informationen ein und wechseln dann zur nächsten Seite.
1. Auf der nächsten Seite geben Sie die erforderlichen Informationen ein und übermitteln das Formular. Sie werden zur Registerkarte **E-Commerce** zurückgeführt, wo Sie die Initialisierung sehen sollten, die begonnen wurde.
1. Um den Initialisierungsstatus später anzuzeigen, **Aktualisieren** Sie oder kehren später zur Registerkarte **E-Commerce** zurück.
    
Wenn E-Commerce von LCS aus initialisiert wird, stellt das System mehrere Komponenten bereit, die für E-Commerce erforderlich sind, und ordnet sie der Umgebung zu. Nachdem das Bereitstellen abgeschlossen ist, wird die Registerkarte **E-Commerce** auf der Seite **Retailverwaltung** aktualisiert, um der Bereitstellung zu entsprechen. Die Seite zeigt die aktuellsten Anpassungsbereitstellungen und den aktuellen Status aller anderen Bereitstellungen an. Sie schließt auch Links zur E-Commerce-Website und dem E-Commerce-Website-Generator ein, in dem Websites erstellt werden.

## <a name="access-commerce-site-builder"></a>Auf Commerce-Website-Generator zugreifen

Um auf den Commerce-Website-Generator zuzugreifen, gehen Sie zur Registerkarte **E-Commerce** auf der Seite **Retail-Verwaltung** in LCS und wählen Sie den Link **E-Commerce-Websiteverwaltungs-Tool** aus. Auf der Zielseite des Site Builders wird eine Ansicht auf Mandantenebene angezeigt. Auf dieser Seite können Sie folgende Aktivitäten durchführen:

- Die Einstellungen auf Mandantenebene ändern.
- Zu einer von Ihnen erstellten Site navigieren und die Berechtigung zum Anzeigen haben. 
- Auf Überprüfungsfunktionen wie Moderation und Berichterstattung zugreifen.
- Erstellen einer neuer Site. Weitere Informationen zum Erstellen einer neuen Website finden Sie unter [Eine E-Commerce-Website erstellen](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]