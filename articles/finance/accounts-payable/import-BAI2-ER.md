---
title: Erweiterten Bankabstimmungsimport mithilfe der elektronischen Berichterstellung einrichten
description: In diesem Thema wird erläutert, wie Sie die elektronische Berichterstellung verwenden, um den erweiterten Bankabstimmungsimportprozess für BAI2-Auszüge einzurichten.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544501"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Erweiterten Bankabstimmungsimport mithilfe der elektronischen Berichterstellung einrichten

[!include [banner](../includes/banner.md)]

Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 Finance automatisch mit Bankbuchungen abstimmen. In diesem Thema wird die Einrichtung der Importfunktion für Ihre BAI2-Bankauszüge erläutert.

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfiguration der elektronischen Berichterstellung einrichten

1. Wechseln Sie zu **Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Auf der Kachel für den Konfigurationsanbieter **Microsoft** wählen Sie **Repositorys** aus.
3. Wählen Sie **Global** und dann **Öffnen** aus.
4. Wenn eine Verbindung zum Repository hergestellt werden muss, wählen Sie den blauen Link im Dialogfeld aus.
5. Suchen Sie in der Konfigurationsliste nach **Kontoauszugsmodell \> Kontoauszugsmodell von BAI2**.
6. Wählen Sie das **BAI2**-Format aus.
7. Wählen Sie im Inforegister **Versionen** die neueste Version, und wählen Sie dann **Importieren** aus.

## <a name="set-up-the-bank-statement-format"></a>Bankauszugsformat einrichten

1. Gehen Sie zu **Barmittel und Bankverwaltung \> Einrichtung \> Einrichtung der erweiterten Bankabstimmung \> Bankauszugsformat**.
2. Wählen Sie **Neu** aus.
3. Legen Sie die Felder **Auszugsformat** und **Name** fest.
4. Aktivieren Sie das Kontrollkästchen **Allgemeines elektronisches Importformat**.
5. Legen Sie das Feld **Formatkonfiguration importieren** auf das Format **BAI2** fest.

## <a name="set-up-the-bank-account"></a>Bankkonto einrichten

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Öffnen Sie das Bankkonto.
3. Legen Sie auf dem Inforegister **Abstimmung** die Option **Erweiterte Bankabstimmung** auf **Ja** fest.
4. Legen Sie im Feld **Auszugsformat** das Format **BAI2** fest, das Sie zuvor erstellt haben.

## <a name="import-the-bank-statement"></a>Bankauszug importieren

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankauszug für Abstimmung \> Bankauszüge**.
2. Wählen Sie oben auf der Seite **Kontoauszüge** die Option **Auszug importieren** aus.
3. Legen Sie das Feld **Bankkonto** auf das Bankkonto im Auszug fest.
4. Legen Sie im Feld **Auszugsformat** das Format **BAI2** fest, das Sie zuvor erstellt haben.
5. Wählen Sie **Durchsuchen** und die Datei **BAI** aus.
6. Wählen Sie **Hochladen** aus.
7. Wählen Sie **OK** aus, um die ausgewählte Datei zu importieren.
