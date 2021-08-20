---
title: Sie können aus Abstimmungsgründen nur das Hauptkonto als Habenkonto hinzufügen
description: Wenn Sie in der Transportverwaltung einen Abstimmungsgrund einrichten, können Sie nur das Hauptkonto als Habenkonto hinzufügen.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750881"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Sie können aus Abstimmungsgründen nur das Hauptkonto als Habenkonto hinzufügen

KB-Nummer: 4603538

## <a name="symptoms"></a>Symptome

Wenn Sie in der Transportverwaltung einen Abstimmungsgrund einrichten, können Sie nur das Hauptkonto als Habenkonto hinzufügen. Sie können keine Kostenstelle oder eine andere Dimension als Habenkonto hinzufügen. Über das Sollkonto können Sie jedoch andere Dimensionen auswählen.

## <a name="resolution"></a>Lösung

Wenn die Abstimmung nicht zur Bezahlung des Kreditors, sondern zur Gutschrift auf ein bestimmtes Hauptkonto durchgeführt wird, können Sie beim Einrichten des Abstimmungsgrunds keine finanzielle Dimension für das Habenkonto auswählen.

Wenn für die Kontostruktur ein bestimmter Wert für die Finanzdimension des Habenhauptkontos erforderlich ist, kann die resultierende Kreditorenerfassung nicht automatisch gebucht werden, da der Wert für die Finanzdimension fehlt. Daher müssen Sie zuerst das Habenkonto manuell angeben, indem Sie die Seite **Rechnungserfassung** verwenden.

Da für das Habenkonto ein Dimensionswert erforderlich ist, kann das Kreditoenrechnungserfassung nicht automatisch gebucht werden. Sie müssen sie manuell buchen, nachdem Sie den Dimensionswert manuell zum Hauptkonto für die Kreditlinie hinzugefügt haben.
