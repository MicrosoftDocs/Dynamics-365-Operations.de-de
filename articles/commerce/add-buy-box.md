---
title: Kauffeldmodul
description: Dieses Thema enthält Kauffeldmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae3da8ee77636a2d2257e01f5876f5542469f7da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986053"
---
# <a name="buy-box-module"></a>Kauffeldmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält Kauffeldmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Der Begriff *Kauffeld* bezieht sich in der Regel auf einen Produktdetailseiten-Bereich, der „über der Falte“ angezeigt wird und die wichtigsten Informationen enthält, die erforderlich sind, um einen Produkteinkauf abzuschließen. (Ein Bereich, der „über der Falte“ ist, wird angezeigt, wenn die Seite zuerst geladen wird, sodass Benutzer nicht nach unten scrollen müssen, um sie zu sehen.)

Ein Kauffeldmodul ist ein spezieller Container, der verwendet wird, um alle zu Module verwenden, die im Kauffeldbereich einer Produktdetailseite angezeigt werden.

Die URL einer Produktdetailseite, die in einer Produktkennung enthalten ist. Alle Informationen, die erforderlich sind, um ein Kauffeldmodul zu stellen, werden von dieser Produktkennung berechnet. Wenn eine Produktkennung nicht bereitgestellt wird, wird das Kauffeldmodul nicht ordnungsgemäß auf einer Seite dargestellt. Daher kann ein Kauffeldmodul nur auf Seiten mit Produktkontext verwendet werden. Um es auf einer Seite ohne Produktkontext (z. B. einer Homepage oder einer Marketingseite) zu verwenden, müssen Sie zusätzliche Anpassungen vornehmen.

Das folgende Bild zeigt ein Beispiel eines Kaufelementmoduls auf einer Produktdetailseite.

![Beispiel eines Kaufelementmoduls](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Kaufen Sie Feldmoduleigenschaften und -Slots 

In einer Produktdetailseite wird ein Kauffeld in zwei Bereiche unterteilt: einen Medienbereich auf der linken und einen Inhaltsbereich auf der rechten Seite. Standardmäßig beträgt das Verhältnis der Breite der Medienbereichsspalte zur Breite der Inhaltsbereichsspalte 2:1. Auf mobilen Geräten werden diese beiden Regionen gestapelt, so dass die Regionen übereinander angezeigt werden. Mithilfe von Themen können Sie die Spaltenbreiten und den Stapelrang anpassen.

Ein Kauffeldmodul gibt den Titel, die Beschreibung, den Preis und die Bewertungen eines Produkts wieder. Außerdem können Kreditoren Produktvarianten mit unterschiedlichen Produktattributen wie Größe, Stil und Farbe auswählen. Wenn eine Produktvariante ausgewählt wird, werden andere Eigenschaften im Kauffeld, (beispielsweise die Produktbeschreibung und Bilder) aktualisiert, um die verschiedenen Informationen neu zu berechnen. 

Eine Mengenauswahl wird bereitgestellt, damit Kreditoren die Menge der zu kaufenden Artikel angeben können. Die maximale Menge, die gekauft werden kann, kann in den Site-Einstellungen festgelegt werden.

Über das Kauffeld können Kunden auch Aktionen ausführen, z. B. ein Produkt in den Warenkorb legen, ein Produkt zu ihrer Wunschliste hinzufügen und einen Abholort auswählen. Diese Aktionen können für ein Produkt oder eine Produktvariante ausgeführt werden. Um ein Produkt zu einer Wunschliste hinzuzufügen, muss der Kunde angemeldet sein.

Mithilfe von Designs können Sie die Reihenfolge der Produkteigenschaften und Aktionssteuerelemente der Kaufbox entfernen oder ändern. 

## <a name="module-properties"></a>Moduleigenschaften

- **Überschriften-Tag** – Diese Eigenschaft definiert das Überschriften-Tag für den Produkttitel. Wenn sich das Kauffeld oben auf der Seite befindet, sollte diese Eigenschaft auf **h1** festgelegt werden, um die Zugänglichkeitsstandards zu erfüllen. 

- **Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren** – Mit dieser Eigenschaft können im Kauffeld Links zu Produkten angezeigt werden, die dem aktuell angezeigten Artikel ähneln. Diese Funktion ist in Commerce Version 10.0.13 und höher verfügbar.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Module, die im Kauffeldmodus verwendet werden können

- **Mediengalerie** - Dieses Modul wird verwendet, um die Bilder eines Produkts auf einer Produktdetailseite anzuzeigen. Weitere Informationen zu diesem Modul finden Sie unter [Mediengaleriemodul](media-gallery-module.md).
- **Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen. Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen. Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).
- **Social Share** – Dieses Modul kann dem Kauffeld hinzugefügt werden, damit Benutzer Produktinformationen in sozialen Medien teilen können. Weitere Informationen finden Sie unter [Social Share-Modul](social-share-module.md).

## <a name="buy-box-module-settings"></a>Kauffeldmoduleinstellungen

Die folgenden Kaufelementmoduleigenschaften können unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden:

- **Warenkorbartikel-Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann. Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.
- **Bestand** – Informationen zum Anwenden von Bestandeinstellungen finden Sie unter [Wenden Sie Bestandeinstellungen an](inventory-settings.md).
- **Produkt in den Warenkorb legen** – Mit dieser Eigenschaft wird das Verhalten angegeben, nachdem ein Artikel zum Warenkorb hinzugefügt wurde. Die möglichen Werte sind **Zur Warenkorbseite navigieren**, **Nicht zur Warenkorbseite navigieren** und **Benachrichtigung anzeigen**. Wenn der Wert auf **Zur Warenkorbseite navigieren** festgelegt ist, werden Benutzer Warenkorbseite weitergeleitet, nachdem Sie einen Artikel hinzugefügt haben. Wenn der Wert auf **Nicht zur Warenkorbseite navigieren** festgelegt ist, werden Benutzer nach dem Hinzufügen eines Artikels nicht zur Warenkorbseite weitergeleitet. Wenn der Wert auf **Benachrichtigung anzeigen** festgelegt ist, wird Benutzern eine Bestätigungsbenachrichtigung angezeigt, und sie können weiter die Seite mit den Produktdetails durchsuchen. 

> [!IMPORTANT]
> Die Website-Einstellungen **Produkt in den Warenkorb legen** sind im Release Dynamics 365 Commerce 10.0.11 verfügbar. Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

Das folgende Bild zeigt ein Beispiel einer Benachrichtigung Zum Warenkorb hinzugefügt auf der Fabrikam-Site.

![Beispiel eines Benachrichtigungs-Moduls](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit-Interaktion

Das Kauffeldmodul ruft Produktinformationen mithilfe der Commerce Scale Unit Anwendungsprogrammschnittstellen (APIs) ab. Die Produktkennung von der Produktdetailseite wird verwendet, um alle Informationen abzurufen.

## <a name="add-a-buy-box-module-to-a-page"></a>Hinzufügen eines Kauffeldmodul zu einer Seite

Um ein Kauffeldmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.
1. Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Kauffeld** aus.
1. Geben Sie unter **Name des Fragments** den Namen **Kauffeldfragment** ein und wählen Sie **OK** aus.
1. Im Slot **Mediengallerie**, der das Kauffeldmodul enthält, wählen Sie die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Mediengallerie** und dann **OK** aus.
1. Im Slot **Auswahl speichern**, der das Kauffeldmodul enthält, wählen Sie die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auswahl speichern** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **PDP Vorlage** ein und wählen **OK**.
1. Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.
1. Auf dem Seitenüberblick wählen Sie den Slot **Haupt** und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Fragment hinzufügen**.
1. Wählen Sie im Dialogfeld **Fragment auswählen** das Fragment **Kauffeldfragment** aus, das Sie zuvor erstellt haben, und wählen Sie dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **PDP-Vorlage** aus. Unter **Seitenname** geben Sie **PDP-Seite** ein und wählen dann **OK** aus.
1. Im Slot **Hauptseite** der neuen Seite wählen Sie die Ellipsen-Schaltfläche (**...**) und wählen Sie **Fragment hinzufügen**.
1. Wählen Sie im Dialogfeld **Fragment auswählen** das Fragment **Kauffeldfragment** aus, das Sie zuvor erstellt haben, und wählen Sie dann **OK** aus.
1. Seite speichern und Vorschau anzeigen. Fügen Sie die **? productid=&lt;Produktkennung&gt;**-Abfragezeichenfolgenparameter der URL der Vorschauseite hinzu. So wird der Produktkontext verwendet, um die Vorschauseite zu stellen und zu rendern.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen. Ein Kauffeld sollte auf der Produktdetailseite angezeigt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Shopauswahlmodul](store-selector.md)

[Mediengaleriemodul](media-gallery-module.md)

[Containermodul](add-container-module.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)

[Social Share-Modul](social-share-module.md)

[Lagerverfügbarkeit für Retail Channels berechnen](calculated-inventory-retail-channels.md)

[SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md)
