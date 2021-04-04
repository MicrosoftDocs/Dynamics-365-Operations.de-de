---
title: Verwaltungskomponenten im Add-On zur elektronischen Rechnungsstellung
description: Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung des Add-Ons für die elektronische Rechnungsstellung beziehen.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592573"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Verwaltungskomponenten im Add-On zur elektronischen Rechnungsstellung

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dieses Thema enthält Informationen zu den Komponenten, die sich auf die Verwaltung des Add-Ons für die elektronische Rechnungsstellung beziehen. Außerdem finden Sie Informationen zum Konfigurieren des Add-On-Diensts für die elektronische Rechnungsstellung.

## <a name="azure"></a>Azure

Verwenden Sie Microsoft Azure, um die Geheimnisse für den Schlüsseltresor und das Speicherkonto zu erstellen. Verwenden Sie dann die Geheimnisse in der Konfiguration des Add-Ons für die elektronische Rechnungsstellung.

## <a name="lifecycle-services"></a>Lifecycle Services

Verwenden Sie Microsoft Dynamics Lifecycle Services (LCS), um das Add-On für die Microservices für Ihr LCS-Bereitstellungsprojekt zu aktivieren.

> [!NOTE]
> Für die Installation des Microservice-Add-Ons in LCS ist mindestens ein virtueller Tier 2-Computer erforderlich. Weitere Informationen zur Umgebungsplanung finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) ist die Schnittstelle für die Konfiguration des Add-Ons für die elektronische Rechnungsstellung. Ressourcen wie Umgebungen und Funktionen für die elektronische Rechnungsstellung werden in RCS erstellt, verwaltet und gehostet. Wenn die Ressourcen bereit sind, werden sie im Add-On-Service für die elektronische Rechnungsstellung veröffentlicht.

Informationen zur RCS-Anmeldung finden Sie unter [Regulatory services](https://marketing.configure.global.dynamics.com/).

Weitere Informationen zu RCS finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Integration mit dem Add-On für die elektronische Rechnungsstellung

Bevor Sie RCS zum Konfigurieren elektronischer Rechnungen verwenden können, müssen Sie RCS konfigurieren, um die Kommunikation mit dem Add-On für die elektronische Rechnungsstellung zu ermöglichen. Diese Konfiguration führen Sie auf der Registerkarte **Add-On für die elektronische Rechnungsstellung** der Seite **Parameter für elektronische Berichterstellung** durch.

#### <a name="service-endpoint"></a>Dienstendpunkt

Das Add-On für die elektronische Rechnungsstellung ist in mehreren Azure-Rechenzentrumsregionen verfügbar. In der folgenden Tabelle ist die Verfügbarkeit pro Region aufgeführt.

| Azure-Rechenzentrumgeografie |
|----------------------------|
| USA, Osten                    |
| USA, Westen                    |
| Norden, Europa                   |
| Westen, Europa                    |

### <a name="service-environments"></a>Dienstumgebungen

Service-Umgebungen sind logische Partitionen, die erstellt werden, um die Ausführung der Funktionen für die elektronische Rechnungsstellung im zugehörigen Add-On zu unterstützen. Die Sicherheitsgeheimnisse und digitalen Zertifikate sowie die Governance (d. h. Zugriffsberechtigungen) müssen auf der Ebene der Service-Umgebung konfiguriert werden.

Kunden können beliebig viele Service-Umgebungen erstellen. Alle von einem Kunden erstellten Service-Umgebungen sind voneinander unabhängig.

Service-Umgebungen müssen in RCS erstellt und verwaltet werden. Wenn die Service-Umgebungen bereit sind, müssen sie im Add-On für die elektronische Rechnungsstellung veröffentlicht werden.

#### <a name="service-environment-status"></a>Status der Service-Umgebung

Service-Umgebungen können über den Status verwaltet werden. Mögliche Optionen sind:

- **Nicht veröffentlicht** – Die Umgebung wurde erstellt, aber noch nicht veröffentlicht.
- **Veröffentlicht** – Die Umgebung wurde im Add-On für die elektronische Rechnungsstellung veröffentlicht.
- **Geändert** – Die Attribute einer veröffentlichten Umgebung wurden geändert, die Änderungen wurden jedoch noch nicht veröffentlicht.

#### <a name="customer-secrets"></a>Kundengeheimnisse

Der Add-On-Dienst für die elektronische Rechnungsstellung ist verantwortlich für die Speicherung aller Ihrer Geschäftsdaten in den Azure-Ressourcen, die Ihrem Unternehmen gehören. Um sicherzustellen, dass der Dienst ordnungsgemäß funktioniert und auf alle Geschäftsdaten, die für das Add-On für die elektronische Rechnungsstellung erforderlich sind und von ihm generiert werden, nur über das Add-On zugegriffen wird, müssen Sie zwei Azure-Hauptressourcen erstellen:

- ein Azure-Speicherkonto (Blob-Speicher) zum Speichern elektronischer Rechnungen
- einen Azure-Schlüsseltresor zum Speichern von Zertifikaten und des URI (Uniform Resource Identifier) des Speicherkontos

> [!NOTE]
> Ein dedizierter Schlüsseltresor und ein Speicherkonto für den Kunden müssen speziell für die Verwendung mit dem Add-On für die elektronische Rechnungsstellung zugewiesen werden.

Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Benutzer

Jede Service-Umgebung muss die Benutzer auflisten, die aus Dynamics 365 Finance und Dynamics 365 Supply Chain Management im Add-On für die elektronische Rechnungsstellung eine Verbindung herstellen können.

#### <a name="publication"></a>Veröffentlichung

Service-Umgebungen müssen im Add-On für die elektronische Rechnungsstellung veröffentlicht werden, bevor sie genutzt werden können. Finance und Supply Chain Management können nur auf veröffentlichte Umgebungen zugreifen. Darüber hinaus muss eine Service-Umgebung veröffentlicht werden, bevor Aktualisierungen ihrer Attribute für den elektronischen Rechnungsstellungsdienst in Kraft treten.

### <a name="connected-applications"></a>Verbundene Anwendungen

Verbundene Anwendungen sind die Instanzen von Finance und Supply Chain Management, die Sie möglicherweise über RCS erreichen möchten. Neben der Anwendungs-URL und ihrem Mandanten enthält eine verbundene Anwendung die Anmeldeinformationen, mit denen RCS eine Verbindung zur Umgebung herstellen kann.

Über die verbundenen Anwendungen können Sie einen Teil der Funktion für die elektronische Rechnungsstellung in Finance und Supply Chain Management so konfigurieren, dass die gesamte Funktion für die elektronische Rechnungsstellung funktioniert.

## <a name="finance-and-supply-chain-management"></a>Finance und Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Integration mit dem Add-On für die elektronische Rechnungsstellung

Bevor Sie mit Finance und Supply Chain Management elektronische Rechnungen über das Add-On für die elektronische Rechnungsstellung ausstellen können, muss das Add-On so konfiguriert sein, dass die Kommunikation mit dem Dienst möglich ist.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Add-On-Integrationsfunktion für die elektronische Rechnungsstellung

Um die Kommunikation zwischen Finance und Supply Chain Management sowie dem Add-On für die elektronische Rechnungsstellung zu ermöglichen, müssen Sie die Funktion **Add-On-Integration für die elektronische Rechnungsstellung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.

#### <a name="service-endpoint"></a>Dienstendpunkt

Der Service-Endpunkt ist die URL, unter der sich das Add-On für die elektronische Rechnungsstellung befindet. Bevor elektronische Rechnungen ausgestellt werden können, muss der Dienstendpunkt in Finance und Supply Chain Management konfiguriert werden, um die Kommunikation mit dem Dienst zu ermöglichen.

Rufen Sie **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente** auf, um den Dienstendpunkt zu konfigurieren. Geben Sie anschließend auf der Registerkarte **Übermittlungsdienste** im Feld **Add-On-URL für die elektronische Rechnungsstellung** die URL ein – wie in der Tabelle im Abschnitt **Dienstendpunkt** beschrieben.

#### <a name="environments"></a>Umgebungen

Der Umgebungsname, der in Finance und Supply Chain Management eingegeben wird, bezieht sich auf den Namen der Umgebung, die in RCS erstellt und im Add-On für die elektronische Rechnungsstellung veröffentlicht wird.

Die Umgebung muss auf der Registerkarte **Übermittlungsdienste** der Seite **Parameter elektronischer Dokumente** konfiguriert werden, sodass jede Anfrage zur Ausstellung elektronischer Rechnungen die Umgebung enthält, in der das Add-On für die elektronische Rechnungsstellung bestimmen kann, welche elektronische Rechnungsfunktion die Anfrage verarbeiten muss.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Elektronische Rechnungen in RCS konfigurieren](e-invoicing-configuration-rcs.md)
- [Elektronische Rechnungen in Finance und Supply Chain Management ausstellen](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
