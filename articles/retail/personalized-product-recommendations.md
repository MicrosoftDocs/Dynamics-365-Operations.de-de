---
title: Personalisierte Produktempfehlungen
description: "Dieses Thema enthält Informationen zu Dynamics 365 for Retail-Produktempfehlungen, die im Feld Verkaufsstelle (POS)- Gerät angezeigt werden können."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 7925a37c595f5ffa040747462d3ea60a3da41858
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2018

---

# <a name="personalized-product-recommendations"></a>Personalisierte Produktempfehlungen

[!include [banner](includes/banner.md)]

> [!NOTE]
> Wir entfernen die aktuelle Version des Produktempfehlungs-Service, da wir für diese Funktion einen besseren Algorithmus und neuere Einzelhandels-ausgerichtete Funktionen neu entwerfen. Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen](../dev-itpro/migration-upgrade/deprecated-features.md) 

In Dynamics 365 for Retail können Produktempfehlungen auf dem POS-Gerät angezeigt werden. Empfehlungen sind Artikel, die Ihre Kunden möglicherweise interessieren und zwar auf Basis der ihrer Einkaufshistorie, Artikel auf einem Wunschzettel und Artikel, die andere Kunden online und in der physische Filiale gekauft haben. Für Einzelhändler mit großen Katalogen, helfen Empfehlungen den Kunden bei der Produkterfassung. Indem Produkte zur Schau gestellt werden, die sich an den Interessen und Kaufgewohnheiten eines Kunden orientieren, erhalten Einzelhändler Upsell-Möglichkeiten und die Kundenbindung wird gestärkt. In Dynamics 365 for Retail werden Produktempfehlungen von kognitiven Diensten und Microsoft Azure Machine Learning unterstützt.


<a name="scenarios"></a>Szenarien
---------

Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert. Sie sind in Cloud POS oder Modern POS (MPOS) verfügbar.

1.  Auf der **Produktdetails** Seite:

-   Wenn ein Shopmitarbeiter eine **Produktdetails** Seite besucht, wenn er auf die vorherigen Buchungen über verschiedene Kanälen schaut, schlägt das Empfehlungsmodul zusätzliche Artikel vor, die wahrscheinlich zusammen eingekauft werden.
-   Falls der Shopmitarbeiter einen Kunden der Buchung hinzufügt und dann eine **Produktdetails** Seite besucht, stellt das Empfehlungsmodul personalisierte Empfehlungen mithilfe der Buchungshistorie des Kunden zur Verfügung.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Auf der **Transaktionen** Seite:

-   Das Empfehlungsmodul schlägt Artikel auf Basis der gesamten Liste von Artikeln im Warenkorb vor.
-   Falls der Shopmitarbeiter einen Kunden der Buchung hinzufügt stellt das Empfehlungsmodul personalisierte Empfehlungen mithilfe der Buchungshistorie des Kunden und des Warenkorbs zur Verfügung.

> [!NOTE]
> Zum Anzeigen von Empfehlungen auf der Seite **Buchung** muss der Einzelhändler das Bildschirmlayout in Dynamics 365 for Retail aktualisieren. Das Steuerelement **Empfehlungen** muss auf der Seite **Buchung** abgelegt werden. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Auf der **Kundendetails** Seite:
    -   Das Empfehlungsmodul schlägt Artikel auf Basis der Benutzerkennung und von Artikeln in der Wunschliste vor.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Konfigurieren von Dynamics 365 for Retail zum Aktivieren von POS-Empfehlungen
Um Produktempfehlungen einzurichten, muss Folgendes eingerichtet werden:

1.  Überprüfen Sie, ob Sie die richtige **Juristische Person** ausgewählt haben.
2.  Navigieren Sie zu **Entitätsshop** auf **Retail-Verkauf**, und klicken Sie dann **Aktualisieren**. Dies verwendet die Demodaten (oder Ihre Daten) aus der betrieblichen Datenbank und verschieben sie in den Entitätsspeicher.
3.  Optional: Um Empfehlungen zum Buchungsbildschirm anzuzeigen, navigieren Sie zu **Bildschirmlayout**, wählen das Bildschirmlayout, starten den **Bildschirmlayoutdesigner** und dann legen das **Empfehlungssteuerelement** ab.

4.  Wechseln Sie **Einzelhandelsparameter**, wählen Sie **Machine-Llearning** aus, wählen Sie die Option **Ja** unter **POS-Empfehlungen aktivieren** aus.
5.  Weitere Empfehlungen zu POS erhalten Sie mit dem Konfigurationseinzelvorgang **1110**. Um Änderungen widerzuspiegeln der im POS-Designer durchgeführt wurden, aktivieren Sie Kanalkonfigurationseinzelvorgang **1070**.

## <a name="how-does-it-work"></a>Wie funktioniert das?
Wenn Sie die **Entitätsspeicher** Entität aktualisieren, finden folgenden Aktionen statt.

-   Daten in dem von den kognitiven Diensten erforderlichem Format werden aus der operationalen Datenbank von Dynamics 365 for Retail extrahiert und an den Entitäts-Store gesendet.
-   Die Daten werden von Azure Data Factory (ADF) verwendet, um die Daten mithilfe der Hive-Skripte als Teil der ADF-Aktivitäten bereinigen. Bereinigte Daten werden im Blob gespeichert.
-   Daten vom Blob-Speicher werden von den Cognitive-Services-API verwendet, um ein Empfehlungsmodell zu schulen.

Wenn Sie **Empfehlungen aktivieren** aktivieren und die Konfigurationseinzelvorgänge aktivieren, werden folgenden Aktionen ausgeführt.

-   Anmeldeinformationen und ID für das Modell werden der API entnommen und in der operationalen Datenbank von Dynamics 365 for Retail, in der web.config für AOS und auch auf dem Retail-Server gespeichert.
-   Model-Anmeldeinformationen und - kennung werden für CRT bereitgestellt, so dass Anforderungen für Produktempfehlungen aus Cloud POS und MPOS im onlinemodus durchgeführt werden können.

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Beheben Sie Probleme, wo Sie Produktempfehlungen bereits aktiviert haben 
> - Navigieren Sie zu **Einzelhandelsparameter** > **Lernfähigkeit einer Maschine** > **Produktempfehlungen sperren** und führen Sie **Globaler Konfigurationsjob aus**. Wenn Sie nicht in der Lage sind, die Registerkarte **Lernfähigkeit einer Maschine** zu suchen, wenden Sie sich bitte an den Dynamics Support. 
> 
> - Wenn Sie die**Empfehlungssteuerung** Ihrem Buchungsbildschirm mithilfe von **Designer für Bildschirmlayout** hinzugefügt haben, entfernen Sie diese auch. 



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät](add-recommendations-control-pos-screen.md)




