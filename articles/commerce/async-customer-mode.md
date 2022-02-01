---
title: Asynchroner Debitorerstellungsmodus
description: Dieses Thema beschreibt den asynchronen Debitorerstellungsmodus in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 43418b61778d187364d4d52a05178078a37623eb
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984269"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynchroner Debitorerstellungsmodus

[!include [banner](includes/banner.md)]

Dieses Thema beschreibt den asynchronen Debitorerstellungsmodus in Microsoft Dynamics 365 Commerce.

In Commerce gibt es zwei Arten der Debitorerstellung: synchron (oder sync) und asynchron (oder async). Standardmäßig werden Debitoren synchron erstellt. Mit anderen Worten, sie werden in Echtzeit in der Commerce-Zentrale erstellt. Der sync-Modus für die Debitorerstellung ist von Vorteil, da neue Debitoren sofort kanalübergreifend durchsucht werden können. Es hat jedoch auch einen Nachteil. Weil es [Commerce Data Exchange: Echtzeitservice](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)-Aufrufe an die Commerce-Zentrale erzeugt, kann die Leistung beeinträchtigt werden, wenn viele Aufrufe zur Debitorerstellung gleichzeitig getätigt werden.

Wenn die Option **Debitor im asynchronen Modus erstellen** auf **Ja** gesetzt ist im Funktionsprofil des Geschäfts (**Retail und Commerce \> Kanaleinrichtung \> Einrichtung Onlineshop \> Funktionsprofile**), werden Echtzeit-Serviceaufrufe nicht zum Erstellen von Debitordatensätzen in der Debitordatenbank verwendet. Der asynchrone Debitorerstellungsmodus wirkt sich nicht auf die Leistung der Commerce-Zentrale aus. Jedem neuen asynchrone Debitordatensatz wird eine temporäre GUID (Globally Unique Identifier) zugewiesen und als Debitorenkontokennung verwendet. Diese GUID wird Benutzern der Verkaufsstelle (POS) nicht angezeigt. Stattdessen werden diese Benutzer **Ausstehende Synchronisierung** als Debitorenkontokennung sehen.

> [!IMPORTANT]
> Wann immer der POS offline geschaltet wird, erstellt das System die Debitoren selbst dann automatisch asynchron, wenn der asynchrone Debitorenerstellungsmodus deaktiviert ist. Daher müssen Administratoren der Commerce-Zentrale einen wiederkehrenden Batchauftrag für den **P-Einzelvorgang**, den Einzelvorgang **Debitoren und Geschäftspartner im async-Modus synchronisieren** (früher als **Debitoren und Geschäftspartner im async-Modus synchronisieren** bezeichnet) und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren in der Commerce-Zentrale in synchrone Debitoren konvertiert werden.

## <a name="async-customer-limitations"></a>Asynchrone Debitorenbeschränkungen

Die asynchrone Debitorenfunktionalität weist derzeit die folgenden Einschränkungen auf:

- Asynchrone Debitorendatensätze können nur bearbeitet werden, wenn der Debitor in der Commerce-Zentrale erstellt und die neue Debitorenkonto-ID wieder mit dem Kanal synchronisiert wurde.
- Kundenkarten können nur dann an asynchrone Debitoren ausgegeben werden, wenn die neue Debitorenkonto-ID wieder mit dem Kanal synchronisiert wurde.

## <a name="async-customer-enhancements"></a>Verbesserungen bei asynchronen Debitoren

Ab Commerce-Version 10.0.24 können Sie die **Die erweiterte asynchrone Debitorenerstellung aktivieren**-Funktion im **Funktionsverwaltung**-Arbeitsplatz aktivieren. Diese Funktion schließt die Lücke zwischen asynchronem und synchronisiertem Debitorenerstellungsmodus in POS und E-Commerce auf folgende Weise:

- Mitgliedschaften können nicht mit asynchronen Debitoren verknüpft werden.
- Asynchrone Debitoren können Titel hinzugefügt werden.
- Sekundäre E-Mail-Adressen und Telefonnummern können für asynchrone Debitoren nicht erfasst werden.

Ab Commerce-Version 10.0.22 können Sie die **Die asynchrone Erstellung für Debitorenadressen aktivieren**-Funktion im **Funktionsverwaltung**-Arbeitsplatz aktivieren. Mit dieser Funktion können neu erstellte Debitorenadressen asynchron sowohl für Synchronisierungskunden als auch für asynchrone Debitoren gespeichert werden.

Nachdem Sie die zuvor erwähnten Funktionen aktiviert haben, müssen Sie einen wiederkehrenden Batchauftrag für den **P-Einzelvorgang**, den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren in der Commerce-Zentrale in synchrone Debitoren konvertiert werden.

### <a name="customer-creation-in-pos-offline-mode"></a>Debitorenerstellung im POS-Offlinemodus

Wie zuvor erwähnt: wann immer das POS offline geschaltet wird, erstellt das System die Debitoren selbst dann automatisch asynchron, wenn der asynchrone Debitorenerstellungsmodus deaktiviert ist. Daher müssen Administratoren der Commerce-Zentrale einen wiederkehrenden Batchauftrag für den **P-Einzelvorgang**, den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren in der Commerce-Zentrale in synchrone Debitoren konvertiert werden.

> [!NOTE]
> Wenn die Option **Gemeinsam genutzte Debitorendatentabellen filtern** auf **Ja** auf der Seite **Handelskanalschema** (**Retail und Commerce \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbankgruppe**) gesetzt ist, werden Debitorendatensätze nicht im POS-Offlinemodus erstellt. Weitere Informationen finden Sie unter [Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Debitorenverwaltung in Geschäften](customer-mgmt-stores.md)

[Asynchrone Debitoren in synchrone Debitoren konvertieren](convert-async-to-sync.md)

[Debitorattribute](dev-itpro/customer-attributes.md)

[Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
