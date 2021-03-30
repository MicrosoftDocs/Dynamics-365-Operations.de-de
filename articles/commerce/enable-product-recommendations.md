---
title: Produktempfehlungen aktivieren
description: Dieses Thema erläutert, wie Produktempfehlungen erstellt werden, die auf dem maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basieren, welches Microsoft Dynamics 365 Commerce-Kunden zur Verfügung steht.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcb3b542d290e01a3cddc73ae163ed2ef420771b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238790"
---
# <a name="enable-product-recommendations"></a>Produktempfehlungen aktivieren

[!include [banner](includes/banner.md)]

Dieses Thema erläutert, wie Produktempfehlungen erstellt werden, die auf dem maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basieren, welches Microsoft Dynamics 365 Commerce-Kunden zur Verfügung steht. Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Produktempfehlungen Vor-Prüfung

Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für Commerce-Kunden unterstützt werden, die ihren Speicher für die Nutzung von Azure Data Lake Storage migriert haben. 

Die folgenden Konfigurationen müssen im Backoffice aktiviert sein, bevor Empfehlungen aktiviert werden können:

1. Stellen Sie sicher, dass Azure Data Lake Storage in der Umgebung gekauft und erfolgreich überprüft wurde. Weitere Informationen finden Sie unter [Stellen Sie sicher, dass Azure Data Lake Storage in der Umgebung gekauft und erfolgreich überprüft wurde](enable-ADLS-environment.md).
2. Stellen Sie sicher, dass die Aktualisierung des Entitätsspeichers automatisiert wurde. Weitere Informationen finden Sie unter [Stellen Sie sicher, dass die Aktualisierung des Entitätsspeichers automatisiert wurde](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Bestätigen Sie, das die Azure AD Identitätskonfiguration einen Eintrag für Empfehlungen enthält. Weitere Informationen zur Durchführung dieser Aktion finden Sie unten.

Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden. Weitere Informationen zu diesem Einrichtungsprozess finden Sie unter [Mit Maßnahmen arbeiten](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD Identitätskonfiguration

Dieser Schritt ist für alle Kunden erforderlich, die eine Infrastruktur als Servicekonfiguration (IaaS) ausführen. Für Kunden, die mit Service Fabric (SF) arbeiten, sollte dieser Schritt automatisch erfolgen. Wir empfehlen, zu überprüfen, ob die Einstellung wie erwartet konfiguriert ist.

### <a name="setup"></a>Einstellung

1. Suchen Sie im Backoffice nach den Seiten **Azure Active Directory Anwendungen**.
2. Überprüfen Sie, ob ein Eintrag für RecommendationSystemApplication-1 vorhanden ist.

Wenn der Eintrag nicht vorhanden ist, fügen Sie einen neuen Eintrag mit den folgenden Informationen hinzu:

- **Client-ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Name** – RecommendationSystemApplication-1
- **Benutzeridentifikation** – RetailServiceAccount

Seite speichern und schließen 

## <a name="turn-on-recommendations"></a>Empfehlungen aktivieren

Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:

1. In der Commerce-Zentrale suchen Sie nach **Funktionsverwaltung**.
1. Wählen Sie **Alles** aus, um eine Liste der verfügbaren Funktionen anzuzeigen. 
1. Geben Sie im Suchfeld **Empfehlungen** ein.
1. Wählen Sie die Funktion **Produktempfehlungen** aus.
1. Wählen sie im Eigenschaftsbereich **Produktempfehlungen** die Option **Jetzt aktivieren** aus.

![Aktivieren von Empfehlungen](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten. Es kann bis zu mehreren Stunden dauern, bis die Listen an der Verkaufsstelle (POS) oder in Dynamics 365 Commerce angezeigt werden.

## <a name="configure-recommendation-list-parameters"></a>Konfigurieren Sie Empfehlungslistenparameter

Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte. Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen. Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Empfehlungen für POS-Geräte anzeigen

Nachdem Empfehlungen im Commerce-Back-Office aktiviert wurden, muss der Empfehlungsbereich zum Bildschirm der POS-Steuerung über das Layouttool hinzugefügt werden. Informationen zu diesem Vorgang finden Sie unter [Hinzufügen eines Empfehlungssteuerelements zum Transaktionsbildschirm auf POS-Geräten](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalisierte Empfehlungen aktivieren

In Dynamics 365 Commerce können Einzelhändler können Produktempfehlungen (auch als Personalisierung bezeichnet) zur Verfügung stellen. Auf diese Weise können die personalisierten Empfehlungen online und am Point of Sale (POS) in das Kundenerlebnis einbezogen werden. Wenn die Personalisierungsfunktion aktiviert ist, kann das System die Kauf- und Produktinformationen eines Benutzers verknüpfen, um individuelle Produktempfehlungen zu generieren.

Weitere Informationen zum Empfangen von personalisierten Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Produktempfehlungen am POS hinzufügen](product.md)

[Empfehlungen zum Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]