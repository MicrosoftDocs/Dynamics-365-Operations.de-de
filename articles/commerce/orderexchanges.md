---
title: Konfigurieren und Verarbeiten eines Austausch für eine Rücklieferung
description: In diesem Thema wird erläutert, wie Sie einen Austausch für eine Rücklieferung im Dynamics 365 Commerce konfigurieren.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6d7688e78a375bc262b1156c5439c0fff7cd1f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459086"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Konfigurieren und Verarbeiten eines Austausch für eine Rücklieferung

[!include [banner](includes/banner.md)]

In älteren Versionen von Dynamics 365 Commerce werden Rücklieferungen für Kundenaufträge mithilfe des Rücklieferungsdokuments in der Zentralverwaltung verarbeitet. Doch das Rücklieferungsdokument kann auch ausschließlich für die Bearbeitung von Produkten verwendet werden, die zurückgegeben werden. Die zurückgelieferten Produkte werden durch eine negative Menge in den Rücklieferungspositionen angegeben. Dagegen wird im Umsatz eine positive Menge angegeben. Das Rücklieferungsdokument unterstützt jedoch keine positiven Mengen. Aufgrund dieser Einschränkung wurden in früheren Versionen der App keine Szenarien unterstützt, in denen Produktumtauschaktivitäten mithilfe des Rücklieferungsdokuments durchgeführt wurden.

Allerdings wurden Funktionen hinzugefügt, die Szenarien unterstützen, in denen der Umtausch mithilfe von Rücklieferungen erfolgt. Commerce verwendet nun das Auftragsdokument anstelle des Rücklieferungsdokuments, um die Transaktionsarten zu verarbeiten.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Konfigurieren von Commerce für die Unterstützung von Rücklieferungen

Gehen Sie folgendermaßen vor, um das System so zu konfigurieren, dass Umtausch mit Rücklieferungen unterstützt wird.

1. Gehen Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**. Legen Sie im Inforegister **Kundenaufträge** die Option **Rücklieferungen als Aufträge verarbeiten** auf **Ja** fest.
2. Führen Sie den Auftrag **Globaler Konfigurationsverteilungszeitplan** (**1110**) aus.

## <a name="make-an-exchange"></a>Durchführen eines Umtauschs

Wenn das System wie im vorigen Abschnitt beschrieben konfiguriert ist, wählt der Verkaufsstellen (POS)-Benutzer immer noch einen Auftrag oder eine Verkaufsrechnung aus, um eine Rücklieferung zu verarbeiten. Dies hat sich seit den vorherigen Versionen der App nicht geändert. Wenn jedoch die Rückgabeartikel in den Einkaufskorb gelegt wurden, kann der Benutzer dem Einkaufskorb neue Auftragspositionen hinzuzufügen.

Für diese neuen Auftragspositionen muss der Benutzer alle Attribute definieren, die für die Verarbeitung von Kundenauftragsposition erforderlich sind. Diese Attribute enthalten die Lieferarten und den Erfüllungsstandort. Die Zahlung, die für die Transaktion fällig ist, ist der Nettobetrag der Rücklieferungspositionen und Auftragspositionen. Erfolgt die Zahlung für die Transaktion, wird die Rücklieferung in der Zentralverwaltung als Auftragsdokument gebucht, und das System erstellt sofort eine Rechnung für die Rückgabepositionen.

Zur besseren Übersicht über die unterschiedlichen Mengen für den Einkaufskorb wurden dem Einkaufskorb drei neue Betragsfelder hinzugefügt. Mithilfe des Bildschirmdesigners können Sie diese neuen Felder in der POS-Benutzeroberfläche (UI) bereitstellen.

- **Einzahlung angewendet** – Der Einzahlungsbetrag, der in einer Transaktion verwendet wird, wenn der Benutzer einen Kundenauftrag auswählt. Wenn die Einzahlung nicht überschrieben wird und eine Einzahlung von 10 Prozent konfiguriert wurde, beläuft sich der Betrag in diesem Feld auf 90 Prozent des Gesamtbetrags des Kundenauftrags.
- **Betrag ausführen** – Der Gesamtbetrag für Positionen, in denen die Lieferart bei der Erstellung oder Bearbeitung des Kundenauftrags oder bei einem Umtausch eines Kundenauftrags auf **Ausführen** festgelegt wurde. Der Betrag in diesem Feld enthält die Steuern und Belastungen.
- **Rückgabebetrag** – Der Gesamtbetrag für Positionen, die negative Mengen für den Kundenauftragsumtausch haben. Der Betrag in diesem Feld enthält die Steuern und Belastungen.
