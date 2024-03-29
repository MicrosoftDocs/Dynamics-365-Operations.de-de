---
title: Feldbeschreibungen anzeigen und exportieren
description: Dieser Artikel erläutert, wie eine Feldbeschreibung angezeigt und die Seite "Feldbeschreibungen" verwendet wird, um eine Beschreibung zu exportieren.
author: twheeloc
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.form: FieldDescriptions
ms.openlocfilehash: d2d59796b312d50d69bf7722b605c159a933a283
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292365"
---
# <a name="view-and-export-field-descriptions"></a>Feldbeschreibungen anzeigen und exportieren

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Dieser Artikel erläutert, wie eine Feldbeschreibung angezeigt und die Seite "Feldbeschreibungen" verwendet wird, um eine Beschreibung zu exportieren.

Einige der komplexeren Felder haben Beschreibungen. Diese Beschreibungen werden angezeigt, wenn Sie den Mauszeiger über ein Feld bewegen. Sie können Bescheibungen auf der Seite **Feldbeschreibungen** anzeigen und exportieren.

Nicht alle Seiten haben Feldbeschreibungen. Wir möchten Beschreibungen nur für die komplexeren Felder bereitstellen, und nicht für Felder, bei denen die Verwendung offensichtlich ist. Daher verfügen einige Seiten über keine Feldbeschreibungen, andere über ein paar und komplexeren Seiten, wie ein Großteil der Parameter-Seiten, verfügen über viele Beschreibungen.

Wenn Sie Zugriff auf die Entwicklungsumgebung haben, können Sie neue Feldbeschreibungen hinzufügen. Beispielsweise können Sie einer Feldbeschreibung unternehmensspezifische Informationen hinzufügen. Weitere Informationen finden Sie unter [Feldbeschreibungen anpassen](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Siehe hierzu auch die Feldbeschreibungen auf der Benutzeroberfläche.

Sie können Felder anzeigen, indem Sie über ein Feld fahren. Ist keine Beschreibung verfügbar, sehen Sie den Feldnamen beim Bewegen über das Feld.

> [!NOTE]
> In Dynamics AX 7.0. (Februar 2016) können Feldbeschreibungen nur auf der Seite **Feldbeschreibungen** eingesehen werden.

Die folgende Abbildung zeigt die Feldbeschreibung, die angezeigt wird, wenn Sie mit den Mauszeiger über das Feld **Artikel während der Inventur sperren** bewegen.

[![Beispiel einer Feldbeschreibung.](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Verwenden Sie die Seite "Feldbeschreibung", um Feldhilfe anzuzeigen und zu exportieren.

Die Seite **Feldbeschreibungen** ermöglicht es Ihnen, Feldbeschreibungen anzuzeigen und zu exportieren. Sie können die Beschreibungen finden, die für eine Seite jeweils verfügbar sind.

### <a name="view-the-descriptions-for-a-page"></a>Die Beschreibungen für eine Seite anzeigen

Um die Beschreibungen einer Seite anzuzeigen, führen Sie diesen Schritt aus:

- Geben Sie im Feld **Eine Seite auswählen** den Namen der Seite ein. Alternativ klicken Sie auf den Pfeil, um eine Liste aller Seiten öffnen und dann die Liste zu durchsuchen oder zu filtern.

Sie können beispielsweise den Namen der Seite verwenden, der in der Benutzeroberfläche (UI)angezeigt wird (z. B. **Debitoren**) oder den Codename (AOT-Name), der verfügbar ist, wenn man mit der rechten Maustaste auf eine Seite klickt (z. B. **CustTable**).

Informationen über die verschiedenen Methoden zum Filtern der Seitenliste finden Sie Abschnitt "Nach einer Seite suchen" weiter unten in diesem Artikel.

Wenn Sie die Option **Felder ohne eine Beschreibung einbeziehen** auf **Ja** festlegen, werden alle Felder auf der Seite angezeigt, unabhängig davon, ob sie eine Feldbeschreibung haben.

### <a name="export-the-descriptions-for-a-page"></a>Die Beschreibungen für eine Seite exportieren

Um die Beschreibungen einer Seite zu exportieren, führen Sie die folgenden Schritte aus:

1. Wählen Sie im Feld **Eine Seite auswählen** eine Seite aus.
2. Klicken Sie auf die Schaltfläche **In Microsoft Office öffnen** in der oberen rechten Ecke und dann auf **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Nach einer Seite suchen

Es gibt mehrere Möglichkeiten, im Feld **Eine Seite auswählen** eine Seite zu suchen. In vielen Fällen müssen Sie auf den Pfeil im Feld **Eine Seite auswählen** klicken, um die Dropdownliste zu öffnen und aus einer gefilterten Liste von Seiten auszuwählen.

- Geben Sie einen Teil des Namens ein, und öffnen Sie dann die Dropdownliste, um aus einer gefilterten Liste von Seiten auszuwählen.
- Öffnen Sie die Dropdownliste und klicken Sie entweder auf die Überschrift **Seitenname** oben auf der Liste oder auf die Überschrift **AOT-Name der Seite**. Dadurch wird ein Dialogfeld geöffnet, in dem Sie erweiterte Filteroptionen verwenden können, wie **Seitenname beginnt mit**.
- Geben Sie den vollständigen Namen der Seite ein. Wenn Sie diese Option verwenden, empfiehlt es sich, die Dropdownliste zu öffnen, um zu sehen, was noch in der Liste ist, auch wenn Feldbeschreibungen angezeigt werden.

    - Wenn es eine einzelne exakte Entsprechung des Namens gibt, werden die Feldbeschreibungen für diese Seite angezeigt.
    - Wenn mehr als eine exakte Übereinstimmung vorliegt, werden keine Beschreibungen angezeigt. Öffnen Sie die Dropdownliste, und wählen Sie die gewünschte Seite.
    - Wenn der Name, den Sie eingeben, Teil des Namens einer anderen Seite ist, werden die Beschreibung für Ihre Seite angezeigt. Wenn Sie aber die Liste öffnen, sehen Sie zusätzliche Seiten, die diesen Namen beinhalten.

Es werden beispielsweise keine Beschreibungen angezeigt, wenn Sie im Feld **Eine Seite auswählen** **Inventur** eingeben. Wenn Sie die Dropdownliste öffnen, sehen Sie, dass es zwei Seiten mit der Bezeichnung **Inventur** gibt, sowie mehrere Seiten, die das Wort "Inventur" im Namen enthalten. Wenn Sie die Seite auswählen, die den AOT-Namen **InventJournalCount** hat, werden die Feldbeschreibungen für diese Seite angezeigt. Wenn Sie jedoch die Dropdownliste erneut öffnen, werden Sie sehen, dass die Liste jetzt alle Seiten enthält, die "InventJournalCount" als Teil ihres AOT-Seitennamens haben.

## <a name="troubleshooting"></a>Problembehandlung

In den folgenden Abschnitten finden Sie Informationen, zur Behebung von Problem, die auftreten können, wenn Sie Feldbeschreibungen verwenden.

### <a name="i-cant-find-a-field-description"></a>Ich kann eine Feldbeschreibung nicht finden

Wir sind daran, Beschreibungen für die komplexeren Felder hinzuzufügen. Wenn Sie Hilfe zu einem bestimmten Feld benötigen, informieren Sie uns, indem Sie diesem Artikel einen Kommentar hinzufügen.

### <a name="the-field-description-isnt-helpful"></a>Die Feldbeschreibung ist nicht hilfreich

Informieren Sie uns, indem Sie diesem Artikel einen Kommentar hinzufügen. Wenn möglich, beschreiben Sie die zusätzlichen Informationen, die Sie benötigen.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Ich kann ein Feld auf der Seite "Feldbeschreibung" nicht finden

Um alle Felder auf einer Seite anzuzeigen, setzen Sie die Option **Inklusive-Felder ohne eine Beschreibung** auf **Ja** fest. Klicken Sie auf das Feld **Seite auswählen**, um sicherzustellen, dass Sie die richtige Seite ausgewählt haben. Wenn der eingegebene Name Teil eines anderen Feldnamens ist, haben Sie möglicherweise die Seite mit dem längeren Namen ausgewählt.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Ich kann eine Seite auf der Seite "Feldbeschreibung" nicht finden

Informationen über die verschiedenen Methoden zum Suchen von Seiten finden Sie Abschnitt "Nach einer Seite suchen" weiter oben in diesem Artikel. Wenn Sie den genauen Namen der Seite eingegeben haben, werden die Feldbeschreibungen möglicherweise nicht angezeigt, wenn mehr als eine Seite gleichen Namens vorhanden ist. Klicken Sie auf den Pfeil im Feld **Eine Seite auswählen**, um eine gefilterte Liste der verfügbaren Seiten zu öffnen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Anpassen von Feldbeschreibungen](../../dev-itpro/user-interface/customize-field-help.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
