---
title: Seriennummergesteuerte Produkte in POS zurückgeben
description: In diesem Artikel werden die Funktionen zum Validieren von Artikeln mit Seriennummer als Teil des Rückgabeprozesses in der Microsoft Dynamics 365 Commerce Point-of-Sale-Anwendung (POS) beschrieben.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b2af301180dc2284400b887ce36357660bdd86fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860320"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Seriennummergesteuerte Produkte in POS zurückgeben

[!include [banner](includes/banner.md)]

In diesem Artikel werden die Funktionen zum Validieren von Artikeln mit Seriennummer als Teil des Rückgabeprozesses in der Microsoft Dynamics 365 Commerce Point-of-Sale-Anwendung (POS) beschrieben.

> [!NOTE]
> In der Commerce-Version 10.0.20 und höher wird eine neue Funktion mit dem Namen **Einheitliche Retourenbearbeitungserfahrung in POS** verfügbar. Um die Seriennummernvalidierung während der Retourenbearbeitung in POS zu verwenden, müssen Sie diese Funktion aktivieren. Informationen zu anderen Funktionen, die diese Funktion bietet, wenn sie aktiviert ist, finden Sie unter [Retouren im POS erstellen)](POS-returns.md).
>
> Nachdem die Funktion aktiviert wurde, kann sie nicht mehr deaktiviert werden.

## <a name="options-for-validating-serialized-returns"></a>Optionen zur Validierung serialisierter Retouren

Wenn die Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** aktiviert ist, können Unternehmen eine Validierung von Rücksendungen von Artikeln mit Seriennummernkontrolle über POS durchführen. Diese Funktion kann Benutzer warnen, wenn die zurückgegebene Seriennummer von der ursprünglich verkauften Seriennummer abweicht. In der Commerce-Version 10.0.20 und höher ist die Nachricht, die Benutzer erhalten, nur eine Warnmeldung. Benutzer können eine Rücksendung weiterhin gegen eine Seriennummer bearbeiten, die sich von der ursprünglich verkauften Seriennummer unterscheidet.

Sie konfigurieren die Seriennummernvalidierung für eine Organisation, nachdem die Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** aktiviert wurde, indem Sie zu **Retail and Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter** in der Commerce-Zentralverwaltung gehen. Auf der Registerkarte **Bestand** auf dem Inforegister **Lagerbestandsvorgänge** stellen Sie die Option **Validierung von Seriennummern bei POS-Rücksendungen aktivieren** auf **Ja**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Retouren für Artikel mit Seriennummer in POS verarbeiten

Wenn die Option **Validierung von Seriennummern bei POS-Rücksendungen aktivieren** auf **Ja** gesetzt wird, kann der Benutzer, wenn ein Artikel mit Seriennummer über POS zurückgegeben wird, die Seriennummer für die Rücksendeposition im Detailbereich auf der Seite **Retournierbare Produkte** eingeben. Wenn die eingegebene Seriennummer nicht mit der Originalseriennummer übereinstimmt, die für den Verkaufsvorgang verkauft wurde, erhält der Benutzer eine Warnmeldung. Die Anwendung hindert den Benutzer jedoch nicht daran, die Retoure weiterhin zu buchen.

> [!NOTE]
> Derzeit unterstützt POS die Validierung von Seriennummern nur bei Rücksendungen, bei denen die ursprünglich bestellte Menge nicht mehr als eins beträgt. Wenn die ursprüngliche Verkaufsauftragsposition in einem Nicht-POS-Kanal erstellt wurde und die Menge, die für den Artikel mit Seriennummer in einer bestimmten Verkaufsposition bestellt wurde, mehr als eins beträgt, kann der Artikel nicht korrekt über POS zurückgegeben werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Retouren in POS erstellen](POS-returns.md)
