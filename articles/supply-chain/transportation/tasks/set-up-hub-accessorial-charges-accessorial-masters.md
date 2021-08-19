---
title: Hub-Zusatzgebühren und Zusatzleistungsmaster einrichten
description: Im folgenden Verfahren wird dargestellt, wie ein Zusatzleistungsmaster für einen Hub erstellt und dieser Master verwendet wird, um eine Hub-Zusatzgebühr zu erstellen.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e67992c9e744b6337cf4921e06cc7886dead8021102d263022f67940c3e7669b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720131"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Hub-Zusatzgebühren und Zusatzleistungsmaster einrichten

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren wird dargestellt, wie ein Zusatzleistungsmaster für einen Hub erstellt und dieser Master verwendet wird, um eine Hub-Zusatzgebühr zu erstellen. Das Verfahren verwendet das USMF-Dataset. Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen.


## <a name="set-up-a-hub-master"></a>Einen Hubmaster einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Zusatzleistungsmaster".
2. Klicken Sie auf "Neu".
3. Geben Sie einen Wert in das Feld "Zusatzleistungsmaster" ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Wählen Sie im Feld "Zusatzleistungstyp" "Hub" aus.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="set-up-a-hub-accessorial-charge"></a>Hubzusatzgebühr einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Hubzusatzgebühren".
2. Klicken Sie auf "Neu".
3. Geben Sie einen Wert in das Feld "Kennung für Hubzusatzgebühren" ein.
4. Klicken Sie im Feld "Hub" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
6. Wählen Sie im Feld "Hubposition" eine Option aus.
    * Sie können den Zuschlag entweder als Abholung oder Lieferung erstellen. Je nach getroffener Auswahl wird der Zuschlag dem entsprechenden Transportsegment auf den Arbeitsplan angewendet.  
7. Klicken Sie im Feld "Zusatzleistungsmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie den Master aus, den Sie soeben erstellt haben.  
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]