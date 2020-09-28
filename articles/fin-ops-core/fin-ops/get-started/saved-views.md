---
title: Gespeicherte Ansichten
description: In diesem Thema wird beschrieben, wie Sie die gespeicherten Ansichtsfunktionen verwenden.
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: b948da0bff8de3b8ad783b3e3f52100a29fab109
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802894"
---
# <a name="saved-views"></a>Gespeicherte Ansichten

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Einführung

Die Personalisierung spielt eine wichtige Rolle und erlaubt es Benutzern und Organisationen, die Benutzerfreundlichkeit zu optimieren, um ihren Anforderungen zu entsprechen. Weitere Details über die Personalisierung, finden Sie unter [Personalisieren Sie die Benutzerfreundlichkeit](personalize-user-experience.md).

Mit traditioneller Personalisierung können Benutzer nur einen Satz Personalisierungen pro Seite haben. Die Funktion **Gespeicherte Ansichten** erweitert sich auf die Personalisierung auf mehrere wichtige Arten:

- Ansichten erlauben es Benutzern, mehrere Personalisierungen pro Formular zu erhalten, so dass rasch hin und her gewechselt werden kann. Somit kann ein Benutzer mehrere Ansichten einer Seite optimieren, wenn jede Ansicht angepasst wurde, um die Anforderungen der Ausführung einer bestimmten Aufgabe anzupassen. 
- Die Ansicht, die für bestimmte Seitentypen erstellt werden, können auch von Benutzern hinzugefügte Filter enthalten, die es Benutzern ermöglichen, rasch zu den oft verwendeten gefilteretn Datensets zurückzukehren. Weitere Details im Abschnitt [Seiten, die Ansichten unterstützen](saved-views.md#what-pages-support-views). 
- Ansichten können für Benutzer in bestimmten Sicherheitsrollen und für bestimmte juristische Personen veröffentlicht werden. Daher kann jeder Benutzer, der eine bestimmte Rolle und Zugriff auf eine angegebene juristische Person hat, auf diese Ansicht zugreifen und sie verwenden, auch wenn dieser Benutzer keine Berechtigung zum Personalisieren hat. Dieses Veröffentlichungsfunktion ermöglicht es Organisationen, Unternehmensstandardansichten zu definieren, die für ihr Geschäft optimiert werden. Weitere Informationen finden Sie im Abschnitt [Verwalten von Personalisierungen auf Organisationsebene mit Ansichten](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- Anders als traditionelle Personalisierung werden Ansichten nicht automatisch gespeichert, wenn ein Benutzer Personalisierungen ausführt oder eine Liste filtert. Explizite Speicherungen sind erforderlich, um Benutzern die Flexibilität zu geben, eine Ansicht zu erstellen, bevor oder nachdem die mit dieser Ansicht verknüpften Änderungen vorgenommen wurden. Diese Anforderung stellt auch sicher, dass Ansichtsdefinitionen nicht unbeabsichtigt durch Filter oder Personalisierungen geändert werden, die nicht für die langfristige Verwendung vorgesehen sind. Elemente, die das System im Rahmen der typischen Seitennutzung automatisch speichert (z. B. Spaltenbreiten oder der erweiterte oder reduzierte Status von Abschnitten), werden pro Ansicht gespeichert.
- Ansichten können zu Geschäftsbereichen als Kacheln, Listen oder Links hinzugefügt werden. Daher kann ein gefilterter Datensatz in einem Arbeitsbereich angezeigt werden, und Benutzer können einen Satz Personalisierungen, die für diesen Datensatz relevant sind, mit einer Kachel oder Verknüpfung zuordnen.

## <a name="switching-between-views"></a>Wechsel zwischen Ansichten

Nachdem Ansichten für eine Umgebung verfügbar gemacht wurden, enthält jede Seite oben, die Ansichten unterstützt, ein reduziertes Ansichtsauswahlsteuerelement, das den Namen der aktuellen Ansicht anzeigt.

Es gibt zwei Größenvarianten der Ansichts-Auswahl: 

- **Auswahl für große Ansicht** – Seiten, die prominent eine Liste haben, verfügen über eine Auswahl für große Ansicht aus mehreren Gründen. Am wichtigsten ist, dass die größere Anzeigen-Auswahl die Seiten angezeigt, bei denen die Ansicht benutzerdefinierte Filter enthalten kann. Da Filter in der Ansicht enthalten sind, garantiert die größere Anzeigen-Auswahl auch, dass die Ansichtsnamen häufig die beste Beschreibung der Angaben enthalten, die auf dem Bildschirm angezeigt werden und die Erwartung ist, dass Benutzer häufiger auf diesen Seitentypen zwischen Ansichten wechseln.
- **Auswahl für kleine Ansicht** – Alle anderen Vollbildseiten (mit Ausnahme von Arbeitsbereichen und des Dashboards) beinhalten eine Auswahl für kleine Ansicht, die neben der Seitenbeschriftung angezeigt wird. Ansichten auf diesen Seiten enthalten nur Personalisierungen und keine benutzerdefinierte Filter. Auf diesen Seiten umfasst die Beschriftung oder der Datensatztitel häufig die wichtigsten Informationen oben auf der Seite. Das kleinere Format der Ansichtsauswahl spiegelt auch die niedrigere Häufigkeit der Ansichtsumschaltung, die auf diesen Seiten erwartet wird, wider. 
 
Wenn Sie den Ansichtsnamen auswählen, wird die Ansichtsauswahl geöffnet und zeigt die Liste der verfügbaren Ansichten für diese Seite an.

- **Standardansicht** – Die Ansicht **Standard** ist die einsatzbereite Ansicht der Seite, auf der keine Personalisierungen angewendet werden.
- **Persönliche Ansichten** – Die Ansichten ohne Vorhängeschlösser stellen Ihre persönlichen Ansichten dar. Dies sind Ansichten, die Sie entweder erstellt haben oder die IHnen ein Administrator zugewiesen hat.
- **Gesperrte Ansichten** – Neben einigen Ansichten (wie die Ansicht **Standard** und Ansichten, die für Ihre Rolle veröffentlicht werden) wird ein Vorhängeschlosssymbol in der Ansichtsauswahl angezeigt. Dieses Symbol zeigt an, dass Sie die Ansichten nicht bearbeiten können. Allerdings werden Änderungen, die die Seitenverwendung widerspiegeln, automatisch gespeichert. Diese Änderungen umfassen Änderungen an der Breite einer Rasterspalte und Änderungen am erweiterten oder reduzierten Status eines Inforegisters. Wenn Sie Personalisierungsrechte haben, können Sie die Aktion **Speichern unter** verwenden, um eine persönliche Ansicht zu erstellen, die auf einer gesperrten Ansicht basiert.
- **Neue Ansichten** – Veröffentlichte Ansichten, die noch nicht geöffnet wurden, weisen auf der linken Seite des Ansichtsnamens ein Funkensymbol auf.

Um zu einer anderen Ansicht zu wechseln, öffnen Sie die Ansichts-Auswahl und wählen Sie die Ansicht aus, die Sie laden möchten. 

## <a name="creating-and-modifying-views"></a>Ansichten erstellen und ändern

Im Gegensatz zur herkömmlichen Personalisierung werden Ansichten nicht automatisch gespeichert, wenn ein Benutzer die Seite personalisiert oder wenn ein Benutzer einen Filter auf eine Liste anwendet oder diese sortiert. Eine explizite Aktivität ist erforderlich, um diese Änderungen für eine Ansicht zu speichern. Diese Anforderung gibt den Benutzern die Flexibilität, eine Ansicht zu erstellen, bevor oder nachdem die mit dieser Ansicht verknüpften Änderungen vorgenommen wurden. Außerdem wird sichergestellt, dass Ansichtsdefinitionen nicht unbeabsichtigt durch einmalige Filter oder Personalisierungen geändert werden. Beachten Sie, dass typische Elemente für die Seitennutzung (z. B. Spaltenbreiten oder der erweiterte oder reduzierte Status von Abschnitten) auch in gesperrten Ansichten automatisch in der aktuellen Ansicht gespeichert werden.

Um sicherzustellen, dass der aktuelle Status der Ansicht bekannt ist, wird ein Sternchen (\*) neben dem aktuellen Ansichtsnamen angezeigt, wenn Sie eine Ansicht durch Personalisieren oder Filtern ändern. Dieses Symbol zeigt an, dass Sie eine nicht gespeicherte, geänderte Version dieser Ansicht anzeigen.

Wenn Sie die diese Änderungen speichern möchten, führen Sie die folgenden Schritte aus.

1. Wählen Sie den Ansichtsnamen aus, um die Ansichts-Auswahl zu öffnen.
2. Um die vorhandene Ansicht zu ändern, wählen Sie **Speichern** aus. Beachten Sie, dass diese Aktion für gesperrte Ansichten nicht verfügbar ist. 
3. Um eine neue Ansicht zu erstellen.

    1. Wählen Sie **Speichern unter**. 
    2. Geben Sie einen Namen und eine (optionale) Beschreibung ein.
    3. Wählen Sie **Speichern**.

## <a name="changing-the-default-view"></a>Die Standardansicht ändern

Die Standardansicht ist die Ansicht, die das System beim ersten Öffnen der Seite zu öffnen versucht. Sie sollten die Standardansicht auf jene Ansicht festlegen, die Sie voraussichtlich am häufigsten verwenden werden. 

> [!NOTE]
> Es gibt eine einzige globale Standardansicht für alle Unternehmen. Wenn Sie die Standardansicht ändern, wird diese Ansicht standardmäßig geöffnet, unabhängig von der juristischen Person, in der Sie sich gerade befinden. 

Um die Standardansicht für eine Seite zu ändern, führen Sie die folgenden Schritte aus:

1. Wechseln Sie zur Ansicht, die Sie standardmäßig verwenden. 
2. Wählen Sie den Ansichtsnamen aus, um die Ansichts-Auswahl zu öffnen. 
3. Wählen Sie **Weiter** und anschließend **Als Standard festsetzen** aus.

Möchten Sie eine neue Ansicht (mithilfe der Aktivität **Speichern unter**) erstellen, können Sie diese neue Ansicht zur Standardansicht machen, indem Sie die Option **Als Standard festsetzen** festlegen, bevor Sie die Ansicht speichern.

Beachten Sie, dass in einigen Fällen die der Standardansicht zugeordnete Abfrage beim ersten Öffnen einer Seite nicht ausgeführt wird. Wenn Sie also beispielsweise über eine Kachel die Seite öffnen, wird die Abfrage der Kachel unabhängig von der Abfrage, die der Standardansicht zugeordnet ist, ausgeführt. Wenn Sie darüber hinaus eine Seite öffnen, die eine **Standard**-Ansicht aufweist, für die bereits eine Abfrage definiert ist, wird die ursprüngliche Abfrage anstelle der Abfrage der Standardansicht ausgeführt. In diesem Fall erhalten Sie beim Laden der Ansicht eine Informationsnachricht. Wenn Sie die Ansicht wechseln, nachdem die Seite geladen wurde, sollte die Ansichtsabfrage wie erwartet ausgeführt werden können. In Version 10.0.10 und höher enthält die Informationsnachricht, die Sie erhalten, eine eingebettete Aktion, mit der Sie die Abfrage der Standardansicht direkt laden können.

## <a name="managing-personal-views"></a>Verwalten von persönlichen Ansichten

Das Dialogfeld **Verwalten Sie meine Ansichten** bietet grundlegende Verwaltungsfunktionen für Ihre persönlichen Ansichten und die Reihenfolge in der Ansichts-Auswahl. Um diese Seite zu öffnen, wählen Sie den Ansichtsnamen, um das Ansichtsauswahl-Dropdownmenü zu öffnen, wählen Sie **Weiter** und anschließend **Verwalten meiner Ansichten** aus.

Für eine Liste der verfügbaren Ansichten für diese Seite sind die folgenen Aktivitäten verfügbar.

- **Standardansicht ändern** – Verwenden Sie die Aktion **Als Standard festlegen**, um die derzeit ausgewählte Ansicht als Standardansicht für diese Seite festzulegen.
- **Ansichten neu ordnen** – Nutzen Sie die Aktionen **Nach oben** und **Nach unten**, um die Ansichten in einer bestimmten Reihenfolge neu anzuordnen.
- **Ansicht umbenennen** – Verwenden Sie die Aktion **Umbenennen**, um den Namen der momentan ausgewählten persönlichen Ansicht zu ändern. Diese Aktion wird für die gesperrte Ansichten deaktiviert. 
- **Ansicht löschen** – Verwenden Sie die Aktion **Löschen**, um die zurzeit ausgewählte Ansicht dauerhaft von der Seite zu löschen. Es gibt keine Möglichkeit, eine Ansicht wieder herzustellen, nachdem sie gelöscht wurde.

Sämtliche Änderungen, die an diesem Dialogfeld vorgenommen werden, treten in Kraft, wenn Sie die Schaltfläche **Speichern** auswählen.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Verwalten von Personalisierungen auf Organisationsebene mit Ansichten

Um zu verstehen, wie gespeicherte Ansichten dazu beitragen, die Verwaltung von Personalisierungen auf organisatorischer Ebene zu verbessern, werden in diesem Abschnitt einige Unterschiede der Personalisierungsverwaltung mit und ohne die Funktion **Gespeicherte Ansichten** beschrieben.

Ohne Ansichten würden Administratoren einen Satz Personalisierungen für eine Seite über die Seite „Personalisierung“ auf einen Benutzer oder eine Benutzergruppe anwenden. Wenn diese Benutzer Personalisierungsrechte hatten, werden die Personalisierungen dieser Seite angewendet. Allerdings gab es keine Möglichkeit, weitere Benutzer daran zu hindern, die Seite weiter zu personalisieren, was bedeutete, dass die Organisation nicht sicherstellen konnte, dass die Benutzer eine konsistente Benutzeroberfläche hatten. Wenn diese Benutzer keine Personalisierungsrechte haben, werden die Personalisierungen, die Ihnen von einem Administrator zugewiesen wurden, nicht geladen. Wenn neue Benutzer bei einer Organisation angestellt wurden, müssen Administratoren manuell die erforderlichen Personalisierungen für den Benutzer laden. Es gab keinen automatischen Mechanismus, um anzugeben, dass ein bestimmter Satz Personalisierungen für Benutzer in dieser Rolle verfügbar sein sollte.

Mit der Funktion **Gespeicherte Ansichten** wird die organisatorische Verwaltung von Personalisierungen viel einfacher, primär aufgrund der Möglichkeit, Ansichten für Benutzergruppen veröffentlichen zu können. Nachdem eine Ansicht veröffentlicht wurde, kann jeder Benutzer, der eine der definierten Sicherheitsrollen und Zugriff auf eine der angegebenen juristischen Personen hat, die Ansicht sehen und verwenden, auch wenn dieser Benutzer keinen Zugriff auf die Personalisierung hat. Obwohl jeder Benutzer eine Kopie der veröffentlichten Ansicht hat, in der die Elemente für die Seitennutzung automatisch angewendet werden, kann kein Benutzer Personalisierungen oder Abfrageaktualisierungen in einer veröffentlichten Ansicht speichern. Mit anderen Worten, veröffentlichte Ansichten sind gesperrt. Wenn neuen Benutzern außerdem Rollen in juristischen Personen zugewiesen werden, für die Ansichten veröffentlicht wurden, sehen sie automatisch die Ansichten, die ihren Rollen und juristischen Personen zugeordnet sind. Keine weitere Aktivität wird vom Administrator gefordert. Ebenso können Benutzer, die Rollen in einer Organisation wechseln oder Zugang zu verschiedenen juristischen Personen erhalten, möglicherweise nicht mehr auf die Ansichten zugreifen, die zuvor für sie veröffentlicht wurden. Wieder ist keine weitere Aktivität durch den Administrator erforderlich.

Aktualisierungen an einer veröffentlichten Ansicht können einfach an Benutzer verteilt werden, indem die Ansicht zu den entsprechenden Sicherheitsrollen und juristischen Personen erneut veröffentlicht wird.

Dies Veröffentlichungsfunktion ermöglicht es Organisationen, Unternehmensstandardansichten zu definieren, die für ihr Geschäft für Benutzer in bestimmten Sicherheitsrollen optimiert werden.

## <a name="publishing-views"></a>Veröffentlichte Ansichten

Während des Veröffentlichungsprozesses können Ansichten an mindestens eine Sicherheitsrolle für mindestens eine juristische Person zugewiesen werden. Daher kann jeder Benutzer, der Zugriff auf eine juristische Person hat und der einer dieser Rollen zugewiesen ist, auf die Ansichten zugreifen und diese verwenden. Der Benutzer kann die Ansichten jedoch nicht bearbeiten. Standardmäßig können Systemadministratoren auf die Aktion **Veröffentlichen** im Ansichtsauswahl-Dropdownmenü zugreifen. Allerdings können andere vertrauenswürdige Benutzer in Ihrer Organisation auch Zugriff auf die Ansichtsveröffentlichung erhalten über die neue Rolle **Administrator für gespeicherte Ansichten**.

Führen Sie folgende Schritte aus, um eine Ansicht zu veröffentlichen.

1. Erstellen und Speichern einer persönlichen Kopie der Ansicht, die veröffentlicht werden soll. 
2. Mit dieser Ansicht, die derzeit geladen ist, wählen Sie den Ansichtsnamen aus, um das Ansichtsauswahl-Dropdownmenü zu öffnen. 
3. Wählen Sie die Schaltfläche **Mehr** und wählen Sie dann **Veröffentlichen** aus. Das Feld Veröffentlichen wird geöffnet.
4. Geben Sie einen Namen (optional) und eine Beschreibung für die Ansicht ein. Der Name, den Sie eingeben, ist Name, den Benutzer, die diese Ansicht erhalten, in der Ansichts-Auswahl finden. Die Namen von veröffentlichten Ansichten für eine Seite müssen eindeutig sein. Es sind keine Duplikat-Namen zulässig, auch wenn die Liste der Rollen oder juristischen Personen, auf die sie angewendet werden, sich unterscheiden.
5. **Version 10.0.9 und höher:** Legen Sie fest, ob die Ansicht als Standardansicht für die ausgewählten Benutzer veröffentlicht werden soll. Wenn eine Ansicht zur Standardansicht gemacht wird, wird sie beim nächsten Öffnen der Zielseite angezeigt. Die einzelne globale Standardansicht jedes Zielbenutzers wird geändert. Benutzer können jedoch ihre Standardansicht nach dem Veröffentlichen weiterhin ändern.
6. Fügen Sie die Sicherheitsrollen hinzu, die den Benutzer entsprechen, auf die diese Ansicht ausgerichtet ist. 
7. **Version 10.0.13 und höher:** Bestimmen Sie, ob Sie die Ansicht in den untergeordneten Rollen jeder ausgewählten Sicherheitsrolle veröffentlichen möchten. Wenn Sie dies tun, aktivieren Sie das Kontrollkästchen **Untergeordnete Rollen einschließen** in der Zeile für die entsprechenden Sicherheitsrollen. Beachten Sie, dass dieses Kontrollkästchen für Rollen ohne untergeordnete Rollen nicht verfügbar ist.
7. Fügen Sie juristische Personen hinzu, für die diese Ansicht verfügbar sein sollte. 
8. Wählen Sie **Veröffentlichen** aus.

Beachten Sie, dass es in einer Umgebung einige Zeit in Anspruch nehmen kann (bis zu einer Stunde) bis Benutzer die veröffentlichte Ansicht sehen.

> [!NOTE]
> Beachten Sie die folgenden Erwartungen, wenn Sie eine Ansicht für eine juristische Person veröffentlichen oder wenn Sie eine Ansicht als Standardansicht veröffentlichen.
> - Wenn Sie eine Ansicht als Standardansicht für alle oder einige juristische Personen veröffentlichen, können Sie die einzelne globale Standardansicht jedes Zielbenutzers ändern. Wenn ein Benutzer Rollen hat, in denen mehrere Ansichten als Standardansicht veröffentlicht werden, wird die zuletzt veröffentlichte Ansicht als Standardansicht des Benutzers verwendet. 
> - Wenn Sie eine Ansicht für eine juristische Person veröffentlichen, diese jedoch nicht als Standardansicht veröffentlichen, wird den Benutzern die Ansicht in der Ansichtsauswahl zunächst nur für die angegebenen juristischen Personen angezeigt. Nachdem die Ansicht zum ersten Mal geladen wurde, befindet sie sich unabhängig von der juristischen Person immer in der Ansichtsauswahl des Benutzers für diese Seite. 

## <a name="modifying-a-published-view"></a>Ändern einer veröffentlichten Ansicht

Nachdem Sie eine Ansicht veröffentlicht haben, möchten Sie sie möglicherweise ändern. Während Sie keine Liveänderungen an einer veröffentlichten Ansicht machen können, da diese Ansichten zur Bearbeitung für alle Benutzer (einschließlich Herausgeber) gesperrt werden, können Sie eine Ansicht erneut veröffentlichen, um sie zu aktualisieren.

Wenn die Änderungen, die Sie an einer veröffentlichten Ansicht vornehmen möchten, nur die Veröffentlichungsparameter umfasst (der Name und die Beschreibung der Ansicht, oder die Sicherheitsrollen, in der die Ansicht veröffentlicht wird), gehen Sie folgendermaßen vor:

1. Wechseln Sie zur veröffentlichten Ansicht für die Parameter, die Sie aktualisieren möchten. 
2. Wählen Sie im Ansichtsauswahl-Dropdownmenü **Erneut veröffentlichen** aus. Wenn Sie Version 10.0.12 oder früher verwenden, müssen Sie **Veröffentlichen** und dann **Ja** auswählen, um die vorhandene Ansicht zu aktualisieren.
3. Aktualisieren Sie den Namen, die Beschreibung, Sicherheitsrollen und juristischen Personen für die Ansicht. 
4. Wählen Sie **Veröffentlichen** aus. 
5. **Version 10.0.8 und früher:** Wenn Sie den Namen der veröffentlichten Ansicht aktualisiert haben, müssen Sie auch die veröffentlichte Ansicht mit dem alten Namen löschen. (Weitere Informationen finden Sie im Abschnitt [Veröffentlichte Ansichten verwalten](saved-views.md#managing-published-views).)

**Version 10.0.9 und höher:** Wenn Sie diese veröffentlichte Ansicht ursprünglich als Standardansicht ausgewählt haben, ist sie nach der erneuten Veröffentlichung wieder die Standardansicht für Benutzer.

Wenn Änderungen der veröffentlichten Ansicht die Personalisierungen oder Filter umfassen, die der Ansicht zugeordnet sind, folgen Sie diesen Schritten: 

**Version 10.0.13 und höher:** Nehmen Sie die erforderlichen Änderungen direkt an der Ansicht vor. Ein Sternchen (\*) sollte neben dem Ansichtsnamen angezeigt werden.

1. Laden Sie die veröffentlichte Ansicht, die Sie ändern möchten. 
2. Nehmen Sie die erforderlichen Änderungen am lokalen Entwurf vor.
3. Wählen Sie im Ansichtsauswahl-Dropdownmenü **Erneut veröffentlichen** aus.
4. Wählen Sie **Ja** aus, um anzuzeigen, dass Sie die Ansicht zusammen mit den nicht gespeicherten Änderungen veröffentlichen möchten. 
5. Passen Sie alle Veröffentlichungsparameter an, die angepasst werden müssen, und wählen Sie dann **Veröffentlichen** aus. 

**Version 10.0.12 und früher**

1. Laden Sie die veröffentlichte Ansicht, die Sie aktualisieren möchten. 
2. Hiermit wird eine Kopie der veröffentlichten Ansicht gespeichert, um einen lokalen Entwurf der veröffentlichten Ansicht zu erstellen. 
3. Ändern Sie den lokalen Entwurf mit den erforderlichen Änderungen.
4. Veröffentlicht Sie die Ansicht mit dem ursprünglichen Namen. 

## <a name="managing-published-views"></a>Verwalten von veröffentlichten Ansichten

Wie das Verwalten persönlicher Ansichten gibt das Dialogfeld **Meine Ansichten verwalten** Benutzern mit grundlegenden Verwaltungsfunktionen die Rechte zum Veröffentlichen von Ansichten dieser Seite (zusätzlich zu ihren eigenen persönlichen Ansicht). Um diese Seite zu öffnen, wählen Sie den Ansichtsnamen, um das Ansichtsauswahl-Dropdownmenü zu öffnen, wählen Sie **Weiter** und anschließend **Verwalten meiner Ansichten** aus.

Obwohl alle Benutzer eine Registerkarte **Meine Ansichten** mit ihren persönlichen Ansichten sehen, wird Benutzern mit Veröffentlichungsrechten auch eine Registerkarte **Organisationsansichten** angezeigt, auf der alle veröffentlichten und unveröffentlichten Ansichten für diese Seite angezeigt werden. Da möglicherweise mehrere Benutzer Ansichten veröffentlichen, ist es wichtig, dass Sie die vollständige Liste der veröffentlichten Ansichten verwalten können, auch wenn Sie nicht der Benutzer sind, der eine bestimmte Ansicht veröffentlicht hat.

Für eine Liste aller veröffentlichten Ansichten für diese Seite sind die folgenen Aktivitäten verfügbar. 

- **Erneut veröffentlichen** – Verwenden Sie die Aktion **Erneut veröffentlichen**, um eine Ansicht erneut zu veröffentlichen, nachdem Veröffentlichungsparameter (Name, Beschreibung, Sicherheitsrollen oder juristische Personen) geändert wurden.
- **Veröffentlichen** – Verwenden Sie die Aktion **Veröffentlichen** zum Veröffentlichen einer Ansicht, die derzeit nicht veröffentlicht ist. 
- **Veröffentlichung aufheben** – Verwenden Sie die Aktion **Veröffentlichung aufheben**, um eine Ansicht inaktiv zu machen. Die Ansicht ist weiterhin im System verfügbar, aber Benutzer sehen sie erst in der Ansichtsauswahl, wenn die Ansicht erneut veröffentlicht wird.
- **Als persönlich speichern** – Verwenden Sie die Aktion **Als persönlich speichern** zum Erstellen eines persönlichen Entwurfs einer Kopie der veröffentlichten Ansicht. Diese Funktion kann Ihnen helfen, den Inhalt einer Ansicht zu verstehen, die nicht für Sie veröffentlicht wurde oder die noch nicht veröffentlicht wurde. Sie können damit auch eine Ansicht bearbeiten und anschließend erneut veröffentlichen. Diese Funktion wird in Version 10.0.12 eingeführt.
- **Löschen** – Verwenden Sie die Aktion **Löschen**, um eine veröffentlichte oder unveröffentlichte Ansicht dauerhaft zu löschen. Diese Aktion entfernt auch die Ansicht für alle Benutzer im System. Das Entfernen von veröffentlichten Ansichten wird nach dem Auswählen der Schaltfläche **Speichern** wirksam. Nachdem eine Ansicht gelöscht wurde, kann sie nicht wiederhergestellt werden. 

## <a name="managing-views-globally"></a>Ansichten global verwalten

Obwohl auf jeder Seite einige Verwaltungsfunktionen angezeigt werden, wie in diesem Thema angegeben, kann **Systemadministratoren** und **gespeicherte Ansichtsadministratoren** Ansichten für das System ganzheitlicher über die Seite **Personalisierung** verwalten. Diese Seite enthält insbesondere die folgenden Abschnitte und Funktionen: 

- **Veröffentlichte Ansichten** – In diesem Abschnitt werden alle Ansichten aufgelistet, die für Ihre Organisation veröffentlicht wurden. Von hier aus können Sie eine Ansicht erneut veröffentlichen, nachdem Sie die Sicherheitsrollen oder juristischen Personen angepasst haben, auf die die Ansicht abzielt. Sie können Ansichten auch exportieren, löschen oder deren Veröffentlichung aufheben. In Version 10.0.12 und höher können Sie die Aktion **Als persönlich speichern** zum Erstellen einer persönlichen Kopie einer Ansicht verwenden, damit Sie die Ansicht aktualisieren oder deren Inhalt besser verstehen können. 
- **Unveröffentlichte Ansichten** – In diesem Abschnitt werden alle Organisationsansichten in Ihrem System aufgelistet, die derzeit nicht veröffentlicht sind. Diese Ansichten werden am häufigsten über die Importfunktion in das System eingegeben. Sie können diese Ansichten veröffentlichen, exportieren oder löschen. Die Aktion **Schnelle Veröffentlichung**, die in Version 10.0.12 hinzugefügt wurde, kann mehrere Ansichten aus diesem Abschnitt in einer Aktion veröffentlicht werden, indem die vorhandenen Konfigurationen für Sicherheitsrollen und juristische Personen verwendet werden. In Version 10.0.12 und höher können Sie die Aktion **Als persönlich speichern** zum Erstellen einer persönlichen Kopie der Ansicht verwenden, damit Sie die Ansicht aktualisieren oder den Inhalt besser verstehen können.
- **Persönliche Ansichten** – Dieser Abschnitt führt alle Ansichten auf, die von den Benutzern im System erstellt wurden. Von hier aus können Sie eine persönliche Ansicht für die Organisation veröffentlichen oder eine oder mehrere der Ansichten an andere Benutzer kopieren. Sie können diese Ansichten auch nach Bedarf exportieren oder löschen.
- **Benutzereinstellungen** – Wählen Sie einen Benutzer zum Anzeigen aus oder passen Sie die Fähigkeit des Benutzers an, die Personalisierung entweder für das gesamte System oder für bestimmte Seiten zu verwenden, die der Benutzer besucht hat. Sie können die Personalisierungen des Benutzers im System anzeigen und damit interagieren. Sie können auch alle Personalisierungen für diesen Benutzer löschen oder Funktionslegenden für den Benutzer zurücksetzen. Wenn Funktionslegenden zurückgesetzt wurden, werden Popupfenster, in denen neue Funktionen eingeführt wurden und die der Benutzer zuvor abgelehnt hat, beim nächsten Mal wieder angezeigt, wenn der Benutzer auf diese Funktionen trifft.
- **Systemeinstellungen** – Sie können temporär Personalisierung im System für alle Benutzer deaktivieren. In diesem Fall werden keine Personalisierungen für Benutzer angewendet und alle Seiten auf ihren Standardstatus zurückgesetzt. Wenn Sie die Personalisierungen später wieder reaktivieren, werden diese wieder angewendet. Sie können temporär alle Personalisierungen im System für alle Benutzer deaktivieren oder abschalten. Es gibt keine Möglichkeit, Personalisierungen wiederherzustellen, die gelöscht wurden. Deshalb müssen Sie vor diesem Schritt sicherstellen, dass Sie alle Personalisierungen exportiert haben, die Sie später importieren möchten.

Benutzer, die Zugriff auf die Seite **Personalisierung** haben, können die persönlichen oder Organisationsansichten auch importieren, indem sie die Schaltfläche **Ansichten importieren** im Aktivitätsbereich verwenden. In Version 10.0.12 und höher wurde ein Mechanismus hinzugefügt, mit dem Ansichten beim Import sofort veröffentlicht werden können.

## <a name="known-issues"></a>Bekannte Probleme
Eine Liste bekannter Probleme mit gespeicherten Ansichten finden Sie unter [Formulare, die gespeicherte Ansichten vollständig verwenden, erstellen](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Wie aktiviere ich gespeicherte Ansichten im meine Umgebung?

> [!NOTE]
> Für die Funktion **Gespeicherte Ansichten** muss das Personalisierungssystem in Finance and Operations aktiviert sein. Wenn die Personalisierung für die gesamte Umgebung deaktiviert ist, werden Ansichten deaktiviert, selbst wenn Sie die folgenden Schritte ausführen. 

**Version 10.0.13 und höher**

Die Funktion **Gespeicherte Ansichten** ist nicht mehr in der Vorschau vorhanden. Sie ist jetzt direkt über die Funktionsverwaltung in jeder Umgebung verfügbar.

**Versionen 10.0.9 bis 10.0.12**

Die Funktion **Gespeicherte Ansichten** ist in jeder Umgebung direkt in der Funktionsverwaltung verfügbar. Wie für andere öffentliche Vorschaufunktionen unterliegt auch die Aktivierung dieser Funktion in der Produktion den [Zusätzlichen Nutzungsbedingungen](https://go.microsoft.com/fwlink/?linkid=2105274).

**10.0.8/Plattformupdate 32 und früher**

Die Funktion **Gespeicherte Ansichten** kann in Stufe 1 (Dev/Test)- und Stufe 2 (Sandbox)-Umgebungen aktiviert werden, um zusätzliche Test- und Entwurfsänderungen bereitzustellen, indem die folgenden Schritte ausgeführt werden.

1. **Flight aktivieren**: Führen Sie die folgende SQL-Anweisung aus: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Reset IIS** zum Leeren des statischen Flighting-Cache. 
3. **Finden Sie die Funktion**: Gehen Sie zum Arbeitsbereich **Feature-Management**. Wenn **Gespeicherte Ansichten** nicht in der Liste erscheint, wählen Sie **Auf Updates prüfen**.
4. **Aktivieren Sie die Funktion**: Suchen Sie die Funktion **Gespeicherte Ansichten** in der Liste der Funktionen und wählen Sie **Jetzt aktivieren** im Detailbereich.

Alle folgenden Benutzersitzungen beginnen mit aktivierten gespeicherten Ansichten.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Was passiert an vorhandenen Personalisierungen, wenn Ansichten aktiviert werden? 

Wenn Ansichten aktiviert sind, werden alle vorhandenen Personalisierungen für einen Benutzer und ein Formular in eine neue Ansicht namens **Meine Ansicht** gespeichert, die automatisch als Standardansicht festgelegt wird. Damit wird sichergestellt, dass es eine konsistente Benutzerfreundlichkeit gibt bevor und nachdem Ansichten aktiviert werden, mit Ausnahme des Ansichtsauswahlteuerelements, das auf Formularen angezeigt wird.

### <a name="what-pages-support-views"></a>Welche Seiten unterstützen Ansichten? 

Ansichten sind auf den meisten jedoch nicht auf allen Seiten verfügbar. Im Speziellen sind Ansichten in allen Ganzseitenseiten ausgenommen Dashboards und Arbeitsbereiche verfügbar. Nicht-Voll-Bildschirmseiten, zu denen Dialogfelder, Drop-Down-Dialogfelder, Suchen, erweiterte Vorschauen gehören, unterstützen aktuell keine Ansichten. Ansichtenunterstützung für zusätzliche Seitentypen wie Arbeitsbereiche und Dialogfelder werden für eine zukünftige Aktualisierung berücksichtigt werden.

### <a name="who-is-allowed-to-publish-views"></a>Wer kann Ansichten veröffentlichen?

Nur Systemadministratoren und Benutzer, die der Rolle **Administrator für gespeicherte Ansichten** zugewiesen wurden, weisen die Rechte zum Veröffentlichen von Ansichten auf. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Warum kann ich keine Filter in dieser Ansicht speichern? 

Es gibt mehrere Gründe, warum ein Filter ggf. nicht zum Speichern in einer Ansicht angezeigt wird: 

- Die Seite unterstützt möglicherweise das Speichern von Filtern als Teil der Ansichtsdefinition nicht. Beachten Sie, dass nur Seiten mit großen Ansichtsauswahlen es zulassen, Personalisierungen und Abfrageänderungen als Ansicht zu speichern. Weitere Informationen finden Sie im Abschnitt **Zwischen Ansichten wechseln**. 
- Die gewünschte Seite unterstützt Ansichten möglicherweise nicht ordnungsgemäß, da sie die Ansichtsabfrage eventuell vollständig ignoriert oder mit einer temporären Tabelle arbeitet, deren Daten nicht persistent sind. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Welche Daten sehe ich, wenn ich eine Seite besuche?

Für Seiten mit Auswahlmöglichkeiten für kleine Ansichten (nur Personalisierungen können in der Ansicht gespeichert werden) werden dieselben Daten angezeigt, die Sie immer vorfinden, wenn Sie die Seite besuchen. 

Bei Seiten mit Auswahlmöglichkeiten für große Ansichten (sowohl Personalisierungen als auch Abfragen können in der Ansicht gespeichert werden) werden in der Regel die Daten angezeigt, die mit der Abfrage verknüpft sind, die Ihrer Standardansicht zugeordnet ist. Es gibt zwei Hauptausnahmen:

- Wenn Sie also beispielsweise über eine Kachel zu einer Seite navigieren, wird die Abfrage für die Kachel unabhängig von der Abfrage, die der Standardansicht zugeordnet ist, ausgeführt. Wenn Sie diese Kachel erstellt haben, nachdem Ansichten aktiviert wurden, wird durch Auswahl einer Kachel die Seite mit der dieser Kachel zugeordneten Ansicht geöffnet.
- Wenn Sie zu einer Seite navigieren und dieser Eingangspunkt bereits eine definierte Abfrage besitzt, wird die ursprüngliche Abfrage anstelle der Abfrage der Standardansicht ausgeführt. Wenn dies der Fall ist, sollten Sie beim Laden der Ansicht durch eine Informationsmeldung benachrichtigt werden. Sie können auch prüfen, indem Sie zu dieser Ansicht wechseln, nachdem die Seite geladen wird, damit sollte die Ansichtsabfrage unabhängig ausgeführt werden.
