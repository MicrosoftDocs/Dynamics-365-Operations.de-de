---
title: Die Registerkarte „Aktive Preise“ der Seite „Artikelpreis“ enthält kein „Startdatum“
description: Die Registerkarte „Aktive Preise“ der Seite „Artikelpreis“ enthält kein „Startdatum“.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc0071bc508fc1b2fcfa5071f0756434641b7e6f872308ed4febb0cb34d37840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730129"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Die Registerkarte „Aktive Preise“ der Seite „Artikelpreis“ enthält kein „Startdatum“

KB-Nummer: 4613548

## <a name="symptoms"></a>Symptome

Die Registerkarte **Aktive Preise** der Seite **Artikelpreis** enthält kein **Startdatum**.

## <a name="resolution"></a>Lösung

Der Wert **Startdatum** (Gültigkeitsdatum), das für den ausstehenden Preis festgesetzt ist, wird nicht auf den aktiven Preis übertragen.

Bei der Eingabe erhält ein Artikelkostendatensatz zunächst einen Status *Ausstehend* sowie ein gewünschtes Gültigkeitsdatum. Bei Aktivierung des Artikelkostendatensatzes wird der Status zu *Aktiv* und das Gültigkeitsdatum in das Aktivierungsdatum aktualisiert. Daher ist das Aktivierungsdatum des aktiven Preises immer das tatsächliche Datum der Aktivierung.

Weitere Informationen finden Sie unter [Nachkalkulationsversionen – Übersicht](../../cost-management/costing-versions.md).
