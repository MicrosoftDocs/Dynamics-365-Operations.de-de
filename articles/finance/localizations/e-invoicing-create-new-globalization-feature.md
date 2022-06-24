---
title: Erstellen Sie eine Globalisierungsfunktion
description: In diesem Artikel wird erklärt, wie Sie eine Funktion zur Globalisierung erstellen.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c622b350f79d36b8fda12598ceae57ee9c7095e9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889829"
---
# <a name="create-a-globalization-feature"></a>Erstellen Sie eine Globalisierungsfunktion

[!include [banner](../includes/banner.md)]

Sie können eine Funktion für die Elektronische Rechnungsstellung von Grund auf erstellen oder sie auf eine bereits vorhandene Funktion stützen. Wenn Sie eine Funktion von Grund auf erstellen, müssen Sie Konfigurationen für das elektronische Berichtswesen (ER) und andere Komponenten, wie z.B. die Einrichtung der Funktion und die Details der Anwendungseinrichtung, manuell hinzufügen. Wenn Sie eine Funktion erstellen, die auf einer bestehenden Funktion basiert, erbt die neue Funktion alle Konfigurationen und Parameter der Basisfunktion. Sie können überprüfen, was von der Basisfunktion in die neue Funktion kopiert wird.

## <a name="create-a-feature-from-scratch"></a>Erstellen Sie eine Funktion von Grund auf

In diesem Abschnitt wird erläutert, wie Sie eine Funktion für die Elektronische Rechnungsstellung erstellen, wenn im Global Repository keine Globalisierungsfunktion für Ihre Geschäftsszenarien standardmäßig verfügbar ist.

Um eine Funktion zur elektronischen Rechnungsstellung zu erstellen, befolgen Sie diese Schritte.

1. Melden Sie sich bei Ihrem RCS-Konto (Regulatory Configuration Service) an.
2. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie **Hinzufügen** und wählen Sie dann in der Dropdown-Dialogbox die Option **Neue Funktion**.
4. Geben Sie einen Namen und eine Beschreibung für die Funktion der elektronischen Rechnungsstellung ein.
5. Wählen Sie **Funktion erstellen**. Die erste Version der neuen Funktion erscheint rechts auf der Seite und hat den Status **Entwurf**.

    Als nächstes müssen Sie ER-Konfigurationen und Funktionen einrichten. Bevor Sie neue oder bestehende ER-Formatkonfigurationen hinzufügen, vergewissern Sie sich, dass sie in Ihrem lokalen RCS-Repository vorhanden sind.

6. Wählen Sie die Funktion für die Elektronische Rechnungsstellung, an der Sie gerade arbeiten.
7. Wählen Sie auf der Registerkarte **Konfigurationen** **Hinzufügen** aus.
8. Suchen Sie im Raster **Konfigurationen** nach den Formatkonfigurationen, die für die Pipeline zur Verarbeitung benötigt werden (z.B. um elektronische Rechnungsdateien zu generieren oder Antworten von externen Webdiensten zu verarbeiten), und wählen Sie diese aus.
9. Wählen Sie **OK** aus. Sie können die Konfigurationen jetzt in Aktionen der Verarbeitungs Pipeline verwenden. Weitere Informationen finden Sie unter [Arbeiten mit Konfigurationen](e-invoicing-work-configurations.md).
10. Um eine Einrichtung für die Funktion Elektronische Rechnungsstellung hinzuzufügen, erstellen Sie sie auf der Registerkarte **Einrichtungen** der Seite **Neue Funktion**. Weitere Informationen finden Sie unter [Arbeiten mit Funktionen](e-invoicing-feature-setup.md).
11. Schließen Sie die Einrichtung ab und stellen Sie die Funktion für die elektronische Rechnungsstellung in der Umgebung bereit. Weitere Informationen finden Sie unter [Eine Funktion zur Globalisierung vervollständigen, veröffentlichen und bereitstellen](e-invoicing-complete-publish-deploy-globalization-feature.md).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Erstellen Sie Dateiformatkonfigurationen, die von dem bestehenden Rechnungsmodell abgeleitet sind

Sie können diesen Abschnitt überspringen, wenn Sie keine ER-Konfigurationen erstellen müssen, sondern vorhandene Versionen als Basis verwenden können.

Diese Vorgehensweise zeigt Ihnen, wie Sie die Dateiformatkonfigurationen erstellen, die für die neue Funktion der Elektronischen Rechnungsstellung, die Sie erstellen möchten, erforderlich sind. Erstellen Sie die Dateiformatkonfiguration für elektronische Rechnungen und alle anderen Dateiformatkonfigurationen, die Ihre neue Funktion für die elektronische Rechnungsstellung benötigt.

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Im Arbeitsbereich **Elektronische Berichterstellung** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Wählen Sie das **Rechnungsmodell** oder, für brasilianische Szenarien, das **Fiskalmodell**.
4. Wählen Sie **Konfiguration erstellen**, und wählen Sie dann im Dropdown-Dialogfeld die Option **Format basierend auf Datenmodell Rechnung**.
5. Geben Sie einen Namen sowie die Beschreibung für die Formatkonfiguration ein.
6. Wählen Sie im Feld **Formattyp** den Dateierweiterungstyp aus.
7. Wählen Sie im Feld **Datenmodelldefinition** die Stammstruktur, der Sie Ihr Format zuordnen möchten. Zum Beispiel wird **InvoiceCustomer** für die Kundenrechnungsformate verwendet.
8. Wählen Sie **Konfiguration erstellen**.
9. Wählen Sie die neue Formatkonfiguration.
10. Wählen Sie **Designer** aus und verwenden Sie das Formatdesigner-Tool, um das Dateilayout so zu konfigurieren, dass es den Dateiformatspezifikationen entspricht.
11. Schließen Sie die Seite.
12. Wählen Sie in der Registerkarte **Versionen** die **Status ändern** \> **Abschließen** aus.
13. Wählen Sie **Status ändern** \> **Teilen** aus, um die Formatkonfiguration im globalen Repository zu veröffentlichen.

Die neuen Dateiformatkonfigurationen müssen für die Microsoft Domäne freigegeben werden, bevor sie vom Dienst für die elektronische Rechnungsstellung verwendet werden können.

1. Wählen Sie die Formatkonfiguration aus, an der Sie arbeiten. Der Status der Konfiguration muss **Freigegeben** lauten.
2. Wählen Sie auf der Registerkarte **Versionen** **Erweitertes Teilen** \> **Globales Repository**.
3. Wählen Sie auf der Registerkarte **Geteilt mit** **Organisation** aus.
4. Geben Sie in das Feld **Parameter** **microsoft.com** ein, um die Formatkonfiguration mit der Microsoft Domäne zu teilen.
5. Wählen Sie **OK** aus.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Erstellen Sie eine Funktion, die auf einer bestehenden Funktion basiert

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
3. Vergewissern Sie sich im Feld **Konfigurationsanbieter**, dass Ihr aktiver Konfigurationsanbieter ausgewählt ist. Auf diese Weise erscheint die neue Funktion für die Elektronische Rechnungsstellung in der Liste, nachdem sie erstellt wurde. Wenn Ihr aktiver Konfigurationsanbieter nicht ausgewählt ist, wird die neue Funktion aus der Liste herausgefiltert.
4. Wählen Sie **Hinzufügen** und dann im Dropdown-Dialogfeld die Option **Basierend auf der vorhandenen Version** aus.
5. Geben Sie einen Namen und eine Beschreibung für die Funktion ein.
6. Wählen Sie im Feld **Basisfunktion** die Basisversion der Funktion.
7. Wählen Sie **Funktion erstellen**. Die Funktion wird erstellt und hat den Status **Entwurf**.
8. Überprüfen Sie die Funktionskomponenten, um festzustellen, ob Aktualisierungen erforderlich sind:

    - Überprüfen Sie die Konfigurationen, falls Sie die ER-Formate und deren Bindung mit Formatzuordnungen für die Funktion Version anpassen müssen.
    - Überprüfen Sie die Einrichtung, falls Sie die Registerkarte **Aktionen**, **Anwendbarkeitsregeln** oder **Variablen** für die Funktion anpassen müssen.

9. Schließen Sie die Einrichtung ab und stellen Sie die Funktion für die elektronische Rechnungsstellung in der Umgebung bereit. Weitere Informationen finden Sie unter [Eine Funktion zur Globalisierung vervollständigen, veröffentlichen und bereitstellen](e-invoicing-complete-publish-deploy-globalization-feature.md).
