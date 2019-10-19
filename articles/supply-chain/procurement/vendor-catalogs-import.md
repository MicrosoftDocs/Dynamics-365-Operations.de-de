---
title: Lieferantenkataloge importieren
description: In diesem Thema wird beschrieben, wie Lieferantenkatalogdaten importiert werden.
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 9f85b1d1f0b1c2378dd3f278640d984c31923c35
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017873"
---
# <a name="import-vendor-catalogs"></a>Lieferantenkataloge importieren
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Lieferantenkatalogimport

In Dynamics 365 Supply Chain Management können Einkäufer Kataloge erstellen und verwalten, die Unternehmensmitarbeiter beim Bestellen von Artikeln und Dienstleistungen für den internen Gebrauch verwenden können. Beim Erstellen eines Beschaffungskatalogs können Sie die Artikel und Dienstleistungen hinzufügen, die für Mitarbeiter verfügbar sein sollen, indem Sie entweder die Lieferantenkatalogdaten importieren oder die Lieferantenkatalogdaten manuell dem Produktmaster hinzufügen. 

Sie können Katalogdaten hochladen, die von einem Kreditor vom Kunden Microsoft Dynamics 365 übermittelt werden.

Die Produktdaten, die der Lieferant in Form einer Anforderungsdatei für die Katalogverwaltung (CMR-Datei) übermittelt, müssen im XML-Dateiformat vorliegen. Die CMR-Datei sollte alle Details der Produkte enthalten, die der Lieferant für Ihr Unternehmen liefern kann.

## <a name="import-vendor-catalog-data"></a>Importieren von Lieferantenkatalogdaten

Führen Sie zum Importieren der Lieferantenkatalogdaten die folgenden Aufgaben aus:

1.  Richten Sie ein Projekt im Datenverwaltungsarbeitsbereich ein, in dem Sie die Datenenzuordnungsregeln definiert haben. Wählen Sie **Datenverwaltung** und **Einstellungsrollen für Datenprojekte** aus. 

2.  Richten Sie eine Beschaffungskategoriehierarchie ein, und weisen Sie den Beschaffungskategorien Lieferanten zu. Wenn Sie Warencodes verwenden, fügen Sie die Warencodes den Beschaffungskategorien hinzu. Informationen zum Einrichten einer Beschaffungskategoriehierarchie finden Sie unter [Einrichten einer Beschaffungskategoriehierarchie](../procurement/tasks/set-up-procurement-category-hierarchy.md)

3.  Konfigurieren Sie den Lieferanten für den Katalogimport. Wählen Sie einen Kreditor aus, und wählen Sie anschließend **Beschaffung** > **Einstellungen** > **Kreditor für Katalogimport konfigurieren** aus.

4.  Konfigurieren Sie den Workflow für den Katalogimport. Erstellen Sie eine CMR-Dateivorlage und geben Sie diese mit dem Kreditor frei.

5.  Wählen Sie **Beschaffung** \> **Gemeinsam** \> **Kataloge** \> **Lieferantenkataloge**, um einen Lieferantenkatalog zu erstellen. In diesem Katalog werden die Anforderungsdateien für die Katalogverwaltung (CMR-Dateien) gruppiert, die Sie von Ihrem Lieferanten erhalten. 

6.  Laden Sie die CMR-Datei hoch.

7.  Prüfen Sie die Produkte im Lieferantenkatalog, um sie entweder zu genehmigen oder abzulehnen. Die Produkte werden automatisch den Beschaffungskategorien zugeordnet. 
    
Genehmigte Produkte werden dem Produktmaster hinzugefügt und für die ausgewählten juristischen Personen freigegeben. Nur genehmigte Produkte können dem Beschaffungskatalog hinzugefügt werden.

## <a name="generate-a-catalog-import-file-template"></a>Generieren einer Katalogimport-Dateivorlage

Bei der Katalogimport-Dateivorlage handelt es sich um eine XSD-Datei, mit der eine CMR-Datei für Lieferantenprodukte erstellt werden kann. Mithilfe der erstellten CMR-Datei können Sie einen neuen Katalog erstellen, einen vorhandenen Katalog ersetzen oder einen vorhandenen Katalog ändern.

1.  Wählen Sie **Beschaffung** \> **Kataloge** \> **Lieferantenkataloge** aus und doppelklicken Sie auf den Katalog, den Sie verwenden möchten.

2.  Laden Sie eine aktuelle Katalogimportvorlage herunter (XSD-Datei). Auf der Seite **Katalog aktualisieren** auf **Aktivitätsbereich**, auf der Registerkarte **Kataloge** in der Gruppe **Zugehörige Informationen**, **Katalogvorlage generieren**, und wählen Sie **Beschaffungskategorie** aus.

    -   Mit der **Beschaffungskatalog**-Option können Sie eine Katalogvorlage mit den Beschaffungskategorien, in denen der Lieferant zum Liefern von Produkten autorisiert ist erstellen.

3. Wählen Sie im Dialogfeld **Speichern unter** den Ort aus, an dem die Katalogdateivorlage gespeichert werden soll, und speichern Sie sie.

Weitere Informationen und Beispiele finden Sie in diesem Blogbeitrag: [Kreditorenkataloge in Dynamics AX.](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)
