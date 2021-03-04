---
title: Produktkonfigurationsmodelle – Überblick
description: Dieser Artikel definiert Begriffe und Konzepte, die zu den Produktkonfigurationsmodellen relevant sind. Produktkonfigurationsmodelle lassen Sie eine generische Produktstruktur erstellen, die verwendet werden kann, wenn viele Produktvarianten für ein bestimmtes Produkt zu konfigurieren.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87d61203d36722194b98a247609fa126b71b846c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428475"
---
# <a name="product-configuration-models-overview"></a>Produktkonfigurationsmodelle – Überblick

[!include [banner](../includes/banner.md)]

Dieser Artikel definiert Begriffe und Konzepte, die zu den Produktkonfigurationsmodellen relevant sind. Produktkonfigurationsmodelle lassen Sie eine generische Produktstruktur erstellen, die verwendet werden kann, wenn viele Produktvarianten für ein bestimmtes Produkt zu konfigurieren.

Produktkonfigurationsmodelle werden erstellt, um eine allgemeine Produktstruktur darzustellen. Nachdem Sie ein Produktkonfigurationsmodell eingerichtet haben, können Sie ein eindeutig identifizierbares Produkt konfigurieren, das über eine eindeutige Stückliste (BOM) und einen eindeutigen Arbeitsplan verfügt. Produktkonfigurationsmodelle verwenden deklarative Einschränkungen und obligatorische Berechnungen, um die Beziehungen und Einschränkungen zwischen verschiedenen Produktvarianten zu behandeln. Sie können Artikel in Aufträgen, Verkaufsangeboten, Bestellungen und Produktionsaufträgen konfigurieren. In der folgenden Tabelle werden die tabelleneinschränkungsbasierten Begriffe und Konzepte dargestellt.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Komponenten</td>
<td>Komponenten sind die wichtigsten Bausteine eines Produktkonfigurationsmodells. Komponenten werden in einer Strukturdarstellung auf der Seite <strong>Details zum einschränkungsbasierten Produktkonfigurationsmodell</strong> angezeigt. Komponenten können die folgenden Elemente enthalten:
<ul>
<li>Attribute</li>
<li>Einschränkungen</li>
<li>Berechnungen</li>
<li>Unterkomponenten</li>
<li>Benutzeranforderungen</li>
<li>Stücklistenpositionen</li>
<li>Arbeitsplanarbeitsgänge</li>
</ul></td>
</tr>
<tr class="even">
<td>Attribute</td>
<td>Attribute beschreiben alle Funktionen des Produktkonfigurationsmodells. Sie können Attribute verwenden, um die Funktion anzugeben, die ausgewählt werden können, wenn ein eindeutig identifizierbares Produkt konfiguriert wird. Attribute werden in Einschränkungen und Bedingungen verwendet. Wenn Attribute zu einem Produktkonfigurationsmodell erstellt und hinzugefügt werden, wird auf die zugehörigen Attributtypen verwiesen. Ein Standardwert kann für ein Attribut festgelegt werden. Der Standardwert wird in der Konfigurationsbenutzeroberfläche (UI) verwendet, wenn das Produktkonfigurationsmodell konfiguriert wird. Sie können angeben, dass ein Attribut erforderlich, schreibgeschützt oder ausgeblendet ist.
<ul>
<li><strong>Erforderlich</strong> – Ein Wert muss für das Attribut festgelegt werden, wenn das Produkt konfiguriert wird.</li>
<li><strong>Schreibgeschützt</strong> – Der Attributwert wird während einer Konfigurationssitzung angezeigt, er kann jedoch nicht geändert werden.</li>
<li><strong>Ausgeblendet</strong> – Der Attributwert ist in den Einschränkungen und Bedingungen enthalten, er wird jedoch noch nicht während einer Konfigurationssitzung angezeigt.</li>
</ul>
Sie können auch eine Bedingung für Attribute angeben. Wenn die Bedingung erfüllt ist, muss ein Wert für das erforderliche Attribut eingegeben werden. Bedingungen sind Ausdrucke, die erfüllt sein müssen, damit Attribute, Stücklistenpositionen und Arbeitsplan-Arbeitsgänge in ein Produktkonfigurationsmodell einbezogen werden können. Alle in einer Bedingung referenzierten Attribute werden obligatorisch. Es wird empfohlen, Attribute auf der Registerkarte <strong>Attribute</strong> als erforderlich auszuwählen. Dadurch werden erforderliche Attribute besser erkannt. Attributwerte sind ein wichtiger Bestandteil der Wiederverwendung von Konfigurationen. Das System verwendet Attributwerte, um zu bestimmen, ob eine Konfiguration vorhanden ist, die den Auswahlen entspricht, die ein Benutzer während einer Konfigurationssitzung vorgenommen hat.</td>
</tr>
<tr class="odd">
<td>Attributtypen</td>
<td>Attributtypen geben den Satz von Datentypen für Attribute an, die in einem Produktkonfigurationsmodell verwendet werden. Die folgenden Attributtypen werden verwendet:
<ul>
<li><strong>Ganzzahl</strong> mit oder ohne einen Bereich</li>
<li><strong>Dezimal</strong></li>
<li><strong>Text</strong> mit oder ohne eine feste Liste</li>
<li><strong>Aktiv</strong></li>
</ul>
Beim Attributtyp <strong>Boolesch</strong>, <strong>Ganzzahl</strong> mit einem Bereich oder <strong>Text</strong> mit einer festen Liste ist der Satz von Werten verfügbar, wenn ein Produktkonfigurationsmodell eingerichtet ist. <strong>Hinweis:</strong> Der Produktkonfigurations-Solver erkannt nur die folgenden Attributtypen: <strong>Boolesch</strong>, <strong>Text</strong> mit einer festen Liste und <strong>Ganzzahl</strong> mit einem Bereich. Daher können nur diese Attributtypen in den Ausdruckseinschränkungen und Bedingungen verwendet werden.</td>
</tr>
<tr class="even">
<td>Einschränkungen</td>
<td>Einschränkungen beschreiben die Einschränkungen der Produktmodellkonfiguration. Einschränkungen werden verwendet, um sicherzustellen, dass nur gültige Werte ausgewählt werden, wenn ein Produkt konfiguriert wird. Bei Einschränkungen kann es sich um Ausdruckseinschränkungen oder Tabelleneinschränkungen handeln:
<ul>
<li>Ausdruckseinschränkungen können nur für die Komponente verwendet werden, mit der sie verbunden sind. Die Ausdruckseinschränkungen für eine Komponente können jedoch auf Attribute der Unterkomponenten der Komponente verweisen. Der Produktkonfigurations-Solver wird verwendet, um die Einschränkungen aufzulösen, und Sie müssen die Solver-Syntax verwenden, wenn Sie die Einschränkungen schreiben. Weitere Informationen finden Sie im Link zu Ausdruckseinschränkungen und Tabelleneinschränkungen.</li>
<li>Tabelleneinschränkungen müssen definiert werden, damit sie auf eine Komponente in einem Produktkonfigurationsmodell angewendet werden können. Tabelleneinschränkungen können als benutzerdefinierte oder als systemdefinierte Einschränkung vorliegen. Eine benutzerdefinierte Tabelleneinschränkung ist eine Art Matrix, der verwendet werden kann, um den Satz der Kombinationen für die Attributwerte zu beschreiben, die von Attributtypen definiert werden. Wenn beispielsweise Lautsprecher produziert werden, kann die Matrix für eine benutzerdefinierte Tabelleneinschränkung Spalten für das Oberflächenmaterial und das Vordergerippe des Lautsprechers anzeigen.</li>
</ul>
<strong>Beispiel</strong> Lautsprecher sind in vier Oberflächendesigns verfügbar: Schwarz, Eiche, Rosenholz und Weiß. Die Lautsprecher können einen von drei vorderen Grills haben: Beispiel für schwarzen, Metall oder Weiß. Das Ende schwarze ist für alle Grills verfügbar, die jedoch anderen Ende werden bestimmten Grills beschränkt. Die folgende Tabelle enthält ein Beispiel der Informationen, die auf der Registerkarte auf <strong>Zulässige Kombinationen</strong> der Seite <strong>Tabelleneinschränkung bearbeiten</strong> angezeigt werden.
<table>
<thead>
<tr class="header">
<th>Gehäuseoberfläche</th>
<th>Vordergerippe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Schwarz</td>
<td>Schwarz</td>
</tr>
<tr class="even">
<td>Schwarz</td>
<td>Metall</td>
</tr>
<tr class="odd">
<td>Schwarz</td>
<td>Weiß</td>
</tr>
<tr class="even">
<td>Eiche</td>
<td>Schwarz</td>
</tr>
<tr class="odd">
<td>Rosenholz</td>
<td>Weiß</td>
</tr>
<tr class="even">
<td>Weiß</td>
<td>Schwarz</td>
</tr>
<tr class="odd">
<td>Weiß</td>
<td>Weiß</td>
</tr>
</tbody>
</table>
Eine systemdefinierte Tabelleneinschränkung stellt eine Verknüpfung zwischen einem Attributtyp und einem Feld in einer Supply Chain Management-Tabelle dar. Eine systemdefinierte Tabelleneinschränkung verknüpft dynamisch das Attribut Typ mit dem Feld. Die Verknüpfung ermöglicht dem Attribut in einem Produktkonfigurationsmodell die Daten des Felds in der Supply Chain Management-Tabelle widerzuspiegeln.</td>
</tr>
<tr class="odd">
<td>Berechnungen</td>
<td>Berechnungen geben eine Ergänzung zu den Einschränkungen dar. Sie können eine Berechnung nutzen, um arithmetische Operationen auf Attributen vom <strong>Dezimal</strong>-Typ und <strong>Ganzzahl</strong>, oder logische Operationen verwenden, die Attribute des Typs <strong>Text</strong> mit einer festen Liste und des Typs <strong>Boolesch</strong> umfassen. Eine Berechnung hat ein Zielattribut, das das Ergebnis des Berechnungsausdrucks innehat. Der Berechnungsausdruck wird mithilfe des Ausdruckseditors erstellt.</td>
</tr>
<tr class="even">
<td>Unterkomponenten</td>
<td>Unterkomponenten spiegeln die Baumstruktur des Produktkonfigurationsmodells wieder. Sie können Unterkomponenten verwenden, um die Struktur des Produktkonfigurationsmodells zu erstellen. Unterkomponenten verweisen auf vorhandene Komponenten. Daher ist es mithilfe von Unterkomponenten sinnvoll, Komponenten in mehreren Produktkonfigurationsmodellen zu verwenden. Auf der Seite <strong>Stücklistenpositionsdetails</strong> für eine Unterkomponente können Sie einen eindeutigen Wert für die Unterkomponente auswählen. Alternativ können Sie ein Attribut auswählen, für das der Wert ausgewählt wird, wenn das Produktkonfigurationsmodell eingerichtet wird. Um ein Produkt als Komponente oder Unterkomponente einzubeziehen, müssen Sie Folgendes auf der Seite<strong> Produkt erstellen</strong> angeben, wenn Sie das Produkt erstellen:
<ul>
<li>Wählen Sie im Feld <strong>Produkttyp</strong> den Eintrag <strong>Artikel</strong> aus.</li>
<li>Wählen Sie im Feld <strong>Produktuntertyp</strong> den Eintrag <strong>Produktmaster</strong> aus.</li>
<li>Wählen Sie im Feld <strong>Konfigurationstechnologie</strong> den Eintrag <strong>Einschränkungsbasierte Konfiguration</strong> aus.</li>
</ul>
Sie können auf der Registerkarte <strong>Allgemein</strong> der Seite <strong>Details für freigegebene Produkte</strong> anzeigen, ob ein freigegebenes Produkt als Komponente oder Unterkomponente verwendet werden kann. Wenn <strong>Einschränkungsbasierte Konfiguration</strong> im Feld <strong>Konfigurationstechnologie</strong> ausgewählt ist, kann das Produkt als Komponente oder Unterkomponente verwendet werden. Sie können Unterkomponenten ausblenden, sodass dem Benutzer während einer Konfigurationssitzung nicht angezeigt werden. Attribute, Unterkomponenten und Benutzeranforderungen, die der Unterkomponente zugeordnet sind, werden ebenfalls ausgeblendet.</td>
</tr>
<tr class="odd">
<td>Benutzeranforderungen</td>
<td>Benutzeranforderungen stellen eine Abstraktion zwischen Benutzeranforderungen und bestimmten Komponenten und Attributen dar. Sie können eine Benutzeranforderung nicht einem Artikel zuordnen. Beispielsweise kauft ein Debitor für ein Heimkinosystem. Der Verkäufer fragt nach der Größe des Raums, in dem der Debitor das System installieren möchte, um festzustellen, wie viel Watt erforderlich sind. In diesem Beispiel kann die Raumgröße eine Benutzeranforderung sein, mit deren Hilfe der entsprechende Attributwert für eine bestimmte Komponente bestimmt werden kann. Sie können Benutzeranforderungen ausblenden, sodass dem Benutzer während einer Konfigurationssitzung nicht angezeigt werden. Attribute, Unterkomponenten und Benutzeranforderungen, die der Benutzeranforderung zugeordnet sind, werden ebenfalls ausgeblendet. Sie können eine Bedingung schreiben, um zu steuern, ob eine Benutzeranforderung ausgeblendet werden kann. Sie müssen zum Schreiben dieser Bedingung die Optimization Modeling Language (OML)-Syntax verwenden.</td>
</tr>
<tr class="even">
<td>Stücklistenpositionen</td>
<td>Stücklistenpositionen repräsentieren die einzelnen Materialien der Komponenten im Produktkonfigurationsmodell. Auf der <strong>Stücklistenpositionsdetails</strong> Seite sind alle Artikel zur Auswahl. Eine Bedingung kann der Stücklistenposition hinzugefügt werden, sodass die Stücklistenpositionen, die für eine Variante des eindeutig identifizierbaren Produkts ausgewählt werden, variieren können, basierend auf der Auswahl des Benutzers, wenn das Produktkonfigurationsmodell eingerichtet wird. Bedingungen sind Ausdrucke, die erfüllt sein müssen, damit Attribute, Stücklistenpositionen und Arbeitsplan-Arbeitsgänge in ein Produktkonfigurationsmodell einbezogen werden können. Auf der <strong>Stücklistenpositionsdetails</strong> Seite können Sie einen unterschiedlichen Wert auswählen. Alternativ können Sie eine Zuordnung zu einem Attribut durchführen, für das der Wert ausgewählt wird, wenn das Produktkonfigurationsmodell eingerichtet wird.</td>
</tr>
<tr class="odd">
<td>Arbeitsplanarbeitsgänge</td>
<td>Auf der <strong>Details zum Arbeitsplan-Arbeitsgang</strong> Seite können Sie einen unterschiedlichen Wert auswählen. Alternativ können Sie eine Zuordnung zu einem Attribut durchführen, für das der Wert ausgewählt wird, wenn das Produktkonfigurationsmodell eingerichtet wird. Bedingungen werden wie Ausdruckseinschränkungen geschrieben. Bedingungen sind Ausdrucke, die erfüllt sein müssen, damit Attribute, Stücklistenpositionen und Arbeitsplan-Arbeitsgänge in ein Produktkonfigurationsmodell einbezogen werden können.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]