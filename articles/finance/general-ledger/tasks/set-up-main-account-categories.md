---
title: Hauptkontokategorien einrichten
description: In diesem Thema wird erläutert, wie Sie unter Dynamics 365 Finance die Hauptkontokategorien einrichten.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2dcaa27f20ca050d278aa378e90946b8cb40449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815115"
---
# <a name="set-up-main-account-categories"></a>Hauptkontokategorien einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie unter die Hauptkontokategorien einrichten. Hauptkontokategorien werden für die Standardberichte in der Finanzberichterstellung und in Power BI verwendet. Hauptkontokategorien, die standardmäßig erstellt werden, können umbenannt jedoch nicht gelöscht werden. Zusätzliche Kontokategorien können den erstellt und für Berichts- und Analysezwecke verwendet werden. Dieses Thema verwendet die USMF-Demofirma.

## <a name="create-a-main-account-category"></a>Erstellen einer Hauptkontokategorie
1. Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Kontenplan > Kontenplan > Konten > Hauptkontenkategorien**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Hauptkontokategorie** einen eindeutigen Namen ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung für die Hauptkontotypen ein.
5. Wählen Sie im Feld **Hauptkontoart** die Hauptkontoart aus, die mit der Kategorie verknüpft werden soll.

## <a name="link-main-accounts-to-account-category"></a>Verknüpfen von Hauptkonten mit Kontokategorien
1. Klicken Sie auf **Hauptkonten verlinken**.
2. Wählen Sie in der Liste die Hauptkonten aus, die der Hauptkontokategorie zugeordnet werden sollen, indem Sie die Kontrollkästchen in der Spalte **Verknüpft** markieren. Das Zuweisen von Hauptkonten zu einer Hauptkontokategorie fasst die Salden der Konten zusammen wenn diese Kategorie für die Finanzberichte und Analysen verwendet wird.  
3. Wählen oder deaktivieren Sie die Option **Verknüpft**, um die Hauptkonten auszuwählen.
4. Wählen Sie **OK**.
5. Wählen Sie **Ja** aus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]