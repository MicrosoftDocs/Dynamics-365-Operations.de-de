---
title: Einen Lagerort einrichten
description: In diesem Thema wird beschrieben, wie Sie einen Lagerort für die Verwendung mit einem neuen Kanal in Microsoft Dynamics 365 Commerce einrichten.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1fce2570e1b0cc334fc0e92e5e83c53a4566b4a4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345983"
---
# <a name="warehouse-set-up"></a>Lagerort einrichten

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie einen Lagerort für die Verwendung mit einem neuen Kanal in Microsoft Dynamics 365 Commerce einrichten.

Jedem Commerce-Kanal muss ein konfigurierter Lagerort zugeordnet sein. Die folgenden Verfahren bieten die Mindestkonfiguration, die zum Einrichten eines Lagerorts für einen Commerce-Kanal erforderlich ist. Weitere Informationen zur Einrichtung des Lagerorts finden Sie in der [Übersicht über die Lagerortverwaltung](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Standort eines Lagerorts konfigurieren

Vor dem Einrichten eines Lagerorts müssen Sie den Standort eines Lagerorts konfigurieren.

Gehen Sie folgendermaßen vor, um den Standort eines Lagerorts zu konfigurieren.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Standorte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Standort** einen Wert ein.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Legen Sie im Abschnitt **Allgemeines** die entsprechende **Zeitzone** fest.
1. Geben Sie im Abschnitt **Adressen** eine Adresse ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt ein Beispiel für den Standort eines Lagerorts.

![Beispiel: Standort eines Lagerorts.](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Einen Lagerort einrichten

Um einen Lagerort einzurichten, gehen Sie folgendermaßen vor:

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Lagerorte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Lagerort** einen Wert ein.  Wenn es sich um eine 1:1-Zuordnung zu einem Geschäft handelt, sollten Sie den Namen des Geschäfts oder den Namen eines regionalen Vertriebszentrums verwenden.
1. Geben Sie im Feld **Name** einen Wert ein.
1. In der Dropdown-Liste **Standort** wählen Sie den zuvor erstellten Standort des Lagerorts aus.
1. Wählen Sie im Feld **Typ** die Option **Standard**.
    - Wenn Sie ein **Quarantänelager** einrichten möchten, führen Sie zunächst die folgenden Schritte aus, um einen zusätzlichen Lagerort zu erstellen, in dem der **Typ** auf **Quarantäne** eingestellt ist.
    - Wenn Sie ein **Transitlager** einrichten möchten, führen Sie zunächst die folgenden Schritte aus, um einen zusätzlichen Lagerort zu erstellen, in dem der **Typ** auf **Transit** eingestellt ist.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="set-up-inventory-aisles"></a>Lagergänge einrichten

Gehen Sie zum Einrichten von Lagergängen folgendermaßen vor:

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Standorteinrichtung \> Lagergänge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. In der Dropdown-Liste **Lagerort** wählen Sie den zuvor erstellten Lagerort aus.
1. Geben Sie im Feld **Gang** einen Namen ein (beispielsweise „Def”).
1. Geben Sie im Feld **Name** einen Namen ein (beispielsweise „Standardgang”).
1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="set-up-warehouse-inventory-locations"></a>Standorte für Lagerort-Lagerplätze einrichten

Führen Sie die folgenden Schritte aus, um Lagerorte für Standard-, beschädigte und zurückgegebene Bestände einzurichten.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Lagerorte**.
1. Wählen Sie den Lagerort aus, den Sie zuvor erstellt haben.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Aktionsbereich **Lagerort** und dann **Standort des Lagerorts** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus. Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.
    1. Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein. 
    1. Stellen Sie **Manuelles Update** auf **Ja**
    1. Geben Sie im Feld **Standort** den Namen des Lagerorts ein.
    1. Wählen Sie im Aktionsbereich **Speichern** aus.
 1. Wählen Sie im Aktivitätsbereich **Neu** aus.  Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.
    1. Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein.  
    1. Stellen Sie **Manuelles Update** auf **Ja**
    1. Geben Sie im Feld **Lagerort** „Beschädigt“ ein.
    1. Wählen Sie im Aktionsbereich **Speichern** aus.
 1. Wählen Sie im Aktivitätsbereich **Neu** aus.  Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.
    1. Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein. 
    1. Stellen Sie **Manuelles Update** auf **Ja**
    1. Geben Sie im Feld **Lagerort** „Retouren“ ein.
    1. Wählen Sie im Aktionsbereich **Speichern** aus.
    
Die folgende Abbildung zeigt eine Einrichtung eines Lagerort-Standorts in San Francisco.

![Beispiel für die Einrichtung des Standorts eines Lagerorts.](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Vollständige Einrichtung eines Lagerorts

Führen Sie zum Abschließen der Einrichtung eines Lagerorts die folgenden Schritte aus.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Lagerorte**.
1. Wählen Sie den Lagerort aus, den Sie zuvor erstellt haben.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Unter **Bestands- und Lagerortverwaltung**:
    1. Stellen Sie **Standard-Zugangslagerplatz** auf den oben erstellten Standardstandort.
    1. Wählen Sie **Standard-Abgangslagerplatz** als den oben erstellten Standardstandort.
1. Geben Sie im Abschnitt **Adressen** eine Lageradresse ein.
1. Im Abschnitt **Einzelhandel**: 
    1. Geben Sie im **Standard-Rückgabeort** den zuvor erstellten Rückgabeort ein.
    1. Stellen Sie **Geschäft** auf **Ja**.
    1. Legen Sie **Gewicht** auf **1.00** fest. 
    1. Geben Sie im Feld **Lagerdimensionen** den zuvor erstellten Standardlagerplatz ein.
1. Setzen Sie im Abschnitt **Lagerort** die Option **Negativbestand** auf **Ja**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt Details für einen konfigurierten Lagerort.

![Beispiel für einen konfigurierten Lagerort.](media/warehouse-sample.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Lagerortverwaltung](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Übersicht über Kanäle](channels-overview.md)

[Voraussetzungen der Kanaleinrichtung](channels-prerequisites.md)

[Einen Retail Channel einrichten](channel-setup-retail.md)
    
[Einen Onlinekanal einrichten](channel-setup-online.md)

[Einen Callcenterkanal einrichten](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
