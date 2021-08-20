---
title: Dauerauftragsworkflow (Übersicht)
description: Dieses Thema enthält eine Übersicht über den Dauerauftragsworkflow.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b0de1100d36f8399caf4cf73c1883f25e61e3c66341eb5419e8350b90d2362e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779931"
---
# <a name="subscription-workflow-overview"></a>Dauerauftragsworkflow (Übersicht) 

[!include [banner](../includes/banner.md)]


Sie sind Administrator für Daueraufträge in einem Unternehmen, das Daueraufträge für die Wartung von Beleuchtungseinrichtungen anbietet. Ein Debitor tritt an das Unternehmen heran, um einen Dauerauftrag für eine jährliche Wartung seiner Beleuchtungseinrichtungen abzuschließen.

## <a name="setting-up-subscriptions"></a>Einrichten von Daueraufträgen

Der erste Schritt beim Einrichten eines Dauerauftrags besteht im Erstellen einer Dauerauftragsgruppe für die neue Servicevereinbarung bzw. darin, sich zu vergewissern, dass die Dauerauftragsgruppe vorhanden ist. Ist bereits eine Dauerauftragsgruppe vorhanden, muss diese für eine jährliche Fakturierung für den Debitor sowie für die Antizipierung von Umsatzerlösen auf Monatsbasis eingerichtet werden. Weitere Informationen zum Einrichten von Daueraufträgen finden Sie unter [Dauerauftragsgruppen einrichten](set-up-subscription-groups.md).

Nach Erstellung der Dauerauftragsgruppe kann der Dauerauftrag erstellt werden. Weitere Informationen dazu, wie von Daueraufträgen, finden Sie unter[Erstellen von Daueraufträgen auf der Grundlage einer Dauerauftragsgruppe](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Erstellen und Ändern von Dauerauftragsbuchungen

Nach dem Einrichten des Dauerauftrags erstellen Sie die Buchung der Dauerauftragsgebühr für den ersten Rechnungsstellungszeitraum (in diesem Fall: ein Jahr). Bei den Buchungen handelt es sich um Buchungen vom Typ **Regelmäßig**. Das bedeutet, dass lediglich Dauerauftragsbuchungen erstellt werden können, bei denen Anfangs- und Startdatum den im Formular **Periodentypen** erstellten Perioden entsprechen. Weitere Informationen zu kostenlosen Transaktionen finden Sie unter [Dauerauftragsgebühren-Buchungen erstellen](create-subscription-fee-transactions.md).

Nach dem Einrichten des Dauerauftrags für den Debitor erfahren Sie, dass dem Debitor ein Preisnachlass von 10 Prozent auf alle Listenpreise des Serviceangebots gewährt wurde. Der Preis der erstellten Buchungsgebühr muss deshalb entsprechend verringert werden.

Ein paar Stunden später erhalten Sie einen Anruf von Ihrer Kontaktperson beim Debitor, und sie erfahren, dass die Servicevereinbarung für die Beleuchtungseinrichtung zwar immer noch gewünscht wird, gegen Ende des Jahres allerdings eine Erneuerung dieser Einrichtung geplant ist. Aus diesem Grund werden die Wartungsleistungen lediglich bis Oktober 2013 benötigt. Also erstellen Sie eine neue Buchung für Dauerauftragsgebühren vom Typ **Minderungstage**, um die Monatsanzahl des Dauerauftrags für den Debitor zu verringern. Weitere Informationen dazu, wie Sie Tage reduzieren, finden Sie unter [Verringern der Tage für Dauerauftragsgebühren](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Fakturieren und Antizipieren von Dauerauftragsbuchungen

Die Einrichtung des Dauerauftrags ist nun abgeschlossen, und der Dauerauftrag kann dem Debitor in Rechnung gestellt werden. Weitere Informationen zum Fakturieren von Daueraufträgen finden Sie unter [Dauerauftragstransaktionen faktuieren](invoice-subscription-transactions.md).

Zwei Tage später erhalten Sie einen Anruf des Debitors, der darum bittet, die Rechnung nicht in Euro, sondern in US-Dollar auszustellen. Also erstellen Sie eine Gutschrift sowie eine neue Dauerauftragsbuchung in der korrekten Währung. Weitere Informationen zum Erstellen einer Gutschrift für Dauerauftragsbuchungen finden Sie unter [Gutschreiben von Dauerauftragsbuchungen](credit-subscription-transactions.md).

Am Monatsende kann der Monatsumsatz des Dauerauftrags des Debitors für das GuV-Konto sowie für die RIF-Konten antizipiert werden. Weitere Informationen zum Antizipieren von Umsatzerlös für Daueraufträge finden Sie unter [Dauerauftragsumsatz antizipieren](accrue-subscription-revenue.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]