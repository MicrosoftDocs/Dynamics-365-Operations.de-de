---
title: Festlegen allgemeiner Werte für die Verwaltung für technische Änderung
description: Dieses Thema beschreibt, wie Sie allgemeine Werte festlegen, die für Parameter in verschiedenen Teilen der Verwaltung für technische Änderung verwendet werden.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b46bc10f8b75a58b8baefd88aa6a0b79c59d6544
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005401"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Festlegen allgemeiner Werte für die Verwaltung für technische Änderung

[!include [banner](../includes/banner.md)]

Wenn Sie die Verwaltung für technische Änderung festlegen, müssen Sie mehrere Sammlungen von Werten einrichten, die zum Ausfüllen von Dropdown-Listen in anderen Teilen der Benutzeroberfläche (UI) verwendet werden. Sie sollten diese Werte entsprechend den Produkttypen, die Sie herstellen, und Ihren spezifischen Geschäftsanforderungen festlegen.

## <a name="engineering-change-categories"></a>Kategorien der technischen Änderungen

Sie verwenden Verwaltung für technische Änderungs-Kategorien, um Ihre Entwicklungsänderungsaufträge zu organisieren, sodass sie einfacher zu verwalten und zu überprüfen sind. Es kann z. B. sinnvoll sein, einen Workflow festzulegen, bei dem je nach Kategorie eine bestimmte Abteilung die vorgeschlagenen Änderungen überprüfen muss. Daher enthält der Änderungsauftrag ein **Kategorie**-Feld.

Um die Sammlung von Entwicklungsänderungs-Kategorien einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichtung \> Verwaltung für technische Änderung \> Entwicklungsänderungs-Kategorien**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.

## <a name="engineering-change-priorities"></a>Prioritäten der technischen Änderungen

Sie verwenden Änderungsprioritäten, um die Wichtigkeit oder Dringlichkeit eines Änderungsauftrags anzugeben. Sie können Ihnen helfen, die Wichtigkeit eines Änderungsauftrags im Auge zu behalten, sodass Sie leicht erkennen können, welche Aufträge zuerst und wie schnell bearbeitet werden sollten.

Um die Sammlung von Entwicklungsänderungsprioritäten einzurichten, die in Ihrem Unternehmen verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Entwicklungsänderungsprioritäten**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.

## <a name="engineering-change-reasons"></a>Gründe für technische Änderung

Änderungsgründe geben die Ursache oder Art der Änderung im Änderungsauftrag an.

Um die Sammlung von Entwicklungsänderungsgründen einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Entwicklungsänderungsgründe**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.

## <a name="material-disposal-codes"></a>Materialdispositionscodes

Sie verwenden Materialentsorgungscodes, um Materialien zu kategorisieren, die in Ihren fertigen Waren verwendet werden, oder Komponenten, die auf eine bestimmte Art und Weise entsorgt werden müssen oder eine bestimmte Behandlung erfordern, bevor sie dem normalen Müll hinzugefügt werden können. Wenn Sie ein relevantes Produkt zu einem Änderungsauftrag hinzufügen, können Sie einen Entsorgungscode als Teil der Änderungsdetails zuweisen.

Um die Sammlung von Materialentsorgungscodes einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichtung \> Verwaltung für technische Änderung \> Materialentsorgungscodes**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.

## <a name="received-customer-approval"></a>Empfangene Debitorengenehmigung

Wenn Sie Produkte für einen bestimmten Kunden entwerfen, müssen der Entwurf und die Spezifikationen oft validiert werden, bevor das Produkt als fertig festgelegt werden kann. Im Feld **Erhaltene Kundenfreigabe** können Sie angeben, wie weit das Produkt im Prozess der Kundenfreigabe ist und/oder ob die Freigabe erhalten wurde.

Um die Sammlung der Werte für erhaltene Kundenfreigaben einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Erhaltene Kundenfreigabe**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Technische Änderungen - Umwelt- und Sicherheitsvorschriften

Wenn bei der Herstellung eines Produkts standardmäßige Umwelt- und Sicherheitsvorschriften oder firmenspezifische Vorschriften oder Verfahren berücksichtigt werden müssen, können Sie die Umwelt- und Sicherheitscodes verwenden, um diese zu definieren. Im Änderungsauftrag können Sie angeben, welche Codes für die Herstellung eines Produkts gelten, während Sie die Details des betroffenen Produkts bearbeiten.

Um die Sammlung von Zustands- und Sicherheitswerten einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Entwicklungsänderung - Umwelt- und Sicherheitscodes**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.

## <a name="engineering-change-severities"></a>Schweregrade der technischen Änderungen

Sie verwenden Änderungsschweregrade, um den Grad der Auswirkungen anzugeben, der für die Produkte in einem Änderungsauftrag gilt.

Um die Sammlung der Schweregrade für technische Änderungen einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderungen \> Einrichten \> Verwaltung für technische Änderungen \> Schweregrade für technische Änderungen**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.

Sie können Regeln festlegen, die für jeden von Ihnen erstellten Schweregrad gelten. Weitere Informationen darüber, wie Sie diese Regeln zuweisen, finden Sie im nächsten Abschnitt.

## <a name="engineering-change-severity-rule-sets"></a>Schweregradregelsatz für technische Änderung

Mit den Regeln für den Schweregrad von technischen Änderungen legen Sie eine Gruppe von Regeln fest, mit denen Sie den Schweregrad des Änderungsauftrags automatisch berechnen können, basierend auf der Art der Änderungen in den betroffenen Produkten. Um die Schweregrad-Regeln zu verwenden, öffnen Sie die Seite **Parameter für die Verwaltung für technische Änderungen** und legen das Feld **Schweregrad-Regel** auf *Berechnen* oder *Automatisch berechnen* fest.

Wenn das System den Schweregrad bewertet, verarbeitet es die Regeln in der Reihenfolge, in der sie auf der Seite erscheinen, von oben nach unten. Damit eine Regel ausgewählt und ihre Priorität festgelegt werden kann, müssen alle Regeln in einem Regelsatz erfüllt sein.

Um die Regeln festzulegen, die für jeden von Ihnen definierten Schweregrad einer Änderung gelten, gehen Sie zu **Verwaltung für technische Änderungen \> Einrichtung \> Verwaltung für technische Änderungen \> Regelsätze für den Schweregrad technischer Änderungen**. Führen Sie dann einen der folgenden Schritte aus.

- Um einen neuen Regelsatz zu erstellen, wählen Sie **Neu** im Aktivitätsbereich und legen Sie dann die Felder fest, wie später in diesem Abschnitt beschrieben.
- Um einen vorhandenen Regelsatz zu bearbeiten, wählen Sie ihn im Listenbereich aus, wählen Sie **Bearbeiten** im Aktivitätsbereich und legen Sie dann die Felder fest, wie später in diesem Abschnitt beschrieben.
- Um einen bestehenden Regelsatz zu löschen, wählen Sie ihn im Listenbereich aus und wählen Sie dann **Löschen** im Aktivitätsbereich.
- Um die Liste der Regelsätze neu anzuordnen, wählen Sie einen Regelsatz im Listenbereich aus und verwenden dann die Schaltflächen **Aufwärts** und **Abwärts** im Aktivitätsbereich, um ihn neu zu positionieren.

Legen Sie für jeden Regelsatz das folgende Feld fest:

- **Schweregrad** - Wählen Sie den Schweregrad, für den Regeln aufgestellt werden sollen. Sie verwenden die Seite **Schweregrade ändern**, um die Stufen zu erstellen und zu benennen. (Weitere Informationen finden Sie im vorherigen Abschnitt.)

Verwenden Sie die Schaltflächen auf dem Inforegister **Regeln**, um eine Regel für die aktuelle Schweregrad-Einstellung hinzuzufügen oder zu entfernen. Jede Regel hat ein Feld **Regel** und ein Feld **Name**. Die Regeln werden vom System festgelegt und geben die Arten von Änderungen an, die ein Produkt haben kann. Der Name gibt die Art der Änderung an.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]