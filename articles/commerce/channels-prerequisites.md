---
title: Kanaleinstellungen – Voraussetzungen
description: Dieser Artikel bietet einen Überblick über die Voraussetzungen für die Einrichtung von Kanälen in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282294"
---
# <a name="channel-setup-prerequisites"></a>Kanaleinstellungen – Voraussetzungen

[!include [banner](includes/banner.md)]

Dieser Artikel bietet einen Überblick über die Voraussetzungen für die Einrichtung von Kanälen in Microsoft Dynamics 365 Commerce.

Bevor ein Dynamics 365 Commerce Kanal erstellt werden kann, müssen mehrere erforderliche Aufgaben erledigt werden. Die folgenden Listen der erforderlichen Aufgaben sind nach Kanaltyp geordnet.

> [!NOTE]
> Einige Dokumentationen werden noch geschrieben und die Links werden aktualisiert, sobald neue Inhalte veröffentlicht werden.

## <a name="initialization"></a>Initialisierung

- [Seed-Daten initialisieren](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globale Voraussetzungen für alle Kanaltypen erforderlich

- [Ihre Rechtsträgerstruktur definieren und konfigurieren](channels-legal-entities.md) 
- [Ihre Organisationshierarchie konfigurieren](channels-org-hierarchies.md)
- [Einen Lagerort einrichten](channels-setup-warehouse.md)
- [Mehrwertsteuer konfigurieren](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Ein E-Mail-Benachrichtigungsprofil einrichten](email-notification-profiles.md)
- [Einrichten von Nummernkreisen](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Einen Standardkunden und ein Adressbuch einrichten](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Retail Channel-Voraussetzungen

- [Infocodes und Infocodegruppen](info-codes-retail.md)
- [Ein Einzelhandelsfunktionsprofil einrichten](retail-functionality-profile.md)
- [Ein Mitarbeiteradressbuch einrichten](new-address-book.md)
- [Einrichten eines Bildschirmlayouts](pos-screen-layouts.md)
- [Eine Hardwarestation einrichten](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Voraussetzungen für Callcenter-Kanäle

- Callcenter-Parameter
- [Call-Center-Bestellung und Rückerstattungs-Zahlungsmethoden](work-with-payments.md)
- [Zustellarten und Gebühren des Callcenters](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Onlinechannel – Voraussetzungen

- [Ein Onlinefunktionsprofil erstellen](online-functionality-profile.md)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Kanalübersicht](channels-overview.md)

[Organisationen und Organisationshierarchien – Übersicht](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisationshierarchien einrichten](channels-org-hierarchies.md)

[Erstellen juristischer Personen](channels-legal-entities.md)

[Einen Retail Channel einrichten](channel-setup-retail.md)
    
[Einen Onlinekanal einrichten](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
