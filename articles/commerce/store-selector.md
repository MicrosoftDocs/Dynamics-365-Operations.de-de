---
title: Shopauswahlmodul
description: Dieser Artikel enthält das Siteauswahlmodul und es wird beschrieben, wie Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268326"
---
# <a name="store-selector-module"></a>Shopauswahlmodul

[!include [banner](includes/banner.md)]

Dieser Artikel enthält das Siteauswahlmodul und es wird beschrieben, wie Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Kunden können das Filialauswahlmodul verwenden, um ein Produkt in einem ausgewählten Geschäft nach einem Onlinekauf abzuholen. In der Commerce-Version 10.0.13 enthält das Shopauswahlmodul auch zusätzliche Funktionen, mit denen eine Seite **Geschäft suchen** angezeigt werden kann, die Geschäfte in der Nähe zeigt.

Mit dem Filialauswahlmodul können Benutzer einen Ort (Stadt, Bundesland, Adresse usw.) eingeben, um nach Filialen innerhalb eines Suchradius zu suchen. Beim ersten Öffnen des Moduls wird der Browserstandort des Kunden verwendet, um Geschäfte zu suchen (sofern eine Einwilligung vorliegt).

## <a name="store-selector-module-usage"></a>Verwendung des Shopauswahlmodul

- Ein Shopauswahlmodul kann auf einer Produktdetailseite (PDP) verwendet werden, um ein Geschäft zur Abholung auszuwählen.
- Ein Shopauswahlmodul kann auf einer Warenkorbseite verwendet werden, um ein Geschäft zur Abholung auszuwählen.
- Ein Shopauswahlmodul kann auf einer eigenständigen Seite verwendet werden, auf der alle verfügbaren Geschäfte angezeigt werden.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Erfüllungsgruppen-Einrichtung in der Commerce-Zentralverwaltung

Damit die Shopauswahl verfügbare Geschäfte anzeigen kann, muss die Erfüllungsgruppe in der Commerce-Zentralverwaltung eingerichtet werden. Weitere Informationen finden Sie unter [Erfüllungsgruppen einrichten](customer-orders-overview.md#set-up-fulfillment-groups).

Darüber hinaus müssen für jedes Geschäft in der Erfüllungsgruppe der Breiten- und Längengrad des Geschäftsstandorts in der Zentralverwaltung definiert werden.

Um den Längen- und Breitengrad für den Geschäftsstandort in der Commerce-Zentralverwaltung zu konfigurieren, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Lagerverwaltung \> Einstellungen \> Lageraufschlüsselung**.
1. Wählen Sie im linken Bereiche den Lagerortstandort aus.
1. Wählen Sie im Inforegister **Adressen** **Erweitert** aus.

    ![Beispiel für Geschäftsdetails in der Zentralverwaltung.](./media/Store-address.png)

1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Geben Sie im Inforegister **Allgemein** Werte für **Breitengrad** und **Längengrad**.

    ![Beispiel für die Einrichtung von Längen- und Breitengraden für ein Geschäft in der Zentralverwaltung.](./media/Store-latitude-longitude.png)

1. Wählen Sie im Aktionsbereich **Speichern** aus. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Geschäft aus dem Geschäftsauswahlmodul ausblenden

Einige Geschäfte in einer Auftragserfüllungsgruppe sind möglicherweise keine gültigen Abholorte. Um sicherzustellen, dass nur gültige Abholorte als Optionen im Geschäftsauswahlmodul angezeigt werden, befolgen Sie diese Schritte in Commerce headquarters.

1. Gehen Sie zu **Retail und Commerce \> Commerce-Einrichtung \> Auftragserfüllungsgruppen \> Alle Geschäfte**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Löschen Sie unter **Einrichtung** für jedes Geschäft, das kein gültiger Abholort ist, das Kontrollkästchen **Ist ein Abholort**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Führen Sie den Verteilungsplan-Einzelvorgang 1070 **Kanalkonfiguration** aus.

## <a name="bing-maps-integration"></a>Bing Maps-Integration

Das Filialauswahlmodul ist in die [Bing Maps REST-Anwendungsprogrammierschnittstellen (APIs)](/bingmaps/rest-services/) integriert, um die Geocodierungs- und Vorschlagssuchfunktionen von Bing zu verwenden. Ein Bing Maps-API-Schlüssel ist erforderlich und muss auf der Seite „Freigegebene Parameter“ in Commerce Headquarters hinzugefügt werden. Die Geocodierungs-API wird verwendet, um einen Standort in Breiten- und Längengrade umzuwandeln. Die Integration in die Vorschlagssuche-API wird verwendet, um Suchvorschläge anzuzeigen, wenn Benutzer Standorte in das Suchfeld eingeben.

Für die Vorschlagssuche-REST-API müssen Sie sicherstellen, dass die folgenden URLs gemäß der Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) Ihrer Website zulässig sind (Content Security Policy, CSP). Diese Einstellung erfolgt im Commerce Site Builder, indem zulässige URLs zu verschiedenen Inhaltssicherheitsrichtlinien der Website hinzugefügt werden (z. B. **img-src**). Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie](manage-csp.md). 

- Fügen Sie der **connect-src**-Richtlinie **&#42;.bing.com** hinzu.
- Fügen Sie der **img-src**-Richtlinie **&#42;.virtualearth.net** hinzu.
- Fügen Sie der **script-src**-Richtlinie **&#42;.bing.com und &#42;.virtualearth.net** hinzu.
- Fügen Sie der **script style-src**-Richtlinie **&#42;.bing.com** hinzu.

## <a name="pickup-in-store-mode"></a>Modus „Im Shop abholen“

Das Filialauswahlmodul unterstützt den Modus **Im Shop abholen**, der eine Liste der Geschäfte anzeigt, in denen ein Produkt zur Abholung verfügbar ist. Außerdem werden die Öffnungszeiten und der Produktbestand für jedes Geschäft in der Liste angezeigt. Das Shopauswahlmodul benötigt den Kontext eines Produkts, um die Produktverfügbarkeit zu rendern und damit der Benutzer das Produkt zum Warenkorb hinzufügen kann, wenn der Liefermodus des Produkts auf **Abholung** im ausgewählten Geschäft festgelegt ist. Weitere Informationen finden Sie unter [Bestandseinstellungen](inventory-settings.md). 

Das Shopauswahlmodul kann einem Kauffeldmodul auf einer PDP-Seite hinzugefügt werden, um Filialen anzuzeigen, in denen ein Produkt zur Abholung verfügbar ist. Es kann auch einem Einkaufswagenmodul hinzugefügt werden. In diesem Fall zeigt das Filialauswahlmodul die Abholoptionen für jeden Positionsartikel im Warenkorb an. Das Shopauswahlmodul kann auch über Erweiterungen und Anpassungen zu anderen Seiten oder Modulen hinzugefügt werden.

Damit dieses Szenario funktioniert, sollten Produkte so konfiguriert werden, dass der Liefermodus **Abholung** verwendet wird. Andernfalls wird das Modul nicht auf den Produktseiten angezeigt. Einzelheiten zum Konfigurieren des Liefermodus finden Sie unter [Lieferarten einrichten](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Das folgende Bild zeigt ein Beispiel eines Speicherauswahlmoduls, das auf einem PDP verwendet wird.

![Beispiel eines in einer PDP verwendeten Shopauswahlmoduls.](./media/BOPIS.PNG)

> [!NOTE]
> In Version 10.0.16 und höher kann eine neue Funktion aktiviert werden, mit der eine Organisation mehrere Optionen für Abhollieferarten für Kunden definieren kann.  Wenn diese Funktion aktiviert ist, werden die Ladenauswahl und andere Module von E-Commerce erweitert, um es den Einkäufern zu ermöglichen, aus möglicherweise mehreren Abhollieferoptionen auszuwählen, sofern diese konfiguriert sind.  Weitere Informationen zu dieser Funktion finden Sie in [dieser Dokumentation](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Modus „Geschäfte suchen“

Das Filialauswahlmodul unterstützt auch den Modus **Geschäfte suchen**. In diesem Modus kann eine Geschäftsstandortseite erstellt werden, auf der die verfügbaren Geschäfte und ihre Informationen angezeigt werden. In diesem Modus funktioniert das Shopauswahlmodul ohne Produktkontext und kann als eigenständiges Modul auf jeder Websiteseite verwendet werden. Wenn die relevanten Einstellungen für das Modul aktiviert sind, können Benutzer außerdem ein Geschäft als ihr bevorzugtes Geschäft auswählen. Wenn ein Geschäft als bevorzugtes Geschäft eines Benutzers ausgewählt wird, wird die Geschäfts-ID im Browsercookie beibehalten. Daher muss der Benutzer eine Cookiezustimmungsnachricht akzeptieren.

Die folgende Abbildung zeigt ein Beispiel eines Filialauswahlmoduls, das zusammen mit einem Kartenmodul auf einer Geschäftsstandortseite verwendet wird.

![Beispiel eines Shopauswahlmoduls und eines Kartenmoduls auf einer Seite mit Shopstandorten.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Eine Karte rendern

Das Shopauswahlmodul kann zusammen mit dem Kartenmodul verwendet werden, um die Geschäftsstandorte auf einer Karte anzuzeigen. Weitere Informationen zum Kartenmodul finden Sie unter [Kartenmodul](map-module.md).

## <a name="store-selector-module-properties"></a>Eigenschaften des Shopauswahlmoduls

| Eigenschaftenname | Wert | Beschreibung |
|---------------|-------|-------------|
| Überschrift | Text | Die Überschrift für das Modul. |
| Modus | **Geschäfte suchen** oder **Im Shop abholen** | Der Modus **Geschäfte suchen** zeigt verfügbare Geschäfte an. Im Modus **Im Shop abholen** können Benutzer ein Geschäft zur Abholung auswählen. |
| Stil | **Dialog** oder **Inline** | Das Modul kann entweder inline oder in einem Dialogfeld gerendert werden. |
| Als bevorzugter Shop festlegen | **True** oder **False** | Wenn diese Eigenschaft auf **True** festgelegt ist, können Benutzer einen bevorzugten Shop festlegen. Für diese Funktion müssen Benutzer eine Cookiezustimmungsnachricht akzeptieren. |
| Alle Shops anzeigen | **True** oder **False** | Wenn diese Eigenschaft auf **True** festgelegt ist, können Benutzer die Eigenschaft **Suchradius** umgehen und alle Geschäfte anzeigen. |
| Vorschlagssuchoptionen: Maximale Ergebnisse | Nummer | Diese Eigenschaft definiert die maximale Anzahl von Vorschlagssuchergebnissen, die über die Bing Vorschlagssuche-API angezeigt werden können. |
| Suchradius | Nummer | Diese Eigenschaft definiert den Suchradius für Geschäfte in Meilen. Wenn kein Wert angegeben wird, wird der Standardsuchradius von 50 Meilen verwendet. |
| Nutzungsbedingungen | URL |  Diese Eigenschaft gibt die URL zu den Nutzungsbedingungen an, die für die Verwendung des Bing Maps-Dienstes erforderlich ist. |

## <a name="site-settings"></a>Standorteinstellungen

Das Shopauswahlmodul respektiert die [Einstellungen „Produkt in den Warenkorb legen“](add-cart-settings.md). Nachdem ein Artikel über das Shopauswahlmodul zum Warenkorb hinzugefügt wurde, sehen Website-Benutzer die entsprechend konfigurierten Workflows.

## <a name="add-a-store-selector-module-to-a-page"></a>Hinzufügen eines Shopauswahlmoduls zu einer Seite

Im Modus **Im Shop abholen** kann das Modul nur auf PDPs und Warenkorbseiten verwendet werden. Sie müssen den Modus auf **Im Shop abholen** im Eigenschaftsbereich des Moduls festlegen.

- Informationen zum Hinzufügen eines Shopauswahlmoduls zu einem Kauffeldmodul finden Sie unter [Kauffeldmodul](add-buy-box.md). 
- Informationen zum Hinzufügen eines Shopauswahlmoduls zu einem Einkaufswagenmodul finden Sie unter [Einkaufswagenmodul](add-cart-module.md)

Führen Sie die folgenden Schritte aus, um das Filialauswahlmodul so zu konfigurieren, dass verfügbare Filialen für eine Geschäftsstandortseite angezeigt werden, wie in der Abbildung weiter oben in diesem Artikel dargestellt.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** geben Sie unter **Vorlagenname** **Containervorlage** ein und wählen Sie **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. Im Dialogfenster **Eine neue Seite erstellen** geben Sie unter **Seitenname** **Store-Standorte** ein und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Wählen Sie eine Vorlage** die **Marketing-Vorlage**, die Sie erstellt haben, und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** ein Seitenlayout (z.B. **Flexibles Layout**) und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**. 
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie in der Dialogbox **Module auswählen** das Modul **Container mit 2 Spalten** und wählen Sie dann **OK**.
1. Legen Sie im Eigenschaftsbereich des Moduls den **Breite**-Wert auf **Container füllen** fest.
1. Legen Sie den Wert **Portspaltenkonfiguration für sehr kleine Ansicht** auf **100 %** fest.
1. Legen Sie den Wert **Portspaltenkonfiguration für kleine Ansicht** auf **100 %** fest.
1. Legen Sie den Wert **Portspaltenkonfiguration für mittlere Ansicht** auf **33 % 67 %** fest.
1. Legen Sie den Wert **Portspaltenkonfiguration für große Ansicht** auf **33 % 67 %** fest.
1. Im Bereich **Container mit 2 Spalten** markieren Sie die Auslassungspunkte (**...**) und wählen dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Auswahl speichern** und dann **OK** aus.
1. Legen Sie im Eigenschaftsbereich des Moduls den **Modus**-Wert auf **Geschäfte suchen** fest.
1. Legen Sie den Wert **Suchradius** in Meilen fest.
1. Legen Sie andere Eigenschaften wie z. B. **Als bevorzugten Shop festlegen**, **Alle Geschäfte anzeigen** und **Automatischen Vorschlag aktivieren** nach Bedarf fest.
1. Im Bereich **Container mit 2 Spalten** markieren Sie die Auslassungspunkte (**...**) und wählen dann **Modul hinzufügen**.
1. Wählen Sie in der Dialogbox **Module auswählen** das Modul **Map** und wählen Sie dann **OK**.
1. Legen Sie im Eigenschaftsbereich des Moduls nach Bedarf weitere Eigenschaften fest.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
 
## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Schnelleinführung zur Produktdetailseite](quick-tour-pdp.md)

[Schnelleinführung zum Einkaufskorb und Auscheckvorgang](quick-tour-cart-checkout.md)

[Lieferarten einrichten](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Bing Maps für Ihr Unternehmen verwalten](dev-itpro/manage-bing-maps.md)

[Bing Maps-REST-APIs](/bingmaps/rest-services/)

[Kartenmodul](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
