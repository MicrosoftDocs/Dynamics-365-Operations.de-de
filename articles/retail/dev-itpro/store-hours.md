---
title: Erstellen und Aktualisieren von Geschäftszeiten
description: In diesem Thema wird beschrieben, wie Sie Geschäftszeiten in Retail Headquarters anlegen und aktualisieren.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 811d499a3eb8133e5ffd29bb4ae6a0c57708accd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023441"
---
# <a name="create-and-update-store-hours"></a>Erstellen und Aktualisieren von Geschäftszeiten

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Übersicht

Von einem einzigen Ort aus können Einzelhändler die Geschäftszeiten für verschiedene Filialen über geografische Regionen hinweg anlegen, pflegen und verwalten. Die Geschäftszeiten können dann an POS-Terminals angezeigt werden. Auf diese Weise können die Kassierer die Ladenöffnungszeiten mit den Kunden teilen und den Käufern, die an Beständen in anderen Filialen interessiert sind, besser helfen. Die Geschäftszeiten können auch auf Belegen gedruckt werden, falls der Kunde später in die Filiale zurückkehren möchte.

Mehrere Geschäftszeiten können über verschiedene Kanäle konfiguriert werden. Zu diesen Kanälen gehören Filialen, Call Center, mobile Geräte und E-Commerce-Sites.

Wenn ein Kunde einen Abholauftrag für eine andere Filiale hat, kann der Kassierer einen Termin auswählen, an dem die Abholung in dieser Filiale verfügbar sein wird. Das Store Lookup liefert einen Verweis auf die Daten und Zeiten des Ladens. Der Kassierer kann ein Datum und einen Ort auswählen und einen Abholbeleg mit den Geschäftszeiten ausdrucken.

Diese Funktionalität ist in Microsoft Dynamics 365 Retail ab Version 8.1.2 verfügbar.

## <a name="configure-store-hours"></a>Konfigurieren der Geschäftszeiten

Führen Sie diese Schritte aus, um die Geschäftszeiten zu konfigurieren.

1. Gehen Sie zu **Einzelhandel** \> **Kanaleinrichtung** \> **Standzeiten**.
2. Wählen Sie **Neu**, um eine neue Geschäftszeitenvorlage zu erstellen. Um eine vorhandene Vorlage zu verwenden, wählen Sie die Vorlage im linken Bereich aus.
3. Definieren Sie im Dialogfenster **Hinzufügen Bereich** den Datumsbereich, die Geschäftszeiten und eventuell erforderliche Feiertage.

    - Wenn sich die Geschäftszeiten nicht ändern, wählen Sie **Nie endet** im Feld **Enddatum**.
    - Wenn die Geschäftszeiten für einen bestimmten Monat, eine bestimmte Woche oder einen bestimmten Tag gelten, setzen Sie die entsprechenden Daten in den Feldern **Startdatum** und **Enddatum**.

    > [!NOTE]
    > Sie können mehrere Vorlagen erstellen, deren Start- und Enddatum sich überschneiden. So können Sie z.B. für Filialen in verschiedenen Zeitzonen Geschäftszeiten definieren.

    ![Dialogbox Hinzufügen Bereich](../dev-itpro/media/Storehours1.png "Dialogbox Hinzufügen Bereich")

4. Ordnen Sie die Ladenöffnungsvorlage den Filialen zu, in denen sie verwendet werden soll. Wählen Sie im Dialogfenster **Organisationsknoten auswählen** die Filialen, Regionen und Organisationen aus, denen die Vorlage zugeordnet werden soll.

    - Jeder Filiale kann nur eine Ladenöffnungsvorlage zugeordnet werden.
    - Verwenden Sie die Pfeiltasten, um Filialen, Regionen oder Organisationen auszuwählen. Der Kalender steht den Filialen oder Filialgruppen zur Verfügung und ist am POS als Referenz sichtbar.

    ![Dialogfeld Organisationsknoten auswählen](../dev-itpro/media/Storehours2.png "Dialogfeld Organisationsknoten auswählen")

5. Führen Sie auf der Seite **Verteilungsplan** die Jobs **1070** und **1090** aus, um die Geschäftszeiten für die Kasse verfügbar zu machen.

## <a name="add-store-hours-to-printed-receipts"></a>Hinzufügen von Geschäftszeiten zu gedruckten Belegen

Führen Sie diese Schritte aus, um den gedruckten Kassenbelegen Geschäftszeiten hinzuzufügen.

1. Öffnen Sie den Beleg-Designer.
2. Wählen Sie **Fußzeile** in der linken unteren Ecke.
3. Ziehen Sie das Element **Geschäftszeiten** aus dem linken Bereich in die Fußzeile am unteren Rand der Belegablage.
4. Sie können die Standardbeschriftung auf dem Element **Geschäftszeiten** beliebig bearbeiten.
5. Speichern Sie den Beleg und schließen Sie den Belegdesigner.
6. Führen Sie auf der Seite **Verteilungsplan** die Jobs **1070** und **1090** aus.
7. Melden Sie sich am POS an.
8. Schließen Sie einen Verkauf ab und wählen Sie, um eine Quittung zu drucken.

Die Bons enthalten nun auch die Geschäftszeiten. Wenn in der Vorlage Feiertage enthalten waren, werden diese auf dem Beleg angezeigt.

![Belegbeispiel](../dev-itpro/media/Storehours3.png "Belegbeispiel")
