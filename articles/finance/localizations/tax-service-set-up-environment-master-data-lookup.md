---
title: Eine Umgebung für die Masterdatensuche einrichten
description: In diesem Thema wird erläutert, wie Sie Ihre Umgebung für die Verwendung der Masterdaten-Suchfunktion für die Steuerberechnung einrichten.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 348643d7213b8c053d6a15b4b716a3ce75ba2fa2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346373"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Eine Umgebung für die Masterdatensuche einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Ihre Umgebung für die Verwendung der Masterdaten-Suchfunktion für die Steuerberechnung einrichten.

1. Richten Sie die Integration von Power Platform in Lifecycle Services (LCS) ein. Weitere Informationen finden Sie unter [Integration von Microsoft Power Platform – Übersicht über Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Richten Sie Dynamics 365 Finance und Microsoft Dataverse ein. Weitere Informationen finden Sie unter [Die Lösung erhalten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) und [Authentifizierung und Autorisierung](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Legen Sie die folgenden Entitäten fest. Weitere Informationen finden Sie unter [Aktivieren von virtuellen Entitäten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressCityEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeadingEntity
      - VendVendorV2Entity
4. Richten Sie den Dynamics 365 Regulatory Configuration Service (RCS) ein. 
5. Erstellen Sie eine Serviceanforderung für Microsoft, um das Flighting der folgenden Funktionen zu ermöglichen:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Gehen Sie in den Arbeitsbereich **Funktionsverwaltung** und aktivieren Sie die folgenden Funktionen:

      - (Vorschau) Unterstützung von Dataverse-Datenquellen der elektronischen Berichterstellung
      - (Vorschauversion) Unterstützung für Dataverse-Datenquellen des Steuerdienstes
      - (Vorschau) Globalisierungsfunktionen

5. Melden Sie sich mit einem Mandantenadministratorkonto bei RCS an.
6. Gehen Sie zu **Elektronische Berichterstellung** > **Verbundene Anwendungen**. 
7. Wählen Sie **Neu**, um einen Datensatz hinzuzufügen und geben Sie die folgenden Feldinformationen ein. 

   - Geben Sie im Feld **Name** einen Namen ein.
   - Wählen Sie im Feld **Typ** die **Dataverse** aus.
   - Geben Sie im Feld **Anwendung** Ihre Dataverse-URL ein.
   - Geben Sie im Feld **Mandant** Ihren Mandanten ein.
   - Geben Sie im Feld **Benutzerdefinierte URL** Ihre Dataverse-URL ein und fügen Sie „/api/data/v9.1“ an.

8. Wählen Sie **Verbindung prüfen** und beenden Sie den Verbindungsvorgang. 

   [![Schaltfläche „Verbindung prüfen“.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Gehen Sie zu **Elektronische Berichterstellung** > **Steuerkonfigurationen** und importieren Sie Steuerkonfigurationen aus [Steuerkonfigurationen](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Seite „Steuerkonfigurationen“, Steuerdatenmodellstruktur.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Gehen Sie zu **Modellzuordnung steuerpflichtiges Dokument** oder zu **Dataverse Modellzuordnung**, wenn Sie eine Microsoft-Konfiguration verwenden, und wählen Sie im Feld **Verbundene Anwendung** den Datensatz aus, den Sie in Schritt 7 erstellt haben.
11. Legen Sie die **Standard für Modellzuordnung** auf **Ja** fest.

   [![Seite „Modellzuordnung“.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
