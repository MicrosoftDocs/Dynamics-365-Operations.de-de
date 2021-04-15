---
title: Übergeben von zurückgelieferten Artikeln zur Prüfung
description: Beim Erfassen eines zurückgelieferten Artikels können Sie festlegen, dass ein Artikel zur Prüfung gesendet wird, bevor er an das Lager zurückgegeben oder anderweitig veräußert wird.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdee1ed2c7e98843e5dcfe9669e6a7c1eb11173c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810677"
---
# <a name="pass-returned-items-on-to-inspection"></a>Übergeben von zurückgelieferten Artikeln zur Prüfung 

[!include [banner](../includes/banner.md)]


Beim Erfassen eines zurückgelieferten Artikels können Sie festlegen, dass ein Artikel zur Prüfung gesendet wird, bevor er an das Lager zurückgegeben oder anderweitig veräußert wird.

1.  Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Wareneingang**.
    
    \-oder-
    
    Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Produktions-Wareneingang**.

2.  Erfassen Sie den Zugang eines Artikels wie gewohnt im Formular **Lagerplatzerfassung**.
    

    > [!NOTE]
    > <P>Informationen zum Erfassen des Zugangs zurückgelieferter Artikel finden Sie, <A href="register-the-receipt-of-returned-items.md">Erfassen des Empfangs zurückgelieferter Artikel</A></P>



3.  Auf der Registerkarte **Standardwerte** im Bereich **Handhabungsmodus**, wählen Sie das Feld **Quarantäneverwaltung** aus.

Damit wird das System aufgefordert, einen Quarantäneauftrag zu erstellen, und die Person bzw. die Abteilung, die Prüfungen durchführt, antwortet auf diesen Auftrag mithilfe des Formulars **Quarantäneauftrag**.

## <a name="see-also"></a>Siehe auch

[Prüfen von zurückgelieferten Artikeln](take-returned-items-through-inspection.md)

[Angeben zur Entsorgung zurückgelieferter Artikel](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]