---
title: Erweiterbarkeit in Attract
description: In diesem Thema wird beschrieben, wie Sie die Microsoft Dynamics 365 for Talent - Attract-Anwendung erweitern können, indem Sie die Microsoft Power-Plattform verwenden.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304503"
---
# <a name="extensibility-in-attract"></a>Erweiterbarkeit in Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent basiert auf der Common Data Service (CDS) for Apps-Plattform und kann auf verschiedene Weise erweitert werden, indem die Microsoft Power-Plattform und die Funktionen verwendet werden, die von Common Data Service for Apps angeboten werden. Aus diesem Grund können Sie das System konfigurieren und anpassen, indem Sie Microsoft PowerApps und Microsoft Flow verwenden. Sie können auch eine zusätzliche Personen-Analyse erhalten, indem Sie Microsoft Power BI verwenden. Der Einstellungsprozess wird darüber hinaus durch neue benutzerdefinierte Aktivitäten, wie die PowerApps- und Webinhalt-Aktivitäten, noch flexibler als bisher. Wenn Sie diese Aktivitäten verwenden, können Sie den Einstellungsprozess auf Ihre Geschäftsanforderungen und -Prozesse anpassen und sicherstellen, dass das Einstellungsteam und die Kandidaten eine nahtlose angepasste Erfahrung haben.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Nutzen Sie die Microsoft Power Platform 

Da sich alle Attract-Daten in Common Data Service for Apps befinden, können Sie Tools der Microsoft Power-Plattform verwenden, um Ihre Geschäftsanforderungen in Attract zu integrieren.

### <a name="powerapps"></a>PowerApps

Sie können PowerApps verwenden, um leicht Apps zu erstellen, die eine Verbindung mit Ihren Attract-Daten herstellen und Ausdrücke wie die Ausdrücke in Microsoft Excel verwenden, um Logik hinzuzufügen. Apps, die Sie erstellen, indem Sie PowerApps verwenden, können im Internet und auf Apple iOS- und Google Android-Geräten ausgeführt werden.

So können Sie z. B. Hochschulkarrieremessen für Personalbeschaffer erleichtern, indem Sie eine einfache App erstellen, mit der sie Lebensläufe scannen und Kandidaten einer Position in Attract zuweisen können. Alternativ können Sie eine App erstellen, mit der Sie die Compliance-Anforderungen Ihrer Organisation erfüllen. Weitere Informationen zu PowerApps und wie Sie es verwenden, um Apps zu erstellen, finden Sie unter [Daten in Common Data Service for Apps integrieren](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Sie können Microsoft Flow verwenden, um automatisierte Workflows zu erstellen, die auf Attract-Daten basieren. Sie können leicht eine Verbindung mit Hunderten beliebter Apps und Dienstleistungen herstellen, ohne Code schreiben zu müssen. Durch Erstellen von Flüssen, die mit den Attract-Entitäten für Stelle, Kandidat und Bewerbung in Common Data Service for Apps interagieren, können Sie verschiedene Aktionen automatisieren. Wenn ein Kandidat beispielsweise ein Angebot akzeptiert, kann eine Benachrichtigung an ein Onboarding-Team gesendet, oder die Neuigkeiten können auf Twitter angekündigt werden. Weitere Informationen zu Flüssen finden Sie in der [Microsoft Flow-Dokumentation](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Mit Power BI können Sie benutzerdefinierte Berichte und Dashboards erstellen und anzeigen, die Ihnen einen tieferen Einblick in Ihre Attract-Daten geben. Weitere Informationen zu Power BI und zur Erstellung interaktiver Berichte und Dashboards finden Sie in der [Power BI-Dokumentation](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Benutzerdefinierte Aktivitäten 

Sie können benutzerdefinierte Aktivitäten, wie die PowerApps-Apps und Web-Inhalts (iframe)-Aktivitäten auf der Ebene der Stellenprozessvorlage hinzufügen, oder während Sie eine neue Stelle erstellen. Mit diesen Aktivitäten können Sie den Einstellungsprozess anpassen und die einmalige Geschäftslogik Ihrer Organisation in Attract integrieren.

#### <a name="powerapps-activity"></a>PowerApps-Aktivität 

Die PowerApps-Aktivität ermöglicht es dem Ersteller einer Stelle oder Stellenprozessvorlage, eine PowerApps-App im Einstellungsfluss einzubetten. Nachdem Sie die App erstellt und veröffentlicht haben, können Sie die App-ID in den Aktivitätskonfigurationen eingeben. Durch Verwendung einer PowerApps-App können Sie Daten in Common Data Service for Apps lesen und schreiben. Sie können die App sogar mit einem Flow verknüpfen. Beispielsweise verfügen Sie über eine App, die Personalbeschaffer verwenden, um ein Formular auszufüllen, während sie Telefongespräche tätigen. In diesem Fall können Sie die App einem Flow verknüpfen, der bewertet, ob ein Bewerber im Stellenbewerbungsprozess voranschreitet. Dieser Aktivitätstyp kann nur von Mitgliedern des Einstellungsteams angezeigt werden. Weitere Informationen dazu, wie die PowerApps-Aktivität konfiguriert wird, finden Sie unter [Aktivitäten in Attract](./activities-attract.md).

> [!NOTE]
> Die PowerApps-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.

#### <a name="web-content-iframe-activity"></a>Webinhalt (iframe)-Aktivität

Die Webinhalts (iframe)-Aktivität erlaubt es Ihnen, eine benutzerdefinierte Internetlösung einzubetten, die Sie im Einstellungsprozess oder Kandidatenportal erstellt haben. Sie können Daten direkt aus Common Data Service for Apps lesen und schreiben. Sie können die Lösung auch anpassen, sodass sie Flüsse auslöst oder Microsoft Azure-Funktionen nutzt. Weitere Informationen dazu, wie die Webinhalt-Aktivität konfiguriert wird, finden Sie unter [Aktivitäten in Attract](./activities-attract.md).

> [!NOTE]
> Die Webinhalt-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.
