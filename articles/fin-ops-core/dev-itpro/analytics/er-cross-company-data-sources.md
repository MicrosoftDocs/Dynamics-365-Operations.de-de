---
title: Unternehmensübergreifende Datenquellen in der elektronischen Berichterstellung (EB)
description: In diesem Artikel wird erläutert, wie Sie unternehmensübergreifende Datenquellen in der Elektronische Berichterstellung (Electronic Reporting/ER) verwenden können.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
ms.openlocfilehash: ec96533dd2da933d5275adadedc9a92a33e47a38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277725"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Unternehmensübergreifende Datenquellen in der elektronischen Berichterstellung (EB)

[!include[banner](../includes/banner.md)]

Sie können Elektronische Berichterstellung(ER)-Formate entwerfen, um ausgehende Dokumente in verschiedenen Formaten zu generieren. Wenn ein Dokument erzeugt wird, ruft ein ER-Format Datenquellen auf, die in einem entsprechender ER-Modellzuordnung konfiguriert wurden. Um den Zugriff auf Anwendungstabellen für das Abrufen von Datensätzen zu konfigurieren, können Sie ER-Datenquellen vom Typ **Tabellendatensätze** verwenden. Wenn die zugreifende Tabelle eine gemeinsame Tabelle ist (d.h. eine Tabelle, in der Daten ohne Unternehmenskennung gespeichert werden), gibt diese Datenquelle alle Datensätze zurück. Wenn die zugreifende Tabelle eine unternehmensabhängige Tabelle ist (d.h. eine Tabelle, in der Daten pro Unternehmen gespeichert werden), gibt diese Datenquelle nur die Sätze zurück, die für das aktuelle Unternehmen gespeichert wurden (d.h. den Unternehmenskontext, unter dem das ER-Format läuft).

Jede Datenquelle des Typs **Tabellendatensätze** in einer Modellzuordnung kann nun als unternehmensübergreifende Datenquelle gekennzeichnet werden. Daher können Sie Datenquellen vom Typ **Tabellendatensätze** verwenden, um auf unternehmensübergreifende Daten in Anwendungstabellen zuzugreifen.

Wenn Sie eine Datenquelle als unternehmensübergreifend kennzeichnen, tritt folgendes Verhalten auf:

- Bei einer Datenquelle, die auf eine beliebige gemeinsame Tabelle außer CompanyInfo verweist, gibt die Datenquelle alle Datensätze zurück, die in der referenzierten Tabelle vorhanden sind. 
- Für eine Datenquelle, die auf die CompanyInfo-Tabelle verweist, gibt die Datenquelle die Datensätze zurück, die den Bezeichner eines Unternehmens aus dem definierten Bereich enthalten, obwohl CompanyInfo eine gemeinsame Tabelle ist.
- Für jede unternehmensabhängige Tabelle gibt die Datenquelle die Datensätze der Verweistabelle zurück, die den Bezeichner eines Unternehmens aus dem definierten Umfang enthalten.

Wenn im Dialogfeld der Systemabfrage die Option **Abfrage anfordern** für jede Datenquelle aktiviert ist, die als unternehmensübergreifend markiert ist, können Sie manuell eine oder mehrere Unternehmen auswählen, die auf der Registerkarte **Unternehmensbereich** aufgenommen werden sollen.

> [!IMPORTANT]
> Wie andere Filter wird auch der Unternehmensfilter als zuletzt verwendeter Wert für Abfragen bei der Ausführung eines ER-Formats beibehalten. Der Filter wird nicht automatisch geändert, wenn Sie den unternehmensübergreifenden Wert für eine Datenquelle ändern. Um einen anderen unternehmensübergreifenden Wert für eine andere Datenquelle zu verwenden, löschen Sie die entsprechende benutzerspezifische Auswahl.

Für jede Datenquelle, die als unternehmensübergreifend gekennzeichnet ist, können Sie die gewünschten Datensätze über die Funktionen **FILTER** und **WHERE** in ER-Ausdrücken auswählen. Das Feld **dataAreaID** kann auch als Unternehmenskennung verwendet werden. Derzeit ist das Feld **dataAreaID** auf folgende Bedingungstypen beschränkt, wenn die Funktion **FILTER** verwendet wird:

- Es werden nur Bedingungen unterstützt, die einen einzelnen **dataAreaID** Feldvergleich haben.
- Nur Vergleiche mit Ausdrücken, die nicht von Datensatzlistenelementen abhängen, sind erlaubt.

Daher ist der folgende Ausdruck gültig.

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Standardmäßig enthält der Bereich alle Unternehmen der aktuellen Anwendung. Allerdings kann er beschränkt werden. Um den Umfang des unternehmensübergreifenden Datenzugriffs für ein einziges ER-Format einzuschränken, weisen Sie dem Format eine bestimmte Organisationshierarchie zu. Bei der Definition einer Hierarchie für ein ER-Format werden nur Datensätze für juristische Personen zurückgegeben, die in der zugewiesenen Hierarchie dargestellt werden, obwohl das Format unternehmensübergreifende Datenquellen aufruft. Wenn für ein ER-Format eine Referenz auf eine nicht mehr existierende Hierarchie definiert wird, wird der Standardbereich verwendet und das Format ruft unternehmensübergreifende Datenquellen auf. In diesem Fall werden alle Datensätze für Anwendungsunternehmen zurückgegeben.

Beachten Sie, dass, wenn die Option **Entwurf verwenden** für die Zuordnung zu einer einzelnen ER-Format-Organisationshierarchie aktiviert ist, die juristischen Personen aus der Entwurfsversion dieser Hierarchie verwendet werden, um den Bereich für unternehmensübergreifende Datenquellen zu identifizieren. Existiert der Entwurf nicht, werden die juristischen Personen aus der letzten veröffentlichten Version dieser Organisationshierarchie verwendet.

Beachten Sie, dass, wenn die Option **Entwurf verwenden** für die Zuordnung zu einer einzelnen ER-Format-Organisationshierarchie deaktiviert ist, die juristischen Personen aus der letzten Entwurfsversion dieser Organisationshierarchie verwendet werden, um den Bereich für unternehmensübergreifende Datenquellen zu identifizieren. Datumseffektivität von Organisationshierarchien wird im ER-Framework noch nicht unterstützt.

Die Hierarchie kann einem Format in einer bestimmten Seite zugeordnet werden, das über den ER-Arbeitsbereich oder über den Menüpunkt **Organisationsverwaltung** \>Elektronische Berichterstellung\> Formatfilter der juristischen Person erreichbar ist. Um auf die Seite zuzugreifen, muss einem Benutzer das Recht **Formatfilter der juristischen Person pflegen** (ERMaintainFormatMappingLegalEntityFilters) gewährt werden. Zusätzlich zu der Einschränkung, die der Benutzer im Dialogfenster der Systemabfrage manuell festlegen kann, wird die Bereichseinschränkung von hierarchisch strukturierten juristischen Personen für das Format angewendet. Die Schnittmenge dieser Einschränkungen wird bei der Ausführung des Formats verwendet.

Um mehr über diese Funktion zu erfahren, spielen Sie den Aufgabenleitfaden **ER Zugriff auf Datensätze in unternehmensabhängigen Tabellenim unternehmensübergreifenden Modus**, der Teil des Geschäftsprozesses 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677) ist und im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) heruntergeladen werden kann. Dieser Aufgabenleitfaden führt Sie durch den Prozess der Konfiguration einer ER-Modellzuordnung und des ER-Formats für den Zugriff auf Anwendungstabellen im unternehmensübergreifenden Modus.

Laden Sie die folgenden Dateien herunter, um den Aufgabenleitfaden ausführen:

- [ER-Datenmodellkonfiguration - CrossCompanyDataAccessModel.xml](https://download.microsoft.com/download/4/2/5/4258f891-7054-4821-aedd-3721ba25fdd5/CrossCompanyDataAccessModel.xml)
- [ER-Formatkonfiguration - CrossCompanyDataAccessFormat.xml](https://download.microsoft.com/download/3/2/1/321deb75-3ba9-4323-99bf-207a52c60b5c/CrossCompanyDataAccessFormat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
