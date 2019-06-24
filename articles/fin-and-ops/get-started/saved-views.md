---
title: Gespeicherte Ansichten
description: In diesem Thema wird beschrieben, wie Sie die gespeicherten Ansichtsfunktionen verwenden.
author: jasongre
manager: AnnBe
ms.date: 06/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: ea2f2dbd615480bb76e1d04a106ae69bf6f45f4b
ms.sourcegitcommit: fcae2e7938d7dbd94b76b0948b084d90d5fc919c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620777"
---
# <a name="saved-views"></a>Gespeicherte Ansichten

[!include [banner](../includes/banner.md)]
[!include [private preview banner](../includes/private-preview-banner.md)]

## <a name="introduction"></a>Einführung
Die Personalisierung spielt eine wichtige Rolle und erlaubt es Benutzern und Organisationen können,  die Benutzerfreundlichkeit in Microsoft Dynamics 365 for Finance and Operations zu optimieren, um ihren Anforderungen zu entsprechen. Weitere Details über die Personalisierung, finden Sie unter [Personalisieren Sie die Benutzerfreundlichkeit](personalize-user-experience.md).

Mit traditioneller Personalisierung könnten Benutzer einen individuellen Satz Personalisierungen pro Formular haben. Gespeicherte Ansichten erweitern sich auf die Personalisierung auf mehrere wichtige Arten:

-    Ansichten erlauben es Benutzern, mehrere Personalisierungen pro Formular zu erhalten, so dass rasch hin und her gewechselt werden kann. Somit kann ein Benutzer mehrere Ansichten einer Seite optimieren, wenn jede Ansicht angepasst wurde, um die Anforderungen der Ausführung einer bestimmten Aufgabe anzupassen. 

-    Die Ansicht, die für bestimmte Seitentypen erstellt werden, können auch von Benutzern hinzugefügte Filter enthalten, die es Benutzern ermöglichen, rasch zu den oft verwendeten gefilteretn Datensets zurückzukehren. Weitere Details im Abschnitt [Seiten, die Ansichten unterstützen](saved-views.md#what-pages-support-views). 

-    Ansichten können in Sicherheitsrollen veröffentlicht werden, das heißt dass jeder Benutzer mit der Rolle in der Lage ist, diese Ansicht anzuzeigen und zu nutzen, unabhängig von der Möglichkeit des Benutzers, diese zu personalisieren. Dieses Veröffentlichungsfunktion ermöglicht es Organisationen, Unternehmensstandardansichten zu definieren, die für ihr Geschäft optimiert werden. Weitere Details finden Sie im Abschnitt [Verwalten von Personalisierungen auf Organisationsebene mit Ansichten](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    Anders als traditionelle Personalisierungs-Ansichten werden Ansichten nicht automatisch gespeichert, wenn ein Benutzer Personalisierungen explizite ausführt oder eine Liste filtert. Explizite Speicherungen sind notwendig, um Flexibilität bereitzustellen, um eine Ansicht zu erstellen bevor oder nachdem die Änderungen, die mit dieser Ansicht zusammenhängen, eroflgt sind und um sicherzustellen, dass Ansichtsdefinitionen nicht versehentlich über Filter oder Personalisierungen geändert werden, die nicht für langfristige Verwendung vorgesehen werden.  

## <a name="switching-between-views"></a>Wechsel zwischen Ansichten
Nachdem Ansichten für eine Umgebung aktiviert wurden, enthält jede Seite, die auch unterstützt Ansichten unterstützt, ein Ansichtswählsteuerelement oben im Formular, das den Namen der aktuellen Ansicht anzeigt.  

Es gibt zwei Größenvarianten der Ansichts-Auswahl: 

-   **Große Ansichts-Auswahl**: Seiten, die prominent eine Liste haben, verfügen über eine größere Ansichts-Auswahl aus mehreren Gründen. Am wichtigsten ist, dass die größere Anzeigen-Auswahl die Seiten angezeigt, bei denen die Ansicht benutzerdefinierte Filter enthalten kann. Da Filter in der Ansicht enthalten sind, garantiert die größere Anzeigen-Auswahl auch, dass die Ansichtsnamen häufig die beste Beschreibung der Angaben enthalten, die auf dem Bildschirm angezeigt werden und die Erwartung ist, dass Benutzer häufiger auf diesen Seitentypen zwischen Ansichten wechseln.  
 
-   **Kleine Ansichts-Auswahlen**: Alle anderen ganzseitigen Formulare beinhalten eine kleinere Ansichts-Auswahl, die neben der Seitenbeschriftung angezeigt wird. Ansichten auf diesen Seiten enthalten Personalisierungen (und keine benutzerdefinierte Filter). Auf diesen Seiten umfasst die Formularbeschriftung oder der Datensatztitel häufig die wichtigsten Informationen oben im Formular. Das kleinere Format gibt auch eine niedrigere erwartete Häufigkeit für das Wechseln auf diesen Seiten. 
 
Wenn Sie im Feld Ansichtsnamen klicken, wird die Ansichts-Auswahl geöffnet und zeigt die Liste der verfügbaren Ansichten für diese Seite an

-    **Klassische Ansicht**: Die klassische Ansicht ist die Standardansicht der Seite ohne explizite übernommenen Personalisierungen.  
-    **Persönliche Ansichten**: Die Ansichten ohne Vorhängeschlösser stellen Ihre persönlichen Ansichten dar. Dies sind Ansichten, die Sie entweder erstellt haben oder die IHnen ein Administrator zugewiesen hat.  
-    **Gesperrte Ansichten**: Einiges Ansichten (wie die klassische Ansicht und Ansichten, die für Ihre Rolle veröffentlicht sind) verwenden ein Vorhängeschloss neben der Eingabe im Formular und zeigen an, dass Sie diese Ansichten nicht bearbeiten können. Allerdings werden implizite Personalisierungen um die Seitenverwendung automatisch gespeichert, beispielsweise zum Ändern der Breite einer Rasterspalte oder zum Erweitern oder Reduzieren des Inforegisters. Sie können eine persönliche Ansicht basierend auf einer gesperrten Ansicht mithilfe der Aktivität **Eine Kopie speichern** erstellen, wenn Sie Personalisierungsrechte haben.
-    **Neue Ansichten**: Veröffentlichte Ansichten, die noch nicht geöffnet wurden, werden mit einem Funken auf der linken Seite des Ansichtsnamens abgegrenzt.  

Um zu einer anderen Ansicht zu wechseln, öffnen Sie die Ansichts-Auswahl und wählen Sie die Ansicht aus, die Sie laden möchten. 

## <a name="creating-and-modifying-views"></a>Ansichten erstellen und ändern
Anders als traditionelle Personalisierungs-Ansichten werden Ansichten nicht automatisch gespeichert, wenn ein Benutzer Personalisierungen explizite ausführt (oder eine Liste filtert). Eine explizite Aktivität ist erforderlich, um diese Änderungen für eine Ansicht zu speichern. Das gibt dem Benutzer die Flexibilität beim Erstellen einer Ansicht, bevor oder nachdem die Änderungen, die mit dieser Ansicht zusammenhängen, erfolgt sind und um sicherzustellen, dass Ansichtsdefinitionen nicht versehentlich über Filter oder Personalisierungen geändert werden, die nicht für langfristige Verwendung vorgesehen werden. Beachten Sie, dass implizite Personalisierungen (wie erweitern oder reduzieren eines Inforegisters oder das Ändern der Breite einer Rasterspalte) automatisch gespeichert werden in der aktuellen Ansicht, selbst für gesperrte Ansichten. 

Um sicherzustellen dass der aktuelle Status der Ansicht bekannt ist, wenn Sie beginnen, diese Änderungen für eine Ansicht mithilfe einer expliziten Personalisierung oder einer Filterung auszuführen, erscheint ein Sternchen neben dem aktuellen Anzeigennamen und zeigt an, dass Sie eine nicht gespeicherte, geänderte Version dieser Ansicht betrachten.

Wenn Sie die diese Änderungen speichern möchten, führen Sie die folgenden Schritte aus.
1.  Wählen Sie den Ansichtsnamen aus, um die Ansichts-Auswahl zu öffnen.
2.  Um die vorhandenen Ansicht zu ändern:
     1. Wählen Sie **Speichern**. Beachten Sie, dass diese Aktion nicht für gesperrte Ansichten aktiviert ist. 
3.  Um eine neue Ansicht zu erstellen.
     1.    Wählen Sie **Kopie speichern**. 
     2.    Geben Sie einen Namen und eine (optionale) Beschreibung ein.
     3.    Wählen Sie **Speichern**.

## <a name="changing-the-default-view"></a>Die Standardansicht ändern
Die Standardansicht ist die Anzeige, die das System versucht zu öffnen, wenn Sie zur Seite navigieren. Sie sollten dieses auf die Anzeige festlegen, die Sie voraussichtlich oft verwenden werden.  

Um die Standardansicht für eine Seite zu ändern, führen Sie die folgenden Schritte aus: 
1.  Wechseln Sie zur Ansicht, die Sie standardmäßig verwenden. 
2.  Wählen Sie den Ansichtsnamen aus, um die Ansichts-Auswahl zu öffnen. 
3.  Wählen Sie **Weiter** und anschließend **Als Standard festsetzen** aus.  

Möchten Sie eine neue Ansicht (mithilfe der **Eine Kopie speichern**-Aktivität) erstellen, können Sie diese neue Ansicht zur Standardansicht machen, indem Sie die Option **Als Standard festsetzen** festlegen, bevor Sie die Ansicht speichern.  

Beachten Sie, dass in einigen Fällen die Abfrage, die der Standardansicht zugeordnet ist, nicht ausgeführt wird, wenn Sie erstmals zu einer Seite navigieren. Wenn Sie also beispielsweise über eine Kachel zu einer Seite navigieren, wird die Abfrage der Kachel unabhängig von der Abfrage, die der Standardansicht zugeordnet ist, ausgeführt. Falls Sie zu einer Seite navigieren, deren klassische Ansicht bereits eine definierte Abfrage besitzt, wird die ursprüngliche Abfrage anstelle der Abfrage der Standardansicht ausgeführt. Wenn dies der Fall ist, werden Sie durch eine Informationsmeldung benachrichtigt, wenn die Ansicht geladen wird. Der Wechsel von Ansichten, nachdem die Seite geladen wurde, sollte eine Ansichtsabfrage wie erwartet ermöglichen.

## <a name="managing-personal-views"></a>Verwalten von persönlichen Ansichten 
Das Dialogfeld **Verwalten Sie meine Ansichten** bietet grundlegende Verwaltungsfunktionen für Ihre persönlichen Ansichten und die Reihenfolge in der Ansichts-Auswahl. Um diese Seite zu öffnen, klicken Sie auf den Ansichtsnamen um das Ansichtswähldropdownmenü zu öffnen, wählen Sie **Weiter** und anschließend **Verwalten meiner Ansichten** aus.  

Für eine Liste der verfügbaren Ansichten für diese Seite sind die folgenen Aktivitäten verfügbar.  
-    **Ändern Sie die Standardansicht**: Verwenden Sie die Aktion **Als Standard festlegen**, um die derzeit markierte Ansicht als Standardansicht für diese Seite zu erstellen.  
-    **Ordnen Sie Ansichten neu**:  Nutzen Sie die Aktionen **Nach oben** und **Nach unten**, um Ihre Ansichten in einer bestimmten Reihenfolge neu anzuordnen.  
-    **Umbenennen einer Ansicht**: Verwenden Sie die Aktion **Umbenennen**, um den Namen der momentan markierten persönlichen Ansicht zu ändern. Diese Aktion wird für die gesperrte Ansichten deaktiviert. 
-    **Löschen Sie eine Ansicht**: Verwenden Sie die Aktiviät **Entfernen**, um die zurzeit markierte Ansicht von der Seite zu löschen. Es gibt keine Möglichkeit, eine Ansicht wieder herzustellen, nachdem sie gelöscht wurde.  

Sämtliche Änderungen, die an diesem Dialogfeld vorgenommen werden, treten in Kraft, wenn Sie die Schaltfläche **Speichern** auswählen.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Verwalten von Personalisierungen auf Organisationsebene mit Ansichten
Um die Verbesserungen beim Verwalten von Personalisierungen auf Organisationsebene zu verstehen, betrachten wir zuerste, wie die Verwaltung der Personalisierung vor diesen Ansichten gearbeitet hat.  

Ohne Ansichten würden Administratoren einen Satz Personalisierungen für eine Seite für einen Benutzer, eine Benutzergruppe oder für Benutzer verwenden, die das Personalisierungsformular nutzen. Wenn diese Benutzer Personalisierungsrechte hatten, werden die Personalisierungen dieser Seite angewendet. Allerdings gab es keine Möglichkeit, weitere Benutzer daran zu hindern, die Seite weiter zu personalisieren, was bedeutete, dass die Organisation nicht sicherstellen konnte, dass die Benutzer eine konsistente Benutzeroberfläche hatten. Wenn diese Benutzern keine Personalisierungsrechte haben, werden die Personalisierungen, die Ihnen von einem Administrator zugewiesen wurden, nicht geladen. Wenn neue Benutzer bei einer Organisation angestellt wurden, müssen Administratoren manuell die erforderlichen Personalisierungen für den Benutzer laden. Es gab keinen automatischen Mechanismus für das Angeben bestimmter Personalisierungen, die für diesen Benutzer verfügbar sein sollten.

Mit der gespeicherten Ansichtsfunktion wird die organisatorische Verwaltung von Personalisierungen viel einfacher, primär aufgrund der Möglichkeit, Ansichten für Sicherheitsrollen zu veröffentlichen. Nachdem eine Ansicht veröffentlich wurde, kann jeder Benutzer mit der Rolle diese Ansicht anzeigen und nutzen, unabhängig von der Möglichkeit des Benutzers, diese zu personalisieren. Während jeden Benutzer eine Kopie der veröffentlichten Ansicht hat, in der die Seitenverwendung (implizite Personalisierungen) automatisch angewendet wird, kann kein Benutzer Personalisierungen explizite speichern oder Aktualisierungen für die Abfrage der veröffentlichten Ansicht speichern (d.h., dass veröffentlichte Ansichten gesperrt sind). Wenn neue Benutzer eine Rolle zugewiesen erhalten, die in der Ansicht veröffentlicht ist, sehen sie automatisch die Ansichten, die ihren Rollen zugewiesen sind, ohne jegliche Aktivität vom Administrator. Ebenso wenn sich die Rollen eines Benutzers in der Organisation ändern, sind die Ansichten, die der alten Rolle zugeordnet sind, nicht mehr verfügbar ohne eine erneute Aktivität vom Administrator. Aktualisierungen an einer veröffentlichten Ansicht können einfach an Benutzern verteilt werden, indem die Ansicht zu den entsprechenden Sicherheitsrollen erneut veröffentlicht wird.

Dies Veröffentlichungsfunktion ermöglicht es Organisationen, Unternehmensstandardansichten zu definieren, die für ihr Geschäft für Benutzer in bestimmten Sicherheitsrollen optimiert werden.  

## <a name="publishing-views"></a>Veröffentlichte Ansichten
Während des Veröffentlichungsprozesses können Ansichten an mindestens einer Sicherheitsrolle zugewiesen werden und das heißt, dass jeder Benutzer mit der Rolle in der Lage ist, auf diese Ansicht zuzugreifen und diese zu verwenden, obwohl sie die Ansicht nicht bearbeiten können. Aktuell besitzen nur Systemadministratoren Rechte für die Aktivität **Veröffentlichen** im Ansichtsauswahl-Dropdownmenü.  

Führen Sie folgende Schritte aus, um eine Ansicht zu veröffentlichen. 
1.  Erstellen und Speichern einer persönlichen Kopie der Ansicht, die veröffentlicht werden soll. 
2.  Mit dieser Ansicht, die derzeit geladen ist, wählen Sie den Ansichtsnamen aus, um das Ansichtsauswahl-Dropdownmenü zu öffnen. 
3.  Wählen Sie die Schaltfläche **Mehr** und wählen Sie dann **Veröffentlichen** aus. Das Feld Veröffentlichen wird geöffnet.  
4.  Geben Sie einen Namen (optional) und eine Beschreibung für die Ansicht ein. Dies ist der Name, den die Benutzer, die diese Ansicht erhalten, in den Ansichts-Auswahl finden. Beachten Sie, dass keine Duplikat-Namen für veröffentlichte Ansichten für eine Seite zulässig sind, wenn die Liste der Rollen, für die sie angewendet werden, sich unterscheiden.  
5.  Fügen Sie alle Sicherheitsrollen hinzu, die den Benutzer entsprechen, die diese Ansicht erhalten.  
6.  Wählen Sie **Veröffentlichen** aus.

Beachten Sie, dass es in einer Umgebung einige Zeit in Anspruch nehmen kann (bis zu einer Stunde) bis Benutzer die veröffentlichte Ansicht sehen.

## <a name="modifying-a-published-view"></a>Ändern einer veröffentlichten Ansicht
Nachdem Sie eine Ansicht veröffentlicht haben, stellen Sie möglicherweise fest, dass Sie Änderungen für veröffentlichte Ansicht machen möchten. Während Sie keine Liveänderungen für veröffentlichte Ansicht machen können, da diese Ansichten zur Bearbeitung für alle Benutzer (einschließlich Herausgeber) gesperrt werden, können Sie eine Ansicht erneut veröffentlichen, um Aktualisierungen vornehmen.  

Wenn die Änderungen, die Sie an einer veröffentlichten Ansicht vornehmen möchten, nur die Veröffentlichungsparameter umfasst (der Name und die Beschreibung der Ansicht, oder die Sicherheitsrollen, in der die Ansicht veröffentlicht wird), gehen Sie folgendermaßen vor: 
1.  Wechseln Sie zur veröffentlichten Ansicht für die Parameter, die Sie aktualisieren möchten. 
2.  Wählen Sie im Dropdownmenü **Veröffentlichen** aus. 
3.  Wählen Sie **Ja** wenn Sie die vorhandenen Ansicht aktualisieren möchten (oder **Nein** wenn Sie dies unter einem anderen Namen veröffentlichen möchten).
4.  Aktualisieren Sie den Namen, die Beschreibung und/oder die Sicherheitsrolle für die Ansicht. 
5.  Wählen Sie **Veröffentlichen** aus. 
6.  Wenn Sie den Name der veröffentlichten Ansicht aktualisiert haben, müssen Sie auch die veröffentlichte Ansicht mit dem alten Namen löschen (vgl.  Abschnitt **Verwalten von veröffentlichten Ansichten** für weitere Details). 

Wenn Änderungen der veröffentlichten Ansicht die Personalisierungen oder Filter umfassen, die der Ansicht zugeordnet sind, folgen Sie diesen Schritten: 
1.  Wechseln Sie zur veröffentlichten Ansicht, die Sie aktualisieren möchten. 
2.  Hiermit wird eine Kopie der veröffentlichten Ansicht gespeichert, um einen lokalen Entwurf der veröffentlichten Ansicht zu erstellen. 
3.  Ändern Sie den lokalen Entwurf mit den erforderlichen Änderungen.
4.  Veröffentlicht Sie die Ansicht mit dem ursprünglichen Namen. 

## <a name="managing-published-views"></a>Verwalten von veröffentlichten Ansichten
Wie das Verwalten persönlicher Ansichten gibt das Dialogfeld **Verwalten meiner Ansichten** Benutzern mit grundlegenden Verwaltungsfunktionen die Rechte zum veröffentlichten von Ansichten dieser Seite (zusätzlich zu ihren eigenen persönlichen Ansicht). Um diese Seite zu öffnen, wählen Sie den Ansichtsnamen, um das Ansichtsauswahl-Dropdownmenü zu öffnen, wählen Sie **Weiter** und anschließend **Verwalten meiner Ansichten** aus.

Während alle Benutzer eine Registerkarte **Meine Ansichten** mit ihren persönlichen Ansichten sehen, sehen Benutzer mit Veröffentlichungsrechten auch eine Registerkarte **Veröffentlicht**, die alle veröffentlichten Ansichten für diese Seite angezeigt. Da es möglicherweise verschiedene veröffentlichte Ansichten für Benutzer gibt, ist es wichtig, in der Lage zu sein, die gesamte Liste der veröffentlichten Ansichten zu verwalten, unabhängig davon, ob sie der Benutzer waren, der die Ansicht veröffentlicht hat.

Für eine Liste aller veröffentlichten Ansichten für diese Seite sind die folgenen Aktivitäten verfügbar. 

-    **Veröffentlichen**: Verwenden Sie die Aktivität **Veröffentlichen** eine Ansicht mit geänderten veröffentlichten Parametern  (Name, Beschreibung, Sicherheitsrollen).  
-    **Entfernen**: Verwenden Sie die Aktivität **Entfernen**, um eine veröffentlichte Aktivität dauerhaft zu löschen. Diese Aktivität entfernt die Ansicht für alle Benutzer im System.  
 
Sämtliche Änderungen, die an diesem Dialogfeld vorgenommen werden, treten in Kraft, wenn die Schaltfläche **Speichern** ausgewählt ist.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Wie aktiviere ich gespeicherte Ansichten im meine Umgebung? 
Um gespeicherte Ansichten zu aktivieren, muss ein Systemadministrator folgende Schritte ausführen: 
1.  Gehen Sie zur Seite **Benutzereinstellungen** mithilfe der Navigationssuche. 
2.  Die Registerkarte **Einstellungen** auswählen.
3.  Legen Sie die Option **Gespeicherte Ansicht aktiveren** auf **Ja** fest.

Nachdem diese Funktion aktiviert ist, beginnen alle nachfolgenden Benutzersitzungen mit den aktivierten Ansichten.  

Beachten Sie, dass, wenn die Personalisierung für die Umgebung deaktiviert wird, Ansichten aktiviert werden, wenn Sie die oben genannten Schritte ausführen. Dies liegt daran, dass die Ansichtsfunktion auf dem Personalisierungsuntersystem erstellt wird.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Was passiert an vorhandenen Personalisierungen, wenn Ansichten aktiviert werden? 
Wenn Ansichten aktiviert sind, werden alle vorhandenen Personalisierungen für einen Benutzer und ein Formular in eine neue Ansicht namens **Meine Ansicht** gespeichert, die automatisch als Standardansicht festgelegt wird. Damit wird sichergestellt, dass es eine konsistente Benutzerfreundlichkeit gibt bevor und nachdem Ansichten aktiviert werden, mit Ausnahme des Ansichtsauswahlteuerelements, das auf Formularen angezeigt wird.  

### <a name="what-pages-support-views"></a>Welche Seiten unterstützen Ansichten? 
Ansichten sind auf den meisten jedoch nicht auf allen Seiten in Finance and Operations verfügbar. Im Speziellen sind Ansichten in allen Ganzseitenseiten ausgenommen Dashboards und Arbeitsbereiche verfügbar. Nicht-Voll-Bildschirmseiten, die Dialogfelder, Drop-Down-Dialogfelder, Suchen, erweiterte Vorschauen unterstützen aktuell ebenfalls keine Ansichten. Ansichtenunterstützung für zusätzliche Seitentypen wie Arbeitsbereiche und Dialogfelder werden für eine zukünftige Aktualisierung berücksichtigt werden.   

### <a name="who-is-allowed-to-publish-views"></a>Wer kann Ansichten veröffentlichen?
Momentan sind Systemadministratoren die einzigen Benutzer, die über die Rechte verfügen, Ansichten zu veröffentlichen.  Eine neue Sicherheitsrolle ist geplant, die Debitoren mehr Flexibilität geben soll, wer veröffentlichen kann.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Warum kann ich keine Filter in dieser Ansicht speichern? 
Es gibt mehrere Gründe, warum ein Filter ggf. nicht zum Speichern in einer Ansicht angezeigt wird: 

- Die Seite unterstützt möglicherweise das Speichern von Filtern als Teil der Ansichtsdefinition nicht. Beachten Sie, dass nur Seiten mit großen Ansichts-Auswahlen es zulassen, Personalisierungen und Abfrageänderungen als Ansicht zu speichern. Weitere Informationen finden Sie im Abschnitt „Zwischen Ansichten wechseln“. 

- Wenn die Ansicht die Standardansicht ist und der Navigationspfad der Seite eine Abfrage einbezieht, wird die Abfrage möglicherweise zunächst nicht angewendet werden. Die zwei primären Szenarien dafür sind:  
     - Wenn Sie also beispielsweise über eine Kachel zu einer Seite navigieren, wird die Abfrage für die Kachel unabhängig von der Abfrage, die der Standardansicht zugeordnet ist, ausgeführt. 
     - Wenn Sie zu einer Seite navigieren und dieser Eingangspunkt bereits eine definierte Abfrage besitzt, wird die ursprüngliche Abfrage anstelle der Abfrage der Standardansicht ausgeführt. 
     
  Sie sollten durch eine Informationsmeldung benachrichtigt werden, wenn die Ansicht geladen wird. Sie können auch prüfen, indem Sie zu dieser Ansicht wechseln, nachdem die Seite geladen wird, damit sollte die Ansichtsabfrage unabhängig ausgeführt werden.  

- Die gewünschte Seite wird nicht ordnungsgemäß unterstützt, da sie möglicherweise die Ansichtsabfrage vollständig ignoriert. Melden Sie solche Instanzen über den Mechanismus **Rückmeldung**. Um zur Rückmeldungsseite zu gelangen, klicken Sie auf **Hilfe und Support** und anschließend auf **Rückmeldung**.  
