---
title: Falsch berechnete Steuern auf Onlinebestellungen
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Steuern auf Onlinebestellungen falsch berechnet werden oder die Steuergruppe in der Verkaufsposition nicht richtig festgelegt ist.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021102"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Falsch berechnete Steuern auf Onlinebestellungen

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Steuern auf Onlinebestellungen falsch berechnet werden oder die Steuergruppe in der Verkaufsposition nicht richtig festgelegt ist.

## <a name="description"></a>Beschreibung

Wenn ein E-Commerce-Auftrag aufgegeben wird, werden die Steuern falsch berechnet oder die Steuergruppe in der Verkaufsposition ist falsch festgelegt.

## <a name="resolution"></a>Lösung

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Die Mehrwertsteuer für ein Einzelhandelsgeschäft in der Commerce-Zentralverwaltung konfigurieren

Befolgen Sie diese Schritte, um die Mehrwertsteuer für ein Einzelhandelsgeschäft in der Commerce-Zentralverwaltung zu konfigurieren:

1. Rufen Sie **Retail und Commerce \> Kanäle \> Alle Shops** auf.
1. Wählen Sie das Geschäft aus, für das die Mehrwertsteuer konfiguriert werden soll.
1. Konfigurieren Sie im Inforegister **Allgemein** des Abschnitts **Mehrwertsteuer** die Mehrwertsteuerinformationen für den Shop.

> [!NOTE]
> Bei der Produktabholung aus einem Shop stammt die Steuergruppe von dem Shop, der für die Abholung ausgewählt wurde. Weitere Informationen finden Sie unter [Festlegen anderer Steueroptionen für Shops](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Die Mehrwertsteuer für eine Debitorenadresse in der Commerce-Zentralverwaltung konfigurieren

Befolgen Sie diese Schritte, um die Mehrwertsteuer für eine Debitorenadresse in der Commerce-Zentralverwaltung zu konfigurieren:

1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Wählen Sie den Debitor aus, für den die Mehrwertsteuer konfiguriert werden soll.
1. Wählen Sie im Inforegister **Adressen** die Adresse aus, für die die Mehrwertsteuer konfiguriert werden soll. Wählen Sie **Weitere Optionen** und anschließend **Erweitert** aus.
1. Wählen Sie auf der Registerkarte **Allgemein** die Option **Steuergruppe** aus.
1. Wählen Sie im Feld **Mehrwertsteuer** den entsprechenden Wert aus.

> [!NOTE]
> Bei mehrwertsteuerpflichtigem Versand der Debitorenadresse bestimmt die Lieferadresse der Position die Steuergruppe für die Position. Wenn der Debitor an eine vorhandene Adresse versendet, für die bereits eine Steuergruppe konfiguriert ist, wird die vorhandene Steuergruppe verwendet. Standardmäßig haben Adressen beim Erstellen keine Steuergruppe.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Allgemeine Mehrwertsteuergruppen in der Commerce-Zentralverwaltung konfigurieren

Befolgen Sie diese Schritte, um allgemeine Mehrwertsteuergruppen in der Commerce-Zentralverwaltung zu konfigurieren.

1. Rufen Sie **Steuer \> Indirekte Steuern \> Mehrwertsteuer \> Mehrwertsteuergruppen** auf.
1. Wählen Sie in der linken Navigation die zu konfigurierende Steuergruppe aus.
1. Konfigurieren Sie im Inforegister **Auf Adresse des Einzelhandels bezogene Steuer** die Steuern für die Mehrwertsteuergruppe.

> [!NOTE]
> Bei Versand ohne Mehrwertsteuer der Debitorenadresse bestimmen die Lieferadresse der Position sowie die adressbezogenen Steuern, die für die Steuergruppe konfiguriert sind, die Steuergruppe. Weitere Informationen finden Sie unter [Steuern für Online-Shops auf der Grundlage des Ziels einrichten](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Mehrwertsteuer für Onlinebestellungen konfigurieren](../sales-tax-config.md)