---
title: Gutscheine
description: Dieser Artikel bietet eine Übersicht über couponbezogene Funktionen in Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 2594848948b141015adfaa4ec27e2c2b4cc4dcd2
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410764"
---
# <a name="coupons"></a>Gutscheine

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dieser Artikel bietet eine Übersicht über couponbezogene Funktionen in Microsoft Dynamics 365 Commerce.

Coupons sind Codes und Strichcodes, die verwendet werden, um Transaktionen Rabatte hinzuzufügen. Einzelhändler geben Coupons an potenzielle oder Bestandskunden aus, um ihre Markenbekanntheit zu verbessern, die Konversion zu fördern, ihren Kundenstamm zu halten, den Umsatz zu steigern und schließlich den Umsatz zu steigern. Coupons haben sich zu einem der beliebtesten Marketinginstrumente entwickelt und sind eine neue Norm im E-Commerce-Verkauf.

In Dynamics 365 Commerce sind Coupons mit Rabatten verknüpft und gelten als zusätzliche Prüfung zusätzlich zu Rabatten. Jeder Coupon ist mit einem Rabatt verbunden und der verknüpfte Rabatt legt die Produktgruppe fest, für die der Coupon gültig ist.

Preisgruppen, die einem Rabatt zugeordnet sind, definieren die berechtigten Bedingungen, für die ein Coupon verwendet werden kann. Diese Bedingungen umfassen Kundengruppen und Verkaufskanäle. Coupons bieten auch die Eigenschaften **Nutzungslimit** und **Debitor erforderlich**, die verwendet werden können, um optionale Nutzungseinschränkungen zu konfigurieren.

Jeder Coupon kann mehrere Couponcodes und Couponstrichcodes haben, und jeder Code kann seinen eigenen Datumsbereich und Status für die Gültigkeit haben. Wenn der Status eines Codes auf **Inaktiv** gesetzt ist, kann der Code in keinem Kanal verwendet werden.

## <a name="set-up-a-coupon"></a>Einen Coupon einrichten

Bevor Sie einen Coupon einrichten können, müssen Sie den Couponstrichcode und zwei Couponnummernkreise einrichten.

Führen Sie die folgenden Schritte aus, um in Commerce headquarters einen Coupon einzurichten.

1. Navigieren Sie zu **Einzelhandel und Handel \> Lagerverwaltung \> Strichcodes und Beschriftungen \> Maskenzeichen**.
1. Wählen Sie **Hinzufügen** aus, um ein Maskenzeichen vom Typ **Couponcode** zu erstellen. Sie können im Feld **Zeichen** jedes unbenutzte Zeichen auswählen.
1. Navigieren Sie zu **Einzelhandel und Handel \> Lagerverwaltung \> Strichcodes und Beschriftungen \> Strichcodemaske einrichten**.
1. Wählen Sie **Neu** aus, um eine Strichcodemaske vom Typ **Coupon** zu erstellen.
1. Navigieren Sie zu **Einzelhandel und Handel \> Lagerverwaltung \> Strichcodes und Beschriftungen \> Strichcode einrichten**.
1. Wählen Sie **Neu**, um einen Strichcode zu erstellen, der die Strichcodemaske verwendet, die Sie erstellt haben.
1. Wechseln Sie zu **Organisationsverwaltung \> Sequenznummern**.
1. Erstellen Sie zwei Sequenznummern:

    1. Eine Sequenz für die Referenz **Couponnummer**. Diese Sequenz definiert den eindeutigen Bezeichner des Gutscheins.
    1. Eine Sequenz für die Referenz **Couponcode-ID**. Diese Sequenz legt den eindeutigen Bezeichner für jeden Couponcode für einen Coupon fest.

    Für beide Nummernkreise müssen Sie das Feld **Bereich** auf **Unternehmen** festlegen. In den meisten Fällen sollten beide Nummernsequenzen automatisch generiert werden.

1. Navigieren Sie zu **Handelsparameter \> Preise und Rabatte \> Coupons**.
1. Legen Sie das Feld **Couponstrichcodemaske** auf den Strichccode fest, den Sie zuvor erstellt haben.
1. Gehen Sie zu **Handelsparameter \> Nummernsequenzen**.
1. Wählen Sie die Nummernsequenzen aus, die Sie zuvor für die Referenzen **Couponnummer** und **Couponcode-ID** aus.

Um einen Coupon einzurichten, müssen Sie den Rabatt und den Coupon separat erstellen und sie dann verknüpfen, indem Sie den Rabatt im Feld **Rabatt** der Couponkonfiguration auswählen. Nachdem ein Coupon mit einem Rabatt verknüpft ist, werden die Felder **Status**, **Gültigkeitsdatum** und **Ablaufdatum** des verknüpften Rabatts schreibgeschützt, da die Werte durch den Status und die Gültigkeitsdauer des Gutscheins bestimmt werden. Wenn der Status eines Coupons auf **Aktiv** gesetzt ist, wird der Status des verknüpften Rabatts automatisch auf **Aktiviert** aktualisiert. Entsprechend wird, wenn der Status eines Coupons auf **Inaktiv** gesetzt ist, der Status des verknüpften Rabatts automatisch auf **Deaktiviert** aktualisiert.

## <a name="use-a-coupon"></a>Einen Coupon verwenden

Um einen Coupon auf eine Verkaufsbuchung an der Handelsverkaufsstelle (POS) anzuwenden, können Sie einen Couponcode oder einen Couponstrichcode verwenden. Um einen Couponcode zu verwenden, wählen Sie den Vorgang **Couponcode hinzufügen** und geben Sie dann den Code ein. Um einen Couponstrichcode zu verwenden, können Sie den Strichcode entweder mit einem Gerät scannen oder ihn über die Zifferntastatur auf dem **Buchung**-Bildschirm eingeben.

Einzelhändler möchten manchmal, dass Kassierer in der Lage sind, Kunden zur Beschwichtigung oder wegen Produktfehlern feste Rabatte zu gewähren, aber sie möchten keine Couponcodes ausdrucken und an die Kassierer verteilen. In diesem Fall können Sie die Option **Ohne Couponcode anwenden** für den Coupon auf **Ja** setzen. POS-Kassierer können dann die Funktion **Coupon anwenden** im Vorgang **Verfügbare Rabatte anzeigen** verwenden, um einer Buchung einen Coupon hinzuzufügen, ohne den Code manuell einzugeben. Wenn mehrere Couponcodes für einen Coupon existieren, wählt das System automatisch den ersten aktiven Code aus und wendet ihn auf die Buchung an.

Um einem Callcenter-Auftrag einen Gutschein hinzuzufügen, muss ein Callcenter-Benutzer **Coupons** auf der Registerkarte **Verwalten** im Aktionsbereich auf der Auftragsseite auswählen.

Um einer E-Commerce-Bestellung einen Coupon hinzuzufügen, kann der Käufer den Couponcode in das Feld **Angebotscode** im Warenkorb einfügen.

Nachdem ein Coupon zu einem Auftrag hinzugefügt wurde, löst das Preismodul sofort eine Neuberechnung für den gesamten Auftrag aus, unabhängig davon, ob die verzögerte Berechnung aktiviert ist.

> [!NOTE]
> In Commerce-Version 10.0.30 und früher müssen Callcenter-Benutzer einen Coupon zu einem Callcenter-Auftrag hinzufügen und dann **Neu berechnen** in der Gruppe **Berechnen** der Registerkarte **Verkaufen** des Aktionsbereichs auswählen, um den mit diesem Coupon verknüpften Rabatt anzuwenden.

## <a name="coupon-usage-limit"></a>Couponnutzungslimit

Coupons können mit begrenzter Nutzung konfiguriert werden. Das Verwendungslimit kann pro Debitor, Kanal oder global definiert werden. Die Nutzungsgrenze wird pro Couponcode auf einem Coupon erzwungen. So kann ein Einwegcoupon, der zwei Couponcodes hat, zweimal verwendet werden, und zwar einmal mit jedem Couponcode.

Coupons können über alle Verkaufskanäle hinweg verwendet werden. Für Callcenter können Coupons mit begrenzter Nutzung jedoch nur angewendet werden, wenn die Einstellung **Auftragsabschluss aktivieren** für den Callcenter-Kanal aktiviert ist. Wenn die Einstellung **Auftragsabschluss aktivieren** deaktiviert ist, können nur Coupons mit unbegrenzter Nutzung angewendet werden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
