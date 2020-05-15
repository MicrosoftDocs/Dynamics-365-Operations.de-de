---
title: Bereinigung der EB-Migration
description: In diesem Thema wird erläutert, wie Sie die EB-Migrationsbereinigungsfunktion verwenden können, um Probleme mit EB-Vorlagen zu beheben.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 090badd48785dfacf5942426d0fe53629f3c0cda
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321801"
---
# <a name="er-migration-cleanup"></a>Bereinigung der EB-Migration 

[!include[banner](../includes/banner.md)]

Wenn Sie Ihre Finance-Instanzen verwalten, können Sie entscheiden, Ihre aktuelle Instanz zu einem anderen Speicherort zu migrieren. Sie können Ihre Produktionsinstanz beispielsweise zu einer neuen Sandboxumgebung migrieren. Wenn Sie das Elektronische Berichterstellungs-(EB)-Framework konfigurieren, um Vorlagen im Microsoft Azure BLOB-Speicher zu speichern, verweist die **DocuValue**-Tabelle in der neuen Sandboxumgebung auf die BLOB-Speicherinstanz in der Produktionsumgebung. Auf diese Instanz kann jedoch nicht über die Sandboxumgebung zugegriffen werden, da der Migrationsprozess die Migration von Artefakten im BLOB-Speicher nicht unterstützt. Es wird vielmehr erwartet, dass Sie in der neuen Sandbox-Umgebung auf die Instanz des BLOB-Speichers in der Sandbox-Umgebung verweisen, die noch keine EB-Vorlagen bezieht.

Wenn Sie versuchen, ein EB-Format auszuführen, das eine Vorlage zum Generieren von Geschäftsdokumenten verwendet, tritt eine Ausnahme auf, und Sie erhalten eine Benachrichtigung, dass die Vorlage fehlt. Sie erhalten auch eine Anleitung dazu, wie Sie die EB-Migrationsbereinungsoption verwenden, um die EB-Formatkonfiguration, die die Vorlage enthält, zu löschen und dann erneut zu importieren.

[![Ausführen eines EB-Formats](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Sie erhalten eine ähnliche Fehlermeldung, wenn Sie zur Seite **Konfigurationen** (**Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**) navigieren und in der Konfigurationsstruktur versuchen, eine EB-Formatkonfiguration zu löschen, die eine Vorlage verwendet.

[![Löschen eines EB-Formats](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Führen Sie die folgenden Schritte aus, um Probleme mit EB-Vorlagen zu beheben, auf die Sie nicht zugreifen können.

1.  Gehen Sie zur Seite **Organisationsverwaltung** \> **Periodisch** \> **Migrationsbereinigung**.
2.  Wählen Sie eine EB-Formatkonfiguration aus, die nicht ausgeführt oder gelöscht werden kann.
3.  Wählen Sei **Löschen**.
4.  Bestätigen Sie das Löschen der ausgewählten EB-Formatkonfiguration.
5.  [Importieren](download-electronic-reporting-configuration-lcs.md) Sie die gelöschte EB-Formatkonfiguration zur aktuellen Finance-Instanz.

## <a name="applicability"></a>Anwendbarkeit

> [Wichtig] Die Option **Migrationsbereinigung** ist nur das Ziel für EB-Formatkonfigurationen, die nicht zugängliche EB-Vorlagen enthalten. Wenn Sie eine EB-Formatkonfiguration mithilfe der Option **Migrationsbereinigung** löschen, löscht EB die Vorlagen, die sich auf die Konfigurationsartefakte in der einzigen Anwendungsdatenbank beziehen. Das Vorhandensein der entsprechenden physischen Dateien im Blob-Speicher wird nicht überprüft. Stattdessen wird angenommen, dass es keine gibt. Verwenden Sie daher nicht die Option **Migrationsbereinigung** als Alternative zur EB-Konfigurationslöschungsoption auf der Seite **Konfigurationen**. Verwenden Sie die Option **Migrationsbereinigung** nur, wenn die EB-Konfigurationslöschungsoption auf der Seite **Konfigurationen** fehlgeschlagen ist.
>
> Wenn Sie die Option **Migrationsbereinigung** verwenden, um eine EB-Formatkonfiguration zu löschen, wenn die bevorzugte Vorlage im Blob-Speicher verfügbar ist, können Sie zur zugehörige Konfigurationsartefakte in der Anwendungsdatenbank löschen. Die physische Datei der Vorlage im Blob-Speicher bleibt erhalten. Das Überschreiben von Dateien im Blob-Speicher ist nicht mehr zulässig. Weitere Informationen finden Sie unter [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Darüber hinaus können Sie die mithilfe der Migrationsbereinigung in dieser Umgebung gelöschten Konfigurationen nicht mehr erneut importieren. Um dieses Problem zu beheben, müssen Sie die entsprechende Datei im Blob-Speicher suchen und manuell löschen.

[![Importieren eines EB-Formats](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Ein ähnliches Problem kann auftreten, wenn Sie Ihre Anwendungsinstanz an einen anderen Speicherort migrieren, der mehrmals als Migrationsziel verwendet wurde und für den der Blob-Speicher bereits EB-Vorlagendateien enthält.

Dieser Vorgang kann zeitaufwändig sein, da Sie über mehrere EB-Formatkonfigurationen verfügen können. Daher ist die Verwendung der Funktion [Sicherungsspeicher von EB-Vorlagen](er-backup-storage-templates.md) zu bevorzugen, um Vorlagen mit fehlerhaften Verweisen automatisch wiederherzustellen.
