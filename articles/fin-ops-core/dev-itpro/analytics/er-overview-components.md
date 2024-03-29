---
title: Überblick über die Komponenten der elektronischen Berichterstellung
description: In diesem Artikel werden die Komponenten der elektronischen Berichterstellung (EB) beschrieben.
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285030"
---
# <a name="electronic-reporting-components"></a>Überblick über die Komponenten der elektronischen Berichterstellung

[!include [banner](../includes/banner.md)]

Die elektronische Berichterstellung (ER) unterstützt die folgenden Komponententypen:

- Datenmodell
- Modellzuordnung
- Formate
- Metadaten

## <a name="data-model-component"></a>Datenmodellkomponente

Eine Datenmodellkomponente ist eine abstrakte Darstellung der Datenstruktur. Sie beschreibt einen bestimmten Bereich einer Geschäftsdomäne mit ausreichend Details, um die Berichtsanforderungen für diese Domäne zu erfüllen. Eine Datenmodellkomponente besteht aus den folgenden Teilen:

- **Datenmodell** – Ein Satz domänenspezifischer Geschäftseinheiten und einer hierarchisch strukturierten Definition von Beziehungen zwischen diesen Einheiten.
- **Modellzuordnung** – Ausgewählte Anwendungsdatenquellen sind mit einzelnen Elementen eines Datenmodells verknüpft, das zur Laufzeit den Datenfluss und die Regeln für die Eingabe der Geschäftsdaten in eine Datenmodellkomponente angibt.

Die Geschäftseinheit eines Datenmodells wird als Container oder Datensatz dargestellt. Geschäftseinheitseigenschaften werden als Datenelemente oder Felder dargestellt. Jedes Datenelement hat eine(n) eindeutigen Namen, Beschriftung, Beschreibung und Wert. Der Wert jedes Datenelements kann so konzipiert werden, dass er als Zeichenfolge, Ganzzahl, Gleitkommazahl, Datum, Aufzählung oder boolescher Wert erkannt wird. Außerdem kann das Datenelement ein anderer Datensato oder eine Datensatzliste sein.

Eine einzelne Datenmodellkomponente kann mehrere Hierarchien von domänenspezifischen Geschäftsentitäten enthalten. Sie kann auch Modellzuordnungen enthalten, die einen berichtspezifischen Datenfluss bei Laufzeit unterstützen. Die Hierarchien unterscheiden sich durch einen einzelnen Datensatz, der als Stamm zur Modellzuordnung ausgewählt wird. Beispielsweise unterstützt das Datenmodell des Zahlungsdomänenbereichs möglicherweise die folgenden Zuordnungen:


- Unternehmen \> Kreditor \> Zahlungsbuchungen der Kreditorendomäne
- Debitor \> Unternehmen \> Zahlungsbuchungen der Debitorendomäne

Geschäftsentitäten, z. B. Unternehmens- und Zahlungstransaktionen, werden nur einmal erstellt. Verschiedene Zuordnungen können sie nach Bedarf wiederverwenden.

## <a name="model-mapping-component"></a>Modellzuordnungskomponente

Die Modellzuordnung verknüpft Anwendungsdatenquellen mit einzelnen Elementen eines Datenmodells, die zur Laufzeit den Datenfluss und die Regeln für die Eingabe der Geschäftsdaten in eine Datenmodellkomponente angeben.

Eine Modellzuordnung, die ausgehende elektronische Dokumente unterstützt, hat die folgenden Fähigkeiten:

- Sie kann verschiedene Datentypen als Datenquellen für ein Datenmodell verwenden. Diese Datentypen enthalten Tabellen, Datenentitäten, Methoden und Aufzählungen.
- Sie unterstützt Benutzereingabeparameter, die als Datenquellen für ein Datenmodell definiert werden, wenn einige Daten zur Laufzeit angegeben werden müssen.
- Sie unterstützt die Datenumwandlung in die erforderlichen Gruppen. Sie können auch Daten filtern, sortieren und zusammenfassen sowie logisch berechnete Felder anhängen, die mit Formeln entworfen werden, die Microsoft Excel-Formeln ähneln. Weitere Informationen finden Sie unter [Formuladesigner in der elektronischen Berichterstattung (ER)](general-electronic-reporting-formula-designer.md).

Eine Zuordnung, die vorbildliche eingehende elektronische Dokumente unterstützt, umfasst die folgenden Funktionen:

- Sie kann unterschiedliche aktualisierbare Datenelemente als Ziele verwenden. Diese Datenelemente enthalten Tabellen, Datenentitäten und Ansichten. Die Daten können mithilfe der eingehenden Daten von elektronischen Dokumenten aktualisiert werden. Mehrere Ziele können in einer einzelnen Modellzuordnung verwendet werden.
- Sie unterstützt Benutzereingabeparameter, die als Datenquellen für ein Datenmodell definiert werden, wenn einige Daten zur Laufzeit angegeben werden müssen.

Für jede Geschäftsdomäne, die als einheitliche Datenquelle für die Berichterstellung verwendet wird, wird eine Datenmodellkomponente entwickelt. Die einheitliche Datenquelle isoliert die Berichterstellung von der physischen Implementierung der Datenquellen. Die Komponente stellt domänenspezifische Geschäftskonzepte und Funktionen in einem Formular dar, die den ersten Entwurf und die weitere Verwaltung eines Berichterstellungsformats effizienter macht.

## <a name="format-component"></a>Formatkomponente

### <a name="format-components-for-outgoing-electronic-documents"></a>Formatkomponenten für ausgehende elektronische Dokumente

Eine Formatkomponente ist das Schema der Berichtsausgabe, die zur Laufzeit generiert wird. Ein Schema besteht aus folgenden Elementen:

- Ein Format, das die Struktur und den Inhalt des zur Laufzeit generierten ausgehenden elektronischen Dokuments festlegt.
- Datenquellen als Satz von Benutzereingabeparametern und einem domänenspezifischen Datenmodell, das eine ausgewählte Modellzuordnung verwendet.
- Eine Formatzuordnung als Satz von Bindungen von Formatdatenquellen mit einzelnen Elementen des Formats, die den Datenfluss und die Regeln für die Generierung der Formatausgabe zur Laufzeit angeben.
- Eine Formatprüfung als Satz konfigurierbarer Regeln, die die Berichterstellung zur Laufzeit abhängig von ausgeführtem Kontext steuern. Beispielsweise könnte es eine Regel geben, die die ausgehende Generierung der Zahlungen eines Kreditors beendet und eine Ausnahme auslöst, wenn bestimmte Attribute des ausgewählten Kreditors fehlen, z. B: die Bankkontonummer.

Eine Formatkomponente unterstützt die folgenden Funktionen:

- Erstellen einer Berichtsausgabe als individuelle Dateien in unterschiedlichen Formaten, wie Text, XML, Microsoft Word-Dokument oder Arbeitsblatt
- Getrenntes Erstellen mehrerer Dateien und deren Einschließung in Zip-Dateien

Mit einer Formatkomponente können Sie bestimmte Dateien anzufügen, die in der Berichtsausgabe verwendet werden können:

- Excel-Arbeitsmappen, die Arbeitsblätter enthälten, die als Vorlage für Ausgaben im OPENXML-Arbeitsblattformat verwendet werden können
- Word-Dateien, die ein Dokument enthalten, das als Vorlage für Ausgaben im Microsoft Word-Dokumentformat verwendet werden kann
- Andere Dateien, die in die Ausgabe des Formats als vordefinierte Dateien übernommen werden können

Die folgende Abbildung zeigt, wie die Daten für diese Formate fließen.

[![Datenfluss für ausgehende Formatkomponenten](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Um eine einzelne ER-Formatkonfiguration ausführen und ein ausgehendes elektronisches Dokument zu generieren, müssen Sie die Zuordnung der Formatkonfiguration identifizieren.

#### <a name="format-components-for-incoming-electronic-documents"></a>Formatkomponenten für eingehende elektronische Dokumente
Eine Formatkomponente ist das Schema des eingehenden Dokuments, das zur Laufzeit importiert wird. Ein Schema besteht aus folgenden Elementen:

- Ein Format, das die Struktur und den Inhalt des zur Laufzeit importierten eingehenden elektronischen Dokuments festlegt, das Daten enthält. Eine Formatkomponente wird verwendet, um ein eingehendes Dokument in verschiedenen Formaten, z. B. Text und XML, zu analysieren.
- Eine Formatzuordnung, die einzelne Formatelemente an die Elemente eines domänenspezifischen Datenmodells bindet. Zur Laufzeit geben die Elemente im Datenmodell den Datenfluss und die Regeln für das Importieren von Daten von einem eingehenden Dokument an und speichern die Daten anschließend in einem Datenmodell.
- Eine Formatprüfung als Satz konfigurierbarer Regeln, die den Datenimport zur Laufzeit abhängig von ausgeführtem Kontext steuern. Beispielsweise könnte es eine Regel geben, die den Datenimport eines Bankauszugs mit einer Kreditorzahlung beendet und eine Ausnahme auslöst, wenn die Attribute eines bestimmten Kreditors fehlen, z. B: der Lieferantenidentifizierungscode.

Die folgende Abbildung zeigt, wie die Daten für diese Formate fließen.

[![Datenfluss für eingehende Formatkomponenten](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Um eine einzelne ER-Formatkonfiguration auszuführen, um Daten von einem eingehenden elektronischen Dokument zu importieren, müssen Sie die gewünschte Zuordnung einer Formatkonfiguration und auch den Integrationspunkt einer Modellzuordnung identifizieren. Sie können dieselbe Modellzuordnung und Ziele zusammen mit verschiedenen Formaten für unterschiedliche Arten von eingehenden Dokumenten verwenden.


## <a name="component-versioning"></a>Teilversionsverwaltung

Die Versionsverwaltung wird für ER-Komponenten unterstützt. Der folgende Workflow wird für die Verwaltung von Änderungen in ER-Komponenten bereitgestellt:

1. Die ursprünglich erstellte Version ist als **Entwurf**-Version gekennzeichnet. Diese Version kann bearbeitet werden und ist für Testläufe verfügbar.
2. Die **Entwurf**-Version kann in eine **Abgeschlossen**-Version konvertiert werden. Diese Version kann in lokalen Berichtsprozessen verwendet werden.
3. Die **Abgeschlossen**-Version kann in eine **Freigegeben**-Version konvertiert werden. Diese Version wird in Microsoft Dynamics Lifecycle Services (LCS) veröffentlicht und kann in den globalen Berichterstellungsprozessen verwendet werden.
4. Die **Gemeinsam genutzt**-Version kann in eine **Eingestellt**-Version konvertiert werden. Diese Version kann gelöscht werden.

Versionen in einem **Abgeschlossen** oder **Gemeinsam genutzt**-Status sind für anderen Datenaustausch verfügbar. Die folgenden Aktionen können für eine Komponente mit diesen Status ausgeführt werden:

- Die Komponente kann im XML-Format serialisiert und als Datei im XML-Format exportiert werden.
- Die Komponente kann aus einer XML-Datei reserialisiert und als neue Version einer ER-Komponente in der Anwendung importiert werden.

Weitere Informationen finden Sie unter [Importieren einer neuen Datenmodellkonfiguration](er-quick-start1-new-solution.md#ImportDataModel) und [Exportieren der abgeschlossenen Version eines abgeleiteten Formats](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Entwurfsversionen zur Laufzeit

In Ihren persönlichen Benutzerparametern für das EB-Framework können Sie die Option aktivieren, mit der Sie festlegen können, ob die Entwurfsversion einer EB-Konfiguration zur Laufzeit verwendet werden muss. Informationen dazu, wie Sie die Option **Entwurf ausführen** für Ihre EB-Konfigurationen verfügbar machen finden Sie in [Markieren eines benutzerdefinierten Formats als ausführbar](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> Die EB-Benutzerparameter sind unternehmensspezifisch und benutzerspezifisch.

### <a name="draft-format-versions-at-runtime"></a>Entwurfsformatversionen zur Laufzeit

Wenn Sie eine EB-Lösung ausführen, werden die Entwurfsversionen ihrer Formatkomponenten standardmäßig ignoriert. Stattdessen wird nur die relevante Version, die einen anderen Status als **Entwurf** hat, genutzt. Manchmal möchten Sie die EB zwingen, zur Laufzeit die Entwurfsversion Ihrer EB-Formatkonfiguration zu verwenden. Nachdem Sie beispielsweise notwendige Änderungen in Ihrer Entwurfsversion vorgenommen haben, können Sie diese Entwurfsversion für den Testlauf verwenden. Auf diese Weise können überprüfen, ob Ihre Änderungen richtig sind. Um mit der Nutzung dieser Entwurfsformatversion zu beginnen [legen Sie](er-quick-start2-customize-report.md#MarkFormatRunnable) die Option **Entwurf ausführen** der betroffenen EB-Konfiguration auf **Ja** fest.

### <a name="draft-model-mapping-versions-at-runtime"></a>Entwürfe für Modellzuordnungsversionen zur Laufzeit erstellen

Wenn Sie eine EB-Lösung ausführen, werden die Entwurfsversionen ihrer Modellzuordnungskomponenten werden immer verwendet. Manchmal möchten Sie die EB zwingen, zur Laufzeit die Entwurfsversion Ihrer EB-Modellzuordnungskonfiguration zu ignorieren. Ab **Version 10.0.29** können Sie festlegen, dass die Funktion **Option „Entwurf ausführen“ für EB-Modellzuordnungen immer berücksichtigen** die Modellzuordnungsversion, die zur Laufzeit verwendet wird, steuert. Wenn diese Funktion aktiviert ist, tritt das folgende Verhalten auf:

- Wenn die Option **Entwurf ausführen** für eine Modellzuordnungskonfiguration auf **Nein** festgelegt ist, wird zur Laufzeit die höchste Nicht-Entwurfsversion dieser Konfiguration verwendet. Eine Ausnahme wird ausgelöst, wenn die Konfiguration in der aktuellen Finance-Instanz nicht verfügbar ist.
- Wenn die Option **Entwurf ausführen** für eine Modellzuordnungskonfiguration auf **Ja** festgelegt ist, wird zur Laufzeit die Entwurfsversion dieser Konfiguration verwendet.

## <a name="component-date-effectivity"></a>Teildatumswirksamkeit

EB-Formatkomponentenversionen haben ein Gültigkeitsdatum. Sie können das „Gültig ab“-Datum für eine EB-Formatkomponente definieren, um das Datum anzugeben, ab dem diese Komponente für Berichtsprozesse wirksam wird. Das Anwendungs-Sitzungsdatum wird verwendet, um zu definieren, ob eine Komponente für die Ausführung gültig ist. Wenn mehrere Versionen für ein bestimmtes Datum gültig sind, wird die aktuellste Version für die Berichterstattung verwendet.

## <a name="component-access"></a>Teilzugriff

Der Zugriff auf EB-Format- und -Modellzuordnungskomponenten zur Laufzeit hängt von der Einstellung für den Länder- bzw. Regionscode der internationalen Organisation für Normung (ISO) ab. Wenn diese Einstellung für eine ausgewählte Version einer Format- oder Modellzuordnungskonfiguration leer ist, kann der Zugriff auf eine Format- oder Modellzuordnungskomponente von jedem Unternehmen aus zur Laufzeit erfolgen. Wenn die Einstellung ISO-Länder-/Regionscodes enthält, steht eine Format- oder Modellzuordnungskomponente nur von Unternehmen zur Verfügung, die eine primäre Adresse besitzen, die für einen der ISO-Länder-/Regionscodes einer Formatkomponente definiert ist.

Für unterschiedliche Versionen einer Format- oder Modellzuordnungskomponente kann es verschiedene Einstellungen von ISO-Länder-/Regionscodes geben.

Weitere Informationen finden Sie unter [Auf Länderkontext beruhende EB-Modellzuordnungen konfigurieren](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

