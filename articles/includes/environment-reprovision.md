---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459069"
---
Wenn Sie eine Datenbank von einer Umgebung in eine andere kopieren, müssen Sie das Tool zur erneuten Bereitstellung der Umgebung ausführen, bevor die kopierte Datenbank nach Ausführung dieses Schritts voll funktionsfähig ist, um zu gewährleisten, dass alle Commerce-Komponenten aktuell sind.

> [!IMPORTANT]
> Es wird empfohlen, diese Vorgehensweise unabhängig davon durchzuführen, ob Sie Commerce-Komponenten verwenden oder nicht, da die Commerce-Funktionalität in allen Umgebungen enthalten ist. 

Bevor Sie fortfahren, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:
1. Wenn Sie auf die Version vom Juli 2017 (auch bekannt als 7.2) 7.2.11792.56024 aktualisieren, wenden Sie die folgenden X++-Hotfixes der Anwendung in der Zielumgebung an, bevor Sie die Aktualisierung der Daten in dieser Umgebung durchführen. Dadurch wird verhindert, dass während der Aktualisierung der Daten verschiedene Fehler auftreten:

    - KB 4036156 – Upgrade der Retail-Unterversion – ‚Die Reihenfolge der Variantennummern ist nicht festgelegt.‘ Dieses Korrekturpaket enthält auch KB 4035399 und KB 4035751. Beachten Sie, dass Sie mindestens Platform Update 9 haben müssen, um dieses Paket verwenden zu können. Wenn Sie nicht sicher sind, installieren Sie die aktuellen Binärdateien.
    
2. Wenn Sie von Microsoft Dynamics AX 2012 aktualisieren, installieren Sie die folgenden X++-Korrekturen der Anwendung in der Zielumgebung, bevor Sie die Daten aktualisieren:
    - KB 4033183 - Dynamics AX 2012 R2 oder Dynamics AX 2012 R3 Pre-CU8 Nicht-Retail-Upgrade schlägt fehl mit Objekt nicht gefunden für dbo.RETAILTILLLAYOUTZONE.
    - KB 4040692 - Upgrade von Dynamics AX 2012 R3 auf Microsoft Dynamics 365 for Operations 7.2 schlägt fehl auf RetailSalesLine-Duplikatindex auf SalesLineIdx.
    - KB 4035490 - Performanceproblem mit GeneralJournalAccountEntry MainAccount Feldupgradeskript.


Gehen Sie folgendermaßen vor, um das Tool zur erneuten Bereitstellung der Umgebung auszuführen.

1. Wählen Sie in der Bibliothek der freigegebenen Anlagen **Bereitstellbares Softwarepaket** aus.
2. Laden Sie das Tool zur erneuten Bereitstellung der Umgebung herunter.
3. Wählen Sie in der Anlagenbibliothek für Ihr Projekt **Bereitstellbares Softwarepaket** aus.
4. Wählen Sie **Neu** aus, um ein neues Paket zu erstellen.
5. Geben Sie einen Namen und eine Beschreibung für das Paket ein. Sie können **Tool zur erneuten Bereitstellung der Umgebung** als Paketname verwenden.
6. Laden Sie das Paket, das Sie eben heruntergeladen haben, hoch.
7. Wählen Sie auf der Seite **Umgebungsdetails** für die Zielumgebung **Verwalten** > **Aktualisierungen übernehmen** aus.
8. Wählen Sie das Tool zur erneuten Bereitstellung der Umgebung, das Sie eben hochgeladen haben, aus und wählen Sie dann **Übernehmen**, um das Paket zu übernehmen.
9. Überwachen Sie den Fortschritt der Bereitstellung des Pakets. 

Weitere Informationen dazu, wie ein bereitgestelltes Paket übernommen wird, finden Sie unter [Ein bereitgestelltes Paket anwenden](../deployment/create-apply-deployable-package.md). Weitere Informationen dazu, wie ein bereitgestelltes Paket manuell übernommen wird, finden Sie unter [Ein bereitgestelltes Paket installieren](../deployment/install-deployable-package.md).
