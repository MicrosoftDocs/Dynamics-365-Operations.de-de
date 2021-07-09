---
title: Ausgewählte Formelnummer ist nicht für einen Batch-Auftrag genehmigt
description: Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie eine Fehlermeldung, die besagt, dass die ausgewählte Formelnummer nicht für einen Batch-Auftrag genehmigt ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294079"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Ausgewählte Formelnummer ist nicht für einen Batch-Auftrag genehmigt

Fehlercode: PRO2614

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie die folgende Fehlermeldung:

> Die ausgewählte Formelnummer ist nicht für einen Chargenauftrag genehmigt.

## <a name="cause"></a>Ursache

Das System validiert den Vorgang der Fixierung, um sicherzustellen, dass eine genehmigte Formel für das aktive Element verfügbar ist. Wahrscheinlich müssen Sie die Formel genehmigen.

## <a name="resolution"></a>Lösung

Führen Sie die folgenden Schritte aus, um eine Formel zu genehmigen.

1. Gehen Sie zu **Produktinformationsmanagement \> Stücklisten und Formeln \> Formeln**.
1. Wählen Sie die entsprechende Formel aus.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Formel** in der Gruppe **Bearbeiten** die Option **Formel genehmigen**.
1. Wählen Sie im Dialogfeld **Stückliste oder Formel genehmigen** einen Genehmigenden aus und wählen Sie dann **OK**.
