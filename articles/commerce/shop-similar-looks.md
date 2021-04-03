---
title: Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren
description: In diesem Thema wird beschrieben, wie Sie Produktempfehlungen „Produkte mit ähnlichem Aussehen kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: d0b3585ce326e47b119b3f6c41436b9e6494ec87
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478091"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Empfehlungen zu „Ähnliche Outfits kaufen“ aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Produktempfehlungen „Produkte mit ähnlichem Aussehen kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.

Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ in Dynamics 365 Commerce nutzt die Kraft der künstlichen Intelligenz und des maschinellen Lernens (AI-ML), um Kunden Empfehlungen für visuell ähnliche Produkte zu geben. Durch die Bereitstellung von Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“ für alle Einzelhandelskanäle in Commerce können Einzelhändler die Kundenzufriedenheit steigern, indem sie Kunden dabei helfen, leicht zu finden, wonach sie suchen.

Die Funktionalität für Empfehlungen zum „Produkte mit ähnlichem Aussehen kaufen“ verwendet Produktbilder von Startproduktvarianten, um visuell ähnliche Produkte im Produktkatalog eines Einzelhändlers zu finden und zu empfehlen. 

Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“ sind sowohl in POS‑ als auch in E-Commerce-Bereichen verfügbar.

### <a name="example-scenarios"></a>Beispielszenarien

- Ein Kunde sieht sich einen schwarz gestreiften Pullover an und erhält eine Empfehlung für einen ähnlichen Pullover in Rot. Der Kunde wählt das empfohlene Produkt anstelle des ursprünglich angezeigten Produkts aus und erhält dann Empfehlungen für ähnliche Produkte in Rot. 
- Ein Kunde verwendet Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“, um passende Ohrringe für einen Ring zu finden, den der Kunde kaufen möchte.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>In der Commerce-Zentrale die Empfehlung „Produkte mit ähnlichem Aussehen kaufen“ aktivieren

Produktempfehlungen werden nur für Commerce-Kunden unterstützt, die ihren Speicher zu Azure Data Lake Gen2 migriert haben.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Einzelhändler ihren Kunden Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“ zeigen können, sind zwei Schritte erforderlich:

- [Produktempfehlungen aktivieren](enable-product-recommendations.md) in der Commerce-Zentrale.
- Stellen Sie sicher, dass der Medienserver HTTPS-Aufrufe unterstützt.

Damit das Empfehlungsmodul auf die Produktbilder zugreifen kann, müssen Einzelhändler die Produkt-URLs generieren. Folgen Sie diesen Schritten, um Produkt-URLs in der Commerce-Zentrale zu verarbeiten.

1. Wechseln Sie zu **Produktbilder**.
1. Wählen Sie im Aktivitätsbereich **Medienvorlage definieren** aus.
1. Wählen Sie im Eigenschaftenbereich **Medienvorlage definieren** unter **Medien-URLs** die Option **URLs generieren** aus.

> [!NOTE]
> Wenn Sie die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ aktivieren, beginnt der Prozess zum Generieren von Produktempfehlungslisten. Es kann bis zu einem Tag dauern, bis diese Listen online und an den POS-Terminals verfügbar und sichtbar sind.

Führen Sie die folgenden Schritte aus, um die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ in der Commerce-Zentrale zu aktivieren.

1. Navigieren Sie zu **Funktionsverwaltung**.
1. Suchen Sie in der Liste der verfügbaren Funktionen **Produkte mit ähnlichem Aussehen kaufen** und wählen Sie es aus.
1. Wählen Sie im rechten Bereich aus **Aktivieren** aus, um den Dienst einzuschalten.

Die folgende Abbildung zeigt die Funktion **Produkte mit ähnlichem Aussehen kaufen** auf der Seite **Funktionsverwaltung** in der Commerce-Zentrale.

![Die Funktion „Produkte mit ähnlichem Aussehen kaufen“ auf der Seite Funktionsverwaltung in der Commerce-Zentrale](./media/enableshopsimilarlooks.png)

Nach Abschluss der vorhergehenden Aufgaben werden POS-Terminals automatisch um kontextabhängigen Bereich **Produkte mit ähnlichem Aussehen kaufen** erweitert. Durch die Auswahl **Weitere Details** können Benutzer von POS-Terminals zu einer speziellen Seite „Produkte mit ähnlichem Aussehen kaufen“ weitergeleitet werden, auf der weitere Filter angewendet werden können.

> [!NOTE]
> Wenn Sie die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ deaktivieren, sind keine anderen Arten von Produktempfehlungen betroffen. Weitere Informationen zu Produktempfehlungen finden Sie unter [Überblick über Produktempfehlungen](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Mithilfe des Commerce Site Builder eine Schaltfläche mit ähnlichem Aussehen zu den Produktdetailseiten hinzufügen

Nachdem Sie die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ in der Commerce-Zentrale aktiviert haben, können Einzelhändler mit einer Option im Commerce Site Builder eine Schaltfläche **Produkte mit ähnlichem Aussehen kaufen** auf einer beliebigen Produktdetailseite (PDP) zum Kauffeld hinzufügen. Ein Kunde, der diese Schaltfläche auswählt, wird zu einer speziellen Seite „Produkte mit ähnlichem Aussehen kaufen“ weitergeleitet, auf der visuell ähnliche Produkte angezeigt werden. Dort kann der Kunde Auswahlen verwenden, um die Produkte weiter zu filtern.

Gehen Sie folgendermaßen vor, um eine Schaltfläche **Produkte mit ähnlichem Aussehen kaufen** zu einem PDP mithilfe des Commerce Site Builder hinzuzufügen.

1. Öffnen Sie eine vorhandene Site Builder-Seite, die ein Kauffeld enthält.
1. Wählen Sie im linken Navigationsbereich das Kauffeld aus.
1. Wählen Sie im rechten Navigationsbereich das Kontrollkästchen **Link für „Produkte mit ähnlichem Aussehen kaufen“ aktivieren** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen. Nach der Veröffentlichung der Seite enthält die PDP eine Schaltfläche **Produkte mit ähnlichem Aussehen kaufen**.

Die folgende Abbildung zeigt das Kontrollkästchen **Links für „Produkte mit ähnlichem Aussehen kaufen“ aktivieren** und die Schaltfläche **Produkte mit ähnlichem Aussehen kaufen** auf einer Beispiel-PDP im Site Builder.

![Das Kontrollkästchen „Link für Produkte mit ähnlichem Aussehen kaufen“ und die Schaltfläche „Ähnliches Aussehen“ kaufen auf einer Beispiel-PDP im Site Builder aktivieren](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Produktempfehlungen am POS hinzufügen](product.md)

[Empfehlungen zum Transaktionsbildschirm hinzufügen](add-recommendations-control-pos-screen.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
