---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272018"
---
# <span data-ttu-id="6c649-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6c649-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="6c649-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c649-102">SYNOPSIS</span></span>
<span data-ttu-id="6c649-103">Uppdaterar tillståndet för en rekommenderad action för Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="6c649-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="6c649-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c649-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c649-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c649-105">DESCRIPTION</span></span>
<span data-ttu-id="6c649-106">Tillståndet **set-AzSqlElasticPoolRecommendedActionState** cmdlet uppdaterar status för en Azure SQL Elastic pool-Rekommenderad åtgärd.</span><span class="sxs-lookup"><span data-stu-id="6c649-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="6c649-107">Denna cmdlet tillämpar en Rekommenderad åtgärd, återställd eller ignorerad baserat på det nya tillståndet.</span><span class="sxs-lookup"><span data-stu-id="6c649-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="6c649-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c649-108">EXAMPLES</span></span>

### <span data-ttu-id="6c649-109">Exempel 1: uppdatera tillståndet för en Rekommenderad åtgärd till förestående</span><span class="sxs-lookup"><span data-stu-id="6c649-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="6c649-110">Det här kommandot uppdaterar tillståndet för den rekommenderade åtgärden i elastisk pool som heter IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 till väntande.</span><span class="sxs-lookup"><span data-stu-id="6c649-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="6c649-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c649-111">PARAMETERS</span></span>

### <span data-ttu-id="6c649-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="6c649-112">-AdvisorName</span></span>
<span data-ttu-id="6c649-113">Anger namnet på den rådgivare som den rekommenderade åtgärden tillhör.</span><span class="sxs-lookup"><span data-stu-id="6c649-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="6c649-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c649-114">-DefaultProfile</span></span>
<span data-ttu-id="6c649-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6c649-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c649-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6c649-116">-ElasticPoolName</span></span>
<span data-ttu-id="6c649-117">Anger namnet på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="6c649-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="6c649-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="6c649-118">-RecommendedActionName</span></span>
<span data-ttu-id="6c649-119">Anger namnet på Rekommenderad åtgärd för vilken denna cmdlet uppdaterar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="6c649-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="6c649-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c649-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c649-121">Anger namnet på resurs gruppen för den server som innehåller den här elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="6c649-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="6c649-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c649-122">-ServerName</span></span>
<span data-ttu-id="6c649-123">Anger namnet på den server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="6c649-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="6c649-124">-State</span><span class="sxs-lookup"><span data-stu-id="6c649-124">-State</span></span>
<span data-ttu-id="6c649-125">Anger det värde som den här cmdleten uppdaterar det rekommenderade åtgärds tillståndet för.</span><span class="sxs-lookup"><span data-stu-id="6c649-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="6c649-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6c649-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c649-127">Aktiva</span><span class="sxs-lookup"><span data-stu-id="6c649-127">Active</span></span>
- <span data-ttu-id="6c649-128">OAvsluta</span><span class="sxs-lookup"><span data-stu-id="6c649-128">Pending</span></span>
- <span data-ttu-id="6c649-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="6c649-129">PendingRevert</span></span>
- <span data-ttu-id="6c649-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="6c649-130">RevertCancelled</span></span>
- <span data-ttu-id="6c649-131">Ignorera</span><span class="sxs-lookup"><span data-stu-id="6c649-131">Ignored</span></span>
- <span data-ttu-id="6c649-132">Matchar</span><span class="sxs-lookup"><span data-stu-id="6c649-132">Resolved</span></span>

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

### <span data-ttu-id="6c649-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c649-133">-Confirm</span></span>
<span data-ttu-id="6c649-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c649-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c649-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c649-135">-WhatIf</span></span>
<span data-ttu-id="6c649-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c649-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c649-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c649-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c649-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c649-138">CommonParameters</span></span>
<span data-ttu-id="6c649-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c649-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c649-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c649-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c649-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c649-141">INPUTS</span></span>

### <span data-ttu-id="6c649-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6c649-142">System.String</span></span>

### <span data-ttu-id="6c649-143">Microsoft. Azure. commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6c649-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="6c649-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c649-144">OUTPUTS</span></span>

### <span data-ttu-id="6c649-145">Microsoft. Azure. commands. SQL. RecommendedAction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="6c649-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="6c649-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c649-146">NOTES</span></span>
* <span data-ttu-id="6c649-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, elasticpool, MSSQL, rådgivare, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="6c649-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="6c649-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c649-148">RELATED LINKS</span></span>

[<span data-ttu-id="6c649-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="6c649-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="6c649-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6c649-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="6c649-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6c649-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="6c649-152">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6c649-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
