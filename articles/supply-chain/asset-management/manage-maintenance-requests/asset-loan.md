---
title: Anlagendarlehen
description: In diesem Thema wird beschrieben, wie Anlagendarlehen in der Anlagenverwaltung erfasst werden.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cba680d0ad626e0275539d7478a83639a9d22635
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428767"
---
# <a name="asset-loans"></a>Anlagendarlehen

[!include [banner](../../includes/banner.md)]

 

Wenn Ihr Unternehmen Anlagen für Reparatur- oder Wartungsaufträge von internen Standorten oder Kunden erhält und Sie vorübergehend Anlagen an diese Standorte oder Kunden ausleihen, kann die Anlagenverwaltung die Anlagendarlehen verfolgen.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Anlagendarlehen in einer Wartungsanfrage erfassen

1. Wählen Sie **Anlagenverwaltung** \> **Allgemein** \> **Wartungsanfragen** \> **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** aus.
2. Wählen Sie die Wartungsanfrage aus, um ein Anlagendarlehen zu erfassen, und wählen Sie dann **Bearbeiten**.
3. Wählen Sie auf der Seite **Anforderung** die Option **Anlagenausleihe senden** aus.
4. Wählen Sie die Anlage aus, und geben Sie das voraussichtliche Rückgabedatum ein.
5. Wählen Sie **OK**.

> [!NOTE]
> - Sie können eine Anlagenausleihe nur senden, wenn eine Anlage des gleichen Anlagentyps verfügbar ist.
> - Die Anlage, die Sie ausleihen werden, muss über einen Anlagenlebenszyklusstatus verfügen, der es ermöglicht, dass sie als Ausleiheanlage verwendet werden kann, z. B. **Im Lager**. Wenn die Anlagenausleihe erfasst ist, wird der Anlagenlebenszyklusstatus der Anlage automatisch aktualisiert, z. B. in **In Ausleihe**.

Um eine Liste mit allen Anlagen anzuzeigen, die Sie an andere Standorte oder an Kunden ausgeliehen haben, wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagendarlehen** \> **Alle Anlagendarlehen** aus. Wenn das Kontrollkästchen **Beendet** für eine Anlage aktiviert ist, wurde die Anlage als Ihrem Unternehmen zurückgegeben erfasst.

![Wartungsanfragen verwalten](media/06-manage-maintenance-requests.png)

Auf der Seite **Aktive Anlagendarlehen** können Sie eine Liste aller Anlagendarlehen anzeigen, die noch nicht an Ihr Unternehmen zurückgegeben wurden.

## <a name="register-loan-assets-as-returned"></a>Anlagendarlehen als zurückgegeben erfassen

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagendarlehen** \> **Aktive Anlagendarlehen** aus.
2. Wählen Sie das Anlagendarlehen aus, das als zurückgegeben erfasst werden soll, und wählen Sie dann **Anlagendarlehen zurückgeben** aus.
3. Geben Sie im Feld **Zurückgegeben** das Datum und die Uhrzeit ein.
4. Wählen Sie **OK**.
5. Aktualisieren Sie die Listenseite **Aktive Anlagendarlehen**. Sie sehen, dass das Anlagendarlehen nicht mehr in der Liste angezeigt wird.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]