---
title: Eingabehilfefunktionen
description: In diesem Artikel werden die Funktionen erläutert, die für Benutzer gedacht ist, die unter verschiedenen Behinderungen leiden.
author: jasongre
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 4e6a077cc7848448233ed5f94f9b1ba5b385c3fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284022"
---
# <a name="accessibility-features"></a>Eingabehilfefunktionen

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In diesem Artikel werden die Funktionen erläutert, die Benutzer mit verschiedenen Behinderungen dabei unterstützen sollen, diese App zu verwenden. Beispielsweise gibt es Funktionen für Personen, die sehunterstützende Technologien wie Microsoft Windows-Sprachausgabe verwenden.

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows-Sprachausgabe und nur Tastatur-Zugriff

Jedes Feld und Kontrolle besitzt eine Beschriftung und eine Beschreibung von entsprechenden Verknüpfungen. Eine Sprachausgabe kann die Beschriftung und die Beschreibung lesen.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>Verknüpfungen für die am häufigsten ausgeführten Aktivitäten

Für die meisten Benutzer umfasst die tägliche Systemverwendung viele Dateneingabe- und Tastaturinteraktion. Um die Benutzererfahrung zu erhöhen, haben wir Verknüpfungen erstellt, damit Sie schneller zwischen Anwendungen wechseln können und für bestimmte Aktivitäten Tastenkombinationen verwenden können. Weitere Informationen finden Sie unter [Tasten-Kombinationen](shortcut-keys.md).

## <a name="navigation-search"></a>Navigationssuche

Jede Seite, die über das Navigationsbereichsmenü aufgerufen wird, ist auch über den am weitesten links stehende Bereich über das Kästchen **Suchen** verfügbar. Drücken Sie ALT+G, um den Fokus auf das Feld **Suchen** zu richten und geben Sie dann den Namen oder die Beschreibung der Seite ein.

![„Bankkonten“ im Suchfeld eingeben](media/6d08b0be32808221023e2aa92d69fd70.png "'Bankkonten' im Suchfeld eingeben")

Weitere Informationen finden Sie unter [Navigationssuche](navigation-search.md)

> [!NOTE]
> Sie können direkt zu den Seiten auf der obersten Ebene navigieren. Sekundäre Seiten profitieren von Informationen von Kontext oder ihrer übergeordneten Seite.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Aktivitätssuche für Benutzer, die nur die Tastatur nutzen oder für Dropdown-Dateneingaben

Jede Aktivität, die auf einer Seite angegeben wird, kann über eine Tastatur über die Tabulatorsequenz zugegriffen werden. Informationen zur Tabulatorsequenz werden weiter unten in diesem Artikel bereitgestellt. Um die Aktivitäten direkt ausführen, können Sie die Aktivitätssuchenfunktionen verwenden.

### <a name="example"></a>Beispiel

Sie möchten die Aktivität **E-Mail-Benachrichtigungsprotokoll** ausführen, die in der Gruppe **E-Mail-Benachrichtigung** auf der Registerkarte **Auftrag** im Aktivitätsbereich angezeigt wird.

![E-Mail-Benachrichtigungs-Protokollaktivität im Aktivitätsbereich.](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg "'E-Mail-Benachrichtigungs-Protokollaktivität' im Aktivitätsbereich")

Eine Option ist, die Tastatur zu verwenden. Drücken Sie STRG+F6, um den Fokus im Aktivitätsbereich zu verschieben, und die Registerkarte der Verschiebung von allen Registerkarten und Aktivitäten wiederholt zu übertragen, nachdem die Aktivität **E-Mail-Benachrichtigungsprotokoll** im Fokus liegt.

Sie können jedoch auch die Aktivität direkt ausführen. Von Überall auf der Seite klicken Sie Ctrl+Apostrophe ('), um das Suchfeld für Aktivitäten anzuzeigen.

![Suchfeld für Aktivitäten.](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg "Suchfeld für Aktivitäten")

Im Suchfeld tippen Sie Wörter ein, die die Aktion beschreiben. Die Aktivität wird für Sie verfügbar gemacht, und Sie können sie direkt ausführen. Beispielsweise indem Sie **E-Mail**, **benachrich** (ein Teil eines Worts) oder **Protokoll** eingeben, können Sie zur E-Mail-Benachrichtigungs-Protokollfunktionen springen.

![„E-Mail“ im Suchfeld eingeben](media/image4.png "'E-Mail' im Suchfeld eingeben")

![„Benachrich“ im Suchfeld eingeben](media/image5.png "'Benachrich' im Suchfeld eingeben")

![„Protokoll“ im Suchfeld eingeben](media/image6.png "„Protokoll“ im Suchfeld eingeben")

Wenn Sie fertig sind, können Sie Ctrl+Apostrophe erneut drücken, um dem Fokus wieder auf das Feld zu richten, an dem Sie gearbeitet haben, bevor Sie zur Aktivitätssuche wechselten.

Weitere Informationen finden Sie unter [Aktionssuche](action-search.md)

## <a name="tab-sequence"></a>Register Sequenz

In der täglichen Systemverwendung nicht jedes Feld obligatorisch, um jede Aufgabe auszuführen. Daher ist standardmäßig die Tabulatorsequenz "optimiert." Tabstopps werden nur auf diese Felder festgelegt, die für typische Szenarios wichtig sind.

Allerdings stellen Sie möglicherweise fest, dass einige Felder, die Sie häufig aufrufen, um Aufgaben auszuführen, nicht in der Standardtabulatorsequenz enthalten sind. In diesem Fall, wenn Sie Windows-Sprachausgabe auswählen, können Sie die Windows-Sprachausgaben-Tastatur-Aktivitäten nutzen, um auf diese Felder zuzugreifen und ihren Inhalt zu überprüfen. Sie können auch die Option **Erweiterte Tabulatorsequenz** auf der Seite **Optionen** aktivieren. Diese Option macht alle bearbeitbaren und schreibgeschützten Felder Teil der Tabulatorsequenz. Sie können die Seitenpersonalisierung dann verwenden, um eine benutzerdefinierte Tabulatorsequenz zu erstellen und Felder zu unterdrücken, die nicht Teil der Tabulatorsequenz sein müssen. Weitere Informationen über die Personalisierung, finden Sie unter [Personalisieren Sie die Benutzerfreundlichkeit](personalize-user-experience.md).

![Option „Erweiterte Tabulatorsequenz“](media/8c0f12bbb3f26032997ef0ba95d89b6a.png "Option „Erweiterte Tabulatorsequenz“")

## <a name="form-patterns"></a>Formularmuster

Fast 90 Prozent der Seiten in der App sind auf einem kleinen Satz Muster basiert. Diese Muster sind mit *Formularmuster* gekennzeichnet. Jedes Formularmuster wird verwendet, um die Aktivitäten anzugeben, die am häufigsten auf der Seite ausgeführt werden. Ein Formularmuster garantiert Vertrautheit und ein leichtes Verständnis, weil häufig genutzte Aktionen und Daten immer am gleichen Speicherort auf verschiedene Seiten produziert werden. Aufgrund der kleiner Anzahl von Formularmustern, können Benutzer das System, unabhängig von der Anzahl der Seiten, leicht kennen lernen und es verwenden, nachdem sie die Formularmuster kennen.

.Weitere Informationen zu Formularmuster finden Sie unter [Formularstile und -Muster](../../dev-itpro/user-interface/form-styles-patterns.md)

## <a name="responsive-layout"></a>Responsives Layout

Das Produkt wurde so entworfen, dass es auf verschieden Geräten und Formularfaktoren arbeitet, von den kleinsten Bildschirmen bis hin zu großen Bildschirmen mit höchster Auflösung. Mit unserem reagierenden Layoutmodul können Benutzer ein Vergrößerungsniveau von 200 Prozent erzielen (oder in einigen Szenarien mehr als 200 Prozent ).

Auf Smartphones und anderen kleinen Bildschirmen passen sich die Steuerelemente und das Formularlayout an, um sicherzustellen, dass die Kerndaten bevorzugt werden. Zu diesen Reaktionsverhalten kann auch gehören, dass die Anzahl der Spalten in Gruppen und Registerkarten auf eine einzige Spalte reduziert wird, Shell-Elemente ausgeblendet werden und der Aktionsbereich ausgeblendet wird.

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Empfehlungen, um Entwickler und Kunden zu helfen, Eingabehilfen in Ihre Anpassungen zu integrieren.

Weitere Informationen zu Microsoft-Verfahren für das Aktivieren des Zugangs finden Sie unter [Eingabehilfen in Formularen, Produkten und Steuerungen](../../dev-itpro/user-interface/enable-accessibility.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
