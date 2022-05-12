---
title: Leasingerfassungsnamen einrichten
description: In diesem Thema wird erläutert, wie Sie Namen von Leasingerfassungen definieren. Namen von Leasingerfassungen geben die Erfassungen an, in die Einträge gebucht werden, die aus dem Anlagenleasing stammen.
author: moaamer
ms.date: 12/03/2021
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
ms.openlocfilehash: a92461e742f1675e4cfda89e6c80c5b087ff5bfb
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644896"
---
# <a name="set-up-lease-journal-names"></a>Leasingerfassungsnamen einrichten

[!include [banner](../includes/banner.md)]


Namen von Leasingerfassungen geben die Erfassungen an, in die Transaktionen der Anlagenleasing gebucht werden. Nur Erfassungsnamen, die dem **Anlagenleasing**-Erfassungstyp zugeordnet sind, werden in den **Erstmalige Erfassung**- und **Name der monatlichen Erfassung**-Feldern auf der **Parameter für das Anlagenleasing**-Seite angezeigt. Nur der **Kreditorenechnungserfassung**-Erfassungstyp kann dem **Name der Rechnungserfassung**-Feld zugeordnet werden.

Das System sperrt bestimmte Finanzfelder für die Bearbeitung, um Abweichungen zwischen den Transaktionen und den Zeitplänen zu verhindern. Einige Felder, die gesperrt sind, sind: **Konto**, **Beträge**, **Finanzielle Dimensionen**, **Währung** und **Transaktionstyp**. Außerdem können Sie in den Journaleinträgen des Anlagenleasings keine Zeilen für Journaleinträge hinzufügen oder löschen, da dies zu Abweichungen zwischen den Zeitplänen und den Transaktionen führen kann.


Führen Sie die folgenden Schritte aus, um die Namen der Leasingerfassung zu konfigurieren.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Anlagenleasing-Parameter**.
2. Auf der **Allgemeines**-Registerkarte im **Name der Erfassung der erstmaligen Erfassung**-Feld wählen Sie eine Erfassung aus. Alle Journaleinträge der erstmaligen Erfassung werden unter diesem Erfassungsnamen gebucht.
3. Wählen Sie im Feld **Rechnungserfassungsname** eine Erfassung aus. Wenn die **An den Kreditor bezahlen**-Option für das Leasingbuch auf **Ja** festgelegt ist, werden Rechnungen für Miet- und Ausgabenzahlungen unter diesem Erfassungsnamen gebucht.
4. Wählen Sie im Feld **Leasingerfassungsname** eine Erfassung aus. Alle Abschreibungs-, Zins- und kurzfristigen Umgliederungseinträge werden unter diesem Erfassungsnamen gebucht. Wenn die **An den Kreditor bezahlen**-Option für das Leasingbuch auf **Nein** festgelegt ist, werden Einträge für Miet- und Ausgabenzahlungen auch unter diesem Erfassungsnamen gebucht.
5. Wählen Sie im Feld **Name der Leasingänderungserfassung** eine Erfassung aus. Leasinganpassungs-, Kündigungs- und Wertminderungstransaktionen werden auf diesen Erfassungsnamen gebucht. Dem ausgewählten Erfassungsnamen sollte kein Workflow oder keine Genehmigung zugewiesen sein. Wenn der Name der Leasingänderungserfassung nicht definiert ist, werden Leasinganpassungs-, Kündigungs- und Wertminderungstransaktionen an den Erfassungsnamen gebucht, der im Feld **Leasingerfassungsname** ausgewählt ist. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
