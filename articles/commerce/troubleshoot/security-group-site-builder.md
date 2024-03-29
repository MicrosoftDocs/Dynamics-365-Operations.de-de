---
title: Während der ersten Bereitstellung kann keine Sicherheitsgruppe für den Commerce-Website-Generator konfiguriert werden
description: Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Microsoft Azure Active Directory (Azure AD)-Sicherheitsgruppe für den Commerce-Website-Generator beim Erstellen von E-Commerce-Komponenten in Microsoft Dynamics Lifecycle Services (LCS) nicht während der ersten Bereitstellung eines neuen E-Commerce-Mandanten als Option angezeigt werden.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 7098c853c262fd7e0d48231634b232eef71c2b8d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291999"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Während der ersten Bereitstellung kann keine Sicherheitsgruppe für den Commerce-Website-Generator konfiguriert werden

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Microsoft Azure Active Directory (Azure AD)-Sicherheitsgruppe für den Commerce-Website-Generator beim Erstellen von E-Commerce-Komponenten in Microsoft Dynamics Lifecycle Services (LCS) nicht während der ersten Bereitstellung eines neuen E-Commerce-Mandanten als Option angezeigt werden.

## <a name="description"></a>Beschreibung

Wenn Sie die E-Commerce-Komponenten im Rahmen der Bereitstellung eines neuen E-Commerce-Mandanten erstellen, der die Commerce-Website-Generator-Komponente enthält, wird die Azure AD-Sicherheitsgruppe im Dialogfeld nicht als Option angezeigt.

## <a name="resolution"></a>Lösung

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Der E-Commerce-Website einen Benutzer im richtigen Mandanten zur Verfügung stellen

1. Gehen Sie zu [Azure-Portal](https://portal.azure.com/).
1. Befolgen Sie in dem Mandanten, für den das LCS-Projekt Ihrer E-Commerce-Website bereitgestellt wurde, die Anweisungen in [Erstellen einer Basisgruppe und Hinzufügen von Mitglieder mit Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Rufen Sie [LCS](https://lcs.dynamics.com/) auf, und melden Sie sich mit einem Konto an, das über denselben Mandanten wie die Azure AD-Sicherheitsgruppe verfügt, die Sie gerade erstellt haben. Das Konto muss Zugriff haben, um die Azure AD-Sicherheitsgruppe anzuzeigen.
1. Führen Sie die Einrichtungsschritte aus, um die E-Commerce-Website zu konfigurieren. Wenn Sie die E-Commerce-Komponenten bereitstellen, sollte die Sicherheitsgruppe jetzt als Option im Dialogfeld angezeigt werden.

> [!NOTE]
> Um sicherzustellen, dass das Feld im Dialogfeld mit der Liste der Sicherheitsgruppen ausgefüllt ist, müssen Sie **Eingeben** auswählen, sobald Sie den Namen der erstellten Azure AD-Sicherheitsgruppe eingegeben haben. In den Suchergebnissen werden alle Azure AD-Sicherheitsgruppen aufgelistet, die mit dem Suchtext beginnen und auf die der Benutzer Zugriff hat. Sie können einen kürzeren Suchbegriff verwenden, um breitere Suchergebnisse zu ermöglichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erstellen einer Basisgruppe und Hinzufügen von Mitgliedern mit Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Neuen E-Commerce-Mandanten bereitstellen](../deploy-ecommerce-site.md)
