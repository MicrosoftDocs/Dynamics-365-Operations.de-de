---
title: Erstellen eines Callcenterkatalogs
description: "Dieser Artikel bietet einen Überblick über den Prozess zum Erstellen eines Katalogs für ein Callcenter."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 94ff6d74d4a11b3b04be6b69f85e778c3b45de92
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-call-center-catalog"></a>Erstellen eines Callcenterkatalogs

[!include[banner](includes/banner.md)]


Dieser Artikel bietet einen Überblick über den Prozess zum Erstellen eines Katalogs für ein Callcenter. 

In einem Callcenter können Sie Einzelhandelsproduktkataloge verwenden, um die Produkte zu identifizieren, die Sie Kunden anbieten möchten. Callcenter verwenden in der Regel gedruckte Kataloge. Der Entwurf und die Produktion eines gedruckten Katalogs wird außerhalb von Microsoft Dynamics 365 for Retail behandelt. Sie können jedoch ein digitales Formular eines Katalogs erstellen und speichern, indem Sie die gleichen Formulare verwenden, die Sie verwenden, um Online-Einzelhandelskataloge einzurichten. Bevor Sie einen Katalog erstellen können, müssen Sie Sortimente einrichten und die Sortimente einem Callcenter zuweisen. Anschließend fügen Sie Produkte dem Katalog hinzu, indem Sie Produkte aus diesen Sortiment auswählen. Nachdem Produkte dem Katalog hinzugefügt wurden und der Katalog abgeschlossen ist, müssen Sie den Katalog überprüfen, ob die Daten zu überprüfen. Übermitteln Sie dann den Katalog zur Prüfung und Genehmigung. Nachdem der Katalog genehmigt wurde, kann er veröffentlicht werden. Wenn ein Callcenterkatalog erstellt wird, können Sie eine Momentaufnahme der Katalogdaten zum Zeitpunkt erstellen, an dem der Katalog veröffentlicht wird. Mit dieser Momentaufnahmefunktionen können Sie auf eine bestimmte Version des Katalogs zugreifen, auch wenn der Katalog später geändert und aktualisiert wird. Callcenterkataloge können auch eingerichtet werden, um die folgenden optionalen Funktionen einzubeziehen.

-   **Quellcodes** – Codes, die verwendet werden, um die Debitorenreaktion auf bestimmte Katalogmailings zu verfolgen.
-   **Kostenlose Produkte** - Produkte, die in einem Kundenauftrag ohne zusätzliche Gebühr enthalten sind. Diese Produkte werden dem Auftrag automatisch hinzugefügt, wenn der Quellcode für den Katalog in den Auftrag eingegeben wird.
-   **Skripts** - Texte, die eine Callcenterarbeitskraft einem Debitor vorliest, wenn ein Auftrag erstellt wird. Skripts können Grüße oder Einkaufvorschläge enthalten.
-   **Regeln für weiteren Verkauf/ergänzenden Verkauf** - Artikel, die als Vorschlag angezeigt werden, wenn ein bestimmtes Produkt in den Auftrag hinzugefügt wird.

Diese Optionen müssen eingerichtet werden, bevor der Katalog genehmigt und veröffentlicht wird.

## <a name="prerequisites"></a>Erforderliche Komponenten
Schließen Sie folgenden Prozeduren ab, bevor Sie starten:

-   Produkte und Produktsortimente einrichten:.
-   Einrichten von Einzelhandelsprodukten.
-   Einrichten eines Sortiments.
-   Ein Callcenter erstellen.
-   Einrichten eines Callcenters.
-   Hinzufügen des Callcenters zu einer Organisationshierarchie.
-   Erstellen oder Ändern einer Organisationshierarchie.

## <a name="create-a-catalog"></a>Einen Katalog erstellen
Sie müssen zuerst einen Katalog erstellen, dem Katalog Produkte hinzufügen, und dann den Katalog überprüfen und die Attribute für die Produkte aktualisieren.

## <a name="validate-the-catalog"></a>Katalog überprüfen
Nachdem Sie den Katalog eingerichtet haben, müssen Sie ihn prüfen. Der Prüfprozess überprüft, ob die Daten, die für Kanalattribute und Produktattribute erforderlich sind, vollständig und gültig sind, und ob der Katalog veröffentlicht werden kann.

## <a name="submit-the-catalog-for-review-and-approval"></a>Beschaffungskatalog zur Prüfung und Genehmigung übermitteln
Nachdem ein Katalog validiert ist, können Sie den Katalog zur Prüfung und Genehmigung übermitteln. Ein Katalog muss genehmigt werden, bevor er veröffentlicht werden kann. Sie können einen Workflow konfigurieren, damit Kataloge entweder automatisch genehmigt werden oder manuelle Genehmigung erforderlich ist.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Optional: Quellcodes, kostenlose Produkte und Skripts hinzufügen
Sie können außerdem die folgenden Elemente zu einem Callcenterkatalog hinzufügen. Diese Elemente sind optional.

-   **Quellcodes** können von Unternehmen gedruckt werden, die gedruckte Kataloge produzieren, um die Debitorenantwort auf bestimmte Katalogen zu verfolgen. Quellcodes werden häufig auf der Rückseite eines Katalogs gedruckt und in den Auftrag eingegeben, wenn ein Debitor einen Einkauf tätigt. Um einen Quellcode dem Katalog hinzufügen, müssen Sie einen Zielmarkt zuerst schaffen. Der Zielmarkt wird normalerweise einer eigenen oder ausgelehnten Mailingliste zugeordnet.
-   **Kostenlose Produkte** sind Werbeartikel, die kostenlos im Auftrag eines Debitors enthalten sind, wenn auf den Katalog verwiesen wird.
-   **Skripte** können verwendet werden, um die Interaktionen der Arbeitskraft mit den Debitoren im Kontext eines Katalogs oder eines Produkts innerhalb eines Katalogs zu verwalten.

## <a name="publish-the-catalog"></a>Veröffentlichen des Katalogs
Wenn Sie einen Katalog für ein Callcenter veröffentlichen, können Sie die Produktdaten im Katalog abschließen. Die Veröffentlichung gibt außerdem an, dass der Katalog für alle weitere Aktivitäten, die Sie ausführen möchten, bereit ist. So können Sie beispielsweise einen gedruckten Katalog erstellen. Sie können Ihre Kataloge manuell veröffentlichen, oder Sie können einen Stapelverarbeitungsvorgang verwenden, um nach einem Zeitplan zu veröffentlichen. Bevor Sie einen Katalog veröffentlicht können, muss der Katalog überprüft und genehmigt werden. Um den Katalog ändern, nachdem er veröffentlicht ist, können Sie den Katalog zurückziehen und ihn anschließend erneut veröffentlichen.




