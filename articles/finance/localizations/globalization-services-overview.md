---
title: Dynamics 365 Globalisierungsdienste
description: Dieses Thema enthält eine Übersicht über die Microsoft Dynamics 365 Globalisierungsdienste.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018806"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365 Globalisierungsdienste

[!include [banner](../includes/banner.md)]

Die folgenden Globalisierungsdienste können konfiguriert werden, um die in einigen Diensten von Microsoft Dynamics 365 Online vorhandenen Funktionen zu erweitern:

- **Regulatory Configuration Service (RCS)** unterstützt die Konfiguration verschiedener Arten von elektronischen Dokumenten und Berichten. RCS bietet eine erweiterte Version des Designers der elektronischen Berichtserstellung (EB) bei dem das Konfigurations-Repository ein eigenständiger Dienst ist. Weitere Informationen finden Sie unter [Regulatory Configuration Service](rcs-overview.md).
- **Elektronische Rechnungsstellung** vereint konfigurierbare Formate für Transformationen, digitale Signaturen und konfigurierbare Integrationen für die Konnektivität mit externen Webdiensten, einschließlich Zertifizierung und Antwortverarbeitung. Weitere Informationen finden Sie unter [Elektronische Rechnungsstellung](e-invoicing-service-overview.md).
- **Steuerberechnung** bietet mehr Flexibilität durch die Unterstützung mehrerer Steuer-IDs, die Bestimmung von Steuercodes, den Steuerberechnungsdesigner und eine Laufzeit-Engine zur Einhaltung komplexer Steuervorschriften weltweit. Weitere Informationen finden Sie unter [Steuerberechnung](global-tax-calcuation-service-overview.md).

Diese Globalisierungsdienste bieten eine sofort einsatzbereite Integration mit den folgenden Dynamics 365-Onlinediensten.

| Onlinedienst | RCS | Elektronische Rechnungsstellung | Steuerberechnung (Vorschau) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Ja | Ja | Ja | 
| Dynamics 365 Supply Chain Management | Ja | Ja | Ja | 
| Dynamics 365 Project Operations | Ja | Ja | Nicht zutreffend | 
| Dynamics 365 Commerce | Ja | Nicht zutreffend | Nicht zutreffend | 

> [!NOTE]
> Aufgrund der unterschiedlichen Verfügbarkeit von geografischen Azure-Standorten (Geos) für RCS kann die Konfiguration dieses Dienstes dazu führen, dass Debitorendaten außerhalb der für den entsprechenden Dynamics 365-Onlinedienst ausgewählten Geo übertragen werden. Weitere Informationen finden Sie unter [Dynamics 365 und Power Platform: Verfügbarkeit, Datenstandort, Sprache und Lokalisierung](https://aka.ms/rcs/D365Productavailabilityguide).