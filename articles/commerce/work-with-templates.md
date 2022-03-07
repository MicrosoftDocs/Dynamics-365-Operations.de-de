---
title: Arbeiten mit Vorlagen
description: In diesem Thema wird beschrieben, wie Sie in Microsoft Dynamics 365 Commerce mit Vorlagen arbeiten.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ab6ccfac96249b39cb007d9a9fce10475f0c7149
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090793"
---
# <a name="work-with-templates"></a>Arbeiten mit Vorlagen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie in Microsoft Dynamics 365 Commerce mit Vorlagen arbeiten.

Wie in [Übersicht über Vorlagen und Layouts](templates-layouts-overview.md) erläutert wurde, legen die Vorlagen den Satz an Optionen fest, der für nachgeschaltete Autoren verfügbar ist. Vorlagen sind für das Web-Authoring-Team eines Unternehmens aus mehreren Gründen nützlich. Gut strukturierte Vorlagen können bei allen folgenden Zielen hilfreich sein:

- Vereinfachen der Autorenerfahrung für alltägliche Inhaltseditorrollen

    - Filtern von Moduloptionen, sodass nur relevante Module für einen bestimmten Seitenabschnitt angezeigt werden (Beispielsweise kann ein Marketingabschnitt einer Vorlage so konfiguriert werden, dass irrelevante Module herausgefiltert werden, die in diesem Kontext niemals verwendet werden sollten, und die, sollten sie angezeigt werden, die Inhaltserstellungsaufgaben nur erschweren.)
    - Konfigurieren Sie die Standardmoduleinstellung, um die Authoring-Effizienz zu verbessern.
    - Definieren Sie Standardseitenfragmente, um die Authoring-Effizienz zu verbessern. (Beispielsweise werden Kopf- und Fußzeilenfragmente in einer Vorlage automatisch auf jeder nachgelagerten Seite angezeigt.)

- Halten Sie Unternehmensstandorte auf dem Laufenden, indem Sie einen genehmigten Satz von Modulanordnungs- und Konfigurationsoptionen definieren.

    > [!TIP] 
    > Erfolgreiche E-Commerce-Websites bieten Ihren Debitor ein vertrautes, wiederholbares und markengerechtes UX-Designmuster. Mithilfe von Vorlagen können Sie die Konsistenz auf Ihrer Site steuern.

- Verbessern Sie die SEO-Ergebnisse (Search Engine Optimization), indem Sie wiederholbare und programmgesteuert definierte Seitendefinitionen und Metadaten sicherstellen.

> [!NOTE]
> Vorlagen dienen zwar zur Steuerung der Konsistenz auf einer Site, können jedoch theoretisch so konfiguriert werden, dass keine Konsistenz erzwungen wird. Marken- und Site-Administratoren können für die Seiten ihrer Site einen beliebigen Variabilitätsgrad festlegen. Beispielsweise kann eine Vorlage vollständig offen gelassen werden, sodass Inhaltsautoren jedes von ihnen ausgewählte Seitendesign erstellen können. In diesem Fall kommt keiner der Vorteile aus der vorhergehenden Liste zum Tragen.

## <a name="modify-a-template"></a>Eine Vorlage ändern

Vorlagen werden durch Verwendung des Vorlagen-Editors geändert.

Um den Vorlageneditor in Commerce Site Builder zu öffnen, führen Sie einen der folgenden Schritte aus:

- Wählen Sie im Navigationsbereich Ihrer Site **Vorlagen** und dann die zu ändernde Vorlage aus.
- Wählen Sie im Seiteneditor für eine vorhandene Seite links im Gliederungsbaum den obersten Knoten aus. Wählen Sie dann rechts im Eigenschaftenbereich **Vorlage bearbeiten** aus.

Die Gliederungsstrukturansicht links zeigt die Moduloptionen und -strukturen an, die untergeordneten Layouts und Seiten zur Verfügung stehen. Wenn Sie ein Modul in der Gliederungsstruktur auswählen, können Sie die Vorlageneigenschaften für das ausgewählte Modul im Eigenschaftsfenster rechts anzeigen. Einige dieser Eigenschaften gelten nur für die Bearbeitung von Vorlagen. Diese Eigenschaften werden in der folgenden Tabelle näher erläutert.

| Eigenschaftenname | Beschreibung |
|---|---|
| Min. Vorkommen | Diese Eigenschaft definiert die minimale Anzahl von Vorkommen für das ausgewählte Modul. Wenn der Wert beispielsweise auf **1** gesetzt ist, ist das Modul für nachgelagerte Autoren erforderlich. Wird der Wert hingegen auf **0** (null) festgelegt, ist das Modul optional. |
| Max. Vorkommen | Diese Eigenschaft definiert die maximale Anzahl von Vorkommen für das ausgewählte Modul. Wenn der Wert beispielsweise auf **1** festgelegt ist, kann das Modul nur einmal hinzugefügt werden. |
| Min. Module (Container) | Für Module, die andere Module enthalten (z. B. für *Containermodule*), definiert diese Eigenschaft die Mindestanzahl an Gesamtmodulen, die als untergeordnete Module hinzugefügt werden sollten. Für ein Karussellmodul kann der Wert beispielsweise auf eine Zahl festgelegt werden, die größer als 1 ist. |
| Max. Module (Container) | Für Containermodule definiert diese Eigenschaft die maximale Anzahl von Gesamtmodulen, die als untergeordnete Module hinzugefügt werden sollen. Für ein Karussellmodul kann der Wert beispielsweise auf eine Zahl festgelegt werden, die kleiner als 10 ist. |
| Gesperrt | Das boolesche Steuerelement **Gesperrt** wird neben allen Kernmoduleigenschaften angezeigt. Hiermit kann der Vorlagenautor eine Moduleinstellung in der Vorlage sperren. Eine gesperrte Moduleinstellung kann nicht von untergeordneten Layouts oder Seiten überschrieben werden. Sie wird zu einem zentralen bearbeitbaren Eigenschaftswert für alle Layouts und Seiten, die die Vorlage verwenden. |

## <a name="create-a-new-template"></a>Neue Vorlage erstellen

Um eine neue Vorlage in Site Builder zu erstellen, führen Sie diese Schritte aus.

1. Wählen Sie im Navigationsbereich Ihrer Site **Vorlagen** aus, um die Vorlageninspektor-Ansicht zu öffnen.
1. Wählen Sie **Neue Vorlage** aus.
1. Geben Sie im Dialogfeld Vorlagenerstellung einen Namen und eine Beschreibung für die Vorlage ein. Die von Ihnen eingegebenen Werte werden den Autoren angezeigt, wenn sie neue Seiten erstellen. Geben Sie daher Metadaten ein, die für Seitenautoren hilfreich sind. Geben Sie beispielsweise **Diese Vorlage zum Erstellen allgemeiner Marketingseiten verwenden** als Beschreibung ein. Diese Metadaten können später geändert werden.
1. Wählen Sie **OK** aus, um die neue Vorlage zu erstellen und den Vorlagen-Editor zu öffnen. Der Vorlagen-Editor zeigt links einen Gliederungsbaum und rechts einen Eigenschaftsbereich.
1. Erweitern Sie in der Gliederungsstruktur die Knoten und wählen Sie den Slot **HTML-Kopf** aus.
1. Wenn sich in diesem Slot noch keine Module befinden, wählen Sie die Ellipsen-Schaltfläche (**...**) und dann **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** die Option **Standardseitenzusammenfassung** und dann **OK** aus.
1. Wählen Sie in der Gliederungsstruktur das neue Modul aus, und geben Sie im Eigenschaftenbereich die Standardeinstellungen ein, die automatisch für alle untergeordneten Seiten der Vorlage konfiguriert werden sollen. Wenn Sie keine Standardeinstellungen möchten, lassen Sie die Werte leer.
1. Wählen Sie in der Gliederungsstruktur den Slot **Text**, die Ellipsen-Schaltfläche und dann **Modul hinzufügen** aus.
1. Wählen Sie ein Seitencontainermodul (möglicherweise gibt es nur eine Option) und dann **OK** aus.

Unter dem neuen Seitencontainermodul sehen Sie einen neuen Satz an Slots (**Kopf**, **Haupt** usw.). Hier können Sie die Moduloptionen hinzufügen und konfigurieren, die Autoren beim Erstellen von Seiten aus dieser Vorlage zur Verfügung stehen. Wenn Sie einem Slot keine Module hinzufügen, werden standardmäßig alle verfügbaren Modultypen für diesen Slot unterstützt.

Die Vorlage ist jetzt technisch gültig und kann gespeichert, eingecheckt und zum Erstellen neuer Seiten verwendet werden. In den nächsten drei Abschnitten werden jedoch einige andere Standardeinstellungen beschrieben, die Sie möglicherweise zuerst konfigurieren möchten.

## <a name="add-a-header-and-a-footer"></a>Eine Kopf- und Fußzeile hinzufügen

Wenn Ihre Website bereits über ein Kopfzeilenfragment verfügt, folgen Sie diesen Schritten im Site Builder, um eine Kopf- und eine Fußzeile zu einer Vorlage hinzuzufügen.

1. Erweitern Sie in der Gliederungsstruktur den Slot **Text** und dessen untergeordnetes Seitenmodul.
1. Wählen Sie den Slot **Kopf** aus.
1. Wählen Sie die Ellipsen-Schaltfläche für den Slot **Kopf** und dann **Fragment hinzufügen** aus.
1. Suchen Sie nach dem Kopffragment Ihrer Site, wählen Sie es aus, und klicken Sie dann auf **OK**.

Alle Seiten, die die Vorlage verwenden, erben nun automatisch dieses Kopffragment.

Wenn Ihre Site noch kein Kopf-Fragment enthält, lesen Sie [Fragment erstellen](work-with-fragments.md#create-a-fragment), um Informationen zum Erstellen zu erhalten. Schließen Sie dann die vorherige Prozedur ab.

## <a name="change-the-template-theme"></a>Das Vorlagendesign ändern

Um das Standarddesign für alle Seiten festzulegen, die eine Vorlage verwenden, folgen Sie diesen Schritten im Site Builder.

1. Erweitern Sie in der Seitengliederungsstruktur im Feld links den **Text**-Slot.
1. Wählen Sie im **Text**-Slot das Seitencontainermodul aus (z. B. **Standardseite**).
1. Wählen Sie im Eigenschaftenbereich rechts im Feld **Design** ein Design aus.

Standardmäßig verwenden alle neuen Seiten nun das ausgewählte Design. Um die Seiten am Überschreiben dieser Einstellung auf Layout- oder Seitenebene zu hindern, legen Sie die boolesche Steuerung **Gesperrt** auf **True** fest.

## <a name="add-a-script-to-a-template"></a>Einer Vorlage ein Skript hinzufügen

Sie können HTML-**&lt;Skript&gt;**-Elemente hinzufügen, die JavaScript in Ihrer Vorlage enthalten. Auf diese Weise können Sie Standardskriptverhalten im HTML-Kopf sowie in den Abschnitten für Textanfang und -ende Ihrer Seiten bereitstellen.

Um ein Skript zu einer Vorlage in Site Builder hinzuzufügen, gehen Sie folgendermaßen vor.

1. Wählen Sie in der Gliederungsstruktur links den Slot aus, dem Sie das **&lt;Skript&gt;**-Element (z. B. den HTML-Kopf, den Textanfang oder das Textende) hinzufügen möchten.
1. Wählen Sie die Ellipsen-Schaltfläche für den Slot und dann **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** ein Skriptmodul aus (z. B. **Externes Skript** oder **Inlineskript**).
1. Klicken Sie im Eigenschaftsfenster auf der rechten Seite auf die entsprechende Skripteigenschaftssteuerung (z. B. **Inlineskript** oder **Skript-Tags**), geben Sie Ihr Skript ein.
1. Geben Sie im Eigenschaftenbereich weitere optionale Einstellungen ein, die Sie konfigurieren möchten.

> [!TIP]
> Wenn Sie eines Ihrer Skriptmodule für andere Vorlagen wiederverwenden möchten, können Sie diese in Fragmente konvertieren. Auf diese Weise können Sie den Erstellungsprozess effizienter gestalten und den Aktualisierungsprozess zentralisieren. Informationen zum Konvertieren eines Skriptmoduls in ein Fragment finden Sie unter [Eine vorhandene Modulkonfiguration als Fragment speichern](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Speichern, Einchecken, Anzeigen einer Vorschau und Veröffentlichen einer Vorlage

Gehen Sie wie folgt vor, um eine Vorlage im Site Builder zu speichern und einzuchecken.

1. Wählen Sie **Speichern** oben im Vorlageneditor aus. Gespeicherte Änderungen wirken sich erst beim Einchecken auf nachfolgende Seiten aus.
1. Wählen Sie **Beenden Sie die Bearbeitung**. Ihre Änderungen sind jetzt für nachfolgende Workflows erkennbar.

Um eine Vorschau Ihrer Änderungen anzuzeigen, öffnen Sie entweder eine vorhandene Seite, die die Vorlage verwendet, oder erstellen Sie eine neue Seite aus der Vorlage.

Führen Sie einen der folgenden Schritte aus, um die Vorlage auf Ihrer Live-Site zu veröffentlichen, nachdem Sie eine Vorschau der Änderungen an Ihre Vorlage angezeigt haben:

* Navigieren Sie zu **Vorlagen**, wählen Sie die Vorlage und dann **Veröffentlichen** aus.
* Wählen Sie den Layoutnamen aus, um den Layout-Editor zu öffnen, und wählen Sie anschließend **Veröffentlichen** aus.
* Veröffentlichen Sie eine Seite, die auf die unveröffentlichte Vorlage verweist. Die Vorlage wird automatisch veröffentlicht.

> [!WARNING]
> Wenn eine Vorlage oder ein anderes Element des Content Management Systems (CMS) veröffentlicht wird, kann sie im Internet gefunden werden. Veröffentlichen Sie Dokumente oder Assets erst, wenn Sie diese der Öffentlichkeit vorstellen möchten. Dokumentversionen, die gespeichert und eingecheckt, aber noch nicht veröffentlicht wurden, können nur von authentifizierten Systembenutzern erkannt werden.

## <a name="rename-a-template"></a>Eine Vorlage umbenennen

Führen Sie diese Schritte aus, um eine vorhandene Vorlage im Site Builder umzubenennen.

1. Wählen Sie im linken Navigationsbereich **Vorlagen**.
1. Wählen Sie den Vorlagennamen der Vorlage, die Sie umbenennen möchten.
1. Wählen Sie **Bearbeiten**, um mit der Bearbeitung der Vorlage zu beginnen. Beachten Sie, dass Sie eine Vorlage nicht bearbeiten können, wenn eine andere Person die Vorlage bereits bearbeitet.
1. Wählen Sie im Bereich Eigenschaften der Vorlage das Stiftsymbol neben dem Namen der Vorlage.
1. Bearbeiten Sie den Vorlagennamen nach Bedarf.
1. Aktivieren Sie das Kontrollkästchen, um die Namensänderung zu bestätigen.
1. Wählen Sie **Beenden Sie die Bearbeitung**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Arbeiten mit Voreinstellungslayouts](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
