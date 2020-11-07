---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: be8c9d4ef21aeb63e99b512d626f6a38e02c3ab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756653"
---
# <span data-ttu-id="62acc-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="62acc-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="62acc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62acc-102">SYNOPSIS</span></span>
<span data-ttu-id="62acc-103">Uppdaterar tillståndet för en rekommenderad action för Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="62acc-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62acc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62acc-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62acc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62acc-105">DESCRIPTION</span></span>
<span data-ttu-id="62acc-106">Tillståndet **set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet uppdaterar status för en Azure SQL Elastic pool-Rekommenderad åtgärd.</span><span class="sxs-lookup"><span data-stu-id="62acc-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="62acc-107">Denna cmdlet tillämpar en Rekommenderad åtgärd, återställd eller ignorerad baserat på det nya tillståndet.</span><span class="sxs-lookup"><span data-stu-id="62acc-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="62acc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62acc-108">EXAMPLES</span></span>

### <span data-ttu-id="62acc-109">Exempel 1: uppdatera tillståndet för en Rekommenderad åtgärd till förestående</span><span class="sxs-lookup"><span data-stu-id="62acc-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="62acc-110">Det här kommandot uppdaterar tillståndet för den rekommenderade åtgärden i elastisk pool som heter IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 till väntande.</span><span class="sxs-lookup"><span data-stu-id="62acc-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="62acc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62acc-111">PARAMETERS</span></span>

### <span data-ttu-id="62acc-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="62acc-112">-AdvisorName</span></span>
<span data-ttu-id="62acc-113">Anger namnet på den rådgivare som den rekommenderade åtgärden tillhör.</span><span class="sxs-lookup"><span data-stu-id="62acc-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62acc-114">-DefaultProfile</span></span>
<span data-ttu-id="62acc-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="62acc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="62acc-116">-ElasticPoolName</span></span>
<span data-ttu-id="62acc-117">Anger namnet på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="62acc-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="62acc-118">-RecommendedActionName</span></span>
<span data-ttu-id="62acc-119">Anger namnet på Rekommenderad åtgärd för vilken denna cmdlet uppdaterar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="62acc-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62acc-120">-ResourceGroupName</span></span>
<span data-ttu-id="62acc-121">Anger namnet på resurs gruppen för den server som innehåller den här elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="62acc-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62acc-122">-ServerName</span></span>
<span data-ttu-id="62acc-123">Anger namnet på den server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="62acc-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-124">-State</span><span class="sxs-lookup"><span data-stu-id="62acc-124">-State</span></span>
<span data-ttu-id="62acc-125">Anger det värde som den här cmdleten uppdaterar det rekommenderade åtgärds tillståndet för.</span><span class="sxs-lookup"><span data-stu-id="62acc-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="62acc-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="62acc-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62acc-127">Aktiva</span><span class="sxs-lookup"><span data-stu-id="62acc-127">Active</span></span>
- <span data-ttu-id="62acc-128">OAvsluta</span><span class="sxs-lookup"><span data-stu-id="62acc-128">Pending</span></span>
- <span data-ttu-id="62acc-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="62acc-129">PendingRevert</span></span>
- <span data-ttu-id="62acc-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="62acc-130">RevertCancelled</span></span>
- <span data-ttu-id="62acc-131">Ignorera</span><span class="sxs-lookup"><span data-stu-id="62acc-131">Ignored</span></span>
- <span data-ttu-id="62acc-132">Matchar</span><span class="sxs-lookup"><span data-stu-id="62acc-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62acc-133">-Confirm</span></span>
<span data-ttu-id="62acc-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62acc-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62acc-135">-WhatIf</span></span>
<span data-ttu-id="62acc-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62acc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62acc-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62acc-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62acc-138">CommonParameters</span></span>
<span data-ttu-id="62acc-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62acc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62acc-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62acc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62acc-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62acc-141">INPUTS</span></span>

### <span data-ttu-id="62acc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="62acc-142">System.String</span></span>

### <span data-ttu-id="62acc-143">Microsoft. Azure. commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="62acc-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="62acc-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62acc-144">OUTPUTS</span></span>

### <span data-ttu-id="62acc-145">Microsoft. Azure. commands. SQL. RecommendedAction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="62acc-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="62acc-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62acc-146">NOTES</span></span>
* <span data-ttu-id="62acc-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, elasticpool, MSSQL, rådgivare, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="62acc-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="62acc-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62acc-148">RELATED LINKS</span></span>

[<span data-ttu-id="62acc-149">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="62acc-149">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="62acc-150">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="62acc-150">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="62acc-151">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="62acc-151">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="62acc-152">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="62acc-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
