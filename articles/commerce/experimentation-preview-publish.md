---
title: Vorschau und Veröffentlichung eines Experiments
description: In diesem Artikel wird beschrieben, wie Sie ein Experiment in Dynamics 365 Commerce in der Vorschau anzeigen und veröffentlichen.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946132"
---
# <a name="preview-and-publish-an-experiment"></a>Vorschau und Veröffentlichung eines Experiments

In diesem Artikel wird beschrieben, wie Sie in Dynamics 365 Commerce eine Vorschau Ihres Experiments anzeigen und veröffentlichen, nachdem Sie [Ihr Experiment verbunden und Ihre Variationen bearbeitet haben](experimentation-connect-edit.md). Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind. Weitere Schritte werden in separaten Artikeln behandelt.

[ ![User Journey zum Experimentieren – Vorschau und Veröffentlichung.](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Eine Vorschau Ihrer Experimentvarianten anzeigen
Sie können eine Vorschau Ihrer Variationen anzeigen und sie weiter bearbeiten, bis sie so aussehen, wie Sie es möchten.

Um Ihre Experimentvariationen im Commerce Site Builder anzusehen, folgen Sie diesen Schritten.

1. Verwenden Sie im Site Builder das Dropdown-Menü für Variationen unterhalb der Befehlsleiste, um den Inhalt auszuwählen, für den Sie die Vorschau anzeigen möchten. 
1. Wählen Sie in der Befehlsleiste **Vorschau** aus. Eine Vorschau des Inhalts, wenn er veröffentlicht wird, wird angezeigt.
1. Um eine Vorschau einer anderen Variante anzuzeigen, wählen Sie sie aus dem Dropdown-Menü aus, und wählen Sie nochmal **Vorschau**.

## <a name="publish-your-experiment"></a>Ihr Experiment veröffentlichen
Wenn Sie keine Veröffentlichungsgruppe verwenden, um zu planen, wann Ihr Experiment live geschaltet wird, und Sie sofort veröffentlichen möchten, wählen Sie **Veröffentlichen** in der Befehlsleiste. Alle zum Experiment gehörenden Variationen werden veröffentlicht.
    
> [!IMPORTANT]
> Wenn die Seite eine unveröffentlichte URL enthält, müssen Sie zuerst die URL veröffentlichen, da sie sonst für die Benutzer Ihrer Website nicht sichtbar ist. Weitere Details finden Sie unter [Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Verwenden Sie Veröffentlichungsgruppen, um zu planen, wann Ihr Experiment live geschaltet wird
Im Site Builder erstellte Variationen können mithilfe einer Veröffentlichungsgruppe für die Veröffentlichung geplant werden. Innerhalb einer Veröffentlichungsgruppe können Sie eine Seite oder ein Fragment mit Ihrem Experiment verbinden, indem Sie **Experimente** im linken Navigationsbereich auswählen. Sie können dies auch tun, indem Sie **Seiten** oder **Fragmente** auswählen und den Anweisungen in [Verbinden Sie ein Experiment an und bearbeiten Sie Variationen](experimentation-connect-edit.md) folgen. Weitere Informationen zu Veröffentlichungsgruppen finden Sie unter [Arbeiten mit Veröffentlichungsgruppen](publish-groups.md).

Bei der Verwendung von Veröffentlichungsgruppen mit Experimenten sind einige wichtige Überlegungen zu beachten.
- Wenn Sie einer Veröffentlichungsgruppe eine Seite oder ein Fragment hinzufügen, an der bzw. dem ein Experiment ausgeführt wird, wird das Experiment von der Seite oder dem Fragment in der Veröffentlichungsgruppe entfernt.
- Experimente, die mit Seiten einer Live-Site verbunden sind, stehen Seiten innerhalb von Veröffentlichungsgruppen nicht zur Verfügung und umgekehrt. Ebenso stehen Seiten, an denen Experimente in einer Live-Site ausgeführt werden, anderen Experimenten in Veröffentlichungsgruppen nicht zur Verfügung und umgekehrt.
- Wenn Sie eine Veröffentlichungsgruppe veröffentlichen oder planen, wird der gesamte Inhalt der Veröffentlichungsgruppe veröffentlicht, unabhängig davon, ob der Veröffentlichungsgruppe ein Experiment zugeordnet ist.
- Da eine Veröffentlichungsgruppe nach der Veröffentlichung auf einer Live-Site weiterhin besteht, bleiben auch die Experimente in der Veröffentlichungsgruppe bestehen. Daher können Sie andere Experimente nicht mit derselben Seite oder demselben Fragment verknüpfen. Um diese Einschränkung zu vermeiden, löschen Sie alle Veröffentlichungsgruppen mit bestehenden Experimenten. Wenn Sie ein Experiment auf einer Live-Site löschen möchten, das auch in einer Veröffentlichungsgruppe vorhanden ist, löschen Sie es zuerst aus der Veröffentlichungsgruppe.

### <a name="force-variations-for-testing"></a>Variationen zum Testen erzwingen

Sobald der Test live ist, können Sie die Test-ID und die Variations-ID an die URL der Standardseite anhängen, um eine Variation zu Test- oder Automatisierungszwecken zu erzwingen. Wenn beispielsweise die Standardseiten-URL lautet `https://fabrikam.com/modern/homepage`, können Sie eine Variation mit einer URL wie `https://fabrikam.com/modern/homepage?exp=18012910471|18024360464` erzwingen. Sie können die Test-ID und die Variations-ID für Ihre Testvariation aus der Vorschau-URL in **Vorschau** Erfahrung oben erklärt abrufen.

## <a name="previous-step"></a>Vorheriger Schritt
[Experiment verbinden und bearbeiten](experimentation-connect-edit.md)

## <a name="next-step"></a>Nächster Schritt
[Experiment durchführen und überwachen](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
