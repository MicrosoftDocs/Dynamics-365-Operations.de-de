---
title: B2B-Geschäftspartner mithilfe von Kundenhierarchien verstehen
description: In diesem Thema wird beschrieben, wie Sie Kundenhierarchien zur Verwaltung von Geschäftspartnern für Business-to-Business(B2B)-E-Commerce-Sites von Microsoft Dynamics 365 Commerce verwenden.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6e594cbb824a8b823912118e99b819585adc45e
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313831"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>B2B-Geschäftspartner mithilfe von Kundenhierarchien verstehen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Kundenhierarchien zur Verwaltung von Geschäftspartnern für Business-to-Business(B2B)-E-Commerce-Sites von Microsoft Dynamics 365 Commerce verwenden.

In der Commerce-Zentralverwaltung wird eine *Kundenhierarchie*-Entität verwendet, um die Geschäftspartnerorganisationen darzustellen, die Ihre B2B-E-Commerce-Site verwenden werden. Bevor Sie mit der Verwendung von Kundenhierarchien zur Verwaltung von Geschäftspartnern beginnen können, müssen Sie die B2B-E-Commerce-Funktionen in der Commerce-Zentralverwaltung aktivieren und dann einen Nummernkreis für die Kundenhierarchie festlegen.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Die Funktion für B2B-E-Commerce-Funktionen in der Commerce-Zentralverwaltung aktivieren

Um die B2B-E-Commerce-Funktionen nutzen zu können, müssen Sie zuerst die Funktion **Die Verwendung von B2B-E-Commerce-Funktionen aktivieren** in der Commerce-Zentralverwaltung aktivieren.

1. Wechseln Sie zu **Arbeitsbereiche \> Verwaltung von Funktionen**.
1. Verwenden Sie auf der Registerkarte **Alle** das Filterfeld und suchen Sie nach **Modul: Einzelhandel und Handel**.
1. Suchen Sie die Funktion namens **Die Verwendung von B2B-E-Commerce-Funktionen aktivieren** und wählen Sie **Jetzt aktivieren** in der rechten unteren Ecke aus.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Einen Nummernkreis für die Kundenhierarchie festlegen

Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Bezeichnern für Masterdatensätze und Buchungsdatensätze, die Bezeichner benötigen. Sie müssen einen Nummernkreis festlegen, der verwendet wird, um die ID für die Kundenhierarchie zu generieren. Weitere Informationen zu Nummernsquenzen finden Sie unter [Überblick über Nummernsequenzen](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Gehen Sie wie folgt vor, um in der Commerce-Zentralverwaltung einen Nummernkreis für die Kundenhierarchie zu konfigurieren:

1. Wechseln Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Nummernkreise \> Nummernkreise**.
1. Erstellen Sie einen neuen Nummernkreis oder wählen Sie einen vorhandenen Nummernkreis aus, um ihn wiederzuverwenden.
1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**.
1. Fügen Sie in der Registerkarte **Nummernkreise** den Nummernkreis, den Sie zuvor erstellt oder ausgewählt haben der Referenz **Kundenhierarchie-ID** hinzu.

![Der Kundenhierarchie-ID-Referenz hinzugefügter Nummernkreis.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Wie der Genehmigungsprozesses funktioniert

Wenn ein Geschäftspartner den Beitritt zu einer B2B-E-Commerce-Site anfordert, speichert das System die Anfrage als *Interessent*. Eine Persona in der Commerce-Zentralverwaltung, z. B. ein Bereichsleiter (Einzelhandel), kann Partneranfragen genehmigen oder ablehnen. Weitere Informationen zum Verwalten von Geschäftspartneranfragen und zu Genehmigungen von Interessenten finden Sie unter [Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten](manage-b2b-users.md).

Wenn ein Interessent genehmigt wird, erstellt das System zwei neue Kundendatensätze:

- Ein Kundendatensatz vom Typ **Organisation** steht für die Organisation, die Geschäftspartner werden möchte.
- Ein Kundendatensatz vom Typ **Person** steht für die Person, die die Anfrage gestellt hat.

Außerdem wird ein neuer Kundenhierarchiedatensatz unter **Einzelhandel und Handel \> Kunden \> Kundenhierarchien** angelegt. Dieser Kundenhierarchiedatensatz hat die folgenden Eigenschaften:

- **Kundenhierarchie-ID**: die eindeutige ID der Kundenhierarchie. Diese ID verwendet den Nummernkreis, den Sie in den gemeinsam genutzten Commerce-Parametern festgelegt haben.
- **Name** – der Organisationsname des Geschäftspartners, wie in der Onboarding-Anfrage angegeben. Dieses Feld ist bearbeitbar.
- **Zweck** – diese Eigenschaft wird auf den vordefinierten Wert **B2B-Organisation** gesetzt.
- **Organisation**: die Kunden-ID der Geschäftspartnerorganisation.

Die Person, die die Onboardinganfrage eingereicht hat, wird im Inforegister **Hierarchie** hinzugefügt und ihr wird die Rolle **Administrator** zugewiesen. Wenn der Administrator der Geschäftspartnerorganisation auf einer B2B-Site weitere Benutzer hinzufügt, wird ein neuer Kundendatensatz für jeden Benutzer erstellt. Der Kundendatensatz wird auch dem relevanten Kundenhierarchiedatensatz für den Geschäftspartner hinzugefügt und ihm wir die Rolle **Benutzer** hinzugefügt.

### <a name="examples"></a>Beispiele

Eine Person mit dem Namen Sam J. reicht eine Onboardinganfrage im Namen der Microsoft-Organisation ein. Nachdem die Anfrage genehmigt wurde, werden zwei neue Kundenkonten erstellt: eines vom Typ **Person** für Sam J. und eines vom Typ **Organisation** für Microsoft.

Wie das Beispiel in der folgenden Abbildung zeigt, wird auch ein neuer Kundenhierarchiedatensatz erstellt. Dieser Datensatz hat denselben Namen wie die Organisation (**Microsoft**) und die Rolle **Administrator** wird Sam J. zugewiesen. Als Administrator fügt Sam J. alle anderen Microsoft-Benutzer der B2B-Site zu dieser Hierarchie hinzu und weist ihnen die Rolle **Benutzer** zu. In diesem Beispiel wurde Sush R. als Benutzer hinzugefügt.

![Beispiel eines Kundenhierarchiedatensatzes.](../media/CustomerHierarchy2.png)

Um festzustellen, ob ein Kunde einer Kundenhierarchie zugeordnet ist, öffnen Sie den Kundendatensatz. Wie das Beispiel in der folgenden Abbildung zeigt, zeigt das Feld **Kundenhierarchie-ID** im Abschnitt **B2B** im Inforegister **Einzelhandel** an, ob der Kunde zu einer Kundenhierarchie gehört. Die Option **B2B-Administrator** gibt an, ob der Kunde ein Administrator dieser Hierarchie ist.

![Beispiel für den B2B-Abschnitt auf dem Inforegister „Einzelhandel“ eines Kundendatensatzes, in dem der Kunde einer Hierarchie zugeordnet und als Administrator festgelegt ist.](../media/CustomerHierarchyMapping2.png)

In den meisten Fällen sollten die Eigenschaftswerte aller Kundendatensätze in einer Hierarchie übereinstimmen. Da beispielsweise alle Geschäftspartnerbenutzer ähnliche Preise für Produkte erhalten sollten, sollten ihre Preisgruppe und die zugehörigen Konfigurationen übereinstimmen. Das System erzwingt diese Konsistenz jedoch nicht. Daher sind die relevanten Benutzer der Commerce-Zentralverwaltung dafür verantwortlich, dass die Eigenschaftswerte und -konfigurationen für alle Kunden in einer bestimmten Hierarchie übereinstimmen.

Benutzer der Commerce-Zentralverwaltung können sich die Eigenschaftswerte für alle Kundendatensätze in einer Hierarchie nebeneinander ansehen. Wie das Beispiel in der folgenden Abbildung zeigt, können Sie die Option **Allgemein** in der Dropdownliste im Inforegister **Hierarchie** verwenden und dann einen beliebigen Abschnitt des Kundendatensatzes auswählen, um die zugehörigen Eigenschaften anzuzeigen. Benutzer können die Eigenschaftswerte in dieser Ansicht direkt anzeigen. Um alle Werte aus einem Administratorkundendatensatz für alle Benutzer zu kopieren, wählen Sie **Überschreiben** im Inforegister **Hierarchie** aus.

![Beispiel eines Kundenhierarchiedatensatzes mit der Schaltfläche „Überschreiben“ und der Option in der Dropdownliste.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
