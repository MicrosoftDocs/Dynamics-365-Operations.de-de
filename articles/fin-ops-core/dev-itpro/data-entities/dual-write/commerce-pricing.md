---
title: Dynamics 365 Commerce-Preisgestaltungsmodul mit Dynamics 365 Sales verwenden
description: In diesem Thema wird die Verwendung des Microsoft Dynamics 365 Commerce-Preisgestaltungsmoduls zur Erstellung von Verkaufsangeboten in Dynamics 365 Sales beschrieben.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: 70282eb7856ae6b37e885eac2daf49efd971087d7c204af4b653263edb0d8fc4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716069"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce-Preisgestaltungsmodul mit Dynamics 365 Sales verwenden

[!include [banner](../../includes/banner.md)]

In diesem Thema wird die Verwendung des Microsoft Dynamics 365 Commerce-Preisgestaltungsmoduls zur Erstellung von Verkaufsangeboten in Dynamics 365 Sales beschrieben.

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