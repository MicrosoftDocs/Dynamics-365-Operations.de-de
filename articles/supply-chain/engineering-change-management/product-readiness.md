---
title: Produktbereitschaft
description: In diesem Thema wird erklärt, wie Sie Bereitschaftsprüfungen verwenden können, um sicherzustellen, dass die erforderlichen Stammdaten für ein Produkt vervollständigt sind, bevor es in Transaktionen verwendet wird.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8f80458de69a77846259c9a0707c05098d13e12a
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115072"
---
# <a name="product-readiness"></a>Produktbereitschaft

[!include [banner](../includes/banner.md)]

Sie können Bereitschaftsprüfungen verwenden, um sicherzustellen, dass alle erforderlichen Stammdaten für ein Produkt angegeben wurden, bevor es in Transaktionen verwendet wird. Wenn Bereitschaftsprüfungen verwendet werden, wird ein Benutzer oder ein Team für die Validierung bestimmter vordefinierter produktbezogener Daten verantwortlich gemacht. Wenn es eine offene Bereitschaftsprüfung für ein Produkt gibt, kann das Produkt nicht freigegeben oder in Transaktionen verwendet werden.

Das Kontrollkästchen **Aktiv** für ein Engineering-Produkt, eine Variante oder eine Version ist erst verfügbar, nachdem alle erforderlichen Daten eingegeben und überprüft wurden und alle Bereitschaftsprüfungen abgearbeitet wurden. Zu diesem Zeitpunkt kann das Produkt, die Version oder die Variante für andere Firmen freigegeben und in Transaktionen verwendet werden. Sie können Bereitschaftsprüfungen für neue Produkte, neue Varianten und neue Entwicklungsversionen erstellen.

Sie können Bereitschaftsprüfungen auch auf Standardprodukte (nicht technische Produkte) anwenden. Weitere Informationen finden Sie im Abschnitt [Bereitschaftsprüfungen bei Standardprodukten](#standard-products) weiter unten in diesem Thema.

## <a name="types-of-readiness-checks"></a>Arten von Bereitschaftsprüfungen

Es gibt drei Arten von Bereitschaftsprüfungen:

- **Systemprüfung** - Das System prüft, ob ein gültiger Datensatz vorhanden ist. Der Datensatz kann z. B. eine aktive Stückliste (Stückliste) sein.
- **Manuelle Prüfung** - Ein Benutzer prüft, ob der Datensatz gültig ist. Eine Bereitschaftsprüfung könnte z. B. die Validierung der Standardauftragseinstellungen erfordern. In einigen Fällen, z. B. wenn das Produkt noch in der Entwicklung ist und daher nicht auf Lager gelegt wird, sind keine Standard-Auftragseinstellungen erforderlich. Für ein anderes Produkt desselben Typs können jedoch Bestellungsvoreinstellungen erforderlich sein, weil das Produkt auf Lager gehalten werden kann. Es liegt in der Verantwortung des Anwenders zu wissen, wie er korrekt entscheiden kann, ob eine Bereitschaftsprüfung erforderlich ist.
- **Checkliste** - Der Benutzer beantwortet eine Reihe von Fragen aus einer Checkliste, und das System ermittelt, ob die Antworten den Erwartungen entsprechen. Die Checkliste kann ein beliebiges Thema haben. Sie kann z.B. verwendet werden, um festzustellen, ob die Marketingmaterialien oder die Produktdokumentation vollständig sind.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>So werden Readiness Checks für ein neues Engineering-Produkt, eine Variante oder eine Version erstellt

Richtlinien zur Bereitschaftsprüfung können auf der Ebene des freigegebenen Produkts, der freigegebenen Variante und der Engineering-Version angewendet werden.

Wenn Sie eine neues *technisches Produkt* erstellen, bestimmt das System, ob eine [Bereitschaftsüberprüfungsrichtlinie](#assign-policy) angewendet wird. Wenn eine Bereitschaftsprüfungsrichtlinie angewendet wird, treten die folgenden Ereignisse auf:

- Readiness Checks werden für das Produkt erstellt, entsprechend der anwendbaren Richtlinie.
- Die technische Version wird auf inaktiv festgelegt, um das Produkt für die Verwendung zu sperren. Alle technischen Versionen für das Produkt sind auf inaktiv gesetzt.

Wenn eine neue *Variante* erstellt wird, prüft das System, ob dafür eine Bereitschaftsprüfungsrichtlinie gilt. (Bereitschaftsprüfungen können auf Ebene der freigegebenen Variante und auf Ebene der Engineering-Version durchgeführt werden). Wenn eine Bereitschaftsprüfung festgelegt wurde, treten die folgenden Ereignisse auf:

- Readiness Checks werden für das Produkt erstellt, entsprechend der anwendbaren Richtlinie.
- Die technische Version und Variante wird auf inaktiv festgelegt, um das Produkt für die Verwendung zu sperren.

Wenn eine neue Engineeering-*Version* erstellt wird, prüft das System, ob dafür eine Bereitschaftsprüfungsrichtlinie gilt. (Bereitschaftsprüfungen können auf Ebene der freigegebenen Variante und auf Ebene der Engineering-Version durchgeführt werden). Wenn eine Bereitschaftsprüfung festgelegt wurde, treten die folgenden Ereignisse auf:

- Readiness Checks werden für das Produkt erstellt, entsprechend der anwendbaren Richtlinie.
- Die technische Version wird auf inaktiv festgelegt, um das Produkt für die Verwendung zu sperren.

> [!NOTE]
> Sie können Bereitschaftsprüfungen auch auf Standardprodukte (nicht technische Produkte) einrichten. Weitere Informationen finden Sie im Abschnitt [Bereitschaftsprüfungen bei Standardprodukten](#standard-products) weiter unten in diesem Thema.

## <a name="view-readiness-checks"></a>Bereitschaftsprüfungen anzeigen

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Offene Bereitschaftsprüfungen für ein Produkt oder eine Produktversion anzeigen

Um die offenen Bereitschaftsprüfungen für ein Produkt zu finden, öffnen Sie die Seite **Details der freigegebenen Produkte**. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Bereitschaftsprüfungen** die Option **Bereitschaftsprüfungen**.

Um die offenen Bereitschaftsprüfungen für eine Produktversion zu finden, öffnen Sie die Seite **Versionen** für ein freigegebenes Produkt und wählen eine Version. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Checkliste** die Option **Bereitschaftsprüfungen**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Offene Bereitschaftschecks anzeigen, die Ihnen zugewiesen sind

Um die offenen Bereitschaftsprüfungen anzuzeigen, die Ihnen zugewiesen sind, führen Sie einen der folgenden Schritte aus.

- Gehen Sie zu **Verwaltung für technische Änderung \> Allgemein \> Produktbereitschaft \> Meine offenen Bereitschaftsprüfungen**.
- Gehen Sie zu **Produktinformationsmanagement \> Arbeitsbereiche \> Produktbereitschaft für diskrete Fertigung**.

Das Einrichten, das festlegt, wem eine Bereitschaftsprüfung zugewiesen wird, erfolgt für die Bereitschaftsrichtlinie. Bereitschaftsprüfungen können einer Person oder einem Team zugewiesen werden. Wenn eine Bereitschaftsprüfung einem Team zugewiesen ist, gibt es eine Person im Team, die die Bereitschaftsprüfung bearbeiten muss.

## <a name="process-open-readiness-checks"></a>Offene Bereitschaftschecks verarbeiten

### <a name="process-system-and-manual-readiness-checks"></a>Verarbeiten Sie System- und manuelle Bereitschaftsprüfungen

Nachdem Sie die Seite **Bereitschaftsprüfungen** geöffnet haben, können Sie das Thema der System- und manuellen Bereitschaftsprüfungen anzeigen, indem Sie **Zugehörige Informationen anzeigen** im Aktivitätsbereich wählen. Sie können dann die Daten für die Bereitschaftsprüfung vervollständigen und/oder validieren. Offene Bereitschaftsprüfungen haben einen **Status** mit dem Wert *Ausstehend*. Dieser Status zeigt an, dass die Bereitschaftsprüfung noch verarbeitet werden muss. Um eine Bereitschaftsprüfung zu verarbeiten, führen Sie einen der folgenden Schritte aus.

- Wählen Sie im Aktivitätsbereich **Prüfen/abschließen**, um die Bereitschaftsprüfung zu überprüfen und abzuschließen. Wenn Sie fertig sind, wird das Feld **Status** auf *Bestanden* aktualisiert.
- Wählen Sie im Aktivitätsbereich **Überspringen**, wenn Sie eine Bereitschaftsprüfung, die nicht obligatorisch ist, überspringen wollen. Sie haben z. B. eine Bereitschaftsprüfung für Preisberechnungen festgelegt. Sie beschließen jedoch, diese Prüfung zu überspringen, während sich das Produkt noch in der Entwurfsphase befindet. In diesem Fall wird das Feld **Status** auf *Übersprungen* aktualisiert.

Wenn das Feld **Status** für eine Bereitschaftsprüfung auf *Bestanden* aktualisiert wird, kann je nach Konfiguration der Richtlinie ein zusätzlicher Schritt erforderlich sein, um die Bereitschaftsprüfung zu genehmigen. Wählen Sie in diesem Fall **Genehmigung**, um die Bereitschaftsprüfung abzuschließen. Dieser Genehmigungsschritt ist immer erforderlich, wenn die Bereitschaftsprüfung übersprungen wird.

Wenn alle offenen Bereitschaftsprüfungen für ein neues Produkt, eine neue Variante oder eine neue Version abgearbeitet und wie erforderlich genehmigt wurden, wird das Element automatisch aktiv und damit einsatzbereit.

### <a name="process-checklist-readiness-checks"></a>Checklisten-Bereitschaftsprüfungen bearbeiten

Um eine Checkliste zu öffnen, öffnen Sie die Seite **Bereitschaftsprüfungen** und wählen dann im Aktivitätsbereich **Checkliste starten**. Wenn Sie die Checkliste ausgefüllt haben, prüft das System anhand der Einstellungen im Fragebogen, ob die Bereitschaftsprüfung bestanden ist. Wenn die Prüfung bestanden ist, wird das Feld **Status** auf *Bestanden* aktualisiert. Wenn die Bereitschaftsprüfung nicht obligatorisch ist, können Sie sie überspringen. In diesem Fall wird das Feld **Status** auf *Übersprungen* aktualisiert.

Wenn das Feld **Status** für eine Bereitschaftsprüfung auf *Bestanden* aktualisiert wird, kann je nach Konfiguration der Richtlinie ein zusätzlicher Schritt erforderlich sein, um die Bereitschaftsprüfung zu genehmigen. Wählen Sie in diesem Fall **Genehmigung**, um die Bereitschaftsprüfung abzuschließen. Dieser Genehmigungsschritt ist immer erforderlich, wenn die Bereitschaftsprüfung übersprungen wird.

Wenn alle offenen Readiness-Checks für ein neues Produkt, eine Variante oder eine Version abgearbeitet und wie erforderlich genehmigt wurden, wird das Element automatisch aktiv und damit einsatzbereit.

## <a name="create-and-manage-product-readiness-policies"></a>Richtlinien zur Produktbereitschaft erstellen und verwalten

Verwenden Sie Richtlinien zur Produktbereitschaft, um die Bereitschaftsprüfungen zu verwalten, die für ein Produkt gelten. Jede Bereitschaftsrichtlinie enthält eine festgelegte Anzahl von Bereitschaftsprüfungen. Wenn eine Bereitschaftsrichtlinie oder ein freigegebenes Produkt einer Engineering-Produktkategorie zugewiesen wird, haben alle Produkte, die aus dieser Engineering-Produktkategorie erstellt werden, die in der Bereitschaftsrichtlinie angegebenen Bereitschaftsprüfungen.

Um mit Richtlinien zur Produkt-Bereitschaft zu arbeiten, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Richtlinien zur Produkt-Bereitschaft**. Führen Sie dann einen der folgenden Schritte aus.

- Um eine neue Richtlinie zu erstellen, wählen Sie **Neu** im Aktivitätsbereich und legen Sie dann die Felder fest, wie in den folgenden Unterabschnitten beschrieben.
- Um eine bestehende Richtlinie zu bearbeiten, wählen Sie sie im Listenbereich aus, wählen Sie **Bearbeiten** im Aktivitätsbereich und legen Sie dann die Felder wie in den folgenden Unterabschnitten beschrieben fest.
- Um eine bestehende Richtlinie zu löschen, markieren Sie sie im Listenbereich, wählen Sie **Bearbeiten** im Aktivitätsbereich und stellen Sie dann auf der Registerkarte **Allgemein** sicher, dass die Option **Aktiv** auf *Nein* festgelegt ist. Wählen Sie dann **Löschen** im Aktivitätsbereich.

### <a name="header"></a>Übergeordnet

Legen Sie die folgenden Felder in der Kopfzeile einer Richtlinie für die Produktbereitschaft fest.

| Feld | Beschreibung |
|---|---|
| Name | Geben Sie einen Namen für die Richtlinie ein. |
| Beschreibung | Geben Sie eine Beschreibung für die Richtlinie ein. |

### <a name="general-fasttab"></a>Allgemeines Inforegister

Legen Sie die folgenden Felder auf dem Inforegister **Allgemein** einer Richtlinie für die Produktbereitschaft fest.

| Feld | Beschreibung |
|---|---|
| Produkttyp | Wählen Sie, ob die Richtlinie für Produkte vom Typ *Element* oder *Service* gilt. Sie können diese Einstellung nicht mehr ändern, nachdem Sie den Datensatz gespeichert haben. |
| Aktiv | Verwenden Sie diese Option, um die Pflege Ihrer Bereitschaftsrichtlinien zu erleichtern. Legen Sie sie für alle Bereitschaftsrichtlinien, die Sie verwenden, auf *Ja* fest. Legen Sie sie auf *Nein* fest, um eine Bereitschaftsrichtlinie als inaktiv zu markieren, wenn sie nicht verwendet wird. Beachten Sie, dass Sie eine Bereitschaftsrichtlinie, die einer technischen Produktkategorie oder einem feigegebenen Produkt zugewiesen ist, nicht inaktivieren können, und Sie können nur inaktive Bereitschaftsrichtlinien löschen. |

### <a name="readiness-control-fasttab"></a>Bereitschaftskontroll-Inforegister

Fügen Sie für jede Art von Bereitschaftsprüfung, die Sie in die Richtlinie aufnehmen wollen, eine Zeile auf dem Inforegister **Bereitschaftskontrolle** hinzu. Verwenden Sie die folgenden Schaltflächen in der Symbolleiste des Inforegisters, um Zeilen nach Bedarf hinzuzufügen und zu entfernen:

- **Prüfung hinzufügen** - Fügt der Richtlinie eine Standard-Bereitschaftskontrolle hinzu. Wenn Sie diese Schaltfläche wählen, wird das Dialogfeld **Prüfung hinzufügen** angezeigt. Dort können Sie aus einer Liste verfügbarer Prüfungen auswählen.
- **Vorhandenen Fragebogen hinzufügen** - Fügt dem Raster eine leere Zeile hinzu. Sie können dann einen vorhandenen Fragebogen zuweisen, indem Sie die Felder in der folgenden Tabelle festlegen.
- **Kopieren** - Fügt dem Raster eine Kopie der ausgewählten Zeile hinzu.
- **Löschen** - Löscht die ausgewählte Zeile aus dem Raster.

Legen Sie für jede Zeile, die Sie hinzufügen, die folgenden Felder fest.

| Feld | Beschreibung |
| --- | --- |
| Prozessbereich | Wählen Sie den Bereich, auf den sich der Check bezieht. |
| Typ | Wählen Sie, ob es sich um eine Systemprüfung, eine manuelle Prüfung oder eine Checkliste (Fragebogen) handelt. |
| Name | Wenn der Check eine Checkliste ist, geben Sie einen Namen ein. Bei System- und manuellen Checks wird dieses Feld automatisch festgelegt. |
| Beschreibung | Wenn es sich bei dem Check um eine Checkliste handelt, geben Sie eine Beschreibung ein. Bei System- und manuellen Checks wird dieses Feld automatisch festgelegt, und die Beschreibung erklärt den Schwerpunkt des Checks. |
| Prüfungen anwenden auf | Wählen Sie, ob die Zeile Bereitschaftsprüfungen als Reaktion auf ein neues freigegebenes Produkt, eine freigegebene Variante oder eine freigegebene Version generieren soll. |
| Ausführen in | Wählen Sie, ob Bereitschaftsprüfungen, die die Zeile generiert, für alle Firmen oder eine einzelne Firma gelten sollen. |
| Firma | Wenn Sie das Feld **Ausführen in** auf *Einzelne Firma* festlegen, wählen Sie die Firma. |
| Eigentümertyp | Wählen Sie, ob Bereitschaftsprüfungen, die die Zeile generiert, einer Person oder einem Team zugewiesen werden sollen. |
| Eigentümer | Wählen Sie die Person oder das Team aus, der/dem Bereitschaftschecks, die die Zeile erzeugt, zugewiesen werden sollen. |
| Fragebogen | Wählen Sie den Fragebogen aus, der für die Checkliste verwendet werden soll. Die Checkliste ist eine lokale Checkliste in dem Unternehmen, in dem die Bereitschaftsprüfung durchgeführt wird. Das System muss in der Lage sein, auszuwerten, ob die Checkliste korrekt beantwortet wird. Daher muss die Checkliste so festgelegt werden, dass eine Auswertung auf Basis der richtigen Antworten erfolgt. Weitere Informationen zum Erstellen von Fragebögen finden Sie unter [Verwenden von Fragebögen](/dynamicsax-2012/appuser-itpro/using-questionnaires) und den zugehörigen Themen. |
| Automatische Genehmigung | Bereitschaftsprüfungsdatensätze enthalten ein Kontrollkästchen **Genehmigt**, das den Genehmigungsstatus anzeigt. Aktivieren Sie das Kontrollkästchen **Automatische Genehmigung** für Prüfungen, die sofort auf genehmigt festgelegt werden sollen, nachdem der zugewiesene Benutzer sie abgeschlossen hat. Deaktivieren Sie dieses Kontrollkästchen, um eine explizite Genehmigung als zusätzlichen Schritt zu verlangen. |
| Obligatorisch | Aktivieren Sie dieses Kontrollkästchen für Checks, die vom zugewiesenen Benutzer abgeschlossen werden müssen. Obligatorische Prüfungen können nicht übersprungen werden. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Weitere Informationen finden Sie unter Weisen Sie Standard- und Engineering-Produkten Bereitschaftsrichtlinien zu

Wenn Sie ein neues Produkt basierend auf einer Engineering-Kategorie erstellen, erstellen Sie sowohl ein *freigegebenes Produkt* wie auch ein verwandtes *gemeinsames Produkt*. Die Art und Weise, wie Bereitschaftsrichtlinien für ein freigegebenes Produkt aufgelöst werden, hängt davon ab, ob Sie die Funktion *Produktbereitschaftsprüfungen* aktiviert haben. (Weitere Informationen finden Sie im Abschnitt [Bereitschaftsprüfungen bei Standardprodukten](#standard-products) weiter unten in diesem Thema.)

- Wenn die Funktion *Produktbereitschaftsprüfungen* in Ihrem System *deaktiviert* ist, wird die Bereitschaftsrichtlinie festgelegt und nur im Bericht [technische Kategorie](engineering-versions-product-category.md) angezeigt. Um zu erfahren, welche Richtlinie für ein freigegebenes Produkt gilt, überprüft das System das Feld **Produktbereitschaftsrichtlinie** für die zugehörige Engineering-Kategorie. Sie können die Bereitschaftsrichtlinie für ein vorhandenes Produkt ändern, indem Sie die zugehörige Engineering-Kategorie (nicht das freigegebene Produkt) bearbeiten.
- Wenn die Funktion *Produktbereitschaftsprüfungen* *aktiviert* ist, fügt sie ein Feld **Produktbereitschaftsrichtlinie** zur Seite **Produkt** (dort, wo gemeinsam genutzte Produkte eingerichtet sind) und zur Seite **Freigegebenes Produkt** hinzu, (wobei der Wert schreibgeschützt ist und aus dem zugehörigen freigegebenen Produkt stammt). Das System ermittelt die Bereitschaftsrichtlinie für ein freigegebenes Produkt, indem es das zugehörige freigegebene Produkt überprüft. Wenn Sie eine Engineering-Kategorie verwenden, um ein neues Engineering-Produkt zu erstellen, erstellt das System sowohl ein freigegebenes Produkt als auch ein freigegebenes Produkt und kopiert jede Einstellung **Produktbereitschaftsrichtlinie** Einstellung für die Engineering-Kategorie für das neue freigegebene Produkt. Sie können dann die Bereitschaftsrichtlinie für ein vorhandenes Produkt ändern, indem Sie die zugehörige freigegebene Produkt-Kategorie (nicht das freigegebene EngineeringProdukt) bearbeiten.

Um eine Bereitschaftsrichtlinie einem freigegebenen Produkt zuzuweisen, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produkte**.
1. Öffnen oder erstellen Sie das Produkt, dem Sie eine Bereitschaftsrichtlinie zuweisen möchten.
1. Auf dem Inforegister **Allgemeines** legen Sie das Feld **Produktbereitschaftsrichtlinie** auf den Namen der Richtlinie fest, die für das Produkt gelten soll.

Um eine Bereitschaftsrichtlinie einer Engineering-Kategorie zuzuweisen, gehen Sie folgendermaßen vor.

1. Gehen Sie zu **Verwaltung für technische Änderung \> Einrichtung von \> Engineering-Produktkategorie-Details**.
1. Öffnen oder erstellen Sie die Engineering-Kategorie, der Sie eine Bereitschaftsrichtlinie zuweisen möchten.
1. Auf dem Inforegister **Produkt-Bereichtschaftsrichtlinie** legen Sie das Feld **Produktbereitschaftsrichtlinie** auf den Namen der Richtlinie fest, die für das Produkt gelten soll.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Bereitschaftsprüfungen bei Standardprodukten

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Sie können die Produktbereitschaftsprüfung für Standardprodukte (nicht technische Produkte) aktivieren, indem Sie die Funktion *Produktbereitschaftsprüfungen* in der Funktionsverwaltung aktivieren. Diese Funktion nimmt einige kleine Änderungen am Bereitschaftsprüfungssystem vor, sodass es Standardprodukte unterstützt.

### <a name="enable-readiness-checks-on-standard-products"></a>Bereitschaftsprüfungen bei Standardprodukten aktivieren

Führen Sie die folgenden Schritte aus, damit Ihr System Bereitschaftsprüfungen für Standardprodukte durchführen kann.

- Aktivieren Sie die Funktion für technische Änderungsverwaltung in Ihrem System wie in [Übersicht über die Änderungsverwaltung](product-engineering-overview.md) beschrieben.
- Benutzen Sie die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die benannte Funktion *Produktbereitschaftsprüfungen* zu aktivieren.

<!-- KFM: This section requires confirmation before publishing

### How readiness checks are created for standard products

When you create a new non-engineering *released product*, the system determines whether a readiness check policy has been set up for the related shared product. If a policy has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

If a new *variant* is created for a product, the system checks whether readiness checks have been set up on the related shared product. If a readiness check has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

For engineering products, readiness checks are created in the same way that they are created when the *Product readiness checks* feature is turned off. For more information, see the [How readiness checks are created for a new engineering product, variant, or version](#checks-engineering) section earlier in this topic.

-->

### <a name="create-readiness-policies-for-standard-products"></a>Erstellen Sie Bereitschaftsrichtlinien für Standardprodukte

Sie erstellen Bereitschaftsrichtlinien für Standardprodukte genauso wie für technische Produkte. Sehen Sie die Informationen weiter oben in diesem Thema.

### <a name="assign-readiness-policies-to-standard-products"></a>Weisen Sie Bereitschaftsrichtlinien den Standardprodukten zu

Um einem Standardprodukt eine Bereitschaftsrichtlinie zuzuweisen, öffnen Sie das zugehörige freigegebene Produkt und legen Sie das Feld **Produktbereitschaftsrichtlinie** auf den Namen der Richtlinie fest, die angewendet werden soll. Weitere Informationen finden Sie unter [Weisen Sie Standard- und Engineering-Produkten Bereitschaftsrichtlinien zu](#assign-policy), wie zuvor in diesem Thema beschrieben.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Bereitschaftsprüfungen bei Standardprodukten anzeigen und verarbeiten

Wenn diese Funktion aktiviert ist, können Sie Bereitschaftsprüfungen für Standardprodukte genauso anzeigen und verarbeiten wie für technische Produkte. Sehen Sie die Informationen weiter oben in diesem Thema.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
