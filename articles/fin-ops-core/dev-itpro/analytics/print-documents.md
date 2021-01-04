---
title: Dokumentendruck – Übersicht
description: Sie können Dokumente drucken, indem Sie entweder einen lokalen Drucker oder ein mit dem Netzwerk verbundenes Gerät verwenden. Dieser Artikel gibt eine Übersicht, wie Dokumente gedruckt werden.
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1d64a2efeade5e9ba24f4dfe61c861f5a4cbad4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680095"
---
# <a name="document-printing-overview"></a>Dokumentendruck – Übersicht

[!include [banner](../includes/banner.md)]

Sie können Dokumente drucken, indem Sie entweder einen lokalen Drucker oder ein mit dem Netzwerk verbundenes Gerät verwenden. Dieser Artikel gibt eine Übersicht, wie Dokumente gedruckt werden.

## <a name="printing-overview"></a>Drucküberblick

Die Anwendung bietet integrierte Dienstleistungen und benutzerdefinierte Anwendungen, die das Nachverfolgen, Generieren, Speichern und Verteilen von Dokumenten vornehmen, die eine Geschäftsaktivität unterstützen. Sie können Dokumente drucken, indem Sie entweder einen lokalen Drucker oder ein mit dem Netzwerk verbundenes Gerät verwenden. Darüber hinaus können Sie Seiten und Berichte direkt vom Kunden als PDF-Dateien oder Microsoft Office-Dokumente exportieren. Schließlich können Sie mit der verteilten Arbeitsauslastung Geschäftsdokumente direkt von einem mobilen Gerät drucken, indem Netzwerkressourcen verwendet werden. Obwohl das Drucken von Anforderungen variieren kann, müssen alle Branchen Ausdrucke von Geschäftsdokumenten mithilfe der Anwendung erstellen. Das Drucken von Dokumenten auf Netzwerkgeräten von gehosteten Anwendungen stellt verschiedene Herausforderungen dar. Nachfolgend finden Sie einige Beispiele:

- Druckertreiber sind unter Umständen nicht für das Gerät des Benutzers verfügbar.
- Das Gerät des Benutzers verbindet sich nicht mit dem Unternehmensnetzwerk.

Indem ein dedizierter Host verwendet und einigen einfachen Schritten gefolgt wird, können Systemadministratoren Bereitstellungen konfigurieren, sodass Benutzer direkt aus den Geschäftsanwendungen auf Netzwerkgeräten drucken können.

### <a name="application-printing-scenarios"></a>Anwendungsdruckszenarien 

In der folgenden Tabelle werden die drei primären Druckszenarien beschrieben.

| Szenario                        | Ziel                                                      | Lösung |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Drucken, was Sie sehen        | Drucken, was derzeit im Browser angezeigt wird.             | Eine "Drucker freundliche " Version der Webseite wird für den Browser generiert. |
| 2. Interaktives Drucken         | Drucken eines Genauigkeitsdokument lokal an einem verbundenen Gerät. | Sie können eine PDF-Version des Berichts exportieren und im Browser herunterladen. |
| 3. Drucken auf einem Netzwerkgerät | Senden eines Genauigkeitsdokument an ein Domänendruckergerät.     | Ein Genauigkeitsdokument wird an eine Clientanwendung gesendet, die auf einem Server ausgeführt wird, der in der Domäne des Debitors gehostet wird. |

Da die Auflösun je nach spezifischem Szenario ändert, stellt einen integrierten Dienst und Werkzeuge bereit, die dem Benutzer helfen, die Ziele zu erreichen:

- **Szenario 1** wird über das Rendering des Browsers des HTML5 Clients unterstützt.
- **Szenario 2** verwendet Clientanwendungen und Microsoft 365 Dienstleistungen.
- **Szenario 3** erfordert Unterstützung von benutzerdefinierten Anwendungen und von Diensten, die in Microsoft Azure gehostet werden.

Neben der Plattform, die im Azure Abonnement bereitgestellt wird, stellen Finance and Operations-Anwendungen Kunden eine integrierte Azure Anwendung des Erstanbieters bereit, damit sie einfacher Domäne-gehostete Geräte verwenden können, um Dokumente zu drucken.

## <a name="service-overview"></a>Dienstleistungsüberblick
Während Dokumente, die über gehostete Anwendungen produziert werden, darauf warten, auf einem mit dem Netzwerk verbundenen Gerät gedruckt zu werden, werden diese im Azure BLOB-Speicher gespeichert. [Installieren des Document Routing Agent, um das Drucken im Netzwerk zu ermöglichen](install-document-routing-agent.md) verwendet die Azure-Authentifizierung, um einen sicheren Kanal zu den Azure-Diensten herzustellen.

**Ausführungssequenz**

1. Der Bericht wird von Microsoft SQL Server Reporting Services (SSRS) generiert und im Azure BLOB-Speicher gespeichert. Die zugeordneten Druckereinstellungen werden zusammen mit dem Dokument gespeichert.
2. Die Dokument-Routing-Agent Abfragen ruft die Azure Service-Buswarteschlange für aktive Aufträge ab.
3. Das Dokument wird durch den Dokument-Routing-Agenten heruntergeladen und auf den Netzwerkdrucker gespoolt.

Das clientbasierte Lösung ermöglicht Debitoren, ihre Druckenanforderungen zu verwalten. Debitoren, die hohe Druckerarbeitsauslastungen haben, können viele Dokument-Routing-Agenten einrichten, um die Anzahl gleichzeitiger Druckarbeitsgänge zu erhöhen. Alternativ benötigen einige Kunden sehr wenige Installationen des Dokument-Routing-Agenten, um ihre Druckeranforderungen zu behandeln.

### <a name="service-components-for-network-printing"></a>Service-Komponenten für Netzwerkdrucker

Im folgenden Diagramm werden die Grundkomponenten gezeigt, die Netzwerkdruckvorgänge unterstützen.

![[Service-Komponenten für Netzwerkdrucker\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Beachten Sie, dass ein einzelner Drucker mit mehreren Dokument-Routing-Agenten erfasst werden kann. Um die Druckereinstellungen aufzulösen, verwendet die gehostete Dienstleistung den Netzwerkpfad, der jeden Netzwerkdrucker eindeutig identifiziert. Selbst wenn ein Drucker mehrere Kunden erfasst, erscheint dieser als einzelne Auswahl in der Liste der Drucker, die in den Anwendungen verfügbar sind.
