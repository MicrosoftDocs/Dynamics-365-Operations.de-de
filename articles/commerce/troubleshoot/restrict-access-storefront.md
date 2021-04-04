---
title: Den Storefront-Zugriff während des Testens oder der Entwicklung beschränken
description: In diesem Thema wird erläutert, wie Sie beim Durchführen interner Tests oder Entwicklungen den Zugriff auf eine Microsoft Dynamics 365 Commerce-Storefront beschränken.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585343"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Den Storefront-Zugriff während des Testens oder der Entwicklung beschränken

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie beim Durchführen interner Tests oder Entwicklungen den Zugriff auf eine Microsoft Dynamics 365 Commerce-Storefront beschränken.

## <a name="description"></a>Beschreibung

Sie möchten möglicherweise bei internen Tests oder aktiven Entwicklungen den Zugriff auf Ihre Website einschränken, um zu verhindern, dass externe Benutzer auf die veröffentlichten Storefront-Seiten zugreifen.

## <a name="resolution"></a>Lösung

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Azure AD B2C mithilfe von Standardbenutzerflows einrichten

Informationen zum Konfigurieren von Azure Active Directory B2C (Azure AD B2C) für Ihre E-Commerce-Website siehe [Einen B2C-Mandanten in Commerce einrichten](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Den Benutzerzugriff auf Storefront-Seiten beschränken und die Erstellung neuer Benutzer sperren

Befolgen Sie die folgenden Schritte, um den Benutzerzugriff auf Storefront-Seiten im Commerce-Website-Generator zu beschränken.

1. Rufen Sie die Website auf.
1. Wählen Sie unter **Seiten** die Seite aus, für die der Benutzerzugriff beschränkt werden soll.
1. Wählen Sie das Modul oder den Fragmentslot und anschließend **Bearbeiten** aus.
1. Wählen Sie im Eigenschaftenbereich die Option **Anmeldung erforderlich?** und anschließend **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus.

Befolgen Sie diese Schritte, um die Erstellung neuer Benutzer in Azure AD zu sperren.

1. Gehen Sie zu [Azure-Portal](https://portal.azure.com/).
1. Wählen Sie die Azure AD B2C-Anwendung aus, die Sie für Ihren Website-Zugriff erstellt haben.
1. Wählen Sie im linken Navigationsbereich **Benutzerflows** aus.
1. Wählen Sie oben auf der Seite **Benutzerflows** die Option **Neuer Benutzerflow** aus.
1. Wählen Sie auf der Seite **Benutzerflowtyp auswählen** die Option **Vorschau** aus.
1. Wählen Sie in der Mitte der Seite die Option **Anmelden v2** aus. Befolgen Sie dann die Schritte in [Einen B2C-Mandanten in Commerce einrichten](../set-up-b2c-tenant.md), um den Flow als Standardbenutzerflow Ihrer Website für Azure AD B2C während des Testens oder der Entwicklung zu konfigurieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[B2C-Mandanten in Commerce einrichten](../set-up-b2c-tenant.md)

[Angepasste Seiten für die Benutzeranmeldung einrichten](../custom-pages-user-logins.md)