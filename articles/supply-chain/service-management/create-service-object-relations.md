---
title: Erstellen von Serviceobjektbeziehungen
description: In diesem Thema wird beschrieben, wie Serviceobjektbeziehungen für eine Servicevereinbarung und einen Serviceauftrag erstellt werden.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 380514b6e95292597d3eb52ce191d1e282e154ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965904"
---
# <a name="create-service-object-relations"></a>Erstellen von Serviceobjektbeziehungen 

[!include [banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie Serviceobjektbeziehungen für eine Servicevereinbarung und einen Serviceauftrag erstellt werden. Durch Erstellen einer Serviceobjektbeziehung wird das Serviceobjekt einer Servicevereinbarung oder einem Serviceauftrag zugeordnet. Wenn ein Debitor einen Service für einen Artikel anfordert, der ein Serviceobjekt ist, können Sie das Serviceobjekt aus der Liste der Serviceobjektbeziehungen auswählen.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Erstellen einer Serviceobjektbeziehung für einen Servicevertrag

Gehen Sie folgendermaßen vor, um eine Serviceobjektbeziehung für einen Servicevertrag zu erstellen:

1.  Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.

2.  Wählen Sie in der Liste **Serviceverträge** eine vorhandene Servicevereinbarung aus, oder klicken Sie auf **Neu**, um einen neuen Servicevertrag zu erstellen.

3.  Klicken Sie im **Serviceverträge**-Formular im **Aktivitätsbereich** auf der Registerkarte **Servicevereinbarung** in der Gruppe **Referenzen** auf **Serviceobjekte**.

4.  Klicken Sie im Formular **Serviceobjekte** auf **Neu**, und wählen Sie anschließend ein Serviceobjekt für diese Servicevereinbarung aus.

5.  Klicken Sie auf **Funktionen**, um dem Servicevertrag eine Stückliste zuzuweisen, und wählen Sie dann **Vorlagenstücklisten anfügen** aus. Wählen Sie im Formular **Vorlagenstückliste auswählen** im Feld **Vorlagenstückliste** eine Vorlagenstückliste aus. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Erstellen einer Serviceobjektbeziehung für einen Serviceauftrag

Gehen Sie folgendermaßen vor, um eine Serviceobjektbeziehung für einen Serviceauftrag zu erstellen:

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Wählen Sie in der Liste **Serviceaufträge** einen vorhandenen Serviceauftrag aus, oder erstellen Sie einen neuen.

3.  Klicken Sie im **Serviceaufträge**-Formular im **Aktivitätsbereich** auf der Registerkarte **Serviceaufträge** in der Gruppe **Referenzen** auf **Serviceobjekte**.

4.  Klicken Sie im Formular **Serviceobjekte** auf **Neu**, und wählen Sie anschließend ein Serviceobjekt für diese Serviceaufträge aus.

5.  Klicken Sie auf **Funktionen**, um dem Servicevertrag eine Stückliste zuzuweisen, und wählen Sie dann **Vorlagenstücklisten anfügen** aus. Wählen Sie im Formular **Vorlagenstückliste auswählen** im Feld **Vorlagenstückliste** eine Vorlagenstückliste aus. 


## <a name="see-also"></a>Siehe auch

[Serviceobjekte – Übersicht](service-objects.md)

[Serviceobjektbeziehungen](service-object-relations.md)

[Vorlagenstücklisten](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]