---
title: Erfassung von Webaktivitätsereignissen deaktivieren
description: In diesem Artikel wird erläutert, wie Sie Besuchern Ihrer Website erlauben können, die Sammlung von Webaktivitätsereignissen in Microsoft Dynamics 365 Commerce zu kündigen.
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286724"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Erfassung von Webaktivitätsereignissen deaktivieren
[!include [banner](includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Kunden erlauben können, die Sammlung von Webaktivitätsereignissen in Microsoft Dynamics 365 Commerce zu kündigen.

Dynamics 365 Commerce ermöglicht den Websiteadministratoren die Analyse der Webaktivität der Benutzer ihrer E-Commerce-Sites. Auf diese Weise können sie besser verstehen, wie ihre Websites verwendet werden, und die Websites optimieren, um eine verbesserte Benutzererfahrung zu erzielen und Geschäftsziele zu erreichen.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Möglichkeiten für Administratoren, ein Abmeldungs-Erlebnis zu implementieren

Administratoren haben drei Möglichkeiten, ein Abmeldungs-Erlebnis zu implementieren.

### <a name="opt-out-on-behalf-of-users"></a>Kündigen im Namen der Benutzer

In der Kontoverwaltung in der Commerce headquarters können sich Administrator für Benutzer abmelden.

1. Im HQ-Client auf der Seite **Alle Kunden** suchen und wählen Sie einen Kunden aus.
1. Auf der Kundendetailseite im Inforegister **Einzelhandel**, im Abschnitt **Privatsphäre** stellen Sie die Option **Webaktivität nicht verfolgen** auf **Ja**.

    ![Datenschutzeinstellungen.](media/Disablepersonalizationpart2.png)

1. Klicken Sie auf **Speichern** und schließen Sie die Seite.

### <a name="module-based-opt-out-experience"></a>Erfahrung mit modulbasierter Abmeldungs-Erfahrung

Administratoren können authentifizierte Benutzer die Erfassung von Webaktivitätsereignissen selbst deaktivieren lassen. Fügen Sie das Benutzer-Deaktivierungsmodul zu den Profilseiten des Kundenkontos hinzu, um diese Deaktivierungsfunktion zu nutzen.

### <a name="custom-extensions"></a>Benutzerdefinierte Erweiterungen

Administratoren können ihre eigenen Erweiterungen erstellen, um das Abmelde-Erlebnis für Benutzer zu verwalten. Weitere Informationen finden Sie unter [Rufen Sie die Retail Server APIs auf](e-commerce-extensibility/call-retail-server-apis.md) und [Online-Kanal-Erweiterbarkeit](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
