---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252661"
---
# Az.HDInsight-modul
## Beskrivning
Avsnitten i det här avsnittet innehåller Azure PowerShell-cmdlets för Microsoft Azure HDInsight i Azure Resource Manager-ramverket (ARM). Dessa cmdlets används för att hantera HDInsight-kluster och de jobb som körs på dem. Cmdletarna finns i namnområdet Microsoft.Azure.Commands.HDInsight.

## Az.HDInsight-cmdlets
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Lägger till en klusteridentitet i ett klusterkonfigurationsobjekt.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Lägger till en version för en tjänst som körs i ett kluster i ett klusterkonfigurationsobjekt.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Lägger till anpassning av ett Hadoop-konfigurationsvärde och/eller en anpassning av delad bibliotekssamling i ett klusterkonfigurationsobjekt.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Lägger till en SQL-databas som fungerar som en Registrerings- eller Oo metastore i ett klusterkonfigurationsobjekt.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Lägger till en skriptåtgärd i ett klusterkonfigurationsobjekt.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Lägger till en säkerhetsprofil i ett klusterkonfigurationsobjekt.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Lägger till en Azure Storage-nyckel i ett klusterkonfigurationsobjekt.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Inaktiverar övervakning i ett HDInsight-kluster och relevanta loggar slutar flöda till den övervakningsarbetsyta som angetts under aktiverande.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Aktiverar övervakning i ett HDInsight-kluster och relevanta loggar skickas till den arbetsyta för övervakning som anges under aktiverande.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Hämtar och visar alla Azure HDInsight-kluster som är kopplade till den aktuella prenumerationen eller en angiven resursgrupp, eller hämtar ett visst kluster.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Hämtar automatisk skalkonfiguration av HDInsight-kluster.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Visar värdarna för HDInsight-klustret.

### [Get-AzHDInsight Enfn](Get-AzHDInsightJob.md)
Hämtar listan med jobb från ett kluster och visar dem i omvänd kronologisk ordning, eller hämtar ett visst jobb.

### [Get-AzHDInsight EntiffOutput](Get-AzHDInsightJobOutput.md)
Hämtar loggutdata för ett jobb från lagringskontot som är kopplat till ett visst kluster.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Får statusen för att övervaka installationen i klustret.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Hämtar de beständiga skriptåtgärderna för ett kluster och visar dem i kronologisk ordning, eller hämtar information för en viss åtgärd i beständiga skript.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Hämtar egenskaper för HDInsight-tjänsten, till exempel tillgängliga platser och kapacitet.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Hämtar skriptåtgärdshistoriken för ett kluster och visar den i omvänd kronologisk ordning, eller får information om en tidigare körd skriptåtgärd.

### [Invoke-AzHDInsightHiveLow](Invoke-AzHDInsightHiveJob.md)
Skickar en registreringsfråga till ett HDInsight-kluster och hämtar frågeresultat i en enda åtgärd.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Skapar ett Azure HDInsight-kluster i den angivna resursgruppen för den aktuella prenumerationen.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Skapar ett objekt som inte finns kvar och som beskriver automatisk skalkonfiguration av ett Azure HDInsight-kluster.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Skapar schemabaserat villkor för automatisk skalning.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Skapar ett konfigurationsobjekt som inte finns kvar i ett kluster som beskriver en konfiguration av Azure HDInsight-kluster.

### [New-AzhDInsightHiveDefinition](New-AzHDInsightHiveJobDefinition.md)
Skapar ett objekt för en registreringsjobb.

### [New-AzHDInsightMapReduceDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Skapar ett MapReduce-jobbobjekt.

### [New-AzHDInsightPigDefinition](New-AzHDInsightPigJobDefinition.md)
Skapar ett Jobbobjekt av en 10:e plats.

### [New-AzhDInsightSqoopOopDefinition](New-AzHDInsightSqoopJobDefinition.md)
Skapar ett Sqoop-jobbobjekt.

### [New-AzHDInsightStreamingMapReduceDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Skapar ett Streaming MapReduce-jobbobjekt.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Tar bort det angivna HDInsight-klustret från den aktuella prenumerationen.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Tar bort automatisk skalkonfiguration för HDInsight-klustret.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Tar bort en åtgärd för ett persisted script från ett HDInsight-kluster.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Startar om särskilda värdar för HDInsight-kluster.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Anger automatisk skalkonfiguration för ett Azure HDInsight-kluster.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Roterar diskkrypteringsnyckeln för det angivna HDInsight-klustret.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Anger antalet arbetsnoder i ett angivet kluster.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Anger standardinställningen för lagringskonto i ett klusterkonfigurationsobjekt.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Anger gatewayens HTTP-autentiseringsuppgifter för ett Azure HDInsight-kluster.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Anger att en tidigare körd skriptåtgärd ska vara en persisted script-åtgärd.

### [Start-AzHDInsight Ent](Start-AzHDInsightJob.md)
Startar ett definierat Azure HDInsight-jobb på ett angivet kluster.

### [Stop-AzHDInsight Enfn](Stop-AzHDInsightJob.md)
Stoppar ett angivet körningsjobb i ett kluster.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Skickar en ny skriptåtgärd till ett Azure HDInsight-kluster.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Väljer ett kluster som ska användas med Invoke-RmAzureHDInsightHiveJob cmdlet.

### [Wait-AzHDInsight Ent](Wait-AzHDInsightJob.md)
Väntar på slutförande eller fel för ett visst jobb.

