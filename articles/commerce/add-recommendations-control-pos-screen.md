---
title: Empfehlungen dem Transaktionsbildschirm hinzufügen
description: In diesem Artikel wird beschrieben, wie Sie ein Empfehlungssteuerelement zum Transaktionsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 Commerce hinzufügen.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4748ade8d6693666b58cbded2123d3449d191509
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862071"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Empfehlungen dem Transaktionsbildschirm hinzufügen

[!include [banner](includes/banner.md)]


In diesem Artikel wird beschrieben, wie Sie ein Empfehlungssteuerelement zum Transaktionsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 Commerce hinzufügen. Weitere Informationen zu Produktempfehlungsfunktionen finden Sie im [Produktempfehlungsüberblick zur POS-Dokumentation.](product.md).


Sie können Produktempfehlungen auf Ihrem POS-Gerät anzeigen, wenn Sie Commerce verwenden. Um Produktempfehlungen anzuzeigen, müssen Sie dem Buchungsbildschirm eine Steuerung mithilfe des Bildschirmlayoutdesigners hinzufügen. 

## <a name="open-layout-designer"></a>Layoutdesigner öffnen

1. Wechseln Sie zu **Einzelhandel und Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS** &gt; **Bildschirmlayouts**.
2. Suchen Sie mithilfe der Filteroptionen den Bildschirm, dem Sie eine Steuerung hinzufügen möchten. Filtern Sie beispielsweise im Feld **Bildschirmlayout-ID** mit einem Wert von **F2CP16:9M**.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie beispielsweise **Name: F2CP16: 9M Bildschirmlayout-ID: F2CP16: 9M**.
4. Klicken Sie auf **Layout-Designer**
5. Folgen Sie den Aufforderungen, um den Layout-Designer zu starten. Wenn Sie aufgefordert werden, die Anmeldeinformationen einzugeben, geben Sie die gleichen Anmeldeinformationen ein, die verwendet wurden, als die Seite **Bildschirmlayouts** ausgelöst wurde.
6. Wenn Sie sich anmelden, erscheint eine Seite, ähnlich jener unten. Das Layout ist verschieden, abhängig von den Anpassungen, die für Ihre Filiale vorgenommen wurden.


    [![Layout-Designer.](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Einen Anzeigeoption auswählen

Es stehen zwei Optionen für die Konfiguration zur Verfügung. Wählen Sie die Option, die am besten für Ihren Shop passt und folgen Sie den Anweisungen, um die Steueurung eizrichten. Es gibt zwei Optionen:

- Empfehlungen sind immer angezeigt.
- A Registerkarte **Empfehlungen** wird im Gitter auf der rechten Seite des Bildschirms angezeigt.

### <a name="make-recommendations-always-visible"></a>Empfehlungen immer sichtbar machen


1. Reduzieren Sie die Höhe des Buchungspositionsdetailbereichs, so dass er die gleiche Höhe hat wie der Debitorenbereich links.


    [![Höhe des Buchungspositionsdetail-Bereichs reduziert.](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Klicken Sie im Menü auf der linken Seite, und ziehen Sie das Empfehlungssteuerelement zwischen den Buchungspositionsdetailbereich und den Schaltflächenraster im mittleren unteren Transaktlions-Bildschirmrands. Ändern Sie die Steuerung, so dass die Größe in diesen Bereich passt.

    [![Empfehlungssteuerelement dem Layout hinzugefügt.](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.
4. In Commerce gehen Sie zu **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Verteilungszeitpläne**.
5. Wählen Sie in der **1090 Anmelden**
6. Klicken Sie auf **Jetzt ausführen**


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Eine Registerkarte "Empfehlungen" dem Schaltflächengitter auf der rechten Seite des Bildschirms hinzufügen

1. Machen Sie einen Rechtsklick im Leerraum unter der letzten Registerkarte im Schaltflächenraster auf der rechten Seite.

2. Klicken Sie auf **Anpassen**.

    [![Anpassung – Registerkartensteuerelement-Dialogfeld.](./media/pic-5.png)](./media/pic-5.png)

3. Klicken Sie auf **Neue Registerkarte**
4. Suchen Sie die neue Registerkarte, die Sie hinzugefügt haben. Sie müssen möglicherweise einen Bildlauf nach unten machen.
5. Wählen Sie im Dropdown-Menü unter **Inhalte** **Empfohlene Produkte**.

    [![Auswählen empfohlener Produkte im Feld „Inhalte“.](./media/pic-6.png)](./media/pic-6.png)

6. Wählen Sie im Feld **Beschriftung** einen Namen für die Registerkarte "Empfehlungen". Zum Beispiel Tpy 'Empfohlene Produkte'.
7. Wählen Sie im Feld **Fild** das Bild, das auf der Registerkarte angezeigt werden soll.
8. Klicken Sie auf **OK**. Die Registerkarte wird im neuen Schaltflächenraster angezeigt.
9. Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.
10. In Commerce gehen Sie zu **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Verteilungszeitpläne**.
11. Wählen Sie in der **1090 Anmelden**
12. Klicken Sie auf **Jetzt ausführen**

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung](enable-adls-environment.md)

[Produktempfehlungen aktivieren](enable-product-recommendations.md)

[Personalisierte Empfehlungen aktivieren](personalized-recommendations.md)

[Personalisierte Empfehlungen kündigen](personalization-gdpr.md)

[Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren](shop-similar-looks.md)

[Produktempfehlungen in POS hinzufügen](product.md)

[Anpassung der Ergebnisse der AI-ML-Empfehlungen](modify-product-recommendation-results.md)

[Manuell kuratierte Empfehlungen erstellen](create-editorial-recommendation-lists.md)

[Empfehlungen mit Demodaten erstellen](product-recommendations-demo-data.md)

[Produktempfehlungs-FAQs](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]