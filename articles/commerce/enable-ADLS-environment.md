---
title: ADLS in Dynamics 365 Commerce-Umgebung aktivieren
description: In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage (ADLS) für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c037f5603af5af84917084eefa1edd508891c0d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154435"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>ADLS in Dynamics 365 Commerce-Umgebung aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage (ADLS) für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.

## <a name="overview"></a>Übersicht

Bei der Dynamics 365 Commerce-Lösung werden alle Produkt- und Transaktionsinformationen im Entitätsspeicher der Umgebung nachverfolgt. Um diese Daten für andere Dynamics 365-Dienste wie Datenanalyse, Business Intelligence und personalisierte Empfehlungen zugänglich zu machen, muss die Umgebung mit einer kundeneigenen Azure Data Lake Storage Gen 2 (ADLS)-Lösung verbunden werden.

Da ADLS in einer Umgebung konfiguriert ist, werden alle erforderlichen Daten aus dem Entitätsspeicher gespiegelt, während sie weiterhin geschützt sind und vom Kunden gesteuert werden können.

Wenn Produktempfehlungen oder personalisierte Empfehlungen auch in der Umgebung aktiviert sind, erhält der Produktempfehlungsstapel Zugriff auf den dedizierten Ordner in ADLS, um die Kundendaten abzurufen und Empfehlungen basierend auf diesen zu berechnen.

## <a name="prerequisites"></a>Voraussetzungen

Kunden müssen ADLS in einem Azure-Abonnement konfiguriert haben, dessen Inhaber sie sind. Dieses Thema behandelt nicht den Kauf eines Azure-Abonnements oder die Einrichtung eines ADLS-fähigen Speicherkontos.

Weitere Informationen zu ADLS finden Sie in der [offiziellen ADLS-Dokumentation](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurationsschritte

In diesem Abschnitt werden die Konfigurationsschritte beschrieben, die zum Aktivieren von ADLS in einer Umgebung erforderlich sind.

### <a name="enable-adls-in-the-environment"></a>Aktivieren Sie ADLS der Umgebung

1. Melden Sie sich beim Back-Office-Portal der Umgebung an.
1. Suchen Sie nach **Systemparameter** und navigieren Sie zur Registerkarte **Datenverbindungen**. 
1. Setzen Sie **Integration von Data Lake aktivieren** auf **Ja**.
1. Setzen Sie **Data Lake schrittweise aktualisieren** auf **Ja**.
1. Geben Sie die folgenden erforderlichen Informationen ein:
    1. **Anwendungs-ID** // **Anwendungsgeheimnis** // **DNS-Name** – Erforderlich, um eine Verbindung zu KeyVault herzustellen, in dem das ADLS-Geheimnis gespeichert ist.
    1. **Geheimnisname** – Der Geheimnisname, der in KeyVault gespeichert und zur ADLS-Authentifizierung verwendet wird.
1. Speichern Sie Ihre Änderungen in der oberen linken Ecke der Seite.

Das folgende Bild zeigt ein Beispiel für eine ADLS-Konfiguration.

![Beispiel einer ADLS-Konfiguration](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>Testen Sie die ADLS-Verbindung

1. Testen Sie die Verbindung zu KeyVault mit dem Link **Azure Key Vault testen**.
1. Testen Sie die Verbindung zu ADLS mit dem Link **Azure Storage testen**.

> [!NOTE]
> Wenn die Tests fehlschlagen, überprüfen Sie noch einmal, ob alle oben hinzugefügten KeyVault-Informationen korrekt sind, und versuchen Sie es dann erneut.

Sobald die Verbindungstests erfolgreich sind, müssen Sie die automatische Aktualisierung für den Entitätsspeicher aktivieren.

Gehen Sie folgendermaßen vor, um die automatische Aktualisierung für den Entitätsspeicher zu aktivieren.

1. Suchen Sie nach **Entitätsspeicher**.
1. Navigieren Sie in der Liste auf der linken Seite zum **RetailSales**-Eintrag, und wählen Sie **Bearbeiten** aus.
1. Vergewissern Sie sich, dass **Automatische Aktualisierung aktiviert** auf **Ja** gesetzt ist, und wählen Sie **Aktualisieren** und dann **Speichern** aus.

Die folgende Abbildung zeigt ein Beispiel für einen Entitätsspeicher mit aktivierter automatischer Aktualisierung.

![Beispiel eines Entitätsspeichers mit aktivierter automatischer Aktualisierung](./media/exampleADLSConfig2.png)

ADLS ist jetzt für die Umgebung konfiguriert. 

Ist die Konfiguration noch nicht vollständig, befolgen Sie für die Umgebung die Schritte [Produktempfehlungen und -personalisierung aktivieren](enable-product-recommendations.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Produktempfehlungen am POS hinzufügen](product.md)

[Empfehlungen zum Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


