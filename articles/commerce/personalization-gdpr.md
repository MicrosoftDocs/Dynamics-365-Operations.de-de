---
title: Personalisierte Empfehlungen abmelden
description: In diesem Thema wird erläutert, wie Sie über Microsoft Dynamics 365 Commerce Kunden die Möglichkeit geben, sich vom Empfang personalisierter Empfehlungen abzumelden.
author: bebeale
ms.date: 09/15/2020
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
ms.openlocfilehash: 75f41db74512ea758a83de56ffd2a9166712f5e2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352275"
---
# <a name="opt-out-of-personalized-recommendations"></a>Personalisierte Empfehlungen kündigen

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie über Microsoft Dynamics 365 Commerce Kunden die Möglichkeit geben, sich vom Empfang personalisierter Empfehlungen abzumelden.

Während der Kontoerstellung werden neue Kunden automatisch eingerichtet, um personalisierte Empfehlungen zu erhalten. Jedoch bietet Dynamics 365 Commerce Einzelhändlern verschiedene Möglichkeiten, Benutzern zu ermöglichen, diese Empfehlungen nicht zu erhalten und die Verarbeitung ihrer personenbezogenen Daten einzuschränken. Authentifizierte Benutzer, die sich gegen personalisierte Empfehlungen entscheiden, sehen keine personalisierten Listen mehr. Darüber hinaus werden alle persönlichen Daten, die zur Personalisierung gesammelt werden, aus personalisierten Empfehlungsmodellen entfernt.

Weitere Informationen zum Empfangen personalisierter Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Möglichkeiten für Einzelhändler, ein Abmeldungs-Erlebnis zu implementieren

Einzelhändler haben drei Möglichkeiten, ein Abmeldungs-Erlebnis zu implementieren.

### <a name="opting-out-on-behalf-of-users"></a>Deaktivierung im Namen der Benutzer

In der Kontoverwaltung im Commerce-Backoffice können sich Einzelhändler für Benutzer abmelden.

1. Suchen Sie auf der Back-Office-Startseite nach **alle Kunden**.
1. Suchen Sie nach einem Kunden und wählen Sie dann die Registerkarte **Einzelhandel**.

    ![Inforegister „Einzelhandel“.](./media/Disablepersonalizationpart1.png)

1. Unter **Privatsphäre** stellen Sie die Option **Deaktivieren Sie die Personalisierung** auf **Ja** ein.

    ![Datenschutzeinstellungen.](./media/Disablepersonalizationpart2.png)

1. Klicken Sie auf **Speichern** und schließen Sie die Seite.

### <a name="module-based-opt-out-experience"></a>Erfahrung mit modulbasierter Abmeldungs-Erfahrung

Einzelhändler können authentifizierten Benutzern erlauben, sich selbst von personalisierten Empfehlungen abzumelden. Fügen Sie das Benutzer-Deaktivierungsmodul zu den Profilseiten des Kundenkontos hinzu, um diese Deaktivierungsfunktion zu nutzen.

### <a name="custom-extensions"></a>Benutzerdefinierte Erweiterungen

Einzelhändler können ihre eigenen Erweiterungen erstellen, um das Abmelde-Erlebnis für Benutzer zu verwalten. Weitere Informationen finden Sie unter [Rufen Sie die Retail Server APIs auf](e-commerce-extensibility/call-retail-server-apis.md) und [Online-Kanal-Erweiterbarkeit](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Erhalten Sie eine digitale Kopie der personalisierten Empfehlungsdaten für einen authentifizierten Benutzer

Kunden möchten möglicherweise eine digitale Kopie ihrer persönlichen Daten erhalten und auch eine exportierte Ansicht der Ergebnisse ihrer Empfehlungen anzeigen. Wenn ein Kunde diese Informationen anfordert, muss der Einzelhändler eine benutzerdefinierte Erweiterung erstellen, die die Retail Server-Anwendungsprogrammierschnittstelle (API) aufruft und die vollständigen Ergebnisse von der **Tipps für Sie** Liste abruft, basierend auf der Kundennummer des Kunden. Die Ergebnisse können dann im CSV-Format (mit Komma getrennte Werte) exportiert und mit dem Kunden geteilt werden.

Das folgende Beispiel zeigt, wie ein Einzelhändler diese Aufgabe ausführen kann.

1. Der Einzelhändler erstellt eine benutzerdefinierte Erweiterung, um persönliche Empfehlungsdaten im Namen des Benutzers abzurufen. Informationen zum Erstellen von Modulen, zum Klonen vorhandener Module, zum Aufrufen von Retail Server-APIs und zum Aufrufen von Datenaktionen finden Sie unter [Online-Kanal-Erweiterbarkeit](e-commerce-extensibility/overview.md).
2. Die benutzerdefinierte Nebenstelle ruft die **Empfehlungen abrufen** Kerndatenaktion ab und übergibt die erforderlichen Informationen an sie, basierend auf den Anforderungen der Liste. Im Falle der **Tipps für Sie** Liste muss die Erweiterung den richtigen Listennamen und die richtige Kunden-ID an die Datenaktion übergeben.

    Eine Möglichkeit zum Erstellen der benutzerdefinierten Erweiterung besteht darin, das vorhandene Produktsammlungsmodul zu klonen, das zum Zurückgeben von Empfehlungsergebnissen verwendet wird. Durch Klonen dieses vorhandenen Moduls kann ein Einzelhändler den vorhandenen Code ändern und eine neue Schaltfläche hinzufügen, mit der die Empfehlungsergebnisse in eine CSV-Datei exportiert werden. Weitere Informationen finden Sie unter [Klonen Sie eine Modulbibliothek](e-commerce-extensibility/clone-starter-module.md) und [Produktsammelmodule](product-collection-module-overview.md).

    Eine vollständige Ansicht der Retail Server-API-Bibliothek finden Sie unter [Retail Server-Kunden- und Verbraucher-APIs](dev-itpro/retail-server-customer-consumer-api.md).

3. Nachdem die benutzerdefinierte Erweiterung erstellt wurde, kann der Einzelhändler eine CSV-Datei mit allen Empfehlungsergebnissen exportieren, die auf der eindeutigen Kunden-ID des authentifizierten Benutzers basiert.
4. Der Einzelhändler kann die exportierte CSV-Datei mit der vollständigen personalisierten Liste der empfohlenen Produkte für den authentifizierten Benutzer freigeben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Produktempfehlungen in POS hinzufügen](product.md)

[Empfehlungen dem Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
