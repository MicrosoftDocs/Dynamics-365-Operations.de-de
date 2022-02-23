---
title: Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft
description: Dieses Thema beschreibt die Auftragserstellung per Einzelzulauf für Geschäftbuchungen in Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 79f99b9b401de3e3bcca6ec5a13a3b4f7bad6f8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459103"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft

[!include [banner](includes/banner.md)]

In den Versionen Dynamics 365 Retail 10.0.4 und früher ist die Buchung der Aufstellungen ein Vorgang, der am Tagesende durchgeführt wird. Alle Transaktionen werden am Ende des Tages in den Büchern gebucht. Große Transaktionen müssen dann in einem begrenzten Zeitfenster verarbeitet werden, was manchmal zu Lade- und Sperrproblemen und Fehlern bei der Buchung von Aufstellungen führt. Einzelhändler können so außerdem nicht den ganzen Tag über Einnahmen und Zahlungen in ihren Büchern erfassen.

Mit der in Retail-Version 10.0.5 eingeführten Auftragserstellung per Einzelzulauf werden Transaktionen den ganzen Tag über bearbeitet. Am Ende des Tages werden nur eine Abstimmung der Zahlungsmittel und andere Bargeldverwaltungstransaktionen durchgeführt. Diese Funktionalität verteilt den Aufwand für die Erstellung von Aufträgen, Rechnungen und Zahlungen auf den gesamten Tag und sorgt so für eine bessere Leistung und die Möglichkeit, Umsätze und Zahlungen in den Büchern nahezu in Echtzeit zu verbuchen. 


## <a name="how-to-use-trickle-feed-based-posting"></a>So arbeiten Sie mit der Einzelzulaufbuchung
  
1. Um die Buchung auf Basis von Einzelzuläufen für Einzelhandelstransaktionen zu aktivieren, aktivieren Sie die Funktion **Einzelhandelsaufstellungen – Einzelzulauf** mit der Funktionsverwaltung.

    > [!IMPORTANT]
    > Bevor Sie diese Funktion aktivieren, stellen Sie sicher, dass keine ausstehenden Anweisungen zur Veröffentlichung anstehen.

2. Das aktuelle Anweisungsdokument wird in zwei Typen unterteilt: Transaktionsaufstellung und Finanzaufstellung.

      - Die Transaktionsaufstellung erfasst alle nicht gebuchten und geprüften Transaktionen und erstellten Aufträge, Verkaufsrechnungen, Zahlungs‑ und Rabatterfassungen sowie die Einnahmen‑ und Ausgabentransaktionen in der von Ihnen konfigurierten Kadenz. Sie sollten diesen Prozess so konfigurieren, dass er sehr häufig ausgeführt wird, sodass Dokumente erstellt werden, wenn die Einzelhandelstransaktionen über den P-Job in die Zentralverwaltung hochgeladen werden. Mit der Transaktionsaufstellung, die bereits Aufträge und Verkaufsrechnungen erstellt, ist es nicht wirklich notwendig, den Batchauftrag **Lager buchen** zu konfigurieren. Sie können ihn jedoch weiterhin verwenden, um möglicherweise vorhandene geschäftliche Anforderungen zu erfüllen.  
      
     - Die Finanzaufstellung ist für die Erstellung am Ende des Tages ausgelegt und unterstützt nur die Abschlussmethode **Schicht**. Diese Aufstellung beschränkt sich auf die finanzielle Abstimmung und erstellt nur die Erfassungen zu den Differenzbeträgen zwischen gezähltem Betrag und Transaktionsbetrag für die verschiedenen Zahlungsmittel sowie Erfassungen zu anderen Bargeldverwaltungstransaktionen.   

3. Um die Transaktionsaufstellung zu berechnen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Transaktionsaufstellungen stapelweise berechnen**. Um die Transaktionsaufstellungen stapelweise zu buchen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Transaktionsaufstellungen stapelweise buchen**.

4. Um die Finanzaufstellung zu berechnen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Finanzaufstellungen stapelweise berechnen**. Um die Finanzaufstellungen stapelweise zu buchen, gehen Sie zu **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Finanzaufstellungen stapelweise buchen**.

> [!NOTE]
> Die Menüpunkte **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Aufstellungen stapelweise berechnen** und **Retail und Commerce > Retail und Commerce IT > POS-Buchung > Aufstellungen stapelweise buchen** werden mit dieser neuen Funktion entfernt.

Alternativ können Transaktions- und Finanzaufstellungen manuell angelegt werden. Wechseln Sie zu **Retail und Commerce > Kanäle > Shops**, und klicken Sie auf **Aufstellungen**. Klicken Sie auf **Neu**, und wählen Sie dann den Typ der Aufstellung aus, die Sie erstellen möchten. Felder auf der Seite **Aufstellungen** und Aktionen unter der Gruppe **Aufstellung** auf der Seite zeigen relevante Daten und Aktionen basierend auf dem ausgewählten Aufstellungstyp an.
