---
title: Verwalten von e-Commerce Benutzern und Rollen
description: In diesem Artikel wird erläutert, wie Sie Benutzern Zugriff auf die Erstellungsumgebung für Ihre Microsoft Dynamics 365 Commerce-Website gewähren.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 180fc5c0a9c9e247d5bd6ec7f469f313463526df
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279501"
---
# <a name="manage-e-commerce-users-and-roles"></a>Verwalten von e-Commerce Benutzern und Rollen


[!include [banner](includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Benutzern Zugriff auf die Erstellungsumgebung für Ihre Microsoft Dynamics 365 Commerce-Website gewähren.

In der Umgebung zur Site-Erstellung werden von Ihnen in Microsoft erstellte Sicherheitsgruppen verwendet, um den Benutzerzugriff zu steuern und Benutzern die Berechtigung zum Ausführen bestimmter Aufgaben zu erteilen, die Sie in Microsoft Azure Active Directory (Azure AD) erstellen. Zunächst weisen Sie jeder Rolle in der Erstellungsumgebung eine neue oder vorhandene Sicherheitsgruppe aus Azure AD zu. Anschließend erteilen oder widerrufen Sie Berechtigungen für einzelne Benutzer, indem Sie diese Benutzer einer entsprechenden Sicherheitsgruppe hinzufügen oder aus einer Sicherheitsgruppe entfernen.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Übersicht über Rollen in der Erstellungsumgebung

Die Dynamics 365 for Commerce Erstellungsumgebung unterstützt die folgenden Rollen.

| Rolle                 | Beschreibung |
|----------------------|-------------|
| Systemadministrator | Benutzer mit dieser Rolle haben alle Berechtigungen für alle Tools sowie für alle Bewertungen und Überprüfungen. Sie können auch Sites erstellen. |
| Administrator   | Benutzer mit dieser Rolle haben alle Berechtigungen für alle Tools und RnR in einer bestimmten Site-Struktur. |
| Internet-Producer         | Benutzer mit dieser Rolle können Seiten, Fragmente und Vorlagen erstellen, Assets hochladen und verwalten sowie Produkte und Kategorien erweitern. |
| Leser               | Benutzer mit dieser Rolle können Seiten, Vorlagen, Assets, Fragmente, Layouts und Einstellungen anzeigen, aber möglicherweise keine Änderungen vornehmen. |
| RnR-Moderator        | Benutzer mit dieser Rolle können Produktbewertungen moderieren. |

## <a name="system-administrator-role"></a>Systemadministratorrolle

Wenn Sie Dynamics 365 Commerce in der Microsoft Dynamics Lifecycle Services-(LCS-)Umgebung bereitstellen, werden Sie gebeten, eine Sicherheitsgruppe für die Rolle **Systemadministrator** bereitzustellen. Diese Rolle wird dann automatisch auf alle Sites angewendet, die Sie in der von Ihnen konfigurierten Umgebung erstellen. Die Sicherheitsgruppe für diese Rolle kann nur in LCS aktualisiert werden. Auf der Seite **Websiteverwaltung** wird sie für alle Websites als schreibgeschützt angezeigt und dient nur zu Informationszwecken.

## <a name="administrator-role"></a>Administratorrolle

Wenn Sie eine neue Site in Commerce erstellen, werden Sie aufgefordert, eine Sicherheitsgruppe für die Rolle **Administrator** bereitzustellen. In der Tabelle weiter oben in diesem Artikel finden Sie eine Übersicht über die Berechtigungen, die diese Rolle gewährt.

## <a name="add-or-update-security-groups"></a>Hinzufügen oder Aktualisieren von Sicherheitsgruppen

Nachdem Ihre Site erstellt wurde, werden nur Benutzer in den Sicherheitsgruppen angezeigt, die dem **Systemadministrator** zugeordnet sind, und **Administrator**-Rollen können auf die Erstellungsumgebung für diese Site zugreifen. Um Benutzer den Rollen **Internet-Producer**, **RnR-Moderator** und **Leser** zuzuweisen, müssen Sie diesen Rollen Sicherheitsgruppen zuweisen. Gehen Sie folgendermaßen vor, um einer Rolle eine Sicherheitsgruppe hinzuzufügen oder eine Sicherheitsgruppe zu aktualisieren, die derzeit einer Rolle zugewiesen ist.

1. Gehen Sie zu der Site, die Sie aktualisieren möchten.
1. Öffnen Sie in **Websiteverwaltung** die Seite **Sicherheit**.
1. Wählen Sie die zu ändernde Rolle aus.
1. Fügen Sie Sicherheitsgruppen zu Rollen hinzu oder entfernen Sie Sicherheitsgruppen aus Rollen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

[Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site](search-engine-optimization-considerations.md)

[Verwalten der Inhaltssicherheitsrichtlinie](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
