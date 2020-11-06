---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: ed52eb21cfa5d192e4d7d0d79a2dc0847a5fd3ee
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570624"
---
# AzureRM. HDInsight-modul
## Problembeskrivning
Avsnitten i det här avsnittet innehåller Azure PowerShell-cmdlets för Microsoft Azure HDInsight i ramverket Azure Resource Manager (ARM). Dessa cmdletar används för att hantera HDInsight-kluster och de jobb som körs på dem. Det finns cmdlets i Microsoft. Azure. commands. HDInsight-namn området.

## Cmdlets för AzureRM. HDInsight
### [Add-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
Lägger till en kluster identitet till ett kluster konfigurations objekt.

### [Add-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
Lägger till en version för en tjänst som körs i ett kluster till ett kluster konfigurations objekt.

### [Add-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
Lägger till ett konfigurations värde för Hadoop-konfigurering och/eller en struktur för ett kluster konfigurations objekt.

### [Add-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Lägger till en SQL-databas som ska fungera som en registrerings-eller Oozie-metastore till ett kluster konfigurations objekt.

### [Add-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Lägger till en skript åtgärd i ett kluster konfigurations objekt.

### [Add-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Lägger till ett säkerhets-ett kluster konfigurations objekt.

### [Add-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Lägger till en Azure-lagringsenhet till ett kluster konfigurations objekt.

### [Disable-AzureRmHDInsightOperationsManagementSuite](Disable-AzureRmHDInsightOperationsManagementSuite.md)
Inaktiverar Operations Management Suite (OMS) i ett HDInsight-kluster och relevanta loggar slutar flöda till den OMS-arbetsyta som anges vid aktivering.

### [Enable-AzureRmHDInsightOperationsManagementSuite](Enable-AzureRmHDInsightOperationsManagementSuite.md)
Aktiverar Operations Management Suite (OMS) i ett HDInsight-kluster och relevanta loggar skickas till den OMS-arbetsyta som anges vid aktivering.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
Hämtar och visar alla Azure HDInsight-kluster som är kopplade till det aktuella abonnemanget eller en angiven resurs grupp, eller hämtar ett specifikt kluster.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Hämtar listan med jobb från ett kluster och visar dem i omvänd kronologisk ordning, eller hämtar ett specifikt jobb.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
Hämtar loggens utdata för ett jobb från det lagrings konto som är kopplat till ett angivet kluster.

### [Get-AzureRmHDInsightOperationsManagementSuite](Get-AzureRmHDInsightOperationsManagementSuite.md)
Hämtar statusen för Operations Management Suite (OMS) i klustret.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Hämtar de beständiga skript åtgärderna för ett kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
Hämtar egenskaper för HDInsight-tjänsten, till exempel tillgängliga platser och kapacitet.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Hämtar skript åtgärds historiken för ett kluster och visar den i omvänd kronologisk ordning, eller hämtar information om en tidigare körd skript åtgärd.

### [Grant-AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
Ger åtkomst till klustret via HTTP.

### [Grant-AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
Ger RDP-åtkomst till Windows-klustret.

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
Skickar en struktur fråga till ett HDInsight-kluster och hämtar frågeresultat i en åtgärd.

### [New-AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Skapar ett Azure HDInsight-kluster i den angivna resurs gruppen för det aktuella abonnemanget.

### [New-AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Skapar ett icke beständigt kluster konfigurations objekt som beskriver en Azure HDInsight-kluster konfiguration.

### [New-AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Skapar ett Hive Job-objekt.

### [New-AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
Skapar ett MapReduce.

### [New-AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Skapar ett gris-Job-objekt.

### [New-AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Skapar ett Sqoop.

### [New-AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Skapar ett Job-MapReduce.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Tar bort angivet HDInsight-kluster från aktuell prenumeration.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Tar bort en beständiga skript åtgärd från ett HDInsight-kluster.

### [Återkalla-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Inaktiverar HTTP-åtkomst till klustret.

### [Återkalla-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Inaktiverar RDP-åtkomst till ett Windows-kluster.

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
Anger antalet arbets tagare i ett angivet kluster.

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Anger standardinställning för lagrings konto i ett kluster konfigurations objekt.

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Anger att en tidigare körd skript åtgärd ska vara en bestående skript åtgärd.

### [Start-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Startar ett definierat Azure HDInsight-jobb i ett angivet kluster.

### [Stopp-AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Stoppar ett angivet pågående jobb i ett kluster.

### [Skicka-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Skickar en ny skript åtgärd till ett Azure HDInsight-kluster.

### [Use-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Väljer ett kluster som ska användas med Invoke-RmAzureHDInsightHiveJob cmdlet.

### [Wait-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
Väntar på att ett visst jobb ska slutföras eller misslyckande.

