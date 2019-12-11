---
title: Checkoutmoduls
description: In diesem Thema wird beschrieben, wie Sie ein Auscheckenmodul einer Seite hinzufügen und die erforderlichen Eigenschaften festlegen.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697082"
---
# <a name="checkout-module"></a>Auschecken-Modul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie ein Auscheckenmodul einer Seite hinzufügen und die erforderlichen Eigenschaften festlegen.

## <a name="overview"></a>Übersicht

Ein Auscheckenmodul ist ein spezieller Container, der alle Module hostet, die erforderlich sind, um einen Auftrag zu erstellen. Ein Auscheckenmodul kann Module enthalten, die die Versandadresse, die Versandart, die Fakturierungsdaten, Auftragszusammenfassung und andere Informationen bearbeiten, die einem Kundenauftrag zugeordnet sind. Der Bericht stellt einen schrittweisen Fluss dar, die ein Kunde verwendet, um die gesamten relevanten Informationen einzugeben, um eine Bestellung abzuschließen.

Ein Auscheckenmodul rendert Daten basierend auf der Warkenkorb-Kennung Diese Kennung wird als Browsercookie gespeichert. Eine Einkaufskorb-Kennung ist erforderlich, um Informationen im Auscheckenmodul zu rendern, wie Artikel im Auftrag, im Gesamtbetrag und bei den Rabatten.

## <a name="checkout-module-properties"></a>Checkoutmodul-Eigenschaften

Ein Auscheckenmodul hostet einen enthaltenen Satz Module. Mit einer Breiteneigenschaft können Sie angeben, ob die Artikel im Auscheckenmodul die Breite der Kombination anpassen oder den Bildschirm ausfüllen sollen.

Ein Auscheckenmodul hat mehrere Slots, wie **Auscheckinformationen**, **Auftragszusammenfassung** und **Auftrag platziern**. Jeder Slot unterstützt einen Satz Module, die in einem bestimmten Layout auf der Seite angezeigt werden. Zum Beispiel beinhaltet der Slot **Auscheckeninformationen** alle Module, die erforderlich sind, um das Auschecken auszulösen, wie Module für die Postanschrift und die Zahlungsmethode. Der Slot **Auftragszusammenfassung** zeigt eine Auftragszusammenfassung an und unterstützt die Aktivität für das Sperren des Auftrags. Der **Ortsauftrag** Slot unterstützt zudem die Aktivität für das Sperren des Auftrags. Ortsauftragsmodule können in zwei Slots definiert werden, um den Prozess des Platzierens von Aufträgen aus verschiedenen Plattformen zu optimieren.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Module können im Auscheckmodul verwendet werden

- **Versandadresse** – Dieses Modul ermöglicht einem Debitor die Postanschrift für einen Auftrag hinzuzufügen oder auszuwählen. Wenn der Debitor angemeldet ist, werden alle zuvor gespeicherten Adressen für diesen Debitor angezeigt. Der Kunde kann diese dann unter den Adresse auswählen. Der Debitor kann auch eine neue Adresse hinzufügen. Die Versandadresse wird für alle Artikel im Auftrag verwendet, die Versand erfordern. Sie kann nicht für einzelne Positionen angepasst werden. Versandadresseformate werden für jedes Land oder Region definiert, und die länder-/regionsspezifischen Regeln werden für dieses Modul erzwungen. Obwohl dieses Modul keine Adressüberprüfung bereitstellt, kann die Adressüberprüfung ber die Anpassung implementiert werden. Wenn der Auftrag nur Artikel enthält, die im Shop abgeholt werden, wird dieses Modul automatisch ausgeblendet.
- **Lieferoptionen** – Dieses Modul ermöglicht einem Debitor eine Lieferoption für einen Auftrag auszuwählen. Lieferoptionen basieren auf der Versandadresse. Wenn die Versandadresse geändert wird, muss erneut die Lieferoptionen abgerufen werden. Wenn der Auftrag nur Artikel enthält, die im Shop abgeholt werden, wird dieses Modul automatisch ausgeblendet.
- **Containerabschnitt Auschecken** – Dieses Modul ist ein Container, der mehrere Module aufnehmen kann, um einen Bereich innerhalb des Auscheckflusses zu erstellen. So können Sie alle zahlungsrelevanten Module innerhalb dieses Containers speichern, damit diese in einem Bereich angezeigt werden. Dieses Modul wirkt sich nur auf das Layout des Flusses aus.
- **Geschenkkarte** – Dieses Modul ermöglicht es einem Debitor, für einen Auftrag mit einer Geschenkkarte zu bezahlen. Er unterstützt nur Microsoft Dynamics 365 Commerce Geschenkkarten. Eine oder mehrere Geschenkkarten können für einen Auftrag verwendet werden. Wenn der Saldo der Geschenkkarte nicht dem Betrag im Einkaufskorb entspricht, kann die Geschenkkarte mit einer anderen Zahlungsmethode kombiniert werden. Geschenkkarten können nur eingelöst werden, wenn der Debitor angemeldet ist.
- **Treuepunkte** – Dieses Modul ermöglicht einem Debitor für einen Auftrag zu bezahlen, indem er Treuepunkte verwendet. Es bietet eine Übersicht der verfügbaren Punkte und ablaufenden Punkten der Debitor kann die Punktzahl auswählen, die er für die Zahlung verwenden möchte. Wenn der Debitor nicht angemeldet ist oder kein Treuemitglied ist oder wenn der Gesamtbetrag im Einkaufskorb 0 (null) ist, wird dieses Modul automatisch ausgeblendet.
- **Kreditkarte** – Dieses Modul ermöglicht es einem Debitor, für einen Auftrag mit einer Kreditkarte zu bezahlen. Wenn der Gesamtbetrag im Einkaufskorb durch Treuepunkte oder mit einer Geschenkkate bezahlt ist oder 0 (null) ist, wird dieses Modul automatisch ausgeblendet. Kreditkartenintegration wird aus dem Adyen-Zahlungskonnektor bereitgestellt. Weitere Informationen dazu, wie dieser Konnektor verwendet wird, finden Sie unter [Adyen Zahlungskonnektor](https://).
- **Rechnungsadresse** – Dieses Modul ermöglicht einem Debitor Fakturierungsdaten bereitzustellen. Diese Informationen werden zusammen mit den Kreditkarteninformationen verarbeitet, die von Adyen bereitgestellt werden. Dieses Modul enthält eine Option, mti der die Debitoren die Rechnungsadresse als die Versandadresse verwenden können.
- **Kontaktinformationen** – Dieses Modul ermöglicht einem Debitor die Kontaktinformationen (E-Mail-Adresse) für einen Auftrag hinzuzufügen oder zu ändern.
- **Auftrage aufgeben** – Dieses Modul ermöglicht einem Debitor einen Auftrag zu erteilen.
- **Umfangreicher Inhaltsblock** – Dieses Modul enthält ein beliebige Nachricht, die vom Content Management System (CMS) gesteuert wird. Kann beispielsweise eine Meldung enthalten, die angibt, „für Probleme mit Ihrem Auftrag kontaktieren Sie 1-800-FABRIKAM.“ 
- **Auftragszusammenfassung** – Dieses Modul zeigt die Kostenaufschlüsselung eines Auftrags an.
- **Auftragspositionen** – Dieses Modul zeigt eine Übersicht der Artikel, die in einem Auftrag enthalten sind.

## <a name="retail-server-interaction"></a>Retail Server-Interaktion

Die meisten Auschecken-Informationen, wie Postanschrift und Versandart werden im Warenkorb gespeichert und als Teil des Auftrags verarbeitet. Die einzige Ausnahme ist die Kreditkarteninformation. Diese Informationen werden verarbeitet, indem der Adyen-Zahlungskonnektor direkt verwendet wird. Die Zahlung ist genehmigt aber nicht belastet.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Um ein Auschecken-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

Um ein Auschecken-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Fragment \> Neues Fragment** und bezeichnen Sie das neue Fragment mit **Auscheckenfragment**.
1. Hinzufügen eines Auscheckenmoduls dem Fragment.
1. Hinzufügen eines Titels zum Auscheckenmodul.
1. Im Slot **Auscheckeninformationen** fügen Sie die Module Versandadresse, Lieferoptionen, Auschecken-Abschnitt und Kontaktinformationen hinzu. Es sollten nun vier Bereiche im **Auscheckeninformationen** Slot haben.
1. Fügen Sie im Auscheckenabschnitt-Containermodul die Module Geschenkkarte, Treuepunkte und Kreditkarte hinzu. Auf diese Weise stellen Sie sicher, dass alle Zahlungsmethoden zusammen in einem Abschnitt angezeigt werden.
1. Im Slot **Auftragszusammenfassung** fügen Sie die Module Auftragszusammenfassung, Auftrag aufgeben und umfangreicher Inhaltsblock hinzu.
1. Im umfangreichen Inhaltsblockmodul fügen Sie den folgenden Text hinzu **Für Fragen über Ihren Auftrag, kontaktieren Sie 1-800-FABRIKAM.**
1. Im Slot **Auftrag ausführen** fügen Sie Modul Auftrag ausführe hinzu.
1. Wählen Sie **Speichern**. Einige Module können in der Vorschau nicht gerendert werden, weil Sie keinen Einkaufswagenkontext haben.
1. Laden Sie das Fragment hoch und veröffentlichen Sie es.
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
