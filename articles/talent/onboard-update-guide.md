---
title: Onboarding Anleitungen aktualisieren in Dynamics 365 for Talent - Onboard
description: In diesem Thema wird erläutert, wie Onboarding Anleitungen in Microsoft Dynamics 365 for Talent - Onboard aktualisiert und wie Änderungen an den vorhandenen Anleitungen vorgenommen werden.
author: andreabichsel
manager: ''
ms.date: 06/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d2be450685724510db2f0fd2af8545f8f40278e7
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731484"
---
# <a name="update-onboarding-guides-in-dynamics-365-for-talent-onboard"></a>Onboarding Anleitungen aktualisieren in Dynamics 365 for Talent: Onboard

[!include [banner](includes/banner.md)]

Wenn Sie Änderungen an Onboarding Anleitungen vornehmen in Microsoft Dynamics 365 for Talent: Onboard, können sie aktualisiert werden und die Änderungen vornehmen, selbst wenn die Anleitungen bereits übermittelt wurden. Sie haben zwei Optionen zum Aktualisieren einer Onboarding Anleitung:

- Bearbeiten Sie die Onboarding Anleitung direkt, und speichern Sie die Änderungen.
- Bearbeiten Sie die Onboarding Vorlage, und aktualisieren Sie dann die Änderungen per Push auf allen Onboarding Anleitungen, die daraus erstellt wurden.

## <a name="edit-an-onboarding-guide-directly"></a>Bearbeiten eines Onboarding Handbuches direkt

1. Wählen Sie im linken Menü **Anleitungen** aus.
2. Wählen Sie die Anleitung, die Sie bearbeiten möchten.
3. Nehmen Sie alle gewünschten Änderungen vor, und wählen Sie dann **Speichern** aus (das Diskettensymbol).

    ![[Änderungen an einem Onboarding Handbuch ](. /media/onboard-save.png)](./media/onboard-save.png)

Onboard wird automatisch den neuen Mitarbeiters eine E-Mail senden, die angibt, welche Änderungen vorgenommen wurden. Zur einfacheren Kennung erscheint eine rote Markierung **Neu** neben jeder Änderung.

## <a name="update-multiple-guides-by-editing-the-onboarding-template"></a>Aktualisieren Sie mehrere Anleitungen, indem Sie die Onboarding Vorlage bearbeiten

1. Wählen Sie im linken Menü **Vorlagen** aus.
2. Wählen Sie unter **Meine Vorlagen** die Vorlage aus, die Sie bearbeiten möchten.
3. Nehmen Sie alle gewünschten Änderungen vor, und wählen Sie dann **Speichern** aus (das Diskettensymbol).
4. Damit Ihre Änderungen an allen Anleitungen erfolgen, die auf der Vorlage basieren, wählen Sie **Änderungen per Push übertragen** aus.

    ![[Aktualisieren Sie die Änderungen per Push auf allen Onboarding Anleitungen, die daraus erstellt wurden](./media/onboard-push-changes.png)](./media/onboard-push-changes.png)

Die Änderungen werden den neuen Mitarbeitern angezeigt, die die Onboarding Anleitungen öffnen. Allerdings sendet Onboard keine E-Mail-Warnungen an neue Mitarbeiter, um sie zu informieren, dass ihr Onboarding Handbuch geändert hat. Zur einfacheren Kennung erscheint eine rote Markierung **Neu** neben jeder Änderung. 
