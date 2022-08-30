---
title: Zahlungsmittel-basierte Rabatte
description: Dieser Artikel beschreibt eine zahlungsmittelbasierte Rabattfunktion, mit der Einzelhändler Rabatte für bestimmte Zahlungsmitteltypen in Microsoft Dynamics 365 Commerce konfigurieren können.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: 3c28297e62e5b2880a7a39381702d5a1448c91ac
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336732"
---
# <a name="tender-based-discount"></a>Zahlungsmittelbasierter Rabatt

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieser Artikel beschreibt eine zahlungsmittelbasierte Rabattfunktion, mit der Einzelhändler Rabatte für bestimmte Zahlungsmitteltypen in Microsoft Dynamics 365 Commerce konfigurieren können.

Es ist eine gängige Praxis im Einzelhandel, private, gebrandete Kreditkarten zu veröffentlichen. Die Einzelhändler profitieren, da sie bevorzugte Sätze von den Banken erhalten. Darüber hinaus können diese Kreditkarten Kunden dazu anhalten, den Shop häufig zu besuchen, und das Endergebnis des Einzelhändlers verbessern. Deshalb haben Einzelhändler einen Anreiz, die Kundennutzung der gebrandeten Kreditkarten zu erhöhen. Um dieses Ziel zu erreichen, bieten sie Kunden, die diese Kreditkarten verwenden, häufig zusätzliche Rabatte.

Alternativ können Einzelhändler, die nicht gebrandete Kreditkarten bereitstellen, Kunden dazu anhalten, zu bezahlen, indem sie andere Zahlungsmitteltypen, wie Bargeld, Geschenkkarten oder Treuepunkte verwenden. Auf diese Weise können sie dazu beitragen, die Verarbeitungsgebühren für die Kreditkarten zu reduzieren. Daher können Einzelhändler Kunden Rabatte anbieten, die diese alternativen Zahlungsmitteltypen verwenden.

## <a name="tender-based-discount"></a>Zahlungsmittelbasierter Rabatt

Commerce unterstützt einen *zahlungsmittelbasierten Rabatt*, mit dem Einzelhändler einen Rabattprozentsatz konfigurieren können, der auf eine Transaktion angewendet wird, wenn die Transaktionssumme einen bestimmten Betrag überschreitet und der Kunde mit der bevorzugten Zahlungsart bezahlt. Der zahlungsmittelbasierte Rabatt ist stufenbasiert, sodass unterschiedliche Rabattprozentsätze mit unterschiedlichen Schwellenwertbeträgen verknüpft werden können. Der Kunde kann entscheiden, ob eine Teilzahlung oder eine vollständige Zahlung durchführt wird, und das Preisgestaltungsmodul bestimmt den entsprechenden Rabattbetrag. Der zahlungsmittelbasierte Rabatt wird immer auf den Nettobetrag der Verkaufspositionen gewährt.

Der zahlungsmittelbasierte Rabatt kann nur auf Verkaufspositionen angewandt werden, deren Preise nicht gesperrt sind, und wird proportional auf die berechtigten Positionen angewandt. Wenn neue Auftragspositionen einem Auftrag hinzugefügt werden, wird der zahlungsmittelbasierte Rabatt nur auf die neuen Auftragspositionen während der Zahlung angewendet. Wenn ein Kundenauftrag zur Abholung oder Lieferung erteilt wird, aber der zahlungsmittelbasierte Rabatt wird nur auf den Einzahlungsbetrag angewendet. Nachdem der Auftrag erteilte wurde, sind die Preise der Verkaufspositionen während der Erfüllung gesperrt. Auf Saldi, die während der Abholung gezahlt oder während der Lieferung autorisiert werden, wird der zahlungsmittelbasierte Rabatt nicht angewandt. Der Zahlungsmittel-basierte Rabatt kann auf den ganzen Betrag eines Kundenauftrags nur angewendet werden, wenn der Einzelhändler den ganzen Betrag als Einzahlung einzieht, während der Auftrag erteilt wird.

Zahlungsmittelbasierte Rabatte konkurrieren nicht mit artikelbasierten Rabatten wie einfachen Rabatten, Mengenrabatten, Schwellenwertrabatten, Angebots-Sortimentrabatten und manuellen Rabatten. Zahlungsmittelbasierte Rabatte werden immer mit artikelbasierten Rabatten verrechnet. Daher wenn ein exklusiver Rabatt auf einen Artikel angewendet wird, kann der zahlungsmittelbasierte Rabatt trotzdem zusätzlich zu dem exklusiven periodischen Rabatt angewendet werden. Ebenso wenn ein Schwellenrabatt auf die Buchung angewendet wird und der Zahlungsmittel-basierte Rabatt verringert die Summe bis unter die Schwelle, wird der Schwellenrabatt dennoch auf die Buchung angewendet.

Obwohl zahlungsmittelbasierte Rabatte die Zwischensumme einer Buchung verringern, bleiben automatische Gebühren, die auf die Buchung angewendet werden, bestehen. Wenn beispielsweise die Zustellgebühren als 5 $ berechnet werden, da die Zwischensumme mehr als 100 $ war, und wenn der Zahlungsmittel-basierte Rabatt den Betrag verringert, sodass er unter 100 $ liegt, sind die Zustellgebühren noch 5 $ für den Auftrag.

Der zahlungsmittelbasierte Rabatte ist derzeit auf zwei Zahlungstypen beschränkt: Kreditkarten und Barzahlung. Wenn mehrere zahlungsmittelbasierte Rabatte für eine Zahlungsart konfiguriert werden, werden nur die besten Zahlungsmittel-basierten Rabatt angewendet.

## <a name="pos-user-experience"></a>POS-Benutzerumgebung

Wenn ein zahlungsmittelbasierter Rabatt für Bargeld eingerichtet wird und der Kassierer an der Verkaufsstelle (POS) die Schaltfläche **Bar bezahlen** wählt, um eine Mitnahmebuchung durchzuführen, wird der zahlungsmittelbasierte Rabatt automatisch auf die Buchung angewendet. Der reduzierte Betrag wird dann als der Saldo angezeigt. Wählt der Kassierer allerdings die Schaltfläche **Zurück** auf dem Zahlungsbildschirm aus, wird der Rabatt entfernt, und der ursprüngliche Betrag wird im Buchungsbildschirm angezeigt. Der Zahlungsmittel-basierte Rabatt wird entfernt, wenn die Zahlungsposition storniert wird.

Für Kreditkartenzahlungen können Einzelhändler den zahlungsmittelbasierten Rabatt auf einen oder mehrere Typen von Kreditkarten festlegen. Trotzdem kann das System den Kreditkartentyp nicht überprüfen, der verwendet wird, es sei denn, die Karte wird autorisiert. Wenn der Rabatt nach Autorisierung angewendet wird, ist die Zahlungsautorisierung für einen größeren Betrag, die Zahlungserfassung jedochist für einen kleineren Betrag. Um diese Situation zu verhindern, wenn ein Kunde mit einer Kreditkarte bezahlt, erhält der Kassierer eine Aufforderung über ein Dialogfeld, das alle bevorzugten Kreditkarten enthält, mit denen der Kunde einen zusätzlichen Rabatt bekommt. Der Kassierer kann dann fragen, ob der Kunde eine der bevorzugten Karten verwenden möchte, um einen zusätzlichen Rabatt zu erhalten. Wenn der Kassierer eine bevorzugte Karte auswählt, wird der zahlungsmittelbasierte Rabatt auf die Buchung angewendet, und der reduzierte Betrag wird im Zahlungsbildschirm angezeigt. Die Autorisierung gilt für den verringerten Betrag. Wenn der Kunde eine Karte verwendet, die von der abweicht Karte, die der Kassierer ausgewählt hat, wird eine Fehlermeldung angezeigt und die Autorisierung storniert.

## <a name="call-center-user-experience"></a>Callcenter-Benutzerfreundlichkeit

Wenn ein Callcenter-Benutzer während eines Callcenterauftrags **Vollständig** auswählt, erscheint der Bildschirm **Summen**. Zuerst umfassen die Summen auf diesem Bildschirm keine Zahlungsmittel-basierte Rabatte, da die Zahlungsmethode noch nicht ausgewählt wurde. Wenn der Benutzer im Bildschirm **Zahlung hinzufügen** die Zahlungsmethode auswählt, für die der Zahlungsmittel-basierte Rabatt konfiguriert wurde, wird der Zahlungsbetrag automatisch angepasst, sodass er der verbilligten Betrag beinhaltet. Wie ein Kunde am POS, kann sich der Callcenterkunde entscheiden, ob er den Betrag vollständig oder teilweise bezahlen möchte. Basierend auf dem Betrag, der gezahlt wird, wird der Zahlungsmittel-basierte Rabatt auf den Auftrag angewendet.

> [!NOTE]
> Kartenprüfung wird nicht für Callcenteraufträge ausgeführt. Wenn beispielsweise der Callcenterbenutzer Visa als Kreditkarte auswählt, aber der Kunde MasterCard verwendet, wendet das System den Rabatt noch an.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
