---
title: Auswirkung der Erweiterbarkeit von Commerce-Katalogen für B2B-Anpassungen
description: In diesem Artikel werden die Auswirkungen der Erweiterbarkeit der Funktion „Commerce-Kataloge für B2B“ in Microsoft Dynamics 365 Commerce beschrieben.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 06d304226270c9c63c6907190dc1038a38f70e44
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136799"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Auswirkung der Erweiterbarkeit von Commerce-Katalogen für B2B-Anpassungen

[!include [banner](includes/banner.md)]

In diesem Artikel werden die Auswirkungen der Erweiterbarkeit der Funktion **Commerce-Kataloge für B2B** in Microsoft Dynamics 365 Commerce beschrieben.

Wenn Sie den Katalogkontext auf benutzerdefinierte Szenarien erweitern möchten, müssen Ihre Anpassungen möglicherweise aktualisiert werden. Dieses Update folgt dem Standardprozess, den Kunden befolgen müssen, da ihre Anpassungen möglicherweise nicht automatisch die neuesten Funktionen unterstützen, nachdem Upgrades durchgeführt wurden. Wenn Ihre Anpassungen neue Funktionen oder Fehlerbehebungen in ihren Erfahrungen enthalten, empfehlen wir Ihnen, den Anpassungscode entsprechend zu aktualisieren. Dieses Update ähnelt den Änderungen, die Microsoft möglicherweise für den Kerncode vorgenommen hat.

Überprüfen Sie die folgenden Anpassungsfälle, um festzustellen, ob Ihre Anpassungen aktualisiert werden müssen.

> [!NOTE]
> - Alle Merchandising-Anwendungsprogrammierschnittstellen (APIs) sollten katalogfähig sein. Daher ist es wichtig, dass Sie die **CatalogID**-Parameter übergeben.
> - Der Standardkatalog (**CatalogID**=**0**) ist kein gültiger Katalog für angemeldete B2B-Benutzer (Business-to-Business). Daher schlagen alle API-Aufrufe fehl, die „0“ übergeben oder einen Standardwert verwenden, da Websitebenutzer keinen Zugriff auf Katalog 0 haben. Um die richtige Erfahrung zu erhalten, müssen die Kunden-API-Aufrufe aktualisiert werden, damit sie die Katalog-ID übergeben, die in der Katalogauswahl ausgewählt wurde. Wenn Sie einen Standardwert verwenden und der Benutzer den Katalog wechselt, sollte die Website die Daten für den ausgewählten Katalog bereitstellen. Daher sollten angepasste APIs den ausgewählten Katalog übergeben, um mit den APIs übereinzustimmen, die vom Commerce-Kerncode ausgeführt werden.

Die folgenden Anpassungsfälle erfordern Entwicklungsaktualisierungen:

- **Fall 1:** Ein Kunde führt eine eigene [Datenaktivität](e-commerce-extensibility/data-actions.md) ein, die eine produktbezogene API oder Datenaktivität aufruft. Die folgenden Aktualisierungsschritte sind erforderlich:

    1. Wenn die Datenaktivität einen direkten API-Aufruf verwendet, aktualisieren Sie die Datenaktivität so, dass sie die Katalog-ID übergibt, wie in der folgenden Beispielabbildung gezeigt.

        ![Aktualisierte Datenaktivität, die die Katalog-ID übergibt.](./media/customization1_a.png)

    1. Wenn die Datenaktivität eine andere produktbezogene Datenaktivität innerhalb der Anpassung aufruft, muss der Code aktualisiert werden, damit er einige neue Parameter übergibt, z. B. **requestContext**. Der **requestContext**-Parameter wird verwendet, um die aktuelle Katalog-ID abzurufen, wie in der folgenden Beispielabbildung gezeigt.

        ![Aktualisierte Datenaktivität, die den neuen Parameter übergibt.](./media/customization1_b.png)

- **Fall 2:** Ein Kunde hat eine [überschriebene Datenaktivität](e-commerce-extensibility/data-action-overrides.md). Der folgende Aktualisierungsschritt ist erforderlich:

    - Aktualisieren Sie die Datenaktivität wie in Fall 1.

- **Fall 3:** Ein Kunde hat eine Ansichtserweiterung, ein Skriptinjektormodul oder [geklontes Modul](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module). Dazu gehören Aufrufe von APIs oder Datenaktivitäten. Der folgende Aktualisierungsschritt ist erforderlich:

    - Aktualisieren Sie den Code wie in Fall 1, wie in der folgenden Beispielabbildung gezeigt.

       ![Aktualisierter Code, der den neuen Parameter übergibt.](./media/customization3.png)

- **Fall 4:** Ein Kunde verwendet einen **getById**-API-Aufruf. Der folgende Aktualisierungsschritt ist erforderlich:

    - Wechseln Sie zum **getByIds**-API-Aufruf stattdessen, weil der **getById**-API-Aufruf einige Einschränkungen hat und keine Katalogerkennung unterstützt.

- **Fall 5:** Ein Kunde hat eine Datenaktivität, die Informationen für mehrere Produkte abruft, die möglicherweise aus verschiedenen Katalogen stammen. Der folgende Aktualisierungsschritt ist erforderlich:

    - Teilen Sie die API-Aufrufe nach Katalog-ID auf. Bei Warenkorb-APIs kann der Warenkorb beispielsweise Produkte aus verschiedenen Katalogen enthalten. Die Produktlinien sollten nach Katalog-ID gruppiert werden, und sie sollten die API für jeden Katalog separat aufrufen, wie in der folgenden Beispielabbildung gezeigt.

        ![Aktualisierte Datenaktivität, die Produktlinien nach Katalog-ID gruppiert.](./media/customization5.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Commerce-Kataloge für B2B-Websites erstellen](catalogs-b2b-sites.md)

[FAQ zu Commerce-Katalogen für B2B](catalogs-b2b-sites-FAQ.md)

[Katalog-Picker-Modul](catalog-picker.md)
