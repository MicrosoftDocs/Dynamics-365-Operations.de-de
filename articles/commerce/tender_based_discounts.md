---
title: Zahlungsmittel-basierte Rabatte
description: Dieses Thema bietet einen Überblick über Funktionen, mit denen Einzelhändler Rabatte für bestimmte Zahlungsmitteltypen konfigurieren können.
author: bebeale
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 4be0c9a6f0a32016e07b8e31d0aaff44b4a29623
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454652"
---
# <a name="tender-based-discounts"></a>Zahlungsmittel-basierte Rabatte

[!include [banner](includes/banner.md)]


Es ist eine gängige Praxis im Einzelhandel, private, gebrandete Kreditkarten zu veröffentlichen. Die Einzelhändler profitieren, da sie bevorzugte Sätze von den Banken erhalten. Darüber hinaus können diese Kreditkarten Kunden dazu anhalten, den Shop häufig zu besuchen, und das Endergebnis des Einzelhändlers verbessern. Deshalb haben Einzelhändler einen Anreiz, die Kundennutzung der gebrandeten Kreditkarten zu erhöhen. Um dieses Ziel zu erreichen, bieten sie Kunden, die diese Kreditkarten verwenden, häufig zusätzliche Rabatte.

Alternativ können Einzelhändler, die nicht gebrandete Kreditkarten bereitstellen, Kunden dazu anhalten, zu bezahlen, indem sie andere Zahlungsmitteltypen, wie Bargeld, Geschenkkarten oder Treuepunkte verwenden. Auf diese Weise können sie dazu beitragen, die Verarbeitungsgebühren für die Kreditkarten zu reduzieren. Daher können Einzelhändler Kunden Rabatte anbieten, die diese alternativen Zahlungsmitteltypen verwenden.

In Microsoft Dynamics 365 Commerce können Einzelhändler einen Rabattprozentsatz konfigurieren, der auf qualifizierte Leitungen angewendet wird, wenn der Kunde mit der bevorzugten Angebotsart bezahlt. Der Kunde kann entscheiden, ob eine Teilzahlung oder eine vollständige Zahlung durchführt wird, und Commerce bestimmt den entsprechenden Rabattbetrag. Beachten Sie, dass der Rabatt immer auf den Vorsteuerbetrag der qualifizierten Artikel angegeben wird.

Zahlungsmittel-basierte Rabatte konkurrieren nicht mit artikelbezogenen Rabatten, wie z.B. periodische oder manuelle Rabatte. Sie werden immer zusätzlich zu den Artikelrabatten angewendet. Daher wenn ein exklusiver periodischer Rabatt auf einen Artikel angewendet wird, wird der Zahlungsmittel-basierte Rabatt noch zusätzlich zu dem exklusiven periodischen Rabatt angewendet. Ebenso wenn ein Schwellenrabatt auf die Buchung angewendet wird und der Zahlungsmittel-basierte Rabatt verringert die Summe bis unter die Schwelle, wird der Schwellenrabatt dennoch auf die Buchung angewendet.

Obwohl Zahlungsmittel-basierte Rabatte die Zwischensumme der Buchung verringern, bleiben automatische Gebühren, die auf die Buchung angewendet werden, bestehen. Wenn beispielsweise die Zustellgebühren als 5 EUR berechnet werden, da die Zwischensumme mehr als 100 EUR war, und wenn der Zahlungsmittel-basierte Rabatt den Betrag verringert, sodass er unter 100 EUR liegt, sind die Zustellgebühren noch 5 EUR für den Auftrag.


> [!NOTE]
> Zahlungsmittel-basierte Rabatte werden proportional zu qualifizierten Verkaufspositionen verteilt und reduzieren den Vorsteuerbetrag einzelner Positionen. Wenn mehrere Zahlungsmittel-basierte Rabatte für einen Zahlungsmitteltyp (beispielsweise Bargeld) konfiguriert werden, werden nur die besten Zahlungsmittel-basierten Rabatt angewendet.

Zahlungsmittel-basierte Rabatte können nur in die Auftragspositionen übernommen werden, in denen die Preise nicht gesperrt werden. Wenn neue Auftragspositionen einem Auftrag hinzugefügt werden, wird der Zahlungsmittel-basierte Rabatt auf die neuen Auftragspositionen nur während der Zahlung angewendet. Zwar wird ein Kundenauftrag zur Abholung oder Lieferung erteilt, aber der Zahlungsmittel-basierte Rabatt wird nur auf den Einzahlungsbetrag angewendet. Nachdem der Auftrag erteilte wurde, sind die Preise der Verkaufspositionen während der Erfüllung gesperrt. Deshalb wird kein Zahlungsmittel-basierter Rabatt auf jeden beliebigen Saldo angewandt, der während der Abholung gezahlt oder während der Lieferung autorisiert wird. Der Zahlungsmittel-basierte Rabatt kann auf den ganzen Betrag eines Kundenauftrags nur angewendet werden, wenn der Einzelhändler den ganzen Betrag als Einzahlung einzieht, während der Auftrag erteilt wird.

> [!IMPORTANT]
> In Commerce werden derzeit Zahlungsmittel-basierte Rabatte auf zwei Zahlungstypen beschränkt: Kreditkarten und Barzahlung.

## <a name="pos-user-experience"></a>POS-Benutzerumgebung

Wenn der Zahlungsmittel-basierte Rabatt für Bargeld eingerichtet wird und der Kassierer am Point-of-Sale (POS) eine Schaltfläche auswählt, die der Bargeldzahlung zugeordnet ist, wird der Zahlungsmittel-basierte Rabatt automatisch auf die Buchung angewendet. Der reduzierte Betrag wird dann als der Saldo angezeigt. Wählt der Kassierer allerdings die Schaltfläche **Zurück** auf dem Zahlungsbildschirm aus, wird der Rabatt entfernt, und der ursprüngliche Betrag wird im Buchungsbildschirm angezeigt. Der Zahlungsmittel-basierte Rabatt wird entfernt, wenn die Zahlungsposition storniert wird.

Für Kartenzahlungen können Einzelhändler den Zahlungsmittel-basierten Rabatt auf einen oder mehrere Typen von Kreditkarten festlegen. Trotzdem kann das System den Kreditkartentyp nicht überprüfen, der verwendet wird, es sei denn, die Karte wird autorisiert. Wenn der Rabatt nach Autorisierung angewendet wird, ist die Zahlungsautorisierung für einen größeren Betrag, die Zahlungserfassung jedochist für einen kleineren Betrag.

Um diese Situation zu verhindern, sieht der Kassierer ein Dialogfeld, das Kreditkarten enthält, die dem Kunden weitere Einsparungen ermöglichen, wenn ein Kunde mit einer Kreditkarte bezahlt. Der Kassierer kann dann fragen, ob der Kunde eine der bevorzugten Karten verwenden möchte, um einen zusätzlichen Rabatt zu erhalten. Wenn der Kassierer eine bevorzugte Karte verwendet, wird der Zahlungsmittel-basierte Rabatt auf die Buchung angewendet, und der reduzierte Betrag wird im Zahlungsbildschirm angezeigt. Die Autorisierung gilt für den verringerten Betrag. Wenn der Kunde eine Karte verwendet, die von der abweicht Karte, die der Kassierer ausgewählt hat, wird eine Fehlermeldung angezeigt und die Autorisierung storniert.


## <a name="call-center-user-experience"></a>Callcenter-Benutzerfreundlichkeit

Wenn der Benutzer während eines Callcenterauftrags **Vollständig** auswählt, wird der Bildschirm **Summen** angezeigt. Zuerst umfassen die Summen auf diesem Bildschirm keine Zahlungsmittel-basierte Rabatte, da die Zahlungsmethode noch nicht ausgewählt wurde. Wenn der Benutzer im Bildschirm **Zahlung hinzufügen** die Zahlungsmethode auswählt, für die der Zahlungsmittel-basierte Rabatt konfiguriert wurde, wird der Zahlungsbetrag automatisch angepasst, sodass er der verbilligten Betrag beinhaltet. Wie der Kunde am POS, kann sich der Callcenterkunde entscheiden, ob er die gesamte Zahlung oder eine teilweise bezahlt. Basierend auf dem Betrag, der gezahlt wird, wird der Zahlungsmittel-basierte Rabatt auf den Auftrag angewendet.

> [!NOTE]
> Kartenprüfung wird nicht für Callcenteraufträge ausgeführt. Wenn beispielsweise der Callcenterbenutzer Visa als Kreditkarte auswählt, aber der Kunde MasterCard verwendet, wendet das System den Rabatt noch an.

## <a name="exclude-items-from-discounts"></a>Artikel von Rabatten ausschließen

Einzelhändler entscheiden sich häufig, mehrere Produkte wie neue Artikel oder gefragte Artikel aus Rabatten auszuschließen. Möglicherweise möchten sie jedoch dennoch Zahlungsmittel-basierte Rabatte anwenden. Beispielsweise konfiguriert ein Einzelhändler Commerce so, dass keine artikelbasierten Rabatte oder manuellen Rabatte zulässig sind. Wenn der Kunden jedoch mit dem bevorzugten Zahlungsmittel bezahlt, wendet Commerce trotzdem den Zahlungsmittel-basierten Rabatt an. Um Commerce auf diese Weise einzurichten, müssen Einzelhändler unter **Produktinformationsmanagement > Produkte > Freigegebene Produkte** den Artikel auswählen und dann auf dem **Commerce** Inforegister die Optionen **Alle Rabatte verhindern** und **Zahlungsmittel-basierte Rabatte verhindern** auf **Nein** und die Optionen **Rabatte verhindern** und **Manuelle Rabatte verhindern** auf **Ja** setzen.

> [!NOTE]
> Wenn die Konfiguration **Alle Rabatte verhindern** auf **Ja** eingestellt ist, werden keine Rabatte auf das Produkt angewendet. Nicht einmal Zahlungsmittel-basierte Rabatte werden angewendet.
