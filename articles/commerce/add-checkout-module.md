---
title: Checkoutmoduls
description: In diesem Thema wird beschrieben, wie Sie ein Auscheckenmodul einer Seite hinzufügen und die erforderlichen Eigenschaften festlegen.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3805c0faabc8afc3decffb924b7f25332ff1ab16
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025389"
---
# <a name="checkout-module"></a>Auschecken-Modul


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie ein Auscheckenmodul einer Seite hinzufügen und die erforderlichen Eigenschaften festlegen.

## <a name="overview"></a>Übersicht

Ein Auscheckenmodul ist ein spezieller Container, der alle Module hostet, die erforderlich sind, um einen Auftrag zu erstellen. Der Bericht stellt einen schrittweisen Fluss dar, die ein Kunde verwendet, um die gesamten relevanten Informationen einzugeben, um eine Bestellung abzuschließen. Es erfasst die Versandadresse, die Versandmethode und die Rechnungsinformationen. Es enthält auch eine Bestellübersicht und andere Informationen, die sich auf eine Kundenbestellung beziehen.

Ein Auscheckenmodul rendert Daten basierend auf der Warkenkorb-Kennung Diese Kennung wird als Browsercookie gespeichert. Eine Einkaufskorb-Kennung ist erforderlich, um Informationen im Auscheckenmodul zu rendern, wie Artikel im Auftrag, im Gesamtbetrag und bei den Rabatten.

## <a name="checkout-module-properties"></a>Checkoutmodul-Eigenschaften

Ein Checkout-Modul zeigt eine Bestellübersicht an und bietet die Funktionalität zum Aufgeben einer Bestellung. Um alle Kundeninformationen zu erfassen, die erforderlich sind, bevor eine Bestellung aufgegeben werden kann, müssen dem Checkout-Modul zusätzliche Module hinzugefügt werden. Einzelhändler haben daher die Flexibilität, dem Checkout-Flow benutzerdefinierte Module hinzuzufügen oder Module basierend auf ihren Anforderungen auszuschließen.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Module können im Auscheckmodul verwendet werden

- **Versandadresse** – Dieses Modul ermöglicht einem Debitor die Postanschrift für einen Auftrag hinzuzufügen oder auszuwählen. Wenn der Debitor angemeldet ist, werden alle zuvor gespeicherten Adressen für diesen Debitor angezeigt. Der Kunde kann diese dann unter den Adresse auswählen. Der Debitor kann auch eine neue Adresse hinzufügen. Die Versandadresse wird für alle Artikel im Auftrag verwendet, die Versand erfordern. Sie kann nicht für einzelne Positionen angepasst werden. Versandadresseformate werden für jedes Land oder Region definiert, und die länder-/regionsspezifischen Regeln werden für dieses Modul erzwungen. Obwohl dieses Modul keine Adressüberprüfung bereitstellt, kann die Adressüberprüfung ber die Anpassung implementiert werden. Wenn der Auftrag nur Artikel enthält, die im Shop abgeholt werden, wird dieses Modul automatisch ausgeblendet.
- **Lieferoptionen** – Dieses Modul ermöglicht einem Debitor eine Lieferoption für einen Auftrag auszuwählen. Lieferoptionen basieren auf der Versandadresse. Wenn die Versandadresse geändert wird, muss erneut die Lieferoptionen abgerufen werden. Wenn der Auftrag nur Artikel enthält, die im Shop abgeholt werden, wird dieses Modul automatisch ausgeblendet.
- **Containerabschnitt Auschecken** – Dieses Modul ist ein Container, der mehrere Module aufnehmen kann, um einen Bereich innerhalb des Auscheckflusses zu erstellen. So können Sie alle zahlungsrelevanten Module innerhalb dieses Containers speichern, damit diese in einem Bereich angezeigt werden. Dieses Modul wirkt sich nur auf das Layout des Flusses aus.
- **Geschenkkarte** – Dieses Modul ermöglicht es einem Debitor, für einen Auftrag mit einer Geschenkkarte zu bezahlen. Er unterstützt nur Microsoft Dynamics 365 Commerce Geschenkkarten. Eine oder mehrere Geschenkkarten können für einen Auftrag verwendet werden. Wenn der Saldo der Geschenkkarte nicht dem Betrag im Einkaufskorb entspricht, kann die Geschenkkarte mit einer anderen Zahlungsmethode kombiniert werden. Geschenkkarten können nur eingelöst werden, wenn der Debitor angemeldet ist.
- **Treuepunkte** – Dieses Modul ermöglicht einem Debitor für einen Auftrag zu bezahlen, indem er Treuepunkte verwendet. Es bietet eine Übersicht der verfügbaren Punkte und ablaufenden Punkten der Debitor kann die Punktzahl auswählen, die er für die Zahlung verwenden möchte. Wenn der Debitor nicht angemeldet ist oder kein Treuemitglied ist oder wenn der Gesamtbetrag im Einkaufskorb 0 (null) ist, wird dieses Modul automatisch ausgeblendet.
- **Zahlung** – Dieses Modul ermöglicht es einem Kunden, für eine Bestellung mit einer Kreditkarte zu bezahlen. Wenn der Gesamtbetrag im Einkaufskorb durch Treuepunkte oder mit einer Geschenkkate bezahlt ist oder 0 (null) ist, wird dieses Modul automatisch ausgeblendet. Die Kreditkartenintegration wird vom Adyen-Zahlungskonnektor in diesem Modul gewährleistet. Weitere Informationen dazu, wie dieser Konnektor verwendet wird, finden Sie unter [Connector für Adyen-Zahlungen für Dynamics 365](dev-itpro/adyen-connector.md).
- **Rechnungsadresse** – Dieses Modul ermöglicht einem Debitor Fakturierungsdaten bereitzustellen. Diese Informationen werden zusammen mit den Kreditkarteninformationen verarbeitet, die von Adyen bereitgestellt werden. Dieses Modul enthält eine Option, mti der die Debitoren die Rechnungsadresse als die Versandadresse verwenden können.
- **Kontaktinformationen** – Dieses Modul ermöglicht einem Debitor die Kontaktinformationen (E-Mail-Adresse) für einen Auftrag hinzuzufügen oder zu ändern.
- **Textblock** – Dieses Modul enthält ein beliebige Nachricht, die vom Content Management System (CMS) gesteuert wird. Kann beispielsweise eine Meldung enthalten, die lautet: „Für Probleme mit Ihrem Auftrag kontaktieren Sie 1-800-Fabrikam.“ 

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit-Interaktion

Die meisten Auschecken-Informationen, wie Postanschrift und Versandart werden im Warenkorb gespeichert und als Teil des Auftrags verarbeitet. Die einzige Ausnahme ist die Kreditkarteninformation. Diese Informationen werden verarbeitet, indem der Adyen-Zahlungskonnektor direkt verwendet wird. Die Zahlung ist genehmigt aber nicht belastet.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Um ein Auschecken-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

Um ein Auschecken-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Fragment \> Neues Fragment** und bezeichnen Sie das neue Fragment mit **Auscheckenfragment**.
1. Hinzufügen eines Auscheckenmoduls dem Fragment.
1. Hinzufügen eines Titels zum Auscheckenmodul.
1. Fügen Sie die Module Versandadresse, Lieferoptionen, Auscheckenabschnitt-Container und Kontaktinformationen hinzu. 
1. Fügen Sie im Auscheckenabschnitt-Containermodul die Module Geschenkkarte, Treuepunkte und Zahlung hinzu. Auf diese Weise stellen Sie sicher, dass alle Zahlungsmethoden zusammen in einem Abschnitt angezeigt werden.
1. Speichern Sie das Fragment und zeigen Sie es in der Vorschau an. Einige Module, die über keinen Kontext verfügen, können möglicherweise nicht in der Vorschau gerendert werden.
1. Beenden Sie die Bearbeitung des Fragments und veröffentlichen Sie es.
1. Hier können Sie eine Vorlage erstellen, die das neue Auschecken-Fragment verwendet.
1. Hier können Sie eine Auscheckensseite erstellen, die die neue Vorlage verwendet.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
