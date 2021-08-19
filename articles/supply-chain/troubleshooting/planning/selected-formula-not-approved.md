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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712909"
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
