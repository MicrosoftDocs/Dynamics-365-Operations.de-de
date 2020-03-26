---
title: Rabatte im POS anzeigen
description: In diesem Thema wird erläutert, wie Microsoft Dynamics 365 Commerce Vertriebsmitarbeitern dabei hilft, sich über Werbeaktionen zu informieren und wie sie für Cross- und Upsell-Bewegungen genutzt werden können.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 54201de6b242f8100c19a78468476a6308b1b18a
ms.sourcegitcommit: 5554b3abb4365666992efad692ae28e943faebd4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2020
ms.locfileid: "3116555"
---
# <a name="show-discounts-in-pos"></a>Rabatte im POS anzeigen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Werbeaktionen spielen eine wichtige Rolle bei der Motivation von Kunden, die Kaufentscheidungen treffen. Beispielsweise können Feiertage die höchsten Verkaufszahlen für Einzelhändler hervorbringen, da der gesamte Einzelhandelsmarkt mit verlockenden Werbeaktionen und Rabatten überflutet wird. Wenn die Mitarbeiter in den Geschäften die verfügbaren Aktionen kennen und verstehen, können sie diese Aktionen leicht für Cross-Selling und Up-Selling von Artikeln nutzen. In diesem Thema wird erläutert, wie Microsoft Dynamics 365 Commerce Vertriebsmitarbeitern dabei hilft, sich über Werbeaktionen zu informieren und wie sie für Cross- und Upsell-Bewegungen genutzt werden können.

## <a name="learn-about-store-discounts"></a>Erfahren Sie mehr über Ladenrabatte

Der Handel umfasst einen Vorgang mit dem Namen „Alle Rabatte anzeigen“. Diese Operation zeigt alle Rabatte an, die derzeit in einem Geschäft laufen. Die Operation „Alle Rabatte anzeigen“ kann auf eine Schaltfläche in der Verkaufsstelle (POS) abgebildet werden, und diese Schaltfläche kann der Seite **Willkommen** oder der Seite **Transaktion** hinzugefügt werden. Die folgende Abbildung zeigt ein Beispiel für die geöffnete Seite **Alle Rabatte**.

![Alle Rabatte Seite](./media/View_all_discounts.png "Alle Rabatte Seite")

Um die Rabatte anzuzeigen, sucht das System nach allen Rabatten, die eine oder mehrere der folgenden Bedingungen erfüllen:

- Die Preisgruppe des Rabatts stimmt mit der Preisgruppe der Filiale überein.
- Die Preisgruppe des Rabatts wird einem Zugehörigkeits- oder Treueprogramm zugeordnet.
- Die Preisgruppe des Rabatts wird einem Katalog zugeordnet, der mit der Filiale verbunden ist.

Die Seite **Alle Rabatte** zeigt nur einige couponbasierte Rabatte an, da Einzelhändler normalerweise Tausende von Coupons und entsprechende Rabatte für einzelne Kunden erstellen, und diese Seite ist nicht dazu gedacht, kundenspezifische Rabatte anzuzeigen. Coupon-basierte Rabatte werden nur angezeigt, wenn die Option **Beantragen ohne Coupon-Code** in jeder Coupon-Kopfzeile aktiviert ist. In diesem Fall können die Kassierer den Coupon anwenden, ohne einen Couponcode oder Barcode eingeben oder einscannen zu müssen.

Wenn die Option **Anwenden ohne Gutscheincode** eingeschaltet ist, sind verschiedene Szenarien möglich. Beispielsweise können Kassierer den Kunden zur Kundenbeschwichtigung oder aufgrund von Produktmängeln zusätzliche Rabatte gewähren. Gedruckte Coupon-Codes oder Barcodes müssen nicht an die Kassierer verteilt werden. Statt dessen können Kassierer die Schaltfläche **Coupons anwenden** wählen. Der Gutschein wird dann automatisch auf die Transaktion angewendet. Wenn mehrere Coupons zu einem Coupon-Kopf existieren, wählt das System automatisch den ersten aktiven Coupon der Transaktion aus.

Auf der Seite **Alle Rabatte** können Vertriebsmitarbeiter auch nach Rabatten anhand von Schlüsselwörtern suchen. Die Stichwortsuche sucht in den Feldern, die den Rabattnamen und die Rabattbeschreibung enthalten. Vertriebsmitarbeiter können Rabatte auch danach filtern, ob für einen Rabatt ein Gutscheincode erforderlich ist.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Cross-Sell und Upsell unter Verwendung von Rabatten

Mehrfache Rabatte, wie z.B. Mengenrabatte, Mix-and-Match-Rabatte und Schwellenwert-Rabatte, sind eine gute Möglichkeit, Kunden zu motivieren, mehr Produkte zu kaufen, um größere Rabatte zu erhalten. Daher tragen sie auch dazu bei, die Größe des Einkaufswagens eines Kunden und den Umsatz des Einzelhändlers zu erhöhen. Diese Rabatte können auf E-Commerce-Websites, in sozialen Netzwerken und auf Bannern im Geschäft veröffentlicht werden.

Doch selbst wenn alle diese Werbemethoden genutzt werden, könnten Kunden die Gelegenheit verpassen, die Vorteile von Werbeaktionen zu nutzen. Um es den Verkäufern leicht zu machen, zu erfahren, welche Werbeaktionen für eine ausgewählte Linie oder sogar für den gesamten Warenkorb gelten, können die Einzelhändler die Schaltfläche für die Operation „Alle Rabatte anzeigen“ zu einem beliebigen Schaltflächenraster am POS hinzufügen. Wir empfehlen, die Schaltfläche dem Schaltflächenraster für die Seite **Transaktion** hinzuzufügen. Auf diese Weise kann ein Verkäufer eine Transaktionszeile auswählen und dann die Schaltfläche wählen, um alle Rabatte anzuzeigen, die für die ausgewählte Zeile verfügbar sind. Der Vertriebsmitarbeiter kann auch eine andere Registerkarte wählen, um Rabatte anzuzeigen, die für die gesamte Transaktion gelten.

Die bereits erwähnte Seite **Alle Rabatte** zeigt nur die Rabatte an, die mit keinem der angewandten Rabatte konkurrieren. Dieses Verhalten trägt dazu bei, dass, wenn ein Vertriebsmitarbeiter einen Kunden über einen Rabatt informiert und der Kunde die erforderliche Maßnahme ergreift (z.B. wenn der Kunde einen weiteren Artikel kauft, um 10 Prozent Rabatt zu erhalten), der Rabatt auf die Transaktion angewendet wird. Wie bereits erwähnt, werden couponbasierte Rabatte nur dann angezeigt, wenn die Option **Beantragen ohne Coupon-Code** eingeschaltet ist.

In einem einfachen Szenario, in dem alle Rabatte die gleiche Priorität haben, ist der Modus für die gleichzeitige Gewährung von Rabatten **Gemischt**, und die Steuerung der gleichzeitigen Gewährung von Rabatten ist auf **Bester Preis und Mischung innerhalb der Priorität, niemals Mischung über die Prioritäten hinweg** eingestellt. Die Seite **Alle Rabatte** zeigt alle verfügbaren Rabatte für ein Produkt an, da alle Rabatte gebündelt sind und nicht miteinander konkurrieren.

Die folgenden Abbildungen zeigen die Logik, die bestimmt, welche Rabatte in fortgeschrittenen Szenarien angezeigt werden, wie z.B. in einem Szenario, in dem der Modus für die gleichzeitige Gewährung von Rabatten **Bester Preis** oder **Exklusiv** ist und zwei oder mehr Prioritäten verwendet werden. In diesen Szenarien werden die angezeigten Rabatte weiter beeinflusst, je nachdem, ob die Rabattgleichzeitigkeitssteuerung auf **Bester Preis und Verbindung innerhalb der Priorität eingestellt ist, niemals Verbindung über die Prioritäten** oder **Bester Preis nur innerhalb der Priorität, immer Verbindung über die Priorität**.

Die folgende Abbildung zeigt die Logik, die verwendet wird, wenn die Steuerung der Rabattgleichzeitigkeit auf **Bester Preis und Verbindung innerhalb der Priorität, niemals Verbindung über die Prioritäten** gesetzt wird.

![Logik für Bestpreis und Verbindung innerhalb der Priorität, niemals Verbindung über die Prioritäten](./media/Model_1.png "Logik für den besten Preis und die Verbindung innerhalb der Priorität, niemals über die Prioritäten hinweg").

Die folgende Abbildung zeigt die Logik, die verwendet wird, wenn die Steuerung der Rabattgleichzeitigkeit auf **Bester Preis nur innerhalb der Priorität, immer über die Prioritäten hinweg zusammengesetzt** gesetzt wird.

![Logik für Bestpreis nur innerhalb der Priorität, immer über die Priorität zusammengesetzt](./media/Model_2.png "Logik für den besten Preis nur innerhalb der Priorität, immer zusammengesetzt über die Priorität").
