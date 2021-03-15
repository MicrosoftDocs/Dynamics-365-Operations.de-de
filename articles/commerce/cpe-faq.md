---
title: Dynamics 365 Commerce-Auswertungsumgebung – FAQ
description: Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Microsoft Dynamics 365 Commerce-Auswertungsumgebung.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b8d7d7364087dacf3b4479ab008609ecffeaacb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000974"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce-Auswertungsumgebung – FAQ

[!include [banner](includes/banner.md)]

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Microsoft Dynamics 365 Commerce-Auswertungsumgebung.

**Können wir die Commerce-Auswertungsumgebung als E-Commerce-Storefront für Kunden verwenden, die Retail derzeit implementieren?**

Nr. Die Commerce-Auswertungsumgebung dient nur zur Auswertung. Wenn Sie für einen Kunden eine Umgebung benötigen, die den Einzelhandel implementiert, wenden Sie sich an Microsoft.

**Kann die Commerce-Auswertungsumgebung verwendet werden, um die E-Commerce-Funktionen zusätzlich zu einer vorhandenen Anwendung/Umgebung bereitzustellen, die Retail implementiert?**

Nein (meistens). Die Commerce-Auswertungskomponenten sind nur für Umgebungen verfügbar, die den Konfigurationen entsprechen, die in der Anleitung zu den Voraussetzungen und der Bereitstellung angegeben sind. Darüber hinaus sind die erforderlichen Basisdemodaten nicht in Umgebungen verfügbar, die mit einem Erst-Release vor 10.0.8 bereitgestellt wurden. 

**Welche Kosten fallen bei der Bereitstellung der Commerce-Auswertungsumgebung in Microsoft Azure über Microsoft Dynamics Lifecycle Services (LCS) an?**

Eine traditionelle Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce-Zentralverwaltungs-Demo-Umgebung (virtuelle Maschine \[VM\]) wird in Ihrem Azure-Abonnement gehostet. Sie können den [Azure-Preisrechner](https://azure.microsoft.com/pricing/calculator/) verwenden, um die Kosten zu schätzen.

Andere Komponenten wie Commerce Scale Unit, Commerce-Website-Generator und Ihre E-Commerce-Website werden als Software-as-a-Service (SaaS) verfügbar sein und von Microsoft gehostet.

**Welche Azure-Regionen werden derzeit in der Commerce-Auswertungsumgebung unterstützt?**

Die Commerce-Auswertungsumgebung kann nur in der geografischen Region Nordamerika bereitgestellt werden.

**Gibt es eine herunterladbare virtuelle Festplatte (VHD) mit der vollständigen OneBox Virtual Machine-Option (VM)?**

Dynamics 365 Commerce und Commerce Scale Unit sind vollständig Software as a Service (SaaS) und müssen in der Cloud gehostet werden.

**Wie lange kann die Commerce-Auswertungsumgebung verwendet werden?**

Für die Commerce-Auswertungsumgebung gilt eine Frist von 30 Tagen ab dem Datum, an dem SaaS-Komponenten wie Commerce Scale Unit, Commerce-Website-Generator und Ihre E-Commerce-Website bereitgestellt werden.

**Kann ich das Zeitlimit für meine Commerce-Auswertungsumgebung verlängern?**

Die Verlängerung der Frist ist eine Ausnahme von der Norm und wird von Fall zu Fall geprüft. Wenden Sie sich an Ihren Microsoft-Partner, um Unterstützung zu erhalten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Dynamics 365 Commerce-Auswertungsumgebung – Übersicht](cpe-overview.md)

[Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung](provisioning-guide.md)

[Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung](cpe-post-provisioning.md)

[BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren](cpe-bopis.md)

[Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]