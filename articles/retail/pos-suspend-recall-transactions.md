---
title: Transaktionen in der Verkaufsstelle (POS) anhalten und fortsetzen
description: In diesem Thema wird erläutert, wie Benutzer laufende Transaktionen aussetzen und sie später oder in einem anderen Register mit Dynamics 365 Retail wiederaufnehmen können.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: efab3b793eb15e7feffb569492b5c36a2e9d6ec0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025275"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a>Transaktionen in der Verkaufsstelle (POS) anhalten und fortsetzen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Benutzer von Verkaufsstelle (POS) können laufende Buchungen unterbrechen und sie später fortsetzen oder in einem anderen Register fortsetzen. Buchungen erfolgen häufig unterbrochen, um ein Register für eine andere Aufgabe schnell freizugeben, ohne einen Status für die aktuelle Buchung zu verlieren. Beispielsweis beginnt ein Shopangestellter eine Kundentransaktion auf einem mobilen Gerät aber muss diese an einer Kasste mit Geldlade ausführen. In diesem Fall muss der Shop die Buchung im mobilen Gerät gestoppt werden und diese dann auf einer Kasse wieder aufgerufen werden.

## <a name="configure-suspend-and-resume-functionality"></a>Funktionen unterbrechen und wieder aufnehmen konfigurieren

### <a name="pos-operations"></a>POS-Vorgänge

Zwei [POS-Vorgängen](pos-operations.md) können die POS-Support Szenarien unterbrechen und fortsetzen. Sie können diese Arbeitsgänge auf dem [Schaltflächenraster](pos-screen-layouts.md) der Buchungsseite oder der Willkommensseite zuweisen.

- 503: Transaktion aussetzen
- 504: Transaktion zurückrufen

### <a name="receipt-template"></a>Zugangsvorlage

Der POS kann so konfiguriert werden, dass er einen gedruckten Beleg generiert, wenn eine Buchung unterbroche wird. Dieser Beleg kann dann verwendet werden, um die Buchung zu erkennen und später zurückzurufen.

Um dem POS die Möglichkeit zu geben, einen Beleg zu drucken, müssen Sie das Belegformat **Transaktion unterbrechen** dem Shopprofil zuweisen. Sie können das Belegformat entwerfen, dass bestimmte Details zur Transaktion enthält. Beispielsweise kann das Format eines Strichcodes enthalten, um das Scannen zu unterstützen.

### <a name="receipt-numbering"></a>Bonnummerierung

Wei bei POS-Buchungs-Typen, die für einen gedruckten Beleg generiert wurden, können Sie einen Nummernkreis für unterbrochene Buchungen im Abschnitt **Belegnummerierung** des Funktionsprofils der Filiale definieren.

### <a name="void-when-closing-shift"></a>Stornieren, wenn Schicht geschlossen wird

Sie können **Stornieren Sie, wenn Schicht endet** Option verwenden, um festzulegen, dass Benutzer entweder alle unterbrochenen Buchungen unterbrechen oder stornieren, bevor sie ihre Schicht schließen. Während dem **Schicht schließen** Arbeitsgangs forder der POS Benutzer auf, unterbrochene Buchungen anzuzeigen oder zu stornieren.

## <a name="suspend-and-resume-a-transaction"></a>Transaktionen anhalten und fortsetzen

### <a name="suspend-a-transaction"></a>Transaktion aussetzen

Benutzer, die über die entsprechenden Rechte verfügen und die eingeben Bildschirmlayout haben, das den Arbeitsgang **Buchung aussetzen** enthält, können eine Buchung fortsetzen, damit sie an einer anderen Kasse später zurückgerufen werden kann.

Buchungen können unterbrochen werden, wenn sie **nicht** die folgenden Rückvergütungstypen enthalten:

- Aktive Zahlungspositionen
- Geschenkkartepositionen (entweder eine Geschenkkarte ausstellen oder Geschenkkartensaldo hinzufügen)

Eine unterbrochene Buchung hat keine Verkaufsinformations- oder Bestandsverfügbarkeit-Informationen für den Shop.

### <a name="resume-a-suspended-transaction"></a>Ruft eine ausgesetzte Transaktion zurück.

Unterbrochene Transaktionen können in denselben Shop von jedem Benutzer erneut aufgerufen und fortgesetzt werden, der über die entsprechenden Rechte hat und der ebenfalls ein Layout, hat das den Arbeitsgang **Transaktlion zurückrufen** umfasst.

Um schnell und einfach eine unterbrochene Buchung aufzurufen, scannen Sie den Strichcode auf dem gedruckten Beleg, während Sie die Liste der Buchungen vom Arbeitsgang anzeigen **Buchung zurückrufen**.

### <a name="considerations-for-offline-mode"></a>Betrachtungen für Offlinemodus

- Buchungen, die unterbrochen wurden, während der POS im Online-Modus ist, kann nicht im Offline-Modus fortgesetzt werden, weil die Daten nicht mit der Offline-Datenbank synchronisiert werden.
- Wenn Sie eine Buchung unterbrechen, während der POS im Offline-Modus ist, können Sie sie im Offline-Modus zurückrufen, vorausgesetzt, dass der Betrag vom POS nicht in rechnerabhängigem Betrieb geändert wurde, seit die Buchung unterbrochen wurde. Wenn der POS wieder im Online-Modus ist, werden die Daten zu unterbrochene Buchungen verschoben udn von der Offline-Datenbank entfernt. Daher können Sie die Transaktionen nur im Online-Modus fortsetzen. Wenn Sie vom POS wieder in den Offline-Modus wechseln, sind Sie nicht mehr in der Lage, die unterbrochene Transaktionen fortzusetzen, da sie bereits offline aus der Datenbank entfernt wurden.

### <a name="void-a-suspended-transaction"></a>Ausgesetzte Buchung stornieren

Sie können unterbrochene Buchungen stornieren, indem Sie die Buchung zuerst erneut aufrufen und dann **Transaktion stornieren** ausführen oder die Buchung in der Liste **Transaktion zurückrufen** auswählen und **Storniert** auf der App-Leiste auswählen. Alternativ kann der Shop konfiguriert werden, damit Benutzer aufgefordert werden, unterbrochene Transaktionen zu stornieren, wenn sie ihre Schicht schließen.
