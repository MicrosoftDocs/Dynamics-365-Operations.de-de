---
title: Standort- und Parteibeziehungstypen hinzufügen
description: In diesem Thema wird erläutert, wie Sie neue Standort- und Parteibeziehungstypen hinzufügen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 543784e8072f88c10f63e1b44921b9f2d37308c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549697"
---
# <a name="add-location-roles-and-party-relationship-types"></a>Neue Standortrollen und Parteibeziehungstypen hinzufügen 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Lagerplatzrollen hinzufügen

Es gibt zwei Möglichkeiten, neue Standortrollen für Adress- und Kontaktinformationen hinzuzufügen:

-  Fügen Sie es über die Seite **Adresse und Kontaktinformationen** hinzu. Die neue Rolle wird in der Tabelle **LogisticsLocationRole** mit Typ = 0 gespeichert, was bedeutet, dass die Rolle keine Systemrolle ist, die in der **LogisticsLocationRoleType** Enumeration und ihren Erweiterungen definiert ist. Ein Benutzer kann diese Rolle bei der Erstellung von Adress- oder Kontaktinformationen verwenden.

    ![Zweck der Adress- und Inhaltsinformationen](media/Address-Contact.PNG)

-  Fügen Sie diese der Enumerationserweiterung **LogisticsLocationRoleType** hinzu und lassen Sie es über den Datenbanksynchronisierungsprozess auffüllen.

    1.  Erstellen Sie eine Erweiterung zur **LogisticsLocationRoleType** Enumeration und fügen Sie dann die neue Rolle der Erweiterung hinzu. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Erstellen Sie eine neue Ressourcendatei für die neue Rolle und weisen Sie anschließend einen Wert für deren Eigenschaften zu.
     
     ![Neue Ressourcendatei](media/Resource.PNG)
        
    3.  Erstellen Sie eine Datenenauffüllungsklasse und stellen Sie eine Handlermethode zur Verfügung, um die neue Rolle zu füllen. 

        ![Datenauffüllung](media/Dirdata.PNG)

    4.  Um das Auffüllen der neuen Standortrolle zu testen, können Sie eine lauffähige Klasse erstellen und DirDataPopulation::insertLogisticsLocationRoles() in Main() aufrufen. Nachdem dieser Vorgang abgeschlossen ist, sollten Sie die neue Rolle in der Tabelle **LogisticsLocationRole** mit dem Typ \> 0 sehen. Die neue Rolle wird auf der Seite **Adresse und Kontaktinformationen** angezeigt.

        ![Neuen Standort einfügen](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Neue Parteibeziehungstypen hinzufügen 

Es gibt zwei Möglichkeiten, einen neuen Beziehungstyp hinzuzufügen:

-   Fügen Sie sie über die Seite **Beziehungstypen** hinzu. Die neue Beziehung wird unter **DirRelationshipTypeTable** mit systemtype = 0 gespeichert.

    ![Beziehungstypen](media/Relationship.PNG)

-  Fügen Sie diese der Erweiterung der **DirSystemRelationshipType** Enumeration hinzu und lassen Sie es über den Datenbanksynchronisierungsprozess auffüllen.

    1.  Erstellen Sie eine Erweiterung zur **DirSystemRelationshipType** Enumeration und fügen Sie den neuen Beziehungstyp hinzu.

    2. Legen Sie einen Initialisierer für diesen neuen Typ an. Sie finden mehrere Beispiele im Kerncode, eines davon ist  **DirRelationshipTypeChildInitialize**. Dies ist eine Initialisierungsklasse für den Parteienbeziehungstyp "Child". Sie können mit Ihrem Initializer beginnen, indem Sie diesen Code kopieren und einfügen und dann die markierten Bereiche aktualisieren.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Um das Auffüllen des neuen Beziehungstyps zu testen, können Sie eine lauffähige Klasse erstellen und DirDataPopulation::insertDirRelationshipTypes() in Main() aufrufen. Sie sollten den neuen Beziehungstyp in der **DirRelationshipTypeTable** sehen, und der neue Beziehungstyp wird auf der Seite **Beziehungstypen** verfügbar sein.

        ![Ausführbare Klasse](media/Runnable.PNG)
