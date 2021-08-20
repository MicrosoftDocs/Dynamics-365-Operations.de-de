---
title: Mehrere Lagerbuchungen für Chargennummern, wenn „Bei physischer Aktualisierung“ deaktiviert ist
description: Nachdem Sie eine Bestellposition für Artikel angepasst haben, für die die Option „Bei physischer Aktualisierung“ der Chargennummerngruppe auf „Nein“ gesetzt ist, werden mehrere Bestandsbuchungen erstellt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b8aef8835e90b7437bb7833c13c3d287d4ca836bf1fefc01bfeafef1c93329bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768593"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Mehrere Lagerbuchungen für Chargennummern, wenn „Bei physischer Aktualisierung“ deaktiviert ist

KB-Nummer: 4613390

## <a name="symptoms"></a>Symptome

Nachdem Sie eine Bestellposition für Artikel angepasst haben, für die die Option **Bei physischer Aktualisierung** der Chargennummerngruppe auf *Nein* gesetzt ist, werden mehrere Bestandsbuchungen erstellt.

Wenn Sie einen Artikel erstellen, in dem die Option **Bei physischer Aktualisierung** der Chargennummerngruppe auf *Nein* gesetzt ist, erstellt das System automatisch eine neue Chargennummer, wenn Sie eine Bestellpostenmenge ändern und die Bestellseite speichern.

## <a name="resolution"></a>Lösung

Die Einstellung **Bei physischer Aktualisierung** für Chargennummerngruppen funktioniert folgendermaßen:

- Wenn die Option auf *Ja* gesetzt ist, werden neue Chargennummern erst nach einer physischen Aktualisierung erstellt (z. B. wenn Artikel versendet oder empfangen werden).
- Wenn die Option auf *Nein* gesetzt ist, wird jedes Mal, wenn eine entsprechende Aktualisierung erfolgt, eine neue Chargennummer erstellt (z. B. wenn einer Bestellung eine neue Menge hinzugefügt wird).
