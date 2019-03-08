---
title: Coupons für Einzelhandelsverkäufe einrichten
description: Dieses Thema bietet einen Überblick über Einzelhandelscoupons und erläutert deren Einrichtung.
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: bd3596b6c78c5959ca289c73bcc5785eb770be39
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "336588"
---
# <a name="set-up-coupons-for-retail-sales"></a>Coupons für Einzelhandelsverkäufe einrichten

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Überblick über Coupons

Coupons sind Codes und Strichcodes, die verwendet werden, um Buchungen Einzelhandelsrabatte hinzuzufügen. Jeder Coupon kann mehrere Codes haben, und jeder Code kann sein eigenes Gültigkeitsdatum haben.

Jeder Coupon wird einem Kleinrabatt zugeordnet. Die Preisgruppen, die dem Rabatt zugeordnet werden, definieren die Kunden, die einen Coupon oder die Kanäle verwenden können, in denen ein Coupon gültig ist.

Im Grunde genommen sind Coupons zusätzliche Validierungen neben Einzelhandelsrabatten. Der Coupon stellt die Couponcodes und Strichcodes bereit, die erforderlich sind, zusammen mit den Datumsbereichen des Codes. Der Coupon enthält auch optionale Verwendungslimiten und von Kunden erforderliche Eigenschaften. Der Rabatt enthält den Satz von Produkten, für die der Coupon gültig sein soll. Die Preisgruppen für den Rabatt für die Gruppe von Debitoren, von Kanälen oder von Katalogen, für die der Coupon gültig sein soll.

Um einen Coupon zu erstellen, stellen Sie den Rabatt und den Coupon getrennt her. Zum Verknüpfen wählen Sie den Rabatt auf der Couponseite in Microsoft Dynamics 365 for Retail aus.

> [!NOTE]
> Nachdem ein Coupon mit einem Rabatt verknüpft ist, sind einige Felder auf der Rabattseite in Microsoft Dynamics 365 for Retail schreibgeschützt, da sie durch die Einstellungen des Coupons verwaltet werden. Diese Felder enthalten die Felder für die Standarddatumsbereiche.

### <a name="limited-use-coupons"></a>Begrenzte Nutzung der Coupons

Coupons können als Coupons mit begrenzter Nutzung konfiguriert werden. Das Verwendungslimit kann pro Debitor oder Kanal oder als globale Limite definiert werden. Diese Limite wird erzwungen, wenn der Code oder der Strichcode in POS oder für den Auftrag eingegeben oder gescannt wird.

Die Grenze wird pro Couponcode auf einem Coupon erzwungen. So kann ein Einwegcoupon, der zwei Couponcodes hat, zweimal verwendet werden: einmal für jeden Couponcode. Jeder Code auf einem Coupon kann unabhängig auf Aktiv festgelegt werden.

> [!NOTE]
> Wenn ein Couponcode die Nutzungsgrenze erreicht hat, führt das System *nicht* automatisch den Status des Couponcodes auf "verwendet" aus. Das System erlaubt aber keine weitere Verwendung eines Couponcodes, der seine Nutzungsgrenze erreicht hat. Wenn der Status eines Couponcodes manuell auf einen Status anders als "Aktiv" festgelegt wird, dann kann dieser Couponcode nicht in einem beliebigen Kanal verwendet werden.

## <a name="managing-coupons"></a>Verwalten von Coupons

Sie müssen den Rabatt und den Coupon getrennt herstellen. Zum Verknüpfen wählen Sie den Rabatt auf der Couponseite aus. Nachdem ein Coupon mit einem Rabatt verknüpft ist, sind einige Felder auf der Rabattseite schreibgeschützt, da sie durch die Einstellungen des Coupons verwaltet werden. Diese Felder enthalten die Felder für die Standarddatumsbereiche.

Im Grunde genommen sind Coupons zusätzliche Validierungen neben Einzelhandelsrabatten. Der Coupon stellt die Couponcodes und Strichcodes bereit, die erforderlich sind, zusammen mit den Datumsbereichen, der eingeschränkten Nutzung und den Kundenanforderungen für die Nutzung des Codes. Der Rabatt enthält den Satz von Produkten, für die der Coupon gültig sein soll. Die Preisgruppen für den Rabatt für die Gruppe von Debitoren, von Kanälen oder von Katalogen, für die der Coupon gültig sein soll.

## <a name="system-setup-for-coupons"></a>System einrichten für Coupons

Bevor Sie einen Coupon einrichten können, müssen Sie den Couponstrichcode und zwei Couponnummernkreise einrichten.

1. **Maskenzeichen** Auf der Seite zum Erstellen eines neuen Couponcode Maskenzeichens. Sie können jedes nicht verwendete Zeichen auswählen.
2. Auf der Seite **Strichcodemaske - Einstellungen** können Sie eine neue Strichcodemaske erstellen. Legen Sie das Feld **Dateityp** auf **Coupon** fest.
3. Auf der Seite **Strichcode-Einstellungen** erstellen Sie einen neuen Strichcode, der die Strichcodemaske verwendet, die Sie soeben erstellt haben.
4. Auf der Seite **Nummernkreise** werden zwei neue Nummernkreise erstellt. Ein Nummernkreis ist für die Couponcode-Kennung, und die andere Sequenz für die Couponnummer. Die Couponcode-Kennung ist der eindeutige Bezeichner für jeden Couponcode für einen Coupon. Die Couponnummer ist die eindeutige Kennung für den Coupon. Jeder Coupon kann mehrere Codes und Strichcodes besitzen, die den Coupon starten.

    > [!NOTE]
    > Für beide Nummernkreise müssen Sie das Feld **Bereich** auf **Unternehmen** festlegen. In den meisten Fällen sollten Sie beide laufenden Nummern automatisch generieren.

5. Auf der Seite **Freigegebene Einzelhandelsparameter** auf der Registerkarte **Strichcodes**, wählen Sie den Strichcode aus, den Sie eben erstellt haben.
6. Auf der Seite **Retailparameter** auf der Registerkarte **Nummernkreise** wählen Sie die Nummernkreise aus, die Sie für die Couponnummer und Couponcode Kennung erstellten.
7. Sie können die Seite **Coupons** öffnen und jetzt neue Coupons erstellen.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Die Auswirkungen von Teilausführungsaktualisierungen auf Coupons

Couponfunktionen enthalten mehrere eindeutige Funktionen in Dynamics 365 for Retail. Microsoft Dynamics 365 for Retail Headquarters (HQ) und der Kanal können für einzelne Komponenten aktualisiert werden. Daher ist es wichtig, dass Sie beispielsweise wissen, wie einzelne Aktualisierungen die Couponfunktionen als ganzes beeinflussen.

- **HQ wird teilweise aktualisiert, wobei Retail Server und POS nicht aktualisiert werden.** In einer Hauptniederlassungsaktualisierung werden die Coupon- und Rabattseiten aktualisiert, und der Einzelhandelspreis wird ebenfalls aktualisiert. Wenn nur eine dieser zwei Komponenten aktualisiert wird, stimmen mehrere Seiten im Einzelhandel nicht mit den Herstellkostenkalkulationsdaten überein. Daher können unerwartete Rabattberechnungen oder möglicherweise Fehler während der Rabattberechnungen auftreten.
- **HQ wird teilweise aktualisiert, wobei Retail Server und POS nicht aktualisiert werden (N-1).** Nicht alle Einzelhandelsgeschäfte können gleichzeitig aktualisiert werden und es empfiehlt sich, anschließend die Hauptniederlassung zu aktualisieren, bevor Sie Einzelhandelsgeschäfte aktualisieren. Im Szenario N-1 sind neue Funktionen, die den Coupons zugeordnet ist, nicht in den Filialen verfügbar, die noch nicht aktualisiert wurden. So führen die Couponfunktionen "Positionen ausschließen" ein. Wenn Sie "Position ausschließen" verwenden, werden in einer Filiale keine Rabatt angewendet, die nicht in einer früheren Version ausgeführt werden.
- **HQ wird nicht aktualisiert, wobei Retail Server und POS aktualisiert werden (N+1).** Weil das aktualisierte Preismodul im Retail Server für bestehende Rabattcodes der Herstellkostenkalkulationen behandelt werden, sollten mit der Aktualisierung keine funktionalen Auswirkungen auf dieses Szenario haben.
