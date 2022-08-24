---
title: Preisberechnungsfunktionen in POS
description: Dieser Artikel beschreibt verschiedene Preis- und Rabattfunktionen in der Microsoft Dynamics 365 Commerce Point-of-Sale (POS)-Anwendung.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 92bbc3b81b889f106dc113528afbdc37d1106ff3
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294130"
---
# <a name="pricing-functions-in-pos"></a>Preisberechnungsfunktionen in POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieser Artikel beschreibt verschiedene Preis- und Rabattfunktionen in der Microsoft Dynamics 365 Commerce Point-of-Sale (POS)-Anwendung.

Die Dynamics 365 Commerce POS-Anwendung bietet umfangreiche Funktionen, mit denen Mitarbeiter in der ersten Reihe Store Commerce durchführen können. Die folgende Tabelle zeigt die Preis- und Rabattfunktionen, die derzeit in der Anwendung verfügbar sind.

| Funktion                       | POS-Vorgänge |
|--------------------------------|----------------|
| Preise anzeigen                    | [Preisüberprüfung](#price-check) |
| Rabatte anzeigen                 | [Alle Rabatte anzeigen](#view-all-discounts)<br>[Verfügbare Rabatte anzeigen](#view-available-discounts) |
| Preise überschreiben                | [Preisüberschreibung](#price-override) |
| Rabatte anwenden oder entfernen      | [Positionsrabattbetrag](#line-discount-amount)<br>[Positionsrabatt in Prozent](#line-discount-percent)<br>[Gesamter Rabattbetrag](#total-discount-amount)<br>[Rechnungsrabatt gesamt (in Prozent)](#total-discount-percent)<br>[Systemrabatte aus Buchung entfernen](#remove-system-discounts-from-transaction)<br>[Systemrabatte erneut anwenden](#reapply-system-discounts) |
| Gutscheine anwenden oder entfernen        | [Couponcode hinzufügen](#add-coupon-code)<br>[Couponcode entfernen](#remove-coupon-code) |
| Preise und Rabatte berechnen | [Neu berechnen](#recalculate) |

Informationen darüber, wie die vorangehenden Vorgänge in der POS-Anwendung konfiguriert werden können und ob sie den Offline-Modus unterstützen, finden Sie unter [Online- und Offline-Point-of-Sale (POS)-Operationen](pos-operations.md).

## <a name="price-check"></a>Preisüberprüfung

Der Vorgang **Preischeck** ermöglicht es POS-Benutzern, vorkonfigurierte Preise für ein bestimmtes Produkt nachzuschlagen.

## <a name="view-all-discounts"></a>Alle Rabatte anzeigen

Der Vorgang **Alle Rabatte anzeigen** ermöglicht es POS-Benutzern, alle effektiven Werbeaktionen nachzuschlagen, die derzeit im Ladenkanal laufen. Insbesondere listet dieser Vorgang alle Rabatte auf, die einer der folgenden Bedingungen entsprechen:

- Die Preisgruppe des Rabatts stimmt mit der Preisgruppe der Filiale überein.
- Die Preisgruppe des Rabatts wird einem Zugehörigkeits- oder Treueprogramm zugeordnet.
- Die Preisgruppe des Rabatts wird einem Katalog zugeordnet, der mit der Filiale verbunden ist.

Der Vorgang **Alle Rabatte anzeigen** zeigt nur die Rabatte an, die mit keinem der angewandten Rabatte konkurrieren. Dieses Verhalten trägt dazu bei, dass, wenn ein Vertriebsmitarbeiter einen Kunden über einen Rabatt informiert und der Kunde die erforderliche Maßnahme ergreift (z.B. wenn der Kunde einen weiteren Artikel kauft, um 10 Prozent Rabatt zu erhalten), der Rabatt auf die Transaktion angewendet wird. Die gutscheinbasierten Rabatte werden nur dann angezeigt, wenn die Option **Ohne Gutscheincode anwenden** eingeschaltet ist.

Im Vorgang **Alle Rabatte anzeigen** können POS-Benutzer anhand des Namens und der Beschreibung nach Rabatten suchen und Rabatte danach filtern, ob sie einen Gutschein benötigen.

## <a name="view-available-discounts"></a>Verfügbare Rabatte anzeigen

Der Vorgang **Verfügbare Rabatte anzeigen** ermöglicht es POS-Benutzern, alle Rabatte anzuzeigen, die für eine ausgewählte Position in einer Transaktion oder für die gesamte Transaktion gelten. Die Rabatte, die auf eine ausgewählte Position anwendbar sind, umfassen Rabatte, die bereits angewendet wurden, und Rabatte, die noch nicht angewendet wurden, aber angewendet werden können (z. B. Mix-and-Match-Rabatte, die zusätzliche Artikel erfordern). Wenn ein gültiger Rabatt mit einem Gutschein verknüpft ist, bei dem die Option **Ohne Gutscheincode beantragen** eingeschaltet ist, kann der POS-Benutzer auch die Funktion **Gutschein anwenden** innerhalb dieses Vorgangs verwenden, um den Gutschein direkt einzulösen, ohne Gutscheincodes oder Gutschein-Barcodes eingeben oder scannen zu müssen.

## <a name="price-override"></a>Preisüberschreibung

Der Vorgang **Preisüberschreibung** ermöglicht es POS-Benutzern, den Verkaufspreis eines Produkts in einer Transaktion zu überschreiben. Dieser Vorgang funktioniert nur für Produkte, die so konfiguriert sind, dass sie Preisüberschreibungen zulassen.

## <a name="line-discount-amount"></a>Positionsrabattbetrag

Der Vorgang **Zeilenrabattbetrag** ermöglicht es POS-Benutzern, einen Rabattbetrag für einen Einzelposten in einer Transaktion einzugeben. Dieser Vorgang gilt nur für rabattfähige Artikel und respektiert den **Maximalen Zeilenrabattbetrag**, der in der POS-Berechtigungsgruppe für den Benutzer angegeben ist.

## <a name="line-discount-percent"></a>Positionsrabatt in Prozent

Der Vorgang **Positionsrabatt in Prozent** ermöglicht es POS-Benutzern, einen Rabattbetrag in Prozent für einen Einzelposten in einer Transaktion einzugeben. Dieser Vorgang gilt nur für rabattfähige Artikel und respektiert den **Maximalen Zeilenrabattbetrag in Prozent**, der in der POS-Berechtigungsgruppe für den Benutzer angegeben ist.

## <a name="total-discount-amount"></a>Gesamter Rabattbetrag

Der Vorgang **Gesamtrabattbetrag** ermöglicht es POS-Benutzern, einen Rabattbetrag für einen Einzelposten in einer Transaktion einzugeben. Dieser Vorgang gilt nur für rabattfähige Artikel und respektiert den **Maximalen Gesamtrabattbetrag**, der in der POS-Berechtigungsgruppe für den Benutzer angegeben ist. Wenn der eingegebene Rabattbetrag den maximalen Gesamtrabattbetrag übersteigt, wird der Vorgang blockiert und es wird kein Berechtigungsüberschreibungsfluss ausgelöst. Derzeit kann kein Gesamtrabattbetrag auf einen Einkaufswagen angewendet werden, der eine Mischung aus Verkaufsartikeln und Retourenartikeln enthält.

## <a name="total-discount-percent"></a>Rechnungsrabatt gesamt (in Prozent)

Der Vorgang **Gesamtrabatt in Prozent** ermöglicht es POS-Benutzern, einen Rabatt in Prozent für eine Transaktion einzugeben. Dieser Vorgang gilt nur für rabattfähige Artikel und respektiert den **Maximalen Gesamtrabatt in Prozent**, der in der POS-Berechtigungsgruppe für den Benutzer angegeben ist. Wenn der eingegebene Rabattbetrag in Prozent den maximalen Gesamtrabatt in Prozent übersteigt, wird der Vorgang blockiert und es wird kein Berechtigungsüberschreibungsfluss ausgelöst. Derzeit kann kein Gesamtrabatt in Prozent auf einen Einkaufswagen angewendet werden, der eine Mischung aus Verkaufsartikeln und Retourenartikeln enthält.

## <a name="remove-system-discounts-from-transaction"></a>Systemrabatte aus Buchung entfernen

Der Vorgang **Entfernen Sie Systemrabatte aus der Transaktion** ermöglicht es POS-Benutzern, alle angewendeten Systemrabatte (einschließlich gutscheinbasierter Rabatte) von einer Transaktion zu löschen. Nachdem dieser Vorgang ausgeführt wurde, beginnt das Preisfindungsmodul damit, Systemrabatte aus dem Umfang der Rabattberechnung auszuschließen. Der Vorgang **Entfernen Sie Systemrabatte aus der Transaktion** entfernt keine manuellen Rabatte.

## <a name="reapply-system-discounts"></a>Systemrabatte erneut anwenden

Der Vorgang **Systemrabatte erneut anwenden** ermöglicht es POS-Benutzern, vom System berechnete Rabatte erneut auf eine Transaktion anzuwenden, wenn die Rabatte mithilfe des Vorgangs **Entfernen Sie Systemrabatte aus der Transaktion** entfernt wurden. Nachdem dieser Vorgang ausgeführt wurde, beginnt das Preisfindungsmodul damit, Systemrabatte in den Umfang der Rabattberechnung einzuschließen.

## <a name="add-coupon-code"></a>Couponcode hinzufügen

Der Vorgang **Gutscheincode hinzufügen** ermöglicht es POS-Benutzern, einer Transaktion einen Gutschein hinzuzufügen, indem sie einen Gutscheincode eingeben. Alternativ können POS-Benutzer einen Gutscheinstrichcode scannen oder über die Zifferntastatur auf dem **Transaktion**-Bildschirm eingeben.

## <a name="remove-coupon-code"></a>Couponcode entfernen

Der Vorgang **Gutscheincode entfernen** ermöglicht es POS-Benutzern, einen oder mehrere Gutscheine auszuwählen und zu entfernen, die derzeit auf eine Transaktion angewendet werden.

## <a name="recalculate"></a>Neu berechnen

Der Vorgang **Neu berechnen** ermöglicht es POS-Benutzern, eine On-Demand-Preisberechnung auszulösen. Dieser Vorgang ist erforderlich, wenn die Preissperre und/oder die verzögerte Preisberechnung aktiviert ist und der POS-Benutzer Preise und Rabatte nach Warenkorb- oder Bestelländerungen neu berechnen möchte. Der Vorgang **Neu berechnen** berechnet immer den gesamten Auftrag neu. Er kann nicht verwendet werden, um ausgewählte Verkaufszeilen neu zu berechnen. Um manuelle Rabatte auf eine gesperrte Verkaufszeile im POS anzuwenden, müssen POS-Benutzer zuerst den Vorgang **Neu berechnen** zum Freischalten aller Verkaufszeilen verwenden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
