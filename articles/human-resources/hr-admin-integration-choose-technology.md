---
title: Datenintegrationstechnologie auswählen
description: Dieser Artikel enthält Informationen zu verschiedenen Optionen für die Integration in Daten, die von Human Resources verwaltet werden. Er beschreibt die Merkmale verschiedener Integrationstechnologien, damit Integratoren fundierte Entscheidungen darüber treffen können, welche Technologien ihren Anforderungen am besten entsprechen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029887"
---
# <a name="choose-a-data-integration-technology"></a>Datenintegrationstechnologie auswählen

Dynamics 365 Human Resources verwaltet Geschäftsdaten, die für eine Vielzahl von Geschäftsprozessen nützlich sind. Dieser Artikel enthält Informationen zu verschiedenen Optionen für die Integration in Daten, die von Human Resources verwaltet werden. Er beschreibt die Merkmale verschiedener Integrationstechnologien, damit Integratoren fundierte Entscheidungen darüber treffen können, welche Technologien ihren Anforderungen am besten entsprechen.

## <a name="data-integration-vision"></a>Datenintegrationsvision

Microsoft betrachtet Geschäftsdaten als Schlüsselelemente, die ein Unternehmen einzigartig machen. Die Daten Ihres Unternehmens sind sehr wertvoll. Von einem Teil des Unternehmens erfasste und verwaltete Daten beziehen sich auf Daten, die von einem anderen Teil des Unternehmens erfasst wurden. Diese Beziehungen können zur Verbesserung von Geschäftsprozessen und Business Intelligence in Ihrem Unternehmen verwendet werden. Die Bereitstellung eines einfachen, sicheren und stabilen Zugriffs auf Ihre Geschäftsdaten, unabhängig davon, welches System die Daten „besitzt“, ist ein zentraler Grundsatz unserer Vision der Datenintegration in Human Resources.

In der Vergangenheit war die Integration von Daten zwischen mehreren Systemen schwierig.
Microsoft unternimmt Schritte, um die Datenintegration zu vereinfachen, und ein großer Schritt in Richtung dieses Ziels wird durch den [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) verwirklicht.

Zukünftig macht Human Resources Common Data Service zur bevorzugten öffentlichen Schnittstelle für Human Resources-Daten. Im Laufe der Zeit erwarten wir, dass alle wichtigen Daten, die von Human Resources verwaltet werden, in Common Data Service veröffentlicht werden. Wir empfehlen Common Data Service als Technologie der Wahl für die meisten integrierenden Anwendungen. Wir sind uns zwar bewusst, dass derzeit nicht alle für Ihre Anwendung erforderlichen Daten in Common Data Service vorhanden sind und das Ihre Projektlaufzeiten eine alternative Technologie erfordern. Lassen Sie uns deshalb wissen, wenn Common Data Service nicht Ihren Integrationsanforderungen entspricht.

## <a name="integration-technologies"></a>Integrationstechnologien

In den folgenden Abschnitten werden die verschiedenen Datenintegrationstechnologien beschrieben, die für die Verwendung mit Human Resources verfügbar sind.

### <a name="common-data-service-entities"></a>Common Data Service-Entitäten

Common Data Service ist die bevorzugte öffentliche Datenschnittstelle für Human Resources. Common Data Service basiert auf einer ausgereiften Plattform, die aus der Dynamics 365 „XRM“-Plattform hervorgegangen ist, auf der die [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement)-Lösungen aufbauen.

Common Data Service bietet eine Plattform für Datenentitäten und eine API für den Zugriff auf diese Entitäten. Wenn Human Resources in Ihrer Organisation bereitgestellt wird, ist Human Resources mit einer Common Data Service-Instanz verbunden und die Entitäten, die Human Resources-Daten verwalten, werden in dieser Common Data Service-Instanz bereitgestellt, sodass die Entitäten und ihre Daten für jede Anwendung verfügbar sind, die sich mit der Common Data Service-Instance verbindet. Abhängig davon, welche Human Resources-Apps Sie verwenden, führt Human Resources Datenoperationen direkt für Common Data Service-Entitäten aus (dies ist bei Attract und Onboard der Fall) oder synchronisiert Daten mit/von Common Data Service-Entitäten.

Sobald die Datenentitäten, die die Daten verfügbar machen, die Ihre integrierenden App erfordern, in Common Data Service vorhanden sind, können Sie [Common Data Service und die unterstützten APIs](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer) voll nutzen. Zu den unterstützten APIs gehört die [Dynamics 365-Web-API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), die eine OData-Implementierung für den Zugriff auf Common Data Service-Daten bereitstellt.

Die Common Data Service-Entitäten und die zugehörigen APIs sind die beste Option für den Zugriff auf Human Resources-Daten von Webanwendungen, Webdiensten/APIs und von jeder anderen Anwendung, die eine Verbindung zu OData-Feeds herstellt.

> [!NOTE]
> Da die Entscheidung, Common Data Service zur bevorzugten Datenschnittstelle für Human Resources zu machen, erst kürzlich getroffen wurde, stellen Sie möglicherweise fest, dass die Human Resources-Datenentitäten, die Sie für die Integration benötigen, möglicherweise noch nicht in Common Data Service<sup>1</sup> verfügbar sind. Wenn die für Ihre Integration erforderlichen Human Resources-Entitäten noch nicht verfügbar sind, müssen Sie warten, bis die Datenentitäten verfügbar sind, oder Sie müssen eine der anderen unten beschriebenen Integrationstechnologien verwenden.
> 
> Standardmäßig wird die Common Data Service-Integration in neuen Umgebung deaktiviert, die nicht die bereitgestellten Demodaten enthalten. Sie wird in neuen Umgebungen aktiviert, die Demo-Daten enthalten, und die Umgebungen beginnen mit der Datensynchronisierung, sobald die Umgebung bereitgestellt wird. Wenn die Umgebung bereit ist, Daten zu synchronisieren, können Sie die Integration aktivieren.

<sup>1</sup>Eine Liste der Human Resources-Entitäten, die in Common Data Service verfügbar sind, finden Sie unter [Human Resources und Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Für Attract und Onboard sind alle Entitäten in Common Data Service verfügbar.

### <a name="dmfdixf-entities"></a>DMF/DIXF-Entitäten

Human Resources, das hauptsächlich auf derselben Plattform aufbaut wie Finance and Operations-Anwendungen, bietet ein [Data Management Framework (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), das gelegentlich auch als Data Import Export Framework oder DIXF bezeichnet wird, sowie eine Reihe von Datenentitäten, die zum Importieren/Exportieren von Daten in bzw. aus Human Resources verwendet werden können. Auch wenn Common Data Service-Entitäten die bevorzugte Datenintegrationsschnittstelle für Human Resources darstellen, sind DMF-Entitäten weiterhin unter bestimmten Umständen nützlich, beispielsweise:

- Common Data Service-Entitäten sind noch nicht verfügbar.

- Die Integration erfordert leistungsstarke Funktionen zum Import/Export von Massendaten.

Die DMF-Einheiten bieten derzeit die umfassendste Datenabdeckung für Human Resources-Daten.

DMF eignet sich nicht für Echtzeitintegrationen (z. B., wenn sofortiges Benutzerfeedback bei einer Benutzeroberfläche erforderlich ist), da Paketvorgänge geplante Batchaufträge sind und oftmals eine Wartezeit von mindestens 1 bis 2 Minuten haben, ehe der Batch-Dienst den Job für die Ausführung annimmt. Dazu kommt noch die Zeit, die benötigt wird, um eine Import-/Export-Operation durchzuführen.

DMF ist möglicherweise die beste Option, wenn ein hoher Durchsatz erforderlich ist (z. B. ein nächtlicher geplanter Import/Export von vielen tausend Datensätzen).

> [!NOTE]
> DMF ist für Attract und Onboard nicht verfügbar.

### <a name="dmf-package-rest-api"></a>DMF-Paket REST-API

DMF bietet eine [REST-API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) zur Bearbeitung von Datenpaketen. Diese API kann zur programmgesteuerten Interaktion mit DMF verwendet werden und ermöglicht Aktionen wie:

- Importieren eines Datenpakets.

- Exportieren eines Datenpakets.

- Überprüfen des Status eines Import-/Exportvorgangs.

Die DMF-Paket-REST-API wird in Human Resources: Core HR voll unterstützt.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF bietet darüber hinaus eine leistungsstarke Funktion (allgemein bekannt als [Bring Your Own Database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) oder BYOD), mit der Human Resources Daten in Ihre eigene Microsoft Azure-SQL-Datenbank exportieren kann. Dies bietet enorme Flexibilität, da Sie, wenn die Daten in Ihrer eigenen SQL-Datenbank vorhanden sind, alle Anwendungen oder Middleware verwenden können, die eine Verbindung zu einem SQL-Datenspeicher herstellen können.

BYOD sollte im Allgemeinen als schreibgeschützte Lösung betrachtet werden. Während Sie beliebige Daten in der Azure SQL-Datenbank bearbeiten und speichern können (z. B. für Data Mashups), werden in der Azure SQL-Datenbank gespeicherte Daten nicht wieder mit Human Resources synchronisiert.

BYOD eignet sich für Berichtlösungen, Datenintegrationen und Data Mashups als Datenquelle für eine [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/)-Pipeline.

> [!NOTE]
> BYOD ist für Attract und Onboard nicht verfügbar.

### <a name="odata-enabled-entities"></a>OData-fähige Entitäten

Die meisten DMF-Entitäten sind auch für den Zugriff über den Human Resources-Datendienst (OData) konfiguriert. Die Dokumentation für den [Finance and Operations-OData-Dienst](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) gilt im Allgemeinen auch für Human Resources, wobei die Dokumentation zum Erstellen eigener OData-verfügbarer Entitäten nicht gilt.

Obwohl Common Data Service und die OData-Implementierung, die von Common Data Service bereitgestellt wird (durch die [Dynamics 365-Web-API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), dem Human Resources-Datendienst vorgezogen wird, hat der Human Resources-Datendienst eine größere Datenabdeckung für die Human Resources-Daten.

### <a name="excel-add-in"></a>Excel-Add-In

Das [Excel-Add-In](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) verwendet OData-fähige Objekte im Hintergrund. Bietet dem Endbenutzer eine bequeme Möglichkeit, Human Resources-Daten über die vertraute Excel-Benutzeroberfläche abzurufen und zu ändern.

Das Excel-Add-In eignet sich für Ad-hoc-Datenimporte und -Exporte durch Experten von Geschäftsdomänen. Für eine wiederkehrende Datenintegration, die eine programmgesteuerte Automatisierung erfordert, ist eine andere Integrationstechnologie besser geeignet.

### <a name="data-integrator"></a>Datenintegrator

Die Common Data Service-Administrator-Erfahrung bietet einen [Data Integrator-Dienst](https://docs.microsoft.com/powerapps/administrator/data-integrator), der für Datenintegrationen von/nach Common Data Service verwendet werden kann. Der Datenintegrator kann zum Definieren von Integrationsprojekten (häufig basierend auf vordefinierten Vorlagen, die Anwendungsentwickler für bestimmte Integrationen angepasst haben) verwendet werden. Die Integrationsprojekte können so geplant werden, dass sie automatisch nach einem wiederkehrenden Zeitplan oder manuell ausgeführt werden.

Datenintegrator-Projekte eignen sich für Common Data Service-Batch-Integrationen und eignen sich gut für Integrationen zwischen den Anwendungen der Dynamics 365-Familie. Microsoft stellt beispielsweise eine sofort einsatzbereite Datenintegrator-Vorlage zur Verfügung, mit der Daten aus Human Resources in Dynamics 365 Finance integriert werden können. Weitere Informationen finden Sie unter [Integration von Dynamics 365 Human Resources in Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Powerabfrage

Der Datenintegrator unterstützt auch [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (durch seine [Erweiterte Abfragefunktion](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Power Query bietet leistungsstarke, flexible Filter- und Transformationsfunktionen für Daten, einschließlich der umfangreichen M-Formelsprache und ist möglicherweise denen vertraut, die Erfahrungen mit der Entwicklung von Power BI-Berichten haben.

## <a name="deciding-on-an-integration-technology"></a>Entscheidung für eine Integrationstechnologie

Bei so vielen verschiedenen verfügbaren Integrationstechnologien kann es schwierig sein, zu entscheiden, welcher Integrationsansatz verwendet werden soll. Im Laufe der Zeit und insbesondere mit zunehmender Datenabdeckung in Common Data Service wird die Entscheidung leichter, Common Data Service in den meisten Fällen als bevorzugte Datenschnittstelle zu verwenden. Aber bis dahin sind Sie möglicherweise der Meinung, dass Common Data Service Ihre Anforderungen nicht erfüllt. In der folgenden Tabelle sind einige der wichtigsten Merkmale der verschiedenen Integrationstechnologie-Optionen zusammengefasst.

| Technology/Tool/API    | Wiederkehrende Integrationen                   | Synchron/Asynchron                    | Programmatischer Zugriff über eine API        | Angemessene Datenmengen                                   | Datenabdeckung                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service-Entitäten           | Ja, mit Data Integrator oder Middleware | Synchron, Asynchron, Batch (über Datenintegrator) | Ja, über die Dynamics 365-Web-API (OData) | Variiert je nach Anwendungsfall (unterstützt Paging für die interaktive Verwendung) | Verbesserung<sup>2</sup>                       |
| DMF-Entitäten           | Ja, geplant über Middleware        | Asynchron, Batch                                | Ja, über die DMF-Paket-REST-API         | Hoch (Hunderttausende von Datensätzen)                    | Hoch                                |
| DMF-Paket REST-API   | Ja, geplant über Middleware        | Asynchron, Batch                                | Ja                                       | Hoch (Hunderttausende von Datensätzen)                    | API unterstützt alle DMF-Entitäten       |
| BYOD                   | Ja, geplant vom Admin in Human Resources        | Asynchron, Batch                                | Kein<sup>3</sup>                                    | Hoch (Hunderttausende von Datensätzen)                    | Unterstützt alle DMF-Entitäten           |
| OData-fähige Entitäten | Ja, mit Middleware                    | Synchronisieren                                        | Ja, über den Human Resources-Datendienst (OData)  | Variiert je nach Anwendungsfall (unterstützt Paging für die interaktive Verwendung) | Hoch                                |
| Excel-Add-In           | Nein                                       | Synchronisieren                                        | Nein                                        | Mittel (Zehntausende von Datensätzen)                      | Unterstützt alle OData-fähigen Entitäten |
| Datenintegrator        | Ja, geplant in Data Integrator        | Asynchron, Batch                                | Nein                                        | Variiert je nach Anwendungsfall                                       | Unterstützt alle Common Data Service-Entitäten           |

<sup>2</sup>Microsoft investiert stark in die Erhöhung der Datenabdeckung für Common Data Service-Entitäten und empfiehlt Common Data Service als bevorzugte Datenschnittstelle, sobald eine hinreichende Datenabdeckung gegeben ist. Zurzeit ist die Common Data Service-Datenabdeckung im Vergleich zu DMF und OData-fähigen Entitäten gering.

<sup>3</sup>Auf die SQL-Datenbank kann programmgesteuert zugegriffen werden.

## <a name="summary"></a>Summe

Ihre Geschäftsdaten sind ein wertvolles Gut, ihr Wert kann jedoch erheblich beeinträchtigt werden, wenn es schwierig ist, die Daten für Ihre spezifischen Zwecke einzusetzen (z. B. für Berichterstellung, Data Mashups oder benutzerdefinierte Anwendungen). Dynamics 365 Human Resources bietet verschiedene Technologien für die Arbeit mit Ihren Daten außerhalb der Benutzeroberfläche der Human Resources-Anwendung, sodass integrierende Anwendungen auf die Daten zugreifen können. In diesem Thema wurden die verfügbaren Integrationstechnologien und einige ihrer wichtigsten Merkmale beschrieben. Diese Informationen sollen Ihnen helfen, besser darüber entscheiden zu können, welche Ansätze sich für Ihre Integrationsprojekte am besten eignen.

