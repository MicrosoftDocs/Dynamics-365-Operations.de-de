---
title: Ein- und ausgehende Anlagen
description: In diesem Artikel wird erläutert, wie Sie ein- und ausgehende Anlagen in Anlagenverwaltung erfassen.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016535"
---
# <a name="inbound-and-outbound-assets"></a>Ein- und ausgehende Anlagen

[!include [banner](../../includes/banner.md)]

 

Wenn Ihr Unternehmen Reparatur- oder Wartungsarbeiten für Anlagen ausführt, die von anderen Standorten oder Kunden entgegen genommen werden, kann Asset Management sowohl eingehende Anlagen nachverfolgen, die auf dem Weg zu Ihrem Unternehmen sind, als auch ausgehenden Anlagen, die zurückgegeben werden.

> [!NOTE]
> Wenn Sie Lebenszyklusstatus für ein- und ausgehende Anlagen zum Verwalten von Anlagen verwenden möchten, die empfangen und zurückgegeben werden, müssen Sie Lebenszyklusstatus für Wartungsanforderungen und Lebenszyklusmodelle einrichten, die diese Aktivitäten unterstützen. Weitere Informationen finden Sie unter [Wartungsanforderungen](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

Die Einrichtung von Asset Management bestimmt, ob Sie mit ein- und ausgehenden Anlagen arbeiten können.

## <a name="register-assets-as-inbound"></a>Erfassen von Anlagen als eingehend

1. Wählen Sie **Anlagenverwaltung** \> **Wartungsanfragen** \> **Aktive Wartungsanfragen**.
2. Wählen Sie die Wartungsanfrage aus.
3. Wählen Sie **Wartungsanforderungsstatus aktualisieren** aus.
4. Wählen Sie **Eingehend** aus (oder einen anderen Lebenszyklusstatus, den Sie für eingehende Anlagen erstellt haben), und wählen Sie anschließend **OK**.

![Erfassen von Anlagen als eingehend.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Erfassen von eingehenden Anlagen als empfangen

1. Wählen Sie **Anlagenverwaltung** \> **Ein-/ausgehend** \> **Eingehende Anlagen** aus.
2. Wählen Sie die Anlage oder die Wartungsanfrage aus.
3. Wählen Sie **Anlagen entgegennehmen** aus.
4. Geben Sie im Feld **Eingegangen** das Datum und die Uhrzeit ein. Wählen Sie dann **OK** aus. Der Datensatz wird von der Listenseite **Eingehende Anlagen** entfernt.

![Erfassen von eingehenden Anlagen als empfangen.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Erfassen von Anlagen als ausgehend

Wenn Sie den Wartungs- oder Reparaturauftrag erledigt haben, können Sie die Anlage als zurückgegeben erfassen.

1. Wählen Sie **Anlagenverwaltung** \> **Wartungsanfragen** \> **Aktive Wartungsanfragen**.
2. Wählen Sie die Wartungsanfrage aus.
3. Wählen Sie **Wartungsanforderungsstatus aktualisieren** aus.
4. Wählen Sie **Ausgehend** aus (oder einen anderen Lebenszyklusstatus, den Sie für ausgehende Anlagen erstellt haben), und wählen Sie anschließend **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Erfassen von ausgehenden Anlagen als geliefert

1. Wählen Sie **Anlagenverwaltung** \> **Ein-/ausgehend** \> **Ausgehende Anlagen** aus.
2. Wählen Sie die Anlage oder die Wartungsanfrage aus.
3. Wählen Sie **Anlagen liefern** aus.
4. Geben Sie im Feld **Geliefert** das Datum und die Uhrzeit ein. Wählen Sie dann **OK** aus. Der Datensatz wird von der Listenseite **Ausgehende Anlagen** entfernt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]