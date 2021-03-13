---
title: Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen
description: In diesem Thema wird beschrieben, wie Sie Organisationsmodellierungshierarchien für Business-to-Business-Organisationen (B2B) erstellen.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035910"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Organisationsmodellierungshierarchien für Business-to-Business-Organisationen (B2B) in Microsoft Dynamics 365 Commerce erstellen.

In der Commerce-Zentralverwaltung werden Geschäftspartnerorganisationen durch Kunden- und Kundenhierarchie-Entitäten repräsentiert. Die Geschäftspartnerorganisation und deren Benutzer werden als Kunden dargestellt, und Kundenhierarchien werden verwendet, um diese Kunden miteinander zu verknüpfen.

Wenn eine Geschäftspartneranfrage zum Beitritt zu einer B2B-E-Commerce-Website genehmigt wird, werden die folgenden Aktionen ausgeführt:

- Es werden zwei neue Kundendatensätze im System erstellt: ein **Typ: Organisation**-Kundendatensatz für die Geschäftspartnerorganisation und ein **Typ: Person**-Kundendatensatz für den Anforderer (das ist der Geschäftspartnerbenutzer, der die Anfrage eingereicht hat).
- Unter **Kunde \> Kundenhierarchie** wird ein neuer Kundenhierarchiedatensatz erstellt. Dieser Datensatz hat die folgenden Header-Eigenschaften:

    - **Kundenhierarchie-ID** – eine eindeutige ID für die Kundenhierarchie. Diese ID verwendet die Nummernfolge, die in den gemeinsam genutzten Commerce-Parametern in der Commerce-Zentralverwaltung definiert ist.
    - **Name** – der Organisationsname des Geschäftspartners, wie in der Onboarding-Anfrage angegeben.
    - **Zweck** – diese Eigenschaft wird auf den vordefinierten Wert **B2B-Organisation** gesetzt.
    - **Organisation** – die Kunden-ID des Geschäftspartners.

Hier sind die Details des Kundenhierarchiedatensatzes:

- Der Kundendatensatz des Anforderers wid der Kundenhierarchie zugeordnet.
- Die Administratorrolle wird dem Anforderer zugeordnet.

Wenn der Administrator der Geschäftspartnerorganisation auf einer B2B-Website weitere Benutzer hinzufügt, wird in der Commerce-Zentralverwaltung ein neuer Kundendatensatz für jeden Benutzer erstellt. Dieser Kundendatensatz wird auch dem relevanten Kundenhierarchiedatensatz für den Geschäftspartner hinzugefügt und hat die Rolle eines „Benutzers“.

> [!NOTE]
> In den meisten Fällen sollten die entsprechenden Eigenschaftswerte aller Kundendatensätze in einer Hierarchie übereinstimmen. Da beispielsweise alle Geschäftspartnerbenutzer ähnliche Preise für Produkte erhalten sollten, sollten ihre Preisgruppe und die zugehörigen Konfigurationen übereinstimmen. Das System erzwingt diese Konsistenz jedoch nicht. Daher sind die relevanten Benutzer der Commerce-Zentralverwaltung dafür verantwortlich, dass die Eigenschaftswerte und -konfigurationen für alle Kunden in einer bestimmten Hierarchie übereinstimmen.

Benutzer der Commerce-Zentralverwaltung können die Eigenschaftswerte für alle Kundendatensätze in der Hierarchie nebeneinander anzeigen. Wählen Sie die relevanten Kundendatensatzeigenschaften aus, indem Sie die Registerkartennamen im Dropdown-Menü auswählen. Benutzer können die Eigenschaftswerte in dieser Ansicht direkt anzeigen und bearbeiten. Wenn Sie alternativ alle Werte aus dem Administrator-Kundendatensatz auf alle Benutzerkundendatensätze anwenden möchten, wählen Sie in den Details der Kundenhierarchie **Überschreiben** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine B2B-E-Commerce-Website einrichten](set-up-b2b-site.md)

[Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten](manage-b2b-users.md)

[Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites](payment-method.md)

[Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites](quantity-limits.md)
