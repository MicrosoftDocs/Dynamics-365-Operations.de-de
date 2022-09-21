---
title: Produktempfehlungen aktivieren
description: Dieser Artikel erläutert, wie Produktempfehlungen erstellt werden, die auf dem maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basieren, welches Microsoft Dynamics 365 Commerce-Kunden zur Verfügung steht.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460020"
---
# <a name="enable-product-recommendations"></a>Produktempfehlungen aktivieren

[!include [banner](includes/banner.md)]

Dieser Artikel erläutert, wie Produktempfehlungen erstellt werden, die auf dem maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basieren, welches Microsoft Dynamics 365 Commerce-Kunden zur Verfügung steht. Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Produktempfehlungen Vor-Prüfung

1. Stellen Sie sicher, dass Sie über eine gültige Empfehlungslizenz für Dynamics 365 Commerce verfügen.
1. Stellen Sie sicher, dass der Entitätsspeicher mit einem kundeneigenen Azure Data Lake Storage Gen2-Konto verbunden ist. Weitere Informationen finden Sie unter [Stellen Sie sicher, dass Azure Data Lake Storage in der Umgebung gekauft und erfolgreich überprüft wurde](enable-ADLS-environment.md).
1. Bestätigen Sie, das die Azure AD Identitätskonfiguration einen Eintrag für Empfehlungen enthält. Weitere Informationen zur Durchführung dieser Aktion finden Sie unten.
1. Stellen Sie sicher, dass die tägliche Aktualisierung des Entitätsspeichers auf Azure Data Lake Storage Gen2 geplant wurde Weitere Informationen finden Sie unter [Stellen Sie sicher, dass die Aktualisierung des Entitätsspeichers automatisiert wurde](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Aktivieren Sie RetailSale-Messungen für den Entitätsspeicher. Weitere Informationen zum Einrichten dieses Prozesses finden Sie unter [Mit Maßnahmen arbeiten](/dynamics365/ai/customer-insights/pm-measures).
1. Stellen Sie sicher, dass Ihre Umgebung die Servier- und Kochregionen in den derzeit unterstützten Regionen wie folgt konfiguriert hat:

    - **Unterstützte Kochregionen:** EU/US/CA/AU.
    - **Unterstützte Servierregionen:** US/CA/AU. Wenn die Lieferregion nicht mit einer der vorhandenen unterstützten Regionen übereinstimmt, wählt der Empfehlungsdienst die nächstgelegene unterstützte Lieferregion aus.

Nachdem Sie die oben genannten Schritte ausgeführt haben, können Sie Empfehlungen aktivieren.

> [!NOTE]
> Es gibt ein bekanntes Problem, bei dem Empfehlungen nicht angezeigt werden, nachdem die folgenden Schritte ausgeführt wurden. Dieses Problem wird durch Datenflussprobleme in der Umgebung verursacht. Wenn Ihre Umgebung keine Empfehlungsergebnisse anzeigt, konfigurieren Sie die alternativen Daten für den Empfehlungsdienst, indem Sie die Schritte in [Richten Sie einen alternativen Dataflow für Empfehlungen ein](set-up-alternate-data-flow.md) ausführen. Sie müssen über Azure-Administratorberechtigungen verfügen, um diese Schritte ausführen zu können. Wenn Sie Hilfe benötigen, wenden Sie sich an Ihren FastTrack-Vertreter.

## <a name="azure-ad-identity-configuration"></a>Azure AD Identitätskonfiguration

Dieser Schritt ist nur für Kunden erforderlich, die eine Infrastructure-as-a-Service-Konfiguration (IaaS) betreiben. Die Azure AD-Identitätskonfiguration erfolgt automatisch für Kunden, die Azure Service Fabric verwenden. Es wird jedoch empfohlen, zu überprüfen, ob die Einstellung wie erwartet konfiguriert ist.

### <a name="setup"></a>Einrichtung

1. Suchen Sie in der Commerce-Zentralverwaltung nach der Seite **Azure Active Directory-Anwendungen**.
1. Überprüfen Sie, ob ein Eintrag für **RecommendationSystemApplication-1** vorhanden ist. Wenn kein Eintrag vorhanden ist, erstellen Sie einen mit den folgenden Informationen:

    - **Client-ID**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Name**: RecommendationSystemApplication-1
    - **Benutzerkennung**: RetailServiceAccount

1. Seite speichern und schließen 

## <a name="turn-on-recommendations"></a>Empfehlungen aktivieren

Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:

1. In der Commerce-Zentrale suchen Sie nach **Funktionsverwaltung**.
1. Wählen Sie **Alles** aus, um eine Liste der verfügbaren Funktionen anzuzeigen. 
1. Geben Sie im Suchfeld **Empfehlungen** ein.
1. Wählen Sie die Funktion **Produktempfehlungen** aus.
1. Wählen sie im Eigenschaftsbereich **Produktempfehlungen** die Option **Jetzt aktivieren** aus.

![Aktivieren von Empfehlungen.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Die obige Prozedur startet den Prozess zum Generieren von Produktempfehlungslisten. Es kann bis zu mehreren Stunden dauern, bis die Listen an der Verkaufsstelle (POS) oder in Dynamics 365 Commerce angezeigt werden.
> - Diese Konfiguration aktiviert nicht alle Empfehlungsfunktionen. Erweiterte Funktionen, wie beispielsweise personalisierte Empfehlungen, „Ähnliche Outfits kaufen“ und „Artikel mit ähnlicher Beschreibung kaufen“ werden durch dedizierte Einträge in die Funktionsverwaltung gesteuert. Informationen zum Aktivieren dieser Funktionen in der Commerce-Zentralverwaltung finden Sie unter [Personalisierte Empfehlungen aktivieren](personalized-recommendations.md), [Empfehlungen zu „Ähnliche Outfits kaufen“ aktivieren](shop-similar-looks.md) und [Empfehlungen zu „Artikel mit ähnlicher Beschreibung kaufen“ aktivieren](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Konfigurieren Sie Empfehlungslistenparameter

Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte. Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen. Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Empfehlungen in E-Commerce-Umgebungen integrieren

Nachdem Empfehlungen in der Commerce-Zentralverwaltung aktiviert wurden, können die Commerce-Module konfiguriert werden, die zum Anzeigen der Empfehlungsergebnisse für E-Commerce-Umgebungen verwendet werden. Weitere Informationen finden Sie unter [Produktsammelmodule](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Empfehlungen für POS-Geräte anzeigen

Nachdem Empfehlungen in der Commerce-Zentralverwaltung aktiviert wurden, muss der Empfehlungsbereich zum Bildschirm der POS-Steuerung über das Layouttool hinzugefügt werden. Informationen zu diesem Vorgang finden Sie unter [Hinzufügen eines Empfehlungssteuerelements zum Transaktionsbildschirm auf POS-Geräten](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalisierte Empfehlungen aktivieren

In Dynamics 365 Commerce können Einzelhändler können Produktempfehlungen (auch als Personalisierung bezeichnet) zur Verfügung stellen. Auf diese Weise können die personalisierten Empfehlungen online und am Point of Sale (POS) in das Kundenerlebnis einbezogen werden. Wenn die Personalisierungsfunktion aktiviert ist, kann das System die Kauf- und Produktinformationen eines Benutzers verknüpfen, um individuelle Produktempfehlungen zu generieren.

Weitere Informationen zum Empfangen von personalisierten Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Richten Sie einen alternativen Dataflow für Empfehlungen ein](set-up-alternate-data-flow.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Link „Ähnliche Outfits kaufen“ aktivieren](shop-similar-looks.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Produktempfehlungen am POS hinzufügen](product.md)

[Empfehlungen zum Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
