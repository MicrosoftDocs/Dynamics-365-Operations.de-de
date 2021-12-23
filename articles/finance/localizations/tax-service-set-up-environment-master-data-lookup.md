---
title: Masterdatensuche für die Steuerberechnungskonfiguration aktivieren
description: In diesem Thema wird erläutert, wie Sie Masterdaten-Suchfunktion für die Steuerberechnung einrichten und aktivieren.
author: kai-cloud
ms.date: 11/22/2021
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
ms.openlocfilehash: 455e8becfdfa910a3733719653e1a91557b2f59a
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867351"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Masterdatensuche für die Steuerberechnungskonfiguration aktivieren 

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Masterdaten-Suchfunktion für die Steuerberechnung einrichten und aktivieren. Es steht eine Dropdown-Liste zur Auswahl von Werten in der Steuerberechnungskonfiguration für Felder wie **Juristische Person**, **Kreditorenkonto**, **Artikelcode** und **Lieferbedingungen** zur Verfügung. Diese Werte stammen von der verbundenen Microsoft Dynamics 365 Finance-Umgebung mit der Microsoft Dataverse-Datenquelle.

> [!NOTE] 
> Die Masterdaten-Suchfunktion für die Steuerberechnung ist eine optionale Funktion. Sie können die folgenden Schritte überspringen, wenn Sie die Funktion **Unterstützung für Dataverse-Datenquellen des Steuerdienstes** im Regulatory Configuration Service (RCS) deaktivieren. In diesem Fall ist die Dropdown-Liste jedoch in der Steuerberechnungskonfiguration nicht verfügbar.

1. Richten Sie die Microsoft Power Platform-Integration in Microsoft Dynamics Lifecycle Services (LCS) ein. Weitere Informationen finden Sie unter [Integration von Microsoft Power Platform – Übersicht über Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Nachdem Sie diesen Schritt abgeschlossen haben, wird der Name einer Microsoft Power Platform-Umgebung im Abschnitt **Power Platform-Integration** angezeigt.
2. Gehen Sie zum [Microsoft Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), und wählen Sie den Umgebungsnamen aus. Die Umgebungs-URL wird bereitgestellt.
3. Richten Sie Dynamics 365 Finance und Dataverse ein. Weitere Informationen finden Sie unter [Die virtuelle Entitätslösung erhalten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) und [Authentifizierung und Autorisierung](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Legen Sie die folgenden Entitäten fest. Weitere Informationen finden Sie unter [virtuelle Microsoft Dataverse-Entitäten aktivieren](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

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

5. Regulatory Configuration Service (RCS) einrichten. Öffnen Sie den Arbeitsbereich **Funktionsverwaltung** und aktivieren Sie die folgenden Funktionen:

    - Unterstützung von Dataverse-Datenquellen der elektronischen Berichterstellung
    - Unterstützung für Dataverse-Datenquellen des Steuerdienstes
    - Globalisierungsfunktionen

6. Melden Sie sich mit einem Mandantenadministratorkonto bei RCS an.
7. Gehen Sie zu **Elektronische Berichterstellung** > **Verbundene Anwendungen**. 
8. Wählen Sie **Neu**, um einen Datensatz hinzuzufügen und geben Sie die folgenden Feldinformationen ein. 

    - Geben Sie im Feld **Name** einen Namen ein.
    - Wählen Sie im Feld **Typ** die **Dataverse** aus.
    - Geben Sie im Feld **Anwendung** Ihre Dataverse-URL ein.
    - Geben Sie im Feld **Mandant** Ihren Mandanten ein.
    - Geben Sie im Feld **Benutzerdefinierte URL** Ihre Dataverse-URL ein und fügen Sie „/api/data/v9.1“ an.

9. Wählen Sie **Verbindung prüfen** und beenden Sie den Verbindungsvorgang. 

    [![Schaltfläche „Verbindung prüfen“.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Gehen Sie zu **Elektronische Berichterstellung** > **Steuerkonfigurationen** und importieren Sie Steuerkonfigurationen aus [Steuerkonfigurationen](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Seite „Steuerkonfigurationen“, Steuerdatenmodellstruktur.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Gehen Sie zu **Modellzuordnung steuerpflichtiges Dokument** oder zu **Dataverse Modellzuordnung**, wenn Sie eine Microsoft-Konfiguration verwenden, und wählen Sie im Feld **Verbundene Anwendung** den Datensatz aus, den Sie in Schritt 7 erstellt haben.
12. Legen Sie die **Standard für Modellzuordnung** auf **Ja** fest.

    [![Seite „Modellzuordnung“.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
