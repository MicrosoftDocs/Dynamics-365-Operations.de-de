---
title: Leasingerfassungsnamen einrichten
description: In diesem Thema wird erläutert, wie Sie Namen von Leasingerfassungen definieren. Namen von Leasingerfassungen geben die Erfassungen an, in die Einträge gebucht werden, die aus dem Anlagenleasing stammen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880885"
---
# <a name="set-up-lease-journal-names"></a>Leasingerfassungsnamen einrichten

[!include [banner](../includes/banner.md)]

Namen von Leasingerfassungen geben die Erfassungen an, in die Transaktionen der Anlagenleasing gebucht werden. Nur Erfassungsnamen, die dem **Anlagenleasing**-Erfassungstyp zugeordnet sind, werden in den **Erstmalige Erfassung**- und **Name der monatlichen Erfassung**-Feldern auf der **Parameter für das Anlagenleasing**-Seite angezeigt. Nur der **Kreditorenechnungserfassung**-Erfassungstyp kann dem **Name der Rechnungserfassung**-Feld zugeordnet werden.

Führen Sie die folgenden Schritte aus, um die Namen der Leasingerfassung zu konfigurieren.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Anlagenleasing-Parameter**.
2. Auf der **Allgemeines**-Registerkarte im **Name der Erfassung der erstmaligen Erfassung**-Feld wählen Sie eine Erfassung aus. Alle Journaleinträge der erstmaligen Erfassung werden unter diesem Erfassungsnamen gebucht.
3. Wählen Sie im Feld **Rechnungserfassungsname** eine Erfassung aus. Wenn die **An den Kreditor bezahlen**-Option für das Leasingbuch auf **Ja** festgelegt ist, werden Rechnungen für Miet- und Ausgabenzahlungen unter diesem Erfassungsnamen gebucht.
4. Wählen Sie im Feld **Leasingerfassungsname** eine Erfassung aus. Alle Abschreibungs-, Zins- und kurzfristigen Umgliederungseinträge werden unter diesem Erfassungsnamen gebucht. Wenn die **An den Kreditor bezahlen**-Option für das Leasingbuch auf **Nein** festgelegt ist, werden Einträge für Miet- und Ausgabenzahlungen auch unter diesem Erfassungsnamen gebucht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
