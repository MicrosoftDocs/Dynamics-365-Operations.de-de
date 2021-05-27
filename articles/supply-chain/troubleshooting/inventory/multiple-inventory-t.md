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
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026555"
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
