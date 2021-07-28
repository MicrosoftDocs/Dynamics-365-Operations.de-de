---
title: Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung aktivieren
description: In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.
author: bebeale
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9ac440362379475b05c6a37019c25e3a96be3739
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349495"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.

Bei der Dynamics 365 Commerce-Lösung werden alle Produkt- und Transaktionsinformationen im Entitätsspeicher der Umgebung nachverfolgt. Um diese Daten für andere Dynamics 365-Dienste wie Datenanalyse, Business Intelligence und personalisierte Empfehlungen zugänglich zu machen, muss die Umgebung mit einer kundeneigenen Azure Data Lake Storage Gen 2 Lösung verbunden werden.

Da Azure Data Lake Storage in einer Umgebung konfiguriert ist, werden alle erforderlichen Daten aus dem Entitätsspeicher gespiegelt, während sie weiterhin geschützt sind und vom Kunden gesteuert werden können.

Wenn Produktempfehlungen oder personalisierte Empfehlungen auch in der Umgebung aktiviert sind, erhält der Produktempfehlungsstapel Zugriff auf den dedizierten Ordner in Azure Data Lake Storage, um die Kundendaten abzurufen und Empfehlungen basierend auf diesen zu berechnen.

## <a name="prerequisites"></a>Voraussetzungen

Kunden müssen Azure Data Lake Storage in einem Azure-Abonnement konfiguriert haben, dessen Inhaber sie sind. Dieses Thema behandelt nicht den Kauf eines Azure-Abonnements oder die Einrichtung eines Azure Data Lake Storage fähigen Speicherkontos.

Weitere Informationen zu Azure Data Lake Storage finden Sie in der [offiziellen Gen2 Azure Data Lake Storage](https://azure.microsoft.com/pricing/details/storage/data-lake)-Dokumentation.
  
## <a name="configuration-steps"></a>Konfigurationsschritte

Dieser Abschnitt behandelt die Konfigurationsschritte, die zum Aktivieren von Azure Data Lake Storage in einer Umgebung erforderlich sind, und bezieht sich auf Produktempfehlungen.
Eine ausführlichere Übersicht über die zum Aktivieren von Azure Data Lake Storage erforderlichen Schritte finden Sie unter [Stellen Sie den Entity Store als Data Lake zur Verfügung](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Aktivieren Sie Azure Data Lake Storage in der Umgebung

1. Melden Sie sich beim Back-Office-Portal der Umgebung an.
1. Suchen Sie nach **Systemparameter** und navigieren Sie zur Registerkarte **Datenverbindungen**. 
1. Setzen Sie **Integration von Data Lake aktivieren** auf **Ja**.
1. Setzen Sie **Data Lake schrittweise aktualisieren** auf **Ja**.
1. Geben Sie die folgenden erforderlichen Informationen ein:
    1. **Anwendungs-ID** // **Anwendungsschlüssel** // **DNS-Name** – Erforderlich, um eine Verbindung zu KeyVault herzustellen, in dem der Azure Data Lake Storage Schlüssel gespeichert ist.
    1. **Schlüsselname** – Der geheime Schlüssel, der in KeyVault gespeichert und zur Azure Data Lake Storage Authentifizierung verwendet wird.
1. Speichern Sie Ihre Änderungen in der oberen linken Ecke der Seite.

Das folgende Bild zeigt ein Beispiel für eine Azure Data Lake Storage Konfiguration.

![Beispiel einer Azure Data Lake Storage Konfiguration.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Testen Sie die Azure Data Lake Storage Verbindung

1. Testen Sie die Verbindung zu KeyVault mit dem Link **Azure Key Vault testen**.
1. Testen Sie die Verbindung zu Azure Data Lake Storage mit dem Link **Azure Storage testen**.

> [!NOTE]
> Wenn die Tests fehlschlagen, überprüfen Sie noch einmal, ob alle oben hinzugefügten KeyVault-Informationen korrekt sind, und versuchen Sie es dann erneut.

Sobald die Verbindungstests erfolgreich sind, müssen Sie die automatische Aktualisierung für den Entitätsspeicher aktivieren.

Gehen Sie folgendermaßen vor, um die automatische Aktualisierung für den Entitätsspeicher zu aktivieren.

1. Suchen Sie nach **Entitätsspeicher**.
1. Navigieren Sie in der Liste auf der linken Seite zum **RetailSales**-Eintrag, und wählen Sie **Bearbeiten** aus.
1. Vergewissern Sie sich, dass **Automatische Aktualisierung aktiviert** auf **Ja** gesetzt ist, und wählen Sie **Aktualisieren** und dann **Speichern** aus.

Die folgende Abbildung zeigt ein Beispiel für einen Entitätsspeicher mit aktivierter automatischer Aktualisierung.

![Beispiel eines Entitätsspeichers mit aktivierter automatischer Aktualisierung.](./media/exampleADLSConfig2.png)

Azure Data Lake Storage ist jetzt für die Umgebung konfiguriert. 

Ist die Konfiguration noch nicht vollständig, befolgen Sie für die Umgebung die Schritte [Produktempfehlungen und -personalisierung aktivieren](enable-product-recommendations.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Entitätsspeicher als Data Lake zur Verfügung stellen](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Überblick über Produktempfehlungen](product-recommendations.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Produktempfehlungen in POS hinzufügen](product.md)

[Empfehlungen dem Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
