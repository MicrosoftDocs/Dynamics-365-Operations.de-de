---
title: Dynamics 365 Commerce-Preisgestaltungsmodul mit Dynamics 365 Sales verwenden
description: In diesem Artikel wird die Verwendung des Microsoft Dynamics 365 Commerce-Preisgestaltungsmoduls zur Erstellung von Verkaufsangeboten in Dynamics 365 Sales beschrieben.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881393"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce-Preisgestaltungsmodul mit Dynamics 365 Sales verwenden

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird die Verwendung des Microsoft Dynamics 365 Commerce-Preisgestaltungsmoduls zur Erstellung von Verkaufsangeboten in Dynamics 365 Sales beschrieben.

Das Dynamics 365 Commerce-Preisgestaltungsmodul unterstützt die meisten B2C-Preisszenarien (Business-to-Consumer), z. B. Preisgestaltung auf Filialebene, zugehörigkeits- und treuebasierte Preisgestaltung, Rabatte für Angebots-Sortimente, Mengenrabatte und Schwellenrabatte. Das Preisgestaltungsmodul verwendet komplexe Regeln, um den besten Preis für ein bestimmtes Angebot oder eine bestimmte Bestellung zu ermitteln.

Wenn Sie [duales Schreiben](./dual-write-overview.md) verwenden, haben Sie drei Möglichkeiten für Ihre Preisgestaltungsanforderungen. Sie können mit der statischen Preisgestaltung arbeiten, die die Preisliste aus Dynamics 365 Sales verwendet, mit dem Preisgestaltungsmodul von Dynamics 365 Supply Chain Management oder mit dem Preisgestaltungsmodul von Dynamics 365 Commerce. Unter diesen Optionen eignet sich das Preisgestaltungsmodul von Commerce am besten für B2C-Szenarien.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Preisgestaltungsmodul von Commerce in Sales verwenden

> [!NOTE]
> Derzeit kann das Preisgestaltungsmodul von Commerce nur für die Angebotserstellung in Sales verwendet werden. Die Integration von Aufträgen in das Preisgestaltungsmodul von Commerce ist noch nicht verfügbar.

Wenn Benutzer ein Angebot in Sales initiieren, kopiert das Framework für duales Schreiben die Angebotsdetails nach Commerce. Alle Änderungen an vorhandenen oder neu hinzugefügten Angebotspositionen in Sales werden nach Commerce kopiert. Wenn Benutzer das Preisgestaltungsmodul von Commerce verwenden möchten, um das Angebot zu bepreisen, können sie **Angebot bepreisen** auswählen, um die Preise des Angebots basierend auf dem Preisgestaltungsmodul von Commerce zu aktualisieren. Die Preise werden dann automatisch sowohl in Sales als auch in Commerce aktualisiert.

## <a name="prerequisites"></a>Voraussetzungen

- Bevor Sie das Preisgestaltungsmodul von Commerce in Sales verwenden können, müssen Sie die Schritte in [Prospect-to-Cash in Dual-Write](./dual-write-prospect-to-cash.md) ausführen.
- Sie müssen die Bewertung von Handelsvereinbarungen für die manuelle Eingabe deaktivieren, indem Sie die folgenden Schritte ausführen:

    1. Rufen Sie in Ihrer Commerce-Umgebung **Debitoren \> Einrichtung \> Debitorenparameter** auf.
    1. Deaktivieren Sie auf der Registerkarte **Preise** im Inforegister **Handelsvereinbarungsauswertung** das Kontrollkästchen **Manuelle Eingabe**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Prospect-to-cash in Dual-Write](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]