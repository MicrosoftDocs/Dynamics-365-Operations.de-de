---
title: Sie werden aufgefordert, die Einstellungen für die Artikelabdeckung zu speichern, obwohl Sie keine Änderungen vorgenommen haben
description: Sie werden aufgefordert, die Einstellungen für die Artikelabdeckung zu speichern, obwohl Sie keine Änderungen vorgenommen haben.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049468"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Sie werden aufgefordert, die Einstellungen für die Artikelabdeckung zu speichern, obwohl Sie keine Änderungen vorgenommen haben

KB-Nummer: 4615588

## <a name="symptoms"></a>Symptome

In einigen Szenarien erhalten Sie möglicherweise die folgende Meldung, wenn Sie die Seite **Artikelabdeckung** öffnen, nachdem Sie Elemente über die Entität *Artikelabdeckung V2* importiert haben.

> Möchten Sie die Änderungen vor dem Schließen speichern?

Sie erhalten diese Nachricht, obwohl Sie keine Änderungen vorgenommen haben.

## <a name="resolution"></a>Lösung

Die Seite **Artikelabdeckung** enthält eine komplexe Standardlogik, die dazu führen kann, dass die Nachricht angezeigt wird, nachdem kürzlich direkte Änderungen in der Datenbank vorgenommen wurden, z. B. durch Entitätsimport. Zum Beispiel ist das Feld `AREGENERALSETTINGSOVERRIDDEN` Entitätsfeld auf *Nein* gesetzt, aber Sie importieren eine Datei, die neue oder geänderte Werte für Felder wie `PRODUCTCOVERAGEGROUPID` und/oder `VENDORACCOUNTNUMBER` bereitstellt. In diesem Fall, weil das `AREGENERALSETTINGSOVERRIDDEN` Feld auf *Nein* gesetzt ist, werden die Werte automatisch aus den Feldern gelöscht, wenn Sie die Seite **Artikelabdeckung** zum ersten Mal nach dem Import öffnen. Wenn Sie die Änderungen speichern, während das Meldungsfeld Sie dazu auffordert, werden sie in der Datenbank gespeichert. Andernfalls erhalten Sie beim nächsten Öffnen der Seite dieselbe Nachricht.

Um dieses Verhalten zu verhindern, aber auch Werte für Felder wie `PRODUCTCOVERAGEGROUPID` durch Entitätsimport einzuschließen, setzen Sie `AREGENERALSETTINGSOVERRIDDEN` auf *Ja*,  wenn Sie importieren.
