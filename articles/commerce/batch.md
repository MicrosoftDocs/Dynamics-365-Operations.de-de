---
title: Verbesserte Handhabung von Artikeln mit Chargenverfolgung
description: In diesem Artikel geht es um die verbesserte Handhabung von Artikeln mit Chargenverfolgung bei der Buchung von Auszügen in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 736ab8dd21f04d7119cca6d53bfeb5e408b8cbd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881877"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Verbesserte Handhabung von Artikeln mit Chargenverfolgung

[!include [banner](includes/banner.md)]

In diesem Artikel geht es um die verbesserte Handhabung von Artikeln mit Chargenverfolgung bei der Buchung von Auszügen in Microsoft Dynamics 365 Commerce.

Bei Artikeln mit Chargenverfolgung können zum Zeitpunkt des Verkauf keine Chargennummern an der Dynamics 365 Commerce-Verkaufsstelle (point of sale, POS) erfasst werden. Werden Umsätze in der Commerce-Zentralverwaltung mittels Kundenaufträgen oder Auszugsbuchungen gebucht, erwartet Commerce bei bestimmten Konfigurationen jedoch, dass für Artikel mit Chargenverfolgung gültige Chargennummern vorliegen und bei der Rechnungsabwicklung verwendet werden.

Gibt es für Produkte gültige Chargennummern, werden diese bei der Buchung von Auszügen sowohl im Rahmen der Inrechnungstellung von Debitorenaufträgen als auch der Inrechnungstellung von Aufträgen herangezogen. Liegen keine gültigen Chargennummern vor, kann bei der Inrechnungstellung von Debitorenaufträgen keine Buchung erfolgen, und der POS-Benutzer erhält eine Fehlermeldung. Die Auszugsbuchung wechselt selbst dann in den Fehlerstatus, wenn für die Produkte ein negativer Bestand aktiviert wurde.

Dank der Verbesserungen an Commerce wird bei Artikeln mit Chargenverfolgung, für die ein negativer Bestand aktiviert wird, die Inrechnungstellung von Debitorenaufträgen und Aufträgen durch die Auszugsbuchung nicht blockiert, wenn der Bestand bei diesen Artikel null (0) beträgt (0) oder keine Chargennummer vorliegt. Sind keine Chargennummern vorhanden, verwendet die verbesserte Funktion für die Verkaufspositionen eine Standardchargenkennung.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Die bei Debitorenaufträgen zu verwendende Standardchargenkennung festlegen

Legen Sie die bei Debitorenaufträgen zu verwendende Standardchargenkennung wie folgt fest:

1. Gehen Sie zu in der Commerce-Zentralverwaltung zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Commerce-Parameter**.
1. Geben Sie auf der Registerkarte **Debitorenaufträge** im Inforegister **Auftrag** im Feld **Standardchargenkennung** einen Wert ein.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Standardchargenkennung festlegen, die bei der Auszugsbuchung zur Inrechnungstellung von Aufträgen verwendet wird

Geben Sie die Standardchargenkennung ein, die bei der Auszugsbuchung zur Inrechnungstellung von Aufträgen verwendet wird.

1. Gehen Sie zu in der Commerce-Zentralverwaltung zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Commerce-Parameter**.
1. Geben Sie auf der Registerkarte **Buchung** im Inforegister **Lageraktualisierung** im Feld **Standardchargenkennung** einen Wert ein.

> [!NOTE]
> - Eine Standardchargenkennung kann nur dann festgelegt werden, wenn für den entsprechenden Filiallagerort und die Artikel die erweiterte Lagerhaltung aktiviert ist. Zukünftig wird diese Funktion auch unterstützt, wenn die erweiterte Lagerhaltung nicht aktiviert ist.
> - Die Unterstützung zur verbesserten Handhabung von Artikeln mit Chargenverfolgung bei der Auszugsbuchung ohne erweiterte Lagerhaltung wurde in der Commerce-Version 10.0.5 eingeführt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
