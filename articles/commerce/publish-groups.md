---
title: Arbeiten mit Veröffentlichungsgruppen
description: In diesem Thema wird die Funktion der Veröffentlichungsgruppen in Microsoft Dynamics 365 Commerce beschrieben.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 96e55683c46dc196ebac2d0e16f38835c8bfe7df
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915415"
---
# <a name="work-with-publish-groups"></a>Arbeiten mit Veröffentlichungsgruppen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird die Funktion der Veröffentlichungsgruppen in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

E-Commerce-Websites werden das ganze Jahr über ständig mit neuen Inhalten aktualisiert. Aktualisierungen werden häufig stapelweise zu geschäftigen E-Commerce-Ereignissen wie Feiertagen, saisonalen Marketingkampagnen oder Werbemaßnahmen veröffentlicht. Diese Aktualisierungen erfordern häufig, dass Gruppen von Website-Inhalten (z. B. Seiten, Bilder, Fragmente und Vorlagen) gleichzeitig in einer einzigen Aktion bereitgestellt, validiert und veröffentlicht werden.

Die Möglichkeit, Elemente in logischen Gruppen zu gruppieren, die Elemente zusammen veröffentlichen, wobei jede Gruppe ihren eigenen Lebenszyklus hat, bietet den Site-Autoren viele Vorteile. In Commerce werden diese logischen Gruppen als Veröffentlichungsgruppen bezeichnet. Sie ermöglichen es Site-Autoren, Aktualisierungssätze als ihre eigenen konfigurierbaren, testbaren und publizierbaren Entitäten zu verfolgen.

Autoren können eine Vorschau der Aktualisierungen in einer bereitgestellten Veröffentlichungsgruppe anzeigen, ohne dass dies Auswirkungen auf die Live-Site oder andere eigenständige Veröffentlichungsgruppen hat. Autoren können dann die Veröffentlichungsaktion so planen, dass alle Elemente in der Veröffentlichungsgruppe gleichzeitig auf der Live-Site veröffentlicht werden. Die Möglichkeit, Aktualisierungen für Veröffentlichungen zu gruppieren, in der Vorschau anzuzeigen und zu planen, ist für viele Unternehmen auf Unternehmensebene wichtig, die einen erheblichen Jahresumsatz mit ereignisbasierten Meilensteinen für Standortaktualisierungen erzielen.

Unternehmen können durch langsame oder ungültige Inhaltsbereitstellungen Kosten verursachen, die nicht reibungslos verlaufen. Veröffentlichungsgruppen gewährleisten, dass Starts rechtzeitig organisiert, validiert und veröffentlicht werden. Unabhängig davon, ob es sich um große oder kleine Veröffentlichungsgruppen handelt, bieten Veröffentlichungsgruppen ein nützliches Toolset, mit dem Autoren die laufenden Aufgaben zur Aktualisierung von Websites organisieren und vereinfachen können.

## <a name="when-to-use-publish-groups"></a>Wann werden Veröffentlichungsgruppen verwendet?

Sie können Veröffentlichungsgruppen immer dann verwenden, wenn Sie mehrere Dokumente gleichzeitig bereitstellen und veröffentlichen müssen. Wenn Ihre Website beispielsweise den Inhalt jede Saison aktualisiert, können Sie Veröffentlichungsgruppen für diese saisonalen Marketing-Bewegungen erstellen. Ihre Veröffentlichungsgruppe „Autumn Seasonal Update“ enthält möglicherweise neue saisonale Bilder, Fragmente mit saisonalen Marketingnachrichten, Seiten mit saisonalen Produktkollektionen oder andere saisonale Website-Updates.

Ein Vorteil von Veröffentlichungsgruppen besteht darin, dass Sie mehrere Aktualisierungen gleichzeitig durchführen können. Kurz nach dem Update für die Veröffentlichungsgruppe „Autumn Seasonal Update“ wird möglicherweise ein Inhaltsupdate für ein bestimmtes Feiertagswochenende veröffentlicht. In diesem Fall können Sie Inhalte für die Veröffentlichungsgruppe „Autumn Seasonal Update“ bereitstellen, während Sie Inhalte für eine nachfolgende Veröffentlichungsgruppe „Autumn Holiday Update“ bereitstellen. Jede Veröffentlichungsgruppe enthält einen eigenen Satz von Seiten, Bildern, Fragmenten, Vorlagen usw. Sie können diese beiden Veröffentlichungsgruppen unabhängig voneinander, jedoch auf einer gleichzeitigen Zeitachse bereitstellen, in der Vorschau anzeigen und überprüfen. Jede Veröffentlichungsgruppe kann dann so geplant werden, dass sie an bestimmten Daten und zu bestimmten Zeiten auf Ihrer Website live geschaltet wird.

## <a name="turn-on-the-publish-groups-feature"></a>Aktivieren Sie die Funktion zum Veröffentlichen von Gruppen

Die Funktion zum Veröffentlichen von Gruppen ist optional und muss für Ihre Site aktiviert werden.

Gehen Sie folgendermaßen vor, um die Funktion zum Veröffentlichen von Gruppen für Ihre Website in den Commerce-Authoring-Tools zu aktivieren.

1. Wählen Sie im linken Navigationsbereich **Site-Einstellungen** aus, um den Bereich zu erweitern.
1. Wählen Sie unter **Site-Einstellungen** die Option **Funktionen** aus.
1. Legen Sie die Option **Veröffentlichungsgruppen** auf **Ein** fest.

## <a name="create-a-publish-group"></a>Eine Veröffentlichungsgruppe erstellen

Gehen Sie folgendermaßen vor, um eine Veröffentlichungsgruppe für Ihre Website in den Commerce-Authoring-Tools zu erstellen.

1. Wählen Sie im linken Navigationsbereich **Veröffentlichungsgruppen** aus.
1. Wählen Sie in der oberen Befehlsleiste **Neu** aus.
1. Geben Sie im Dialogfeld **Veröffentlichungsgruppe erstellen** unter **Name der Veröffentlichungsgruppe** einen beschreibenden Namen ein. Wählen Sie dann **OK** aus.

## <a name="set-the-publish-group-authoring-context"></a>Den Authoring-Kontext für Veröffentlichungsgruppen festlegen

In Commerce ist der Standard-Authoring-Kontext der Live-Site-Kontext. Der Live-Site-Authoring-Kontext ist die Standardansicht, in der Sie Änderungen direkt an Ihrer Website anzeigen und vornehmen können, ohne eine Veröffentlichungsgruppe zu verwenden. Es handelt sich um die neuesten direkten Aktualisierungen der veröffentlichten Version Ihrer Website. Wenn die Kontextsteuerung unter **Veröffentlichungsgruppen** im linken Navigationsbereich den Namen **Live-Site** anzeigt, arbeiten Sie im Live-Site-Authoring-Kontext. **Live-Site** ist der Standardname der Kontextsteuerung. Andernfalls zeigt das Kontextsteuerelement den Namen einer Veröffentlichungsgruppe an.

Um in einer Veröffentlichungsgruppe zu arbeiten, müssen Sie dazu in den Veröffentlichungsgruppen-Erstellungskontext wechseln. Führen Sie einen dieser Schritte aus, um den Veröffentlichungsgruppenkontext festzulegen.

- Wählen Sie im linken Navigationsbereich direkt unter **Veröffentlichungsgruppen** die Kontextsteuerung aus, und dann den Namen der Veröffentlichungsgruppe in der Liste der angezeigten Optionen. Die Kontextsteuerung wird umbenannt und zeigt den Namen der Veröffentlichungsgruppe an.
- Wählen Sie im linken Navigationsbereich **Veröffentlichungsgruppen**und dann unter **Veröffentlichungsgruppen** den Namen der Veröffentlichungsgruppe aus. Die Kontextsteuerung wird umbenannt und zeigt den Namen der Veröffentlichungsgruppe an.

Nachdem Sie den Autorenkontext für Veröffentlichungsgruppen festgelegt haben, arbeiten Sie in diesem Veröffentlichungsgruppenkontext, wenn Sie eine Vorschau des Websiteinhalts anzeigen und ihn bearbeiten.

Um zum Standardkontext für die Erstellung von Live-Sites zurückzukehren, wählen Sie die Kontextsteuerung und anschließend **Live-Site** aus.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Hinzufügen von Seiten oder anderen Elementen zu einer Veröffentlichungsgruppe

Nachdem Sie einen Authoring-Kontext für Veröffentlichungsgruppen ausgewählt haben und das Kontextsteuerelement im linken Navigationsbereich den Namen anzeigt, können Sie Inhalte wie im Standardkontext für Live-Sites erstellen. Sie können auch vorhandene Seiten oder andere Elemente aus anderen Veröffentlichungsgruppen oder aus dem Live-Site-Kontext hinzufügen.

Gehen Sie folgendermaßen vor, um vorhandene Seiten in eine Veröffentlichungsgruppe zu kopieren.

1. Wählen Sie den Authoring-Kontext aus, aus dem kopiert werden soll, und wählen Sie dann im linken Navigationsbereich **Seiten** aus.
1. Wählen Sie die Seite aus, die einer Veröffentlichungsgruppe hinzugefügt werden soll.
1. Wählen Sie in der Befehlsleiste **In Veröffentlichungsgruppe kopieren** aus.
1. Wählen Sie im Dialogfeld **Veröffentlichungsgruppe auswählen** die Veröffentlichungsgruppe aus, der die Seite hinzugefügt werden soll, und wählen Sie dann **OK** aus.

Mit denselben grundlegenden Schritten können Sie benutzerdefinierte Produktseiten, URLs, Vorlagen, Layouts, Fragmente und Medienbibliotheksassets erstellen oder einer Veröffentlichungsgruppe vorhandene Elemente dieses Typs hinzufügen.

## <a name="validate-a-publish-group"></a>Eine Veröffentlichungsgruppe überprüfen

Um sicherzustellen, dass alle Abhängigkeiten im Inhalt der Veröffentlichungsgruppe erfüllt sind und alle Überprüfungen bestanden wurden, können Sie eine Überprüfung durchführen, um alle Probleme zu identifizieren, die behoben werden müssen, bevor Sie eine Veröffentlichungsaktion planen.

Gehen Sie folgendermaßen vor, um Ihre Veröffentlichungsgruppe zu überprüfen, bevor Sie es planen.

1. Wählen Sie im linken Navigationsbereich **Veröffentlichungsgruppen** aus.
1. Wählen Sie die zu überprüfende Veröffentlichungsgruppe aus.
1. Wählen Sie in der Befehlsleiste **Überprüfen** aus.

Die Validierung wird für alle Inhalte in der Veröffentlichungsgruppe ausgeführt. Alle Probleme, die eine erfolgreiche Veröffentlichungsaktion verhindern, werden in einem Benachrichtigungsfeld oben rechts angezeigt.

> [!NOTE]
> Die Validierung wird immer automatisch ausgeführt, wenn eine Veröffentlichungsgruppe geplant ist. Die Schaltfläche **Überprüfen** in der Befehlsleiste ist jedoch nützlich, um Probleme zu identifizieren, die Sie beheben müssen, bevor Sie versuchen, eine Veröffentlichungsgruppe für den Live-Betrieb zu planen.

## <a name="schedule-a-publish-group-to-go-live"></a>Planen Sie eine Veröffentlichungsgruppe für die Live-Schaltung

Gehen Sie folgendermaßen vor, um eine Veröffentlichungsgruppe für die Veröffentlichung auf Ihrer Site zu planen.

1. Wählen Sie im linken Navigationsbereich **Veröffentlichungsgruppen** aus.
1. Wählen Sie unter **Veröffentlichungsgruppen** die zu planende Veröffentlichungsgruppe aus.
1. Wählen Sie in der Befehlsleiste **Zeitplan bearbeiten** aus. Das Dialogfeld **Zeitplan bearbeiten** wird angezeigt.
1. Wählen Sie das Datum und die Uhrzeit aus, zu der Ihre Veröffentlichungsgruppe live geschaltet werden soll, und wählen Sie dann **OK** aus.

Befolgen Sie die gleichen Schritte, um die Planung einer Veröffentlichungsgruppe aufzuheben, wählen Sie jedoch **Veröffentlichungsgruppe aufheben** im Dialogfeld **Zeitplan bearbeiten** aus.

> [!NOTE]
> Bei sehr großen Veröffentlichungsgruppen kann es bis zu ein oder zwei Minuten dauern, bis sie zu ihrem geplanten Zeitpunkt veröffentlicht werden. Beachten Sie, dass eine Veröffentlichungsaktion nicht sofort ausgeführt wird und dass kleinere Veröffentlichungsgruppen schneller veröffentlicht werden.

## <a name="publish-groups-faq"></a>Häufig gestellte Fragen zu Veröffentlichungsgruppen

**Wie viele Elemente können zu einer Veröffentlichungsgruppe gehören?**

Derzeit gibt es ein Limit von 2.000 Elementen pro Veröffentlichungsgruppe. Beachten Sie, dass es bei sehr großen Veröffentlichungsgruppen einige Minuten dauern kann, bis sie zu ihrem geplanten Zeitpunkt veröffentlicht werden.

**Veröffentlichen Sie Gruppen wie Code-„Zweige“ in der Terminologie der Softwareentwicklung?**

Ja und nein. Veröffentlichungsgruppen können als verzweigte Versionen Ihrer Site betrachtet werden. Auf diese Weise verhalten sie sich wie Zweige. Es gibt jedoch kein Konzept für eine Zusammenführung auf der Ebene einzelner Elemente. Das zuletzt veröffentlichte Element überschreibt nur das, was zuvor vorhanden war, und die letzte Veröffentlichungsaktion ersetzt immer vorherige Veröffentlichungsaktionen.

**Kann ich festlegen, dass zwei Veröffentlichungsgruppen gleichzeitig live geschaltet werden?**

Nr. Aus Performance- und Konfliktgründen werden Sie vom System gezwungen, geplante Veröffentlichungsgruppen im Abstand von mindestens fünf Minuten zu verschieben.

**Kann ich Veröffentlichungsgruppen verwenden, um Mehrkanal-Backoffice-Elemente wie Rabatte und Produktaktualisierungen zu planen?**

Derzeit unterstützt die Funktion „Gruppen veröffentlichen“ nur Website-Inhalte. Microsoft ist sich jedoch bewusst, dass die Integration in Back-Office-Merchandising-Szenarien für die Koordination und Automatisierung von Starts von Mehrkanal-Kampagnen von Nutzen sein kann.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Möglichkeiten zum Hinzufügen von Inhalten](add-manage-content.md)

[Seitenmodellglossar](page-elements-overview.md)

[Dokumentstatus und -Lebenszyklus](document-states-overview.md)

[Arbeiten mit Modulen](work-with-modules.md)

[Arbeiten mit Fragmenten](work-with-fragments.md)

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Anpassen der Sitenavigation](customize-site-navigation.md)
