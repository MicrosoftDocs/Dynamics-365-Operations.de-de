---
title: Das Add-In für Microservices in Lifecycle Services installieren
description: In diesem Artikel wird erklärt, wie Sie das Add-In für die Elektronische Rechnungsstellung in Microsoft Dynamics Lifecycle Services (LCS) installieren.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 26f92262eff07ded3e894ee5513dd8dbaa6f94a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849804"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Das Add-In für Microservices in Lifecycle Services installieren

[!include [banner](../includes/banner.md)]

Die Authentifizierung im Dienst für die elektronische Rechnungsstellung erfordert, dass Sie Ihre Microsoft Dynamics 365 Finance- oder Dynamics 365 Supply Chain Management-Umgebung in der Diensteplattform registrieren, indem Sie das Add-In für Ihre Umgebung in Microsoft Dynamics Lifecycle Services (LCS) installieren.

Um eine Umgebung zu registrieren, führen Sie diese Schritte aus.

1. Melden Sie sich bei Ihrem LCS-Konto an.
2. Wählen Sie auf dem Dashboard für Projekte ein LCS-Projekt aus.
2. Wählen Sie im Projekt im Dashboard **Umgebungs** Ihre bereitgestellte Umgebung aus. Die von Ihnen ausgewählte Umgebung muss ausgeführt werden.
3. Wählen Sie auf der Registerkarte **Power Platform Integration** im Abschnitt **Umgebungs-Add-Ins** die Option **Ein neues Add-In installieren**.
4. Wählen Sie **Elektronische Rechnungsstellung** aus.
5. Geben Sie im **AAD-Anwendungs-ID**-Feld **091c98b0-a1c9-4b02-b62c-7753395ccabe** ein. Dieser Wert ist ein fester Wert. Achten Sie darauf, dass Sie nur einen global eindeutigen Bezeichner (GUID) eingeben. Fügen Sie keine anderen Symbole ein, wie Leerzeichen, Kommas, Punkte oder Anführungszeichen.
6. Geben Sie in das Feld **AAD-Mandanten-ID** die Mandanten-ID Ihres Azure-Abonnementkontos ein. Der Azure Active Directory (Azure AD) Mandant, den Sie angeben, sollte derselbe sein, der auch für Regulatory Configuration Service (RCS) verwendet wird.
7. Überprüfen Sie die Bestimmungen und aktivieren Sie das Kontrollkästchen.
8. Wählen Sie **Installieren**. Nach einigen Minuten sollte sich der Status von **Installieren** in **Installiert** ändern. Möglicherweise müssen Sie die Seite aktualisieren, um diese Änderung zu sehen.

Die Elektronische Rechnungsstellung ist jetzt einsatzbereit.

> [!NOTE]
> Unternehmen verfügen in der Regel über mehrere Umgebungen für Finance oder Supply Chain Management. Zu diesen Umgebungen gehören Produktionsumgebungen, Umgebungen für User Acceptance Tests (UAT) und Entwicklungsumgebungen (Sandbox). Sie müssen das oben beschriebene Verfahren für alle Umgebungen durchführen, die Sie mit der Elektronischen Rechnungsstellung verbinden möchten.