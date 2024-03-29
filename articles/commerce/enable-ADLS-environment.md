---
title: Azure Data Lake Storage in einer Dynamics 365 Commerce-Umgebung aktivieren
description: Dieser Artikel enthält Anweisungen zum Verbinden einer Azure Data Lake Storage Gen2-Lösung mit dem Entitätsspeicher einer Dynamics 365 Commerce-Umgebung. Dies ist ein erforderlicher Schritt, bevor Produktempfehlungen aktiviert werden.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: d7995e826a838796f714ced2f30220201a157f93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284744"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storage in einer Dynamics 365 Commerce-Umgebung aktivieren

[!include [banner](includes/banner.md)]

Dieser Artikel enthält Anweisungen zum Verbinden einer Azure Data Lake Storage Gen2-Lösung mit dem Entitätsspeicher einer Dynamics 365 Commerce-Umgebung. Dies ist ein erforderlicher Schritt, bevor Produktempfehlungen aktiviert werden.

In der Dynamics 365 Commerce-Lösung werden die zum Berechnen von Empfehlungen, Produkten und Buchungen erforderlichen Daten im Entitätsspeicher der Umgebung aggregiert. Um diese Daten für andere Dynamics 365-Dienste wie Datenanalyse, Business Intelligence und personalisierte Empfehlungen zugänglich zu machen, muss die Umgebung mit einer kundeneigenen Azure Data Lake Storage Gen2-Lösung verbunden werden.

Sobald die obigen Schritte abgeschlossen sind, werden alle Kundendaten im Entitätsspeicher der Umgebung automatisch in die Azure Data Lake Storage Gen2-Lösung des Kunden gespiegelt. Wenn Empfehlungsfunktionen über den Arbeitsbereich „Funktionsverwaltung“ in der Commerce-Zentralverwaltung aktiviert werden, wird dem Empfehlungsstapel Zugriff auf dieselbe Azure Data Lake Storage Gen2-Lösung gewährt.

Während des gesamten Prozesses bleiben die Daten der Kunden geschützt und unter ihrer Kontrolle.

## <a name="prerequisites"></a>Voraussetzungen

Ein Entitätsspeicher der Dynamics 365 Commerce-Umgebung muss mit einem Azure Data Lake Gen Storage Gen2-Konto und den zugehörigen Diensten verbunden sein.

Weitere Informationen zu Azure Data Lake Storage Gen2 und zur Einrichtung finden Sie in der [offiziellen Dokumentation zu Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurationsschritte

Dieser Abschnitt behandelt die Konfigurationsschritte, die zum Aktivieren von Azure Data Lake Storage Gen2 in einer Umgebung erforderlich sind, und bezieht sich auf Produktempfehlungen.
Eine ausführlichere Übersicht über die zum Aktivieren von Azure Data Lake Storage Gen2 erforderlichen Schritte finden Sie unter [Entitätsspeicher als Data Lake zur Verfügung stellen](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Aktivieren Sie Azure Data Lake Storage in der Umgebung

1. Melden Sie sich beim Back-Office-Portal der Umgebung an.
1. Suchen Sie nach **Systemparameter** und navigieren Sie zur Registerkarte **Datenverbindungen**. 
1. Setzen Sie **Integration von Data Lake aktivieren** auf **Ja**.
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
> Wenn einer der obigen Tests fehlschlägt, bestätigen Sie nochmals, ob alle oben hinzugefügten KeyVault-Informationen korrekt sind, und versuchen Sie es dann erneut.

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
