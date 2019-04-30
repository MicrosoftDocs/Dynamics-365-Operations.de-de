---
title: Erweiterbarkeit in Attract
description: In diesem Thema wird beschrieben, wie Sie die Microsoft Dynamics 365 for Talent - Attract-Anwendung erweitern können, indem Sie die Microsoft Power-Plattform verwenden.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichsew
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 52790fbe500d9f55bc9cc86fba5d54f30b11e559
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/12/2019
ms.locfileid: "949965"
---
# <a name="extensibility-in-attract"></a>Erweiterbarkeit in Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent ist über die Common Data Service Plattform gebaut und kann auf verschiedene Weise erweitert werden, indem die Microsoft Power Platform  und Funktionen verwendet werden, die Common Data Service anbietet. Aus diesem Grund können Sie das System konfigurieren und anpassen, indem Sie Microsoft PowerApps und Microsoft Flow verwenden. Sie können auch eine zusätzliche Personen-Analyse erhalten, indem Sie Microsoft Power BI verwenden. Der Einstellungsprozess wird darüber hinaus durch neue benutzerdefinierte Aktivitäten, wie die PowerApps- und Webinhalt-Aktivitäten, noch flexibler als bisher. Wenn Sie diese Aktivitäten verwenden, können Sie den Einstellungsprozess auf Ihre Geschäftsanforderungen und -Prozesse anpassen und sicherstellen, dass das Einstellungsteam und die Kandidaten eine nahtlose angepasste Erfahrung haben.

## <a name="extending-option-sets-in-attract"></a>Erweitern von Optionsätzen in Attract

Ein **Optionssatz** (Auswahlliste) ist ein Feldtyp, der in eine Entität einbezogen werden kann. Er definiert einen Satz von Optionen. Wenn ein Optionssatz in einem Formular angezeigt wird, verwendet er ein Dropdownlistensteuerelement.  In Attract gibt es mehrere Felder, die Optionssätze sind.  Wir führen Funktion zur Erweiterung der Optionssätze ein und beginnen mit dem Feld "Ablehnungsgrund", dem Feld "Beschäftigungstyp" und dem Feld "Dienstalter".   Außerdem können lokalisierte Anzeigenbeschriftungen für die von Ihnen hinzugefügten Optionen hinzufügen. Weitere Informationen finden Sie unter [Beschriftungen der Option anpassen](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Die Funktion zur Stellenausschreibung auf LinkedIn erfordert die Nutzung der Felder **Beschäftigungstyp** und **Dienstaltertyp** auf der Seite **Stellendetails**. Die Standardwerte in den Feldern werden von LinkedIn unterstützt und angezeigt, wenn die Stelle gebucht wird. Wenn Sie also Stellen in LinkedIn veröffentlichen und die vorhandenen Optionssatzwerte für diese Felder ändern, wird die Stelle noch veröffentlicht, aber LinkedIn zeigt keine benutzerdefinierten Werte für **Beschäftigungstyp** und **Dienstaltertyp**.  

Im Folgenden werden die Schritte aufgeführt, mit denen das Felds **Ablehnungsgrund** mit den passenden Werten für Ihr Unternehmen aktualisiert werden kann.  

1. Wenn Sie den **Ablehnungsgrund**-Optionssatz verlängern möchten, navigieren Sie zur [PowerApps-Administrator-Website](https://admin.powerapps.com).
2. Sie werden möglicherweise aufgefordert, sich in Ihrem Konto anzumelden. Geben Sie Ihre aus Benutzer-ID- und Kennwort betehenden Anmeldeinformationen aus, die Sie verwenden, um sich in Dynamics365 und/oder in Office365 anzumelden, und klicken Sie dann auf **Weiter**.
3. In der Registerkarte **Umgebungen** wählen die Umgebung, die Sie verwalten möchten, und doppelklicken Sie darauf, um zur Registerkarte **Details** zu gelangen.
4. In der Registerkarte **Details** wählen Sie **Dynamics 365-Verwaltungscenter** aus.
5. Wählen Sie die Instanz aus, die Sie ändern möchten, und wählen Sie **Öffnen** aus.
6. Navigieren Sie zu **Einstellungen** und dann zu **Anpassungen**, und wählen Sie **System anpassen** aus.
7. Suchen Sie nach der Entität, für die Sie den Optionssatz verlängert möchten, indem Sie **Entitäten** auswählen und die Gruppe erweitern. In diesem Beispiel ist es die **Bewerbungsentität**.
8. Wechseln Sie zum Feld, für das Sie den Optionssatz verlängert möchten, indem Sie die Option **Felder** auswählen. In diesem Beispiel ist es **msdyn_rejectionreason**. Doppelklicken Sie auf das Feld.
9. Wählen Sie im Feld **Optionssatz** die Option **Bearbeiten** aus.
10. Wählen Sie das **+**-Feld aus.
11. Geben Sie eine **Beschriftung** ein.  (Diese muss ein eindeutiger Wert sein – keine Duplikate).
12. Wählen Sie **Speichern**.
13. Wählen Sie am oberen Seitenrand **Veröffentlichen** aus.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Nutzen Sie die Microsoft Power Platform 

Da sich alle Attract-Daten in Common Data Service befinden, können Sie Tools der Microsoft Power Platform verwenden, um Ihre Geschäftsanforderungen in Attract zu integrieren.

### <a name="powerapps"></a>PowerApps

Sie können PowerApps verwenden, um leicht Apps zu erstellen, die eine Verbindung mit Ihren Attract-Daten herstellen und Ausdrücke wie die Ausdrücke in Microsoft Excel verwenden, um Logik hinzuzufügen. Apps, die Sie erstellen, indem Sie PowerApps verwenden, können im Internet und auf Apple iOS- und Google Android-Geräten ausgeführt werden.

So können Sie z. B. Hochschulkarrieremessen für Personalbeschaffer erleichtern, indem Sie eine einfache App erstellen, mit der sie Lebensläufe scannen und Kandidaten einer Position in Attract zuweisen können. Alternativ können Sie eine App erstellen, mit der Sie die Compliance-Anforderungen Ihrer Organisation erfüllen. Weitere Informationen zu PowerApps und wie Sie es verwenden, um Apps zu erstellen, finden Sie unter [Daten in Common Data Service for Apps integrieren](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Sie können Microsoft Flow verwenden, um automatisierte Workflows zu erstellen, die auf Attract-Daten basieren. Sie können leicht eine Verbindung mit Hunderten beliebter Apps und Dienstleistungen herstellen, ohne Code schreiben zu müssen. Durch Erstellen von Flüssen, die mit den Attract Stelle, Kandidat und Bewerbung in Common Data Service interagieren, können Sie verschiedene Aktionen automatisieren. Wenn ein Kandidat beispielsweise ein Angebot akzeptiert, kann eine Benachrichtigung an ein Onboarding-Team gesendet, oder die Neuigkeiten können auf Twitter angekündigt werden. Weitere Informationen zu Flüssen finden Sie in der [Microsoft Flow-Dokumentation](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Mit Power BI können Sie benutzerdefinierte Berichte und Dashboards erstellen und anzeigen, die Ihnen einen tieferen Einblick in Ihre Attract-Daten geben. Weitere Informationen zu Power BI und zur Erstellung interaktiver Berichte und Dashboards finden Sie in der [Power BI-Dokumentation](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Benutzerdefinierte Aktivitäten 

Sie können benutzerdefinierte Aktivitäten, wie die PowerApps-Apps und Web-Inhalts (iframe)-Aktivitäten auf der Ebene der Stellenprozessvorlage hinzufügen, oder während Sie eine neue Stelle erstellen. Mit diesen Aktivitäten können Sie den Einstellungsprozess anpassen und die einmalige Geschäftslogik Ihrer Organisation in Attract integrieren.

#### <a name="powerapps-activity"></a>PowerApps-Aktivität 

Die PowerApps-Aktivität ermöglicht es dem Ersteller einer Stelle oder Stellenprozessvorlage, eine PowerApps-App im Einstellungsfluss einzubetten. Nachdem Sie die App erstellt und veröffentlicht haben, können Sie die App-ID in den Aktivitätskonfigurationen eingeben. Durch Verwendung einer PowerApps App können Sie Daten in Common Data Service for Apps lesen und schreiben. Sie können die App sogar mit einem Flow verknüpfen. Beispielsweise verfügen Sie über eine App, die Personalbeschaffer verwenden, um ein Formular auszufüllen, während sie Telefongespräche tätigen. In diesem Fall können Sie die App einem Flow verknüpfen, der bewertet, ob ein Bewerber im Stellenbewerbungsprozess voranschreitet. Dieser Aktivitätstyp kann nur von Mitgliedern des Einstellungsteams angezeigt werden. Weitere Informationen dazu, wie die PowerApps-Aktivität konfiguriert wird, finden Sie unter [Aktivitäten in Attract](./activities-attract.md).

> [!NOTE]
> Die PowerApps-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.

#### <a name="web-content-iframe-activity"></a>Webinhalt (iframe)-Aktivität

Die Webinhalts (iframe)-Aktivität erlaubt es Ihnen, eine benutzerdefinierte Internetlösung einzubetten, die Sie im Einstellungsprozess oder Kandidatenportal erstellt haben. Sie können Daten direkt aus Common Data Service lesen und schreiben. Sie können die Lösung auch anpassen, sodass sie Flüsse auslöst oder Microsoft Azure-Funktionen nutzt. Weitere Informationen dazu, wie die Webinhalt-Aktivität konfiguriert wird, finden Sie unter [Aktivitäten in Attract](./activities-attract.md).

> [!NOTE]
> Die Webinhalt-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.
