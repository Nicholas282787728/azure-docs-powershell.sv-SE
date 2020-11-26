---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261580"
---
# <span data-ttu-id="ecf72-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ecf72-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="ecf72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecf72-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf72-103">Uppdaterar tillståndet för en rekommenderad Azure SQL Server-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ecf72-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="ecf72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecf72-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecf72-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf72-106">**Set-AzSqlServerRecommendedActionState** cmdlet uppdaterar status för en rekommenderad Azure SQL Server-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ecf72-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="ecf72-107">Denna cmdlet tillämpas, återställer eller tar bort den rekommenderade åtgärden baserat på det nya läget.</span><span class="sxs-lookup"><span data-stu-id="ecf72-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="ecf72-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecf72-108">EXAMPLES</span></span>

### <span data-ttu-id="ecf72-109">Example1: uppdatera tillståndet för den angivna rekommenderade åtgärden till väntande</span><span class="sxs-lookup"><span data-stu-id="ecf72-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="ecf72-110">Uppdaterar status för Rekommenderad server åtgärd med namnet "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" till "väntar"</span><span class="sxs-lookup"><span data-stu-id="ecf72-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="ecf72-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecf72-111">PARAMETERS</span></span>

### <span data-ttu-id="ecf72-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="ecf72-112">-AdvisorName</span></span>
<span data-ttu-id="ecf72-113">Anger namnet på den rådgivare som innehåller den rekommenderade åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ecf72-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="ecf72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf72-114">-DefaultProfile</span></span>
<span data-ttu-id="ecf72-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ecf72-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecf72-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="ecf72-116">-RecommendedActionName</span></span>
<span data-ttu-id="ecf72-117">Anger namnet på Rekommenderad åtgärd för vilken denna cmdlet uppdaterar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="ecf72-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="ecf72-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf72-118">-ResourceGroupName</span></span>
<span data-ttu-id="ecf72-119">Anger namnet på serverns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ecf72-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="ecf72-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ecf72-120">-ServerName</span></span>
<span data-ttu-id="ecf72-121">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ecf72-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ecf72-122">-State</span><span class="sxs-lookup"><span data-stu-id="ecf72-122">-State</span></span>
<span data-ttu-id="ecf72-123">Anger det nya värde som den här cmdleten uppdaterar det rekommenderade åtgärds tillståndet för.</span><span class="sxs-lookup"><span data-stu-id="ecf72-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="ecf72-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ecf72-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecf72-125">Aktiva</span><span class="sxs-lookup"><span data-stu-id="ecf72-125">Active</span></span>
- <span data-ttu-id="ecf72-126">OAvsluta</span><span class="sxs-lookup"><span data-stu-id="ecf72-126">Pending</span></span>
- <span data-ttu-id="ecf72-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="ecf72-127">PendingRevert</span></span>
- <span data-ttu-id="ecf72-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="ecf72-128">RevertCancelled</span></span>
- <span data-ttu-id="ecf72-129">Ignorera</span><span class="sxs-lookup"><span data-stu-id="ecf72-129">Ignored</span></span>
- <span data-ttu-id="ecf72-130">Matchar</span><span class="sxs-lookup"><span data-stu-id="ecf72-130">Resolved</span></span>

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

### <span data-ttu-id="ecf72-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecf72-131">-Confirm</span></span>
<span data-ttu-id="ecf72-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecf72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf72-133">-WhatIf</span></span>
<span data-ttu-id="ecf72-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecf72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf72-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecf72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf72-136">CommonParameters</span></span>
<span data-ttu-id="ecf72-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf72-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecf72-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf72-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecf72-139">INPUTS</span></span>

### <span data-ttu-id="ecf72-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf72-140">System.String</span></span>

### <span data-ttu-id="ecf72-141">Microsoft. Azure. commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ecf72-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="ecf72-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecf72-142">OUTPUTS</span></span>

### <span data-ttu-id="ecf72-143">Microsoft. Azure. commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="ecf72-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="ecf72-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecf72-144">NOTES</span></span>
* <span data-ttu-id="ecf72-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, Server, MSSQL, rådgivare, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="ecf72-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="ecf72-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecf72-146">RELATED LINKS</span></span>

[<span data-ttu-id="ecf72-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="ecf72-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="ecf72-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ecf72-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="ecf72-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ecf72-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="ecf72-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ecf72-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="ecf72-151">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ecf72-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)