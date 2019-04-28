---
title: Einrichten der Angebotsverwaltung
description: In diesem Thema wird beschrieben, wie Angebote in Talent eingerichtet werden.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fa0e5d30c06db16e105631e492af022acfcfd66
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "857868"
---
# <a name="set-up-offer-management"></a>Einrichten der Angebotsverwaltung 

[!include [banner](includes/banner.md)]

Wenn ein Kandidat auf die Angebotsphase in Dynamics 365 for Talent: Attract verschoben wird, müssen Sie sicherstellen, dass die Angebote für den Kandidaten schnell nach Bedarf erstellt, genehmigt und dem Kandidaten gesendet werden können. Da die meisten Angebote standardmäßig sind, können Sie aus wiederverwendbaren Vorlagen erstellt werden. In Attract werden alle Angebote in ein Angebotspaket verschoben, das eine Zusammenstellung eines oder mehrerer Angebotsunterlagen ist. 

Dieses Thema führt alle Schritte auf, denen ein Attract-Administrator folgen würde, um verschiedene Angebotpaketvorlagen als Teil der Angebotsverwaltung einzurichten in Attract. Benutzer mit Nicht-Administrator-Rollen haben keinen Zugriff zu diesen Funktionen.

>[!NOTE]
> Angebotsverwaltungsfunktionen werden als Teil für das Einstellungsadd-on verfügbar.

## <a name="offer-data"></a>Angebotsdaten 

Angebotdaten sind die kleinste Einheit in der Angebotpaketvorlage. Ein typisches Angebot besteht aus Standardtext und aus einer Gruppe von Werten. Die Gruppen der Werte sind die einzelnen Bestandteile, die zwischen Angeboten ändern können. Während der Angeboterstellung ist der wichtigste Aspekt, auf den sich der Angebotersteller fokussieren kann, die Liste der Angebotdatenenplatzhaltern, die in einer Angebotpaketvorlage vorhanden sind. Um Angebotdaten einzurichten, gehen Sie folgendermaßen vor.

1.  Gehen Sie zu **Management anbieten**.

1.  Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Angebotdaten** fort.

    >[!NOTE]
    > Auf der Seite **Daten anbieten** werden die Abschnitte **Kandidatendetails** und **Stellendetails** angezeigt. Attract stellt einige Daten-Platzhalterstandards bereit.
    
    > Es gibt Abschnitte auf der Seite, um die verschiedenen Angebotsdatenenplatzhalter zusammen mit den logischen Gruppen zu organisieren. Diese Bereiche können bei der Verwaltung von Angebotdaten und beim Auffüllen von Daten während des Angebotserstellungsprozesses helfen.

1.  Zum Erstellen eines neuen Angebotsdatenabschnittes klicken Sie auf **Fügen Sie einen Abschnitt hinzu**, und geben Sie einen eindeutigen Namen für den Bereich ein.

1.  Um Angebotsdatenenplatzhalter jedem Bereich hinzuzufügen, klicken Sie auf **Fügen Sie Angebotsdaten hinzu** und geben Sie einen eindeutigen Namen für den Platzhalter ein.

1.  Wenn Sie den Namen eines Abschnitts bearbeiten, fahren Sie über den Abschnittsnamen und aktualisieren Sie den Namen.

1.  Um den Namen aller vorhandenen Angebotsdatenenplatzhalter zu bearbeiten, sollten Sie zunächst sicherstellen, dass der Platzhalter nicht bereits Teil einer Vorlage ist. Anschließend fahren Sie über den Namen der Angebotsdatenplatzhalter und aktualisieren Sie den Namen nach Bedarf.

1. Um den Namen aller vorhandenen Angebotsdatenenplatzhalter zu löschen, sollten Sie zunächst sicherstellen, dass der Platzhalter nicht bereits Teil einer anderen Vorlage ist. Anschließend fahren Sie mit dem Mauszeigers über den Platzhalter und wenn das Abfalleimersymbol erscheint, klicken Sie auf den Abfalleimer, um den Angebotsdatenenplatzhalter zu löschen.
    >[!NOTE]
    > Sie können sehen, wie viele Vorlagen ein Angebotsdatenenplatzhalter Teil vom Nummerindikator neben den Angebotsdaten ist. 

1. Wenn Sie einen Abschnitt löschen, fahren Sie über den Namen. Wenn keine der Angebotdatenenplatzhalter innerhalb des Bereichs in jeder Vorlage angezeigt werden, können Sie auf das Abfalleimersymbol klicken, um sie zu löschen. 
    >[!NOTE]
    > Mit dem Löschen des Abschnitts werden auch alle Angebotsdaten-Platzhalter im Bereich gelöscht.

Nachdem die Angebotdatenenplatzhalter eingerichtet wurden, können Sie diese zu einer beliebigen Dokumentvorlage verwenden. Angebotdatenenplatzhalter werden nicht auf eine bestimmte Vorlage beschränkt -- dieselbe Definition kann für alle Vorlagen verwendet werden.

## <a name="offer-data-rules"></a>Angebotdatenregeln

Die meisten Organisation haben Regeln dazu, wie Angebote erstellt werden müssen. Zum Beispiel möchte eine Organisation, dass das maximale Angebot des jährlichen Gehalts für einen bestimmten Standort und ein bestimmtes Dienstalters innerhalb eines bestimmten Bereichs liegt oder dass nur wenige bestimmte Werte für die Angebotsebene für den neuen Mitarbeiter möglich sind. Attract unterstützt derzeit all diese Datenregeln mithilfe einer CSV-Datei.

Um die Datenregeln für die CSV-Datei zu erstellen, gehen Sie folgendermaßen vor.

1.  Festlegen der Angebotdatenenplatzhalter für die Regelsammlung. Zum Beispiel **Jährliches Gehalt**.

1.  Definieren Sie die Angebotsdaten-Platzhalterwerte. Zum Beispiel **Arbeitsort** und **Ebene**.

1.  Geben Sie Spalten 1 und 2 als **Arbeitsort** und **Ebene** an.

1.  Um einen Bereichswert hochzuladen, machen Sie Spalten 3 und 4 für **Jährliches Gehalt**. Um einen bestimmten Wert anstelle eines Bereichs hochladen, lassen Sie nur Spalte 3**Jährliches Gehalt**.

1.  Füllen Sie die Microsoft Excel-Dateien auf Grundlage der notwendigen Rollen auf.

1.  Sicherstellen, dass jede Zeile eine eindeutige Kombination aller Werte ist, die zusammengestellt werden.

1.  Speichern Sie die Datei als CSV-Format.

Um die Datenregeln für die CSV-Datei zu erstellen, gehen Sie folgendermaßen vor.

1.  Gehen Sie zu **Management anbieten**.

1.  Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Angebotdatenregeln** fort.

1.  Klicken Sie auf **Neuer Datensatz**, um das Dialogfeld **Hochladen** anzuzeigen.

1.  Geben Sie einen eindeutigen Namen für den Regelsatz an und laden Sie dann die gespeicherte CSV-Datei hoch.

1.  Klicken Sie auf **Hinzufügen**.
    Die Regelsammlung wird im Hintergrund verarbeitet und Sie sind InApp gemeldete und per E-Mail, sobald diese ausfüllen.

    Sie werden benachrichtigt, wenn es Fehler beim Verarbeiten des Uploads gibt. Sie können das Fehlerprotokoll dann herunterladen, die Datei reparieren und erneut hochladen.

1.  Verwenden Sie die Optionsschaltfläche der Auslassungspunkte (**...**), wenn Sie den Regelsatz herunterladen und die Werte aktualisieren möchten. Nach der Aktualisierung können Sie die Datei erneut hochladen.

1.  Sie können einen vorhandenen Regelsatzupload löschen, wenn der Platzhalter, der definiert ist, von keiner anderen Dokumentvorlage verwendet wird.

>[!NOTE]
> - Jeder Platzhalter kann einen eindeutigen Satz Spalten haben, der davon abhängig ist. Wenn beispielsweise **Jährliches Gehalt** **Arbeitsort** **Ebene** abhängig ist, können Sie einen anderen Regelsatz nicht hochgeladen, **Jährliches Gehalt** aus einem anderen Satz Spalten abhängig ist.

> - Sie können Beispielangebotdatenregelsätze auf der Registerkarte **Beispiele** auf der Seite **Angebotdatenregeln** herunterladen.

> - Wenn ein Angebotersteller die Werte überschreibt, die von der Angebotsdatenregeln empfohlen werden, wird das Angebot als Nicht-Standard gekennzeichnet und die Genehmigung des Angebotsgenehmigungsworkflows wird vorgegeben.

## <a name="document-templates"></a>Dokumentvorlagen

Eine Angebotsunterlagevorlage kann Administratoren helfen, Angebotsschreiben zu erstellen. Die Angebotsunterlagevorlage ist eine Kombination des Texts, der ein Bestandteil des Angebots und ein  definierter Angebotdatenenplatzhalter ist. 

Um eine Angebotsunterlagevorlage zu erstellen, gehen Sie folgendermaßen vor.

1.  Gehen Sie zu **Management anbieten**.

1.  Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Vorlage** fort.

    Die Seite **Vorlagen** zeigt eine Liste der Dokumentvorlagen an, die bereits geladen wurden.

1.  **Klicken Sie auf "Neue Vorlage", um eine neue Vorlage für Freitextrechnungen zu erstellen.**

1.  Klicken Sie auf **Erstellen**, und geben Sie einen eindeutigen Namen für das Kriterium ein.

1.  Verwenden Sie den Rich-Text-Editor, um den Angebotsunterlageinhalt einzufügen oder zu bearbeiten. Sie können Tabellen, Bilder und Links unter Verwendung der Optionen einfügen, die oben im Text-Editors verfügbar sind.

1.  Sie können Angebotdatenenplatzhalter im Angebotvorlagendokument wie folgt eingefügt:

    - Drag & Drop vom rechten Bereich.

    - Hashtag der Angebotdatenenplatzhalter direkt in Position. Typ **\#** und dann starten Sie das Eingeben des Namens des Angebotsdatenenplatzhalters. Wählen Sie in der Dropdownliste eine Option aus. Klicken Sie oder drücken Sie **Eingeben**, um den Angebotdatenenplatzhalter einzufügen.

    >[!NOTE]
    > - Um einen Platzhalter der Angebotsunterlagevorlage zuzuordnen ohne den Wert dem Kandidaten zu zeigen, gehen Sie zu Ddatenenplatzhalter und klicken Sie auf das Symbol **Anheften**. Dies überträgt den einzufügenden dem Abschnitt **Fixierte Angebotdaten** der Angebotsunterlagevorlage. Zum Aufheben, führen Sie die selben Schritte aus aber klicken Sie **Markierung aufheben** in der Liste der Angebotsdatenenplatzhalter.

    > - Um die Liste aktiver Angebotdatenenplatzhalter anzuzeigen, wechseln Sie zur Registerkarte **Aktiv** im rechten Bereich.

    > - Wenn Sie einen Platzhalter einfügen, der durch eine Angebotdatenregelsatz gesteuert wird, können Sie diese Abhängigkeit dieses Angebotdatenenplatzhalters auf anderen Werten finden.

    > - Sie können den Inhalt von einer .doxc-Datei auf Ihren lokalen Rechner **Importieren** und nach Bedarf bearbeiten. Deshalb müssen Sie auch den gesamten Inhalt im Editor nicht eingeben.

1. Um die Angebotsunterlage in der Vorschau anzuzeigen, können Sie die Option **Vorschau** oben auf der Seite nutzen.

1. Wenn Sie steuern, ob ein Angebotersteller die Angebotsunterlageinhalte bearbeiten kann, können Sie die Option **Verwalten Sie die Berechtigung** oben der Seite nutzen. Wenn Sie möchten, dass der Angebotersteller nur Platzhalterwerte einfügen und keine Texte bearbeiten kann, legen Sie den Berechtigungswert auf **Nein** fest.

1. Klicken Sie auf **Speichern**, um den Fortschritt zu speichern. Die Vorlage wird in einem Entwurfstatus gespeichert.

1. Um das Dokument fertigzustellen und es als veröffentlicht zu markieren, klicken Sie auf **Fertig stellen**.

1. Sie können sehen, welche Dokumentvorlagen derzeit aktiv nd s usind im Entwurfmodus und archiviert wurden und nicht mehr in der Dokumentvorlagenbibliotheks-Landungserfahrung verwendet werden.

>[!NOTE]
> Sie können jede Angebotsunterlagenvorlage löschen, die nicht Teil einer vorhandenen Angebotpaketvorlage ist.


## <a name="offer-package-templates"></a>Angebotsvorlagenpaket

Angebotpakete sind die Angebotartefakte, die mit den Kandidaten geteilt werden und aus einer Kombination von einer oder mehrer Angebotsvorlagen besteht. Um eine Angebotsvorlage zu erstellen, gehen Sie folgendermaßen vor.

1.  Gehen Sie zu **Management anbieten**.

1.  Gehen Sie zu **Pakete** im linken Navigationsbereich.

    Eine Liste aktiver Paketvorlagen, die für Angebotersteller zur Nutzung verfügbar sind.

1.  Wenn Sie ein neues Angebotpaket erstellen, klicken Sie auf **Neues Paket**

1.  Geben Sie einen eindeutigen Namen ein und klicken Sie auf **Erstellen**.

1.  Klicken Sie auf **Vorlage hinzufügen**.

    >[!NOTE]
    > - Sie können eine vorhandenen Vorlage auswählen, um eine neue Vorlage zu erstellen oder eine bestehende verwenden.

    > - Wenn Sie sich entschieden haben, eine vorhandene Vorlage hinzuzufügen, müssen Sie prüfen, ob die Angebotsunterlagevorlage gespeichert, abgeschlossen oder als aktiv markiert wurde.
    
    > - Sie können beliebig viele Dokumentvorlagen auswählen. 
    
1.  Klicken Sie auf **Fertig**, um zur **Paketverwaltung** zurückzukehren.

    Sie können die Sequenz von Dokumenten konfigurieren und auch festlegen, ob die Angebotsunterlage für bestimmte Angeboterstellungen erforderlich ist. Der Angebotersteller hat die Option, Dokumente zu löschen, die als **Nicht erforderlich** markiert sind.

1. Um die Angebotpaketvorlage zu speichern, damit sie von anderen Angebotersteller verwendbar ist, klicken Sie auf **Speichern und Veröffentlichen**.

   Um Entwurf-Paketvorlagen anzuzeigen, navigieren Sie zur Registerkarte **Entwürfe**.  Wenn eine Änderung an der Angebotpaketvorlage vorgenommen wird, muss sie erneut gespeichert und veröffentlicht werden.

## <a name="configure-an-offer-process"></a>Konfigurieren eines Angebotsprozesses

Es gibt verschiedene Teile des Angeboterstellungsprozesses, der von einem Attract-Administrator konfiguriert werden kann.

- **Angebotgenehmigungen** - Wählen Sie, ob Angebotgenehmigungen erforderlich sind, bevor das Angebot an den Kandidaten gesendet werden kann. Als Administrator können Sie auch festlegen, ob alle Angebotgenehmigungen in einer Sequenzkennung  oder einem parallelen Genehmigungsworkflow geschehen. Sie können vorgeben, ob auch Angebotgenehmiger einen Kommentar zusammen mit der Angebotgenehmigung hinzufügen müssen. Angebotgenehmigungen sind für alle Angebote zwingend, die nicht Standard sind.

- **Angeboterfahrung des Kandidaten** - Als Administrator, können Sie auswählen, ob alle Angebote ein Ablaufdatum haben, und falls ja, wofür das Standardgegenkonto für das Ablaufdatum sein soll. Sie können auch konfigurieren, ob Kandidaten ein Angebot ablehnen können.

- **E-Unterschriften** - Als Administrator, können Sie die Methode auswählen, die auch Kandidaten verwenden können, um Angebote zu signieren.
    - Adobe Sign- alle Angebotpakete werden auf Adobe Sign übermittelt und unterzeichnet. Jeder Angebotersteller, der die Angebotanforderungen veröffentlicht, muss ein Adobe Sign-Konto haben, um sich mit Attract zu verbinden. Für Adobe Sign-Lizenzen und eine kostenlose Testversion siehe [Link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html)

    - DocuSign - alle Angebotpakete werden auf DocuSign übermittelt und unterzeichnet. Jeder Angebotersteller, der die Angebotanforderungen veröffentlicht, muss ein DocuSign-Konto haben, um sich mit Attract zu verbinden. 
    
    - ESign - Dies ist die Standardeinstellung, wo der Benutzer ein Angebot signieren kann, indem er Namen und Initialen eingibt.


Weitere Informationen zu den Angeboterstellungsprozessund  finden Sie unter [Erstellen, genehmigen und unterzeichnen von Angeboten ](./creating-offers.md).
