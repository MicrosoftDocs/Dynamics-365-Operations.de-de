---
title: Verteilte Auftragsverwaltung (DOM)
description: In diesem Artikel wird die Funktion der verteilten Auftragsverwaltung (Distributed Order Management, DOM) in Microsoft Dynamics 365 Commerce beschrieben.
author: josaw1
ms.date: 11/16/2022
ms.topic: index-page
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.openlocfilehash: cfb89544580141ed397d27886f51fd0f1ac138d2
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785179"
---
# <a name="distributed-order-management-dom"></a>Verteilte Auftragsverwaltung (DOM)

[!include [banner](includes/banner.md)]

In diesem Artikel wird die Funktion der verteilten Auftragsverwaltung (Distributed Order Management, DOM) in Microsoft Dynamics 365 Commerce beschrieben.

DOM ist eine Omnichannel-Lösung zur Optimierung der Auftragserfüllung, die dabei hilft, die Auftragserfüllung in einem Lieferkettennetzwerk zu maximieren. DOM hilft Ihnen sicherzustellen, dass Produkte in den richtigen Mengen, aus den richtigen Quellen und zur richtigen Zeit an Ihre Kunden geliefert werden. DOM kann Ihnen auch dabei helfen, Gewinne zu maximieren, Kosten zu minimieren und Vorgaben der Vereinbarung zum Servicelevel zu erfüllen.

DOM verwendet Mixed Integer Programming (MIP) und prädiktive Analysemodelle, um Optimierungen sowohl auf Chargenebene als auch auf Ebene einzelner Aufträge durchzuführen. Diese Funktion ermöglicht es Einzelhändlern, definierte Regeln zu verwenden, um viele in Konflikt stehende Anforderungen an die Auftragserfüllung auszugleichen. In einem modernen Liefernetzwerk, in dem die Produktabwicklung eventuell über mehrere Kanäle erfolgt, müssen sich Unternehmen schnell an Auftragsänderungen, Lieferengpässe und Nachfragespitzen anpassen. DOM hilft Ihnen, die Auftragserfüllung zu maximieren und die richtigen Quellen für die Produktlieferung zu finden, basierend auf Geschäftsbeschränkungen und -zielen, wie z. B. Kostenminimierung, indem Aufträge von den nächstgelegenen Quellen ausgeführt werden. DOM verwendet die Entfernung zwischen Produkterfüllungsquellen und den Versandzielen, Kostenfaktoren, die als Optimierungsziele definiert sind, sowie Regeln, die als Einschränkungen definiert sind, wie z. B. Bestand an Erfüllungsknoten, um die Auftragserfüllung zu optimieren. DOM ermöglicht die Definition mehrerer Profile, die es Unternehmen ermöglichen, je nach Art des Unternehmens oder Verbrauchersegments unterschiedliche Optimierungsstrategien durchzuführen. 

Die folgende Abbildung zeigt den Lebenszyklus eines Auftrags in einem System für die verteilte Auftragsverwaltung.

![Lebenszyklus eines Auftrags bei der verteilten Auftragsverwaltung (DOM)](./media/flow.png "Lebenszyklus eines Auftrags im DOM-Kontext")

Das folgende Video bietet einen Überblick über die DOM-Funktionen in Dynamics 365 Commerce.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bRYl]

## <a name="set-up-dom"></a>DOM einrichten

1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
2. Erweitern Sie auf der Registerkarte **Konfigurationsschlüssel** den Knoten **Handel**, aktivieren Sie anschließend das Kontrollkästchen **Verteilte Auftragsverwaltung**.
3. Gehen Sie zu **Retail und Commerce \> Verteilte Auftragsverwaltung \> Einrichten \> DOM-Parameter**.
4. Legen Sie auf der Registerkarte **Allgemein** die folgenden Werte fest:

    - **Verteilte Auftragsverwaltung aktivieren** – Setzen Sie diese Option auf **Ja**.
    - **Verwenden von Bing Maps für DOM bestätigen** – Setzen Sie diese Option auf **Ja**.

        > [!NOTE]
        > Sie können diese Option nur dann auf **Ja** setzen, wenn die Option **Bing Karten aktivieren** auf der Registerkarte **Bing Karten** auf der Seite **Freigegebene Commerce-Parameter** (**Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Freigegebene Commerce-Parameter**) ebenfalls auf **Ja** gesetzt ist und wenn im Feld **Bing Karten-Schlüssel** ein gültiger Schlüssel eingegeben wurde.
        >
        > Im Portal von [Bing Karten-Entwicklungscenter](https://www.bingmapsportal.com/) können Sie den Zugriff auf Ihre Bing Karten-API-Schlüssel auf eine Reihe von Domänen beschränken, die Sie angeben. Mit dieser Funktion können Kunden einen strikten Satz von Referenzwerten oder IP-Adressbereichen festlegen, anhand derer der Schlüssel validiert wird. Anforderungen, die von Ihrer Zulassungsliste stammen, werden normal verarbeitet, während Anforderungen, die nicht auf der Liste stehen, der Zugriff verweigert wird. Wahlweise kann der API-Schlüssel mit Domänensicherheit ausgestattet werden. Unveränderte Schlüssel funktionieren weiterhin. Die Zulassungsliste eines Schlüssels ist unabhängig von allen anderen Schlüsseln, damit Sie für jeden Schlüssel verschiedene Regeln festlegen können. Die verteilte Auftragsverwaltung unterstützt nicht die Einrichtung domänenbezogener Eigenschaften.

    - **Einbehaltungsdauer in Tagen** – Geben Sie an, wie lange von DOM-Abläufen erzeugte Erfüllungspläne im System behalten werden sollen. Der Batchauftrag **Einrichten des Löschenauftrag für DOM-Erfüllungsdaten** löscht alle Erfüllungspläne, die älter sind, als die Anzahl der hier angegebenen Tage.
    - **Ablehnungszeitraum (in Tagen)** – Geben Sie an, wie viel Zeit vergehen soll, bis eine abgelehnte Auftragsposition dem gleichen Standort zugewiesen werden kann.

5. Legen Sie auf der Registerkarte **Solver** die folgenden Werte fest:

    - **Max. Versuche zur automatischen Erfüllung** – Geben Sie an, wie häufig die DOM-Modul versuchen soll, eine Auftragsposition an einen Standort zu vermitteln. Wenn die DOM-Modul eine Auftragsposition nicht nach der angegebenen Anzahl der Versuche einem Standort vermitteln kann, wird die Auftragsposition als Ausnahme markiert. In zukünftigen Abläufen wird die Position dann solange übersprungen, bis der Status manuell zurückgesetzt wird.
    - **Regionsradius für lokales Geschäft** – Geben Sie einen Wert ein. In diesem Feld können Sie festlegen, wie Standorte gruppiert und in Bezug auf die Entfernung als gleichwertig betrachtet werden. Wenn Sie beispielsweise **100** eingeben, wird jedes Geschäft oder Verteilzentrum innerhalb eines 100-Meilen-Radius der Erfüllungsadresse in Bezug auf die Entfernung als gleichwertig betrachtet.
    - **Solver-Typ** – Wählen Sie einen Wert aus. Für Commerce sind zwei Solver-Typen freigegeben: **Produktions-Solver** und **Vereinfachter Solver**. Für alle Maschinen, auf denen DOM ausgeführt wird (d. h., alle Server, die zur DOMBatch-Gruppe gehören), muss **Produktions-Solver** ausgewählt werden. Der Produktions-Solver erfordert den Lizenzschlüssel, der standardmäßig in Produktionsumgebungen lizenziert und festgestellt wird. In neueren Ebene 2+-Umgebungen ist der Produktions-Solver bereits aktiviert. Für Nicht-Produktionsumgebungen muss dieser Lizenzschlüssel manuell angegeben werden. Um den Lizenzschlüssel manuellen bereitzustellen, führen Sie die folgenden Schritte aus:

        1. Öffnen Sie in Microsoft Dynamics Lifecycle Services die Bibliothek der freigegebenen Anlage, wählen Sie **Modell** als Anlagentyp aus, und laden Sie die Datei **DOM-Lizenz** herunter.
        1. Starten Sie den Microsoft Internetinformationsdienste (IIS)-Manager, klicken Sie mit der rechten Maustaste auf **AOSService-Website**, und wählen Sie anschließend **Entdecken** aus. Ein Windows Explorer-Fenster wird bei **\<AOS service root\>\\webroot** geöffnet. Notieren Sie den Pfad zu \<AOS Service root\>, da Sie ihn im nächsten Schritt verwenden werden.
        1. Kopieren Sie die Konfigurationsdatei im Verzeichnis **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Gehen Sie zum Client „Headquarters“, und öffnen Sie die Seite **DOM-Parameter**. Wählen Sie auf der Registerkarte **Solver** im Feld **Solver-Typ** die Option **Produktions-Solver** aus, und bestätigen Sie, dass keine Fehlermeldungen angezeigt werden.

        > [!NOTE]
        > Der Vereinfachte Solver wird bereitgestellt, damit Einzelhändler die DOM-Funktion ausprobieren können, ohne eine spezielle Lizenz bereitzustellen. Organisationen können den vereinfachten Solver nicht in Produktionsumgebungen verwenden.
        >
        > Der Produktions-Solver verbessert die Leistung (beispielsweise die Anzahl an Aufträgen und Auftragspositionen, die bei einer Ausführung verarbeitet werden können) und die Ergebniskonvergenz (weil eine Auftragscharge in manchen Fällen nicht die besten Ergebnisse liefert). Für die Regel **partielle Aufträge** ist der Produktions-Solver erforderlich.

6. Gehen Sie zurück zu **Einzelhandel und Handel \> Verteilte Auftragsverwaltung \> Einrichten \> DOM-Parameter**.
7. Weisen Sie auf der Registerkarte **Nummernkreise** anschließend den verschiedenen DOM-Entitäten die erforderlichen Nummernkreise zu.

    > [!NOTE]
    > Bevor die Nummernkreise zugeordnet werden können, müssen Sie die Entitäten auf der Seite **Nummernkreise** (**Organisationsverwaltung \> Nummernkreise \> Nummernkreise**) definieren.

8. Die DOM-Funktion unterstützt die Definition verschiedener Arten von DOM-Regeln, und Organisationen können abhängig von ihren Geschäftsanforderungen mehrere Regeln konfigurieren. DOM-Regeln können für eine Gruppe von Standorten oder einzelne Standorte sowie für eine bestimmte Produktkategorie, ein Produkt oder eine Variante definiert werden. Um die Gruppierung der Lagerplätze zu erstellen, die für die DOM-Regeln verwendet werden müssen, führen Sie die folgenden Schritte aus:

    1. Gehen Sie zu **Retail und Commerce \> Kanaleinstellungen \> Erfüllungsgruppen**.
    2. Geben Sie unter **Neu** einen neuen Namen und eine Beschreibung für die neue Gruppe ein.
    3. Wählen Sie **Speichern** aus.
    4. Wählen Sie **Position hinzufügen** aus, um einem einzelnen Standort zur Gruppe hinzuzufügen. Wählen Sie alternativ **Positionen hinzufügen** aus, um mehrere Standorte hinzuzufügen.

    > [!NOTE]
    > Ab Commerce Version 10.0.12 muss im Arbeitsbereich **Funktionsverwaltung** die **Option, Standorte in der Erfüllungsgruppe als „Versand“ oder „Abholung“ anzugeben** aktiviert sein.
    >
    > Mit dieser Funktion werden der Seite **Erfüllungsgruppe** neue Konfigurationen hinzugefügt, damit Sie festlegen können, ob das Lager für den Versand verwendet werden kann oder ob die Kombination aus Lager und Geschäft für Versand, Abholung oder beides verwendet werden kann. 
    >
    > Wenn Sie die Funktion aktivieren, werden die zur Standortauswahl verfügbaren Optionen beim Erstellen von Abhol- oder Versandaufträgen am POS aktualisiert.
    >
    > Das Aktivieren der Funktion führt auch zu aktualisierten Seiten am POS, wenn die Vorgänge „Alle versenden“ oder „Ausgewählte versenden“ ausgewählt werden.

9. Um Regeln definieren, gehen Sie zu **Retail und Commerce \> Verteilte Auftragsverwaltung \> Einstellungen \> Regeln verwalten**. Die folgenden DOM-Regeln werden derzeit unterstützt:

    - **Mindestlagerbestandsregel** – Durch diesen Regeltyp können Organisationen für andere Zwecke als die Auftragserfüllung "Umzäunungen" für eine bestimmte Menge eines Produkts festlegen. Beispielsweise können Organisationen wünschen, dass DOM nicht den gesamten Bestand berücksichtigt, der in einem Geschäft zur Auftragserfüllung verfügbar ist. Stattdessen müssen Sie einen Lagerbestand für die Laufkundschaft reservieren. Wenn dieser Regeltyp verwendet wird, können Sie beispielsweise den Mindestlagerbestand definieren, der für eine Produktgruppe, ein Einzelprodukt oder eine Produktvariante pro Standort oder Standortgruppe behalten werden soll. Sie können auch einen Mindestbestand definieren, indem Sie eine ergänzende Kategoriehierarchie verwenden. Wenn ein Produkt in mehrere Kategorien fällt, wird einer zusätzlichen Kategorie für alle Regeln, in denen Sie Kategorien verwenden können, höchste Bedeutung beigemessen.
    - **Prioritätsregel für Erfüllungsstandort** – Durch diesen Regeltyp können Organisationen eine Hierarchie der Standorte definieren, um eine Priorität festzulegen, nach der das Modul für die verteilte Auftragsverwaltung versucht, Erfüllungsstandorte für bestimmte Produkte zu finden. Der gültige Prioritätsbereich ist 1 bis 10, wobei 1 die höchste Priorität und 10 die niedrigste Priorität hat. Standorte, die höhere Priorität aufweisen, werden vor Standorten berücksichtigt, die niedrigere Priorität haben. Wenn die Regel als uneingeschränkte Einschränkungsregel definiert wird, werden Aufträge nur an Standorte vermittelt, für die Prioritäten definiert wurden. In DOM wird der Versand von Bestellungen komplett von einem Standort aus bevorzugt. Wenn daher eine vollständige Bestellung und ihre Positionen nicht an einem Standort mit Priorität 1 verfügbar sind, versucht DOM, sie von einem Standort mit Priorität 2 zu erfüllen.
    - **Partielle Auftragsregel** – In Retail Version 10.0.5 wurde der Parameter **Auftrag nur von einem Standort aus erfüllen** in **Maximale Erfüllungsstandorte** geändert. Mit dem alten Parameter konnten Benutzer konfigurieren, ob Bestellungen von nur einem Standort oder von so vielen Standorten wie möglich ausgeführt werden können. Mit dem neuen Parameter können Benutzer angeben, ob die Erfüllung von einer bestimmten Menge von Standorten (bis zu fünf) oder von so vielen Standorten wie möglich erfolgen kann. Für alle Optionen mit Ausnahme der Erfüllung von einem Standort teilt DOM die Position auf, da die Auftragsabwicklung nach Position erfolgt. Diese Regel funktioniert nur mit dem Produktions-Solver.
    - **Regel für Erfüllungsstandort offline** – Mit dieser Regel können Organisationen einen Standort oder eine Standortgruppe für DOM als offline oder als nicht verfügbar angeben, damit diesen Lagerorten keine Aufträge zur Erfüllung zugewiesen werden.
    - **Regel für maximale Ablehnung** – Mit dieser Regel können Organisationen einen Schwellenwert für Ablehnungen definieren. Wenn der Schwellenwert erreicht wird, markiert der DOM-Prozessor einen Auftrag oder eine Auftragsposition als Ausnahme und schließt ihn oder sie durch Entfernen von späterer Bearbeitung aus. Um die Leistung sicherzustellen, betrachtet DOM nicht den Verlauf aller Ablehnungen. 

        Wenn Auftragspositionen einem Standort zugewiesen sind, kann der Standort eine zugewiesene Auftragsposition ablehnen, da er aus bestimmten Gründen möglicherweise nicht in der Lage ist, die Position zu erfüllen. Abgelehnte Positionen werden als Ausnahme markiert und wieder in den Pool für die weitere Verarbeitung bei der nächsten Ausführung gestellt. Bei der nächsten Ausführung versucht DOM, die abgelehnte Position einem anderen Standort zuzuweisen. Der neue Standort kann die zugewiesene Auftragsposition auch ablehnen. Dieser Zyklus von Zuweisung und Ablehnung kann wiederholt ausgeführt werden. Wenn die Anzahl der Ablehnungen den definierten Schwellenwert erreicht, markiert DOM die Auftragsposition als permanente Ausnahme und wählt die Position nicht erneut für eine Zuweisung aus. DOM berücksichtigt die Auftragsposition nur dann wieder für eine erneute Zuweisung, wenn ein Benutzer den Status der Auftragsposition manuell zurücksetzt.

    - **Regel für maximale Entfernung** – Mit dieser Regel können Organisationen die maximale Entfernung definieren, in der sich ein Standort oder eine Standortgruppe befinden kann, um den Auftrag zu erfüllen. Wenn Regeln für maximal überlappende Entfernungen für einen Standort definiert werden, wendet DOM die niedrigste maximale Entfernung an, die für diesen Standort definiert ist.
    - **Regel für maximale Auftragsanzahl** – Mit dieser Regel können Organisationen die maximale Anzahl von Aufträgen definieren, die ein Standort oder eine Standortgruppe bearbeiten kann. Während des Optimierungsprozesses berücksichtigt das System Bestellungen, die nicht von diesen Standorten versendet wurden. Diese Prüfung erfolgt profilübergreifend. Wenn daher überlappende maximale Anzahlen von Bestellungen in Profilen für denselben Standort definiert sind, berücksichtigt das System die maximale Anzahl von Bestellungen, die in allen Profilen definiert ist. 

    Nachfolgend sind einige der allgemeinen Attribute aufgeführt, die für alle vorhergehenden Regeltypen definiert werden können:

    - **Startdatum** und **Enddatum** – Sie können diese Felder verwenden, um die einzelnen Gültigkeitsdaten in Kraft zu setzen.
    - **Deaktiviert** – Nur Regeln, die in diesem Feld den Wert **Nein** haben, werden in einer DOM-Ausführung berücksichtigt.
    - **Unbedingte Einschränkung** – Eine Regel kann als unbedingte oder nicht unbedingte Einschränkung definiert werden. Jede DOM-Ausführung durchläuft zwei Iterationen. In der ersten Iteration wird jede Regel als unbedingte Einschränkungsregel behandelt, unabhängig von der Einstellung dieses Feldes. Das bedeutet, dass jede Regel angewendet wird. Die einzige Ausnahme ist die Regel **Standortpriorität**. In der zweiten Iteration werden die Regeln entfernt, die nicht als unbedingte Einschränkungsregeln definiert wurden, und der Auftrag oder die Auftragspositionen, die bei Anwendung aller Regeln keinen Standorten zugewiesen wurden, werden nun Standorten zugewiesen.

10. Erfüllungsprofile werden verwendet, um eine Regelsammlung, juristische Personen, Auftragsursprünge und Lieferarten zu gruppieren. Jede DOM-Ausführung gilt für ein bestimmtes Erfüllungsprofil. Auf diese Weise können Organisationen eine Gruppe von Regeln für mehrere juristische Personen für Aufträge definieren und ausführen, die bestimmte Auftragsursprünge und -Lieferarten haben. Wenn ein anderer Regelsatz für andere Auftragsursprünge oder Lieferarten ausgeführt werden muss, können die Erfüllungsprofile entsprechend definiert werden. Gehen Sie zum Einrichten von Erfüllungsprofilen folgendermaßen vor:  

    1. Gehen Sie zu **Retail und Commerce \> Verteilte Auftragsverwaltung \> Einrichten \> Erfüllungsprofile**.
    2. Wählen Sie **Neu** aus.
    3. Geben Sie in den Feldern **Profil** und **Beschreibung** Werte ein.
    4. Aktivieren Sie die Option **Ergebnis automatisch übernehmen**. Wenn Sie diese Option auf **Ja** setzen, werden die Ergebnisse der DOM-Ausführung für das Profil automatisch in die Auftragspositionen übernommen. Wenn Sie diese auf **Nein** setzen, können die Ergebnisse nur im Erfüllungsplan angezeigt werden können. Sie werden nicht in die Auftragspositionen übernommen.
    5. Soll das DOM-Profil bei Aufträgen mit jedwedem Auftragsursprung ausgeführt werden, darunter auch Aufträge, bei denen der Auftragsursprung nicht angegeben ist, legen Sie die Option **Aufträge mit leerem Auftragsursprung verarbeiten** auf **Ja** fest. Um das Profil nur bei einigen Auftragsursprüngen auszuführen, können Sie diese auf der Seite **Auftragsursprünge** festlegen. Hierzu folgt später noch eine Erklärung.

        > [!NOTE]
        > Ab Commerce-Version 10.0.12 muss im Arbeitsbereich **Funktionsverwaltung** die **Option, einem Erfüllungsprofil eine Erfüllungsgruppe zuzuweisen** aktiviert sein. Mit dieser Funktion können Sie eine Liste von Lagern angeben, die DOM berücksichtigen soll, wenn die Optimierung mit einem Erfüllungsprofil ausgeführt wird. Wenn diese Lagerliste nicht angegeben ist, sucht DOM nach allen Lagern juristischer Personen, die im Profil definiert sind.
        >
        > Mit dieser Funktion wird auf der Seite **Erfüllungsprofil** eine neue Konfiguration ergänzt, die einer einzelnen Erfüllungsgruppe zugewiesen werden kann. 
        >
        > Wenn Sie die Erfüllungsgruppe auswählen, werden die DOM-Regeln für dieses Erfüllungsprofil effizient mit Bezug zu den in der Erfüllungsgruppe enthaltenen „Versandlagern“ ausgeführt. 
        > 
        > Um diese Funktion sinnvoll einzusetzen, stellen Sie sicher, dass es eine Erfüllungsgruppe gibt, die alle Versandlager enthält, und ordnen Sie diese Erfüllungsgruppe dann dem Erfüllungsprofil zu.

    6. Aktivieren Sie auf dem Inforegister **Juristische Personen** die Option **Hinzufügen**, und wählen Sie dann eine juristische Person aus.
    7. Aktivieren Sie auf dem Inforegister **Regeln** die Option **Hinzufügen**, und wählen Sie dann die Regel aus, die mit dem Profil verknüpft werden soll.
    8. Wiederholen Sie die obigen zwei Schritte, bis dem Profil alle erforderlichen Regeln zugeordnet sind.
    9. Wählen Sie **Speichern**.
    10. Klicken Sie im Aktionsbereich auf die Registerkarte **Einstellungen**, und wählen Sie **Lieferarten** aus.
    11. Wählen Sie auf der Seite **Lieferarten** die Option **Neu** aus.
    12. Wählen Sie im Feld **Unternehmen** aus, die juristische Person aus. Die Liste der Unternehmen wird auf die juristischen Personen beschränkt, die Sie zuvor hinzugefügt haben.
    13. Im Feld **Lieferart** wählen Sie die Lieferart aus, die diesem Profil zugeordnet werden soll. Eine Lieferart kann nicht mehreren aktiven Profilen zugeordnet werden.
    14. Wiederholen Sie die obigen beiden Schritte, bis dem Profil alle erforderlichen Lieferarten zugeordnet sind.
    15. Schließen Sie die Seite **Lieferarten**.
    16. Klicken Sie im Aktionsbereich auf die Registerkarte **Einstellungen**, und wählen Sie **Auftragsursprünge** aus.
    17. Wählen Sie auf der Seite **Auftragsursprünge** die Option **Neu** aus.
    18. Wählen Sie im Feld **Unternehmen** aus, die juristische Person aus. Die Liste der Unternehmen wird auf die juristischen Personen beschränkt, die Sie zuvor hinzugefügt haben.
    19. Wählen Sie im Feld **Auftragsursprung** den Auftragsursprung aus, der diesem Profil zugeordnet werden soll. Ein Auftragsursprung kann nicht mehreren aktiven Profilen zugeordnet werden.
    20. Wiederholen Sie die obigen beiden Schritte, bis dem Profil alle erforderlichen Auftragsursprünge zugeordnet sind.
    21. Schließen Sie die Seite **Auftragsursprünge**.
    22. Legen Sie die Option **Profil aktivieren** auf **Ja** fest. Wenn in den Einstellungen ein Fehler vorhanden ist, erhalten Sie eine Warnmeldung.

## <a name="dom-processing"></a>DOM-Verarbeitung

DOM wird nur in einen Batchauftrag ausgeführt. Um den Batchauftrag für DOM-Ausführungen zu konfigurieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Retail und Commerce \> Verteilte Auftragsverwaltung \> Stapelverarbeitung \> DOM-Verarbeitung für einen Auftrag einrichten**.
1. Wählen Sie im Inforegister **Parameter** im Feld **Erfüllungsprofil** ein Profil aus, für das DOM ausgeführt werden muss.
1. Wählen Sie im Inforegister **Im Hintergrund ausführen** im Feld **Stapelverarbeitungsgruppe** eine konfigurierte Stapelverarbeitungsgruppe aus.
1. Geben Sie im Feld **Aufgabenbeschreibung** einen Namen für den Batchauftrag ein.
1. Wählen Sie **Wiederholung** aus, und definieren Sie die Wiederholung des Batchauftrags.
1. Wählen Sie **OK**.

Zum Zeitpunkt des Verarbeitung berücksichtigt DOM die Reihenfolge und die Auftragspositionen, die im Folgenden beschrieben sind:

- Auftragspositionen, die die Kriterien für Auftragsursprünge, Lieferarten und juristische Person gemäß dem DOM-Profil erfüllen und die auch alle folgenden Kriterien erfüllen:

    - Sie werden von den Handelskanälen erstellt.
    - Sie wurden nie durch DOM vermittelt.
    - Sie wurden zuvor durch DOM vermittelt, sind aber als Ausnahmen markiert und liegen unter halb des maximalen Schwellenwertes für Versuche.
    - Die Lieferart lautet nicht Abholung oder elektronischen Lieferung.
    - Sie sind nicht zur Lieferung markiert.
    - Sie wurden nicht manuell ausgeschlossen.

- Aufträge sind nicht gesperrt

Nach der Anwendung der Regeln, der Bestandseinschränkungen und der Optimierung wählt DOM den Standort aus, der der Lieferadresse des Kunden am nächsten ist. DOM konvertiert Adressen des Typs **Lieferung** in Breiten- und Längenwerte. Anschließend konvertiert es die Lieferadresse auf dem Verkaufsauftrag in Breiten- und Längenwerte und aktualisiert die Breiten- und Längenwerte der Adresse für die zukünftige Verwendung. DOM hängt von Bing Karten ab, um genaue Breiten- und Längenwerte basierend auf Adress-, Stadt- und Postleitzahleninformationen zu bestimmen.

DOM verwendet die Bing Karten-API, um je nach Einstellungen Luft- oder Straßenentfernung zu berechnen. Anhand dieser Informationen ermittelt es dann die Versandkosten. Das Optimierungsmodell priorisiert die Erfüllung einer kompletten Bestellung von einem Standort aus. Auch wenn ein Teil einer Bestellung in der gleichen Stadt oder Postleitzahl verfügbar ist, wurde das Modell optimiert, um die Anzahl der Sendungen zu reduzieren. 

DOM sucht nach verfügbarem Bestand, indem es den verfügbaren Bestand in V2-Lagerentitäten anzeigt. Während jeder Chargenausführung teilt DOM Bestellungen abhängig vom Parameterwert **DOM-Verarbeitung** der Aufgaben in Chargen auf, die im Profil definiert sind. Dieser Parameter hat einen Standardwert von **2000**. Wenn beispielsweise 10.000 Auftragspositionen in einem Lauf optimiert werden und der Parameter **DOM-Verarbeitung** auf den Standardwert von **2000** gesetzt wird, erstellt DOM fünf Chargen, die gleichzeitig verarbeitet werden. Auftragserfüllungspläne werden dann vom Optimierer abgerufen und auf die Position angewendet. Wenn die Auftragsposition auf zwei Standorte aufgeteilt werden muss, stellt DOM sicher, dass Preise und Steuern angemessen auf die Positionen verteilt werden.

![Kriterien für Verkaufsaufträge.](./media/ordercriteria.png "Kriterien für Verkaufsaufträge")

## <a name="results-of-dom-runs"></a>Ergebnisse von DOM-Ausführungen

Wenn das Erfüllungsprofil auf **Automatisch übernehmen** festgelegt ist, werden die Ergebnisse der Ausführung automatisch in die Auftragspositionen übernommen, und der Auftragserfüllungsplan kann separat angezeigt werden. Ist das Erfüllungsprofil nicht auf **Automatisch übernehmen** festgelegt, können nur die Ergebnisse des Durchlaufs nur in der Erfüllungsplanansicht angezeigt werden. 

Um alle erzeugten Erfüllungspläne anzuzeigen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Retail und Commerce \> Verteilte Auftragsverwaltung \> Verteilte Auftragsverwaltung**.
2. Wählen Sie Arbeitsbereich **Verteilte Auftragsverwaltung** die Kachel **Erfüllungspläne** aus.
3. Wählen Sie die ID des relevanten Auftragserfüllungsplans aus, um den Erfüllungsplan anzuzeigen.

    Der Abschnitt mit den Bestelldetails im Erfüllungsplan zeigt die Originalauftragspositionen an, die Teil des Durchlaufs waren. Neben den Standardfeldern für die Auftragspositionen enthält der Abschnitt mit den Bestelldetails auch die folgenden drei DOM-spezifischen Felder:

    - **Erfüllungstyp** – Dieses Feld gibt an, ob die Auftragsposition vollständig, teilweise oder gar nicht an einen Standort vermittelt wurde.
    - **Teilen** – Dieses Feld gibt an, ob die Auftragsposition auf verschiedene Standorte aufgeteilt und an diese vermittelt wurde.
    - **Anzahl Erfüllungsstandorte** – Dieses Feld gibt an, wie viele Erfüllungspositionen für eine Auftragsposition erstellt wurden (basierend auf der Anzahl der Standorte, an die die ursprüngliche Auftragsposition vermittelt wurde).

    Der Abschnitt mit den Auftragserfüllungsdetails zeigt die Zuteilung der Originalauftragspositionen zu den verschiedenen Standorten sowie die jeweiligen Mengen an.

## <a name="order-line-actions-and-statuses"></a>Auftragspositionsaktivitäten und Statusangaben

Im Folgenden werden die Einstellungen für die Auftragsposition beschrieben. Gehen Sie zu **Retail und Commerce \> Kunden \> Alle Aufträge**, um die Auftragsposition zu öffnen.

- Ist der Option **Aus DOM-Verarbeitung ausschließen** auf der Registerkarte **Allgemein** der Auftragsposition auf **Ja** gesetzt, wird der Auftrag oder die Auftragsposition aus der DOM-Verarbeitung ausgeschlossen.
- Im Feld **DOM-Status** auf der Registerkarte **Allgemein** der Auftragsposition kann einer der folgenden Werte festgelegt werden:

    - **Kein** – Die Auftragsposition wurde nie vermittelt.
    - **Vollständig** – Die Auftragsposition wurde erfolgreich vermittelt und einem Standort zugewiesen.
    - **Ausnahme** – Die Auftragsposition wurde vermittelt, kann aber keinem Standort zugewiesen werden. Ausnahmen haben mehrerer Untertypen, die vom DOM-Arbeitsbereich aus angezeigt werden können:

        - **Keine Menge verfügbar** – Es ist kein verfügbarer Lagerbestand verfügbar, mit dem der Auftrag Standorten zugewiesen werden kann.
        - **Maximale Ablehnungen** – Die Auftragsposition hat den maximalen Schwellenwert für Ablehnungen erreicht.
        - **Datenänderungskonflikt** – Die Auftragsposition wurde seit der Vermittlung des Auftrags geändert. Daher kann der Erfüllungsplan nicht in den Auftrag übernommen werden.
        - **Auftragspositionsspezifische Ausnahme** – Es gibt mehrere Ausnahmen in der Auftragsposition.

- DOM kann während der Auftragserfassung im interaktiven Modus ausgeführt werden. Wenn Sie eine Auftragsposition eingeben, können Sie nach der Eingabe des Produkts und der Menge die Option **Position aktualisieren** und dann unter **DOM** die Option **Erfüllungsstandort vorschlagen** auswählen. Dann wird eine auf den DOM-Regeln basierende Liste der Standorte angezeigt, die die Menge in der Auftragsposition erfüllen können. Die Liste ist nach Entfernung sortiert. Wählen Sie einen Standort aus, um den entsprechenden Standort und das Lage in der Auftragsposition festzulegen. Damit diese Funktionen greifen, muss ein aktives Erfüllungsprofil vorhanden sein, dass mit dem Auftragsursprung und der Lieferart in der Auftragsposition übereinstimmt.
- Um die DOM-Ausführungsprotokolle für eine Auftragsposition anzuzeigen, wählen Sie **Auftragsposition** und dann unter **DOM** die Option **DOM-Protokolle anzeigen** aus. In den DOM-Protokolle werden alle Ereignisse und Protokolle angezeigt, die von der DOM-Ausführung generiert wurden. Anhand der Protokolle erkennen Sie einfach, warum der Auftragsposition ein bestimmter Standort zugewiesen wurde und welche Regeln und Einschränkungen zur Zuweisung gehören. Auf der Registerkarte **Verwalten** sind die DOM-Protokolle auch im Auftragskopf verfügbar.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Ausführen eines Bereinigungsauftrags für DOM-Erfüllungspläne

Während die DOM-Verarbeitung ausgeführt wird, werden Erfüllungspläne erstellt. Im Laufe der Zeit verfügt das System über verschiedene Erfüllungspläne. Um die Anzahl der Erfüllungspläne im System zu verwalten, können Sie einen Batchauftrag konfigurieren, der ältere Erfüllungspläne basierend auf dem Wert **Einbehaltungszeitraum in Tagen** löscht.

1. Gehen Sie zu **Retail und Commerce \> Verteilte Auftragsverwaltung \> Stapelverarbeitung \> Einrichtung DOM-Erfüllungsdaten-Löschauftrag**. 
1. Wählen Sie im Feld **Stapelverarbeitungsgruppe** eine konfigurierte Stapelverarbeitungsgruppe aus.
1. Wählen Sie **Wiederholung** aus, und definieren Sie die Wiederholung des Batchauftrags.
1. Wählen Sie **OK**.

## <a name="more-information"></a>Weitere Informationen

Nachfolgend sind einige Hinweise aufgeführt, die Sie bei der Verwendung der DOM-Funktion berücksichtigen sollten:

- Momentan berücksichtigt DOM nur Aufträge, die von den Handelskanälen erstellt werden. Aufträge werden als Aufträge angegeben, wenn die Option **Handelsauftrag** auf **Ja** festgelegt ist.
- Microsoft hat DOM nicht mit den erweiterten Funktionen für die Lagerortverwaltung getestet. Kunden und Partner müssen sollten daher mit Sorgfalt festlegen, ob DOM mit den erweiterten Funktionen und Prozessen für die Lagerortverwaltung kompatibel ist, die für sie relevant sind. Die erweiterte Lagerhaltung ermöglicht konfigurierbare Dimensionen, wie z. B. Bestandsstatus, die kein genaues Verständnis des verfügbaren Bestands liefern. DOM bietet eine erweiterbare Methode zum Festlegen des verfügbaren Bestands für Implementierungen, die erweiterte Lagerhaltung verwenden. Dies kann verwendet werden, um mit benutzerdefinierten Werten für den Bestandsstatus und anderen Dimensionen zu arbeiten.

    Die Erweiterbarkeit in DOM ist begrenzt, da die Optimierung im vorgefertigten MIP-Modell erfolgt, das die Optimierung und ihre Einschränkungen berücksichtigt. Mehrere erweiterbare Punkte sind bereits verfügbar, um die Bestands- und Nachbearbeitungsoptimierung festzulegen. DOM-Profile können je nach Verkaufsursprung und Liefermodus unterschiedlich sein. Der Ursprung des Kundenauftrags kann während der Auftragsaufnahme festgelegt werden, und basierend auf diesen Werten können verschiedene Optimierungsstrategien verwendet werden. DOM unterstützt auch die Erstellung benutzerdefinierter Chargenaufträge, die die DOM-Verarbeitungsaufgabe als Eingabe verwenden und ermöglichen, dass das Profil als Parameter übergeben wird. Daher kann eine Optimierung nach der anderen ausgeführt werden, um verschiedene Geschäftsszenarien zu unterstützen.

- DOM ist nur in der Cloudversion von Commerce verfügbar. Es wird nicht für lokale Bereitstellungen unterstützt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
