---
title: Hinzufügen einer Adresse zu einem Serviceauftrag
description: In diesem Artikel wird beschrieben, wie eine Debitorenadresse zu einem Serviceauftrag hinzugefügt wird.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015724"
---
# <a name="add-an-address-to-a-service-order"></a>Hinzufügen einer Adresse zu einem Serviceauftrag

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie eine Debitorenadresse zu einem Serviceauftrag hinzugefügt wird. Beim Erstellen eines Serviceauftrags werden die Adressinformationen aus dem Projekt übertragen, dem der Serviceauftrag zugeordnet ist. Allerdings können Sie einen alternativen Speicherort von Adressen auswählen, die bereits in Microsoft Dynamics AX für Debitoren, Kreditoren, Standorte, Lagerorte, Serviceaufträge und Projekte eingegeben sind.

Zudem können Sie eine neue Adresse erstellen. Standardmäßig wird die neue Adresse in das Projekt übertragen. Allerdings können Sie angeben, dass die neue Adresse für diese Instanz des Services relevant ist. Die neue Adresse wird dann nicht in das Projekt übertragen.

## <a name="create-a-customer-address-for-a-service-order"></a>Erstellen einer Debitorenadresse für einen Serviceauftrag

Um einem Serviceauftrag eine Adresse hinzuzufügen, führen Sie folgende Schritte aus:

1. Gehen Sie zu **Serviceverwaltung** \> **Serviceaufträge** \> **Serviceaufträge**.

1. Öffnen Sie den Serviceauftrag, für den eine Adresse erstellt werden soll.

1. Öffnen Sie die Registerkarte **Header**.

1. Erweitern Sie das **Adresse**-Inforegister, und wählen Sie dann **Adresse hinzufügen** aus der FastTab-Symbolleiste aus.

1. Geben Sie im Dialog **Neue Adresse** einen eindeutigen Namen für die Adresse ein, und füllen Sie die verbleibenden Felder aus. 

    > [!WARNING]
    > Wenn Sie denselben Namen als vorhandene Adresse eingeben, überschreiben die Informationen, die Sie in die verbleibenden Felder eingeben, die Informationen für die vorhandene Adresse.

1. Wählen Sie **OK** aus, um die neue Adresse in Ihren Serviceauftrag zu kopieren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Angeben einer alternativen Adresse für einen Serviceauftrag

Um einem Serviceauftrag eine alternative Adresse hinzuzufügen, führen Sie folgende Schritte aus:

1. Gehen Sie zu **Serviceverwaltung** \> **Serviceaufträge** \> **Serviceaufträge**.

1. Öffnen Sie den Serviceauftrag, für den eine alternative Adresse erstellt werden soll.

1. Öffnen Sie die Registerkarte **Header**.

1. Erweitern Sie das **Adresse**-Inforegister, und wählen Sie dann **Andere Adresse** aus der FastTab-Symbolleiste aus.

1. Wählen Sie im **Adressauswahl**-Dialog **Serviceaufträge** aus der Dropdown-Liste über dem Raster aus.

1. Wählen Sie eine Adresse und dann **OK** aus, um sie in Ihren Serviceauftrag zu kopieren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]