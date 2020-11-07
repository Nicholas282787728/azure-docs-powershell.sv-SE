---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 4b000ef101b07bf882accb10b0256e0dbea513b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758263"
---
# <span data-ttu-id="6b072-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6b072-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="6b072-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b072-102">SYNOPSIS</span></span>
<span data-ttu-id="6b072-103">Uppdaterar tillståndet för en rekommenderad Azure SQL Server-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="6b072-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b072-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b072-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b072-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b072-105">DESCRIPTION</span></span>
<span data-ttu-id="6b072-106">**Set-AzureRmSqlServerRecommendedActionState** cmdlet uppdaterar status för en rekommenderad Azure SQL Server-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="6b072-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="6b072-107">Denna cmdlet tillämpas, återställer eller tar bort den rekommenderade åtgärden baserat på det nya läget.</span><span class="sxs-lookup"><span data-stu-id="6b072-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="6b072-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b072-108">EXAMPLES</span></span>

### <span data-ttu-id="6b072-109">Example1: uppdatera tillståndet för den angivna rekommenderade åtgärden till väntande</span><span class="sxs-lookup"><span data-stu-id="6b072-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="6b072-110">Uppdaterar status för Rekommenderad server åtgärd med namnet "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" till "väntar"</span><span class="sxs-lookup"><span data-stu-id="6b072-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="6b072-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b072-111">PARAMETERS</span></span>

### <span data-ttu-id="6b072-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="6b072-112">-AdvisorName</span></span>
<span data-ttu-id="6b072-113">Anger namnet på den rådgivare som innehåller den rekommenderade åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6b072-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="6b072-114">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="6b072-114">-RecommendedActionName</span></span>
<span data-ttu-id="6b072-115">Anger namnet på Rekommenderad åtgärd för vilken denna cmdlet uppdaterar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="6b072-115">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="6b072-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b072-116">-ResourceGroupName</span></span>
<span data-ttu-id="6b072-117">Anger namnet på serverns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6b072-117">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="6b072-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b072-118">-ServerName</span></span>
<span data-ttu-id="6b072-119">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="6b072-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6b072-120">-State</span><span class="sxs-lookup"><span data-stu-id="6b072-120">-State</span></span>
<span data-ttu-id="6b072-121">Anger det nya värde som den här cmdleten uppdaterar det rekommenderade åtgärds tillståndet för.</span><span class="sxs-lookup"><span data-stu-id="6b072-121">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="6b072-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6b072-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b072-123">Aktiva</span><span class="sxs-lookup"><span data-stu-id="6b072-123">Active</span></span>
- <span data-ttu-id="6b072-124">OAvsluta</span><span class="sxs-lookup"><span data-stu-id="6b072-124">Pending</span></span>
- <span data-ttu-id="6b072-125">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="6b072-125">PendingRevert</span></span>
- <span data-ttu-id="6b072-126">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="6b072-126">RevertCancelled</span></span>
- <span data-ttu-id="6b072-127">Ignorera</span><span class="sxs-lookup"><span data-stu-id="6b072-127">Ignored</span></span>
- <span data-ttu-id="6b072-128">Matchar</span><span class="sxs-lookup"><span data-stu-id="6b072-128">Resolved</span></span>

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

### <span data-ttu-id="6b072-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b072-129">-Confirm</span></span>
<span data-ttu-id="6b072-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b072-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b072-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b072-131">-WhatIf</span></span>
<span data-ttu-id="6b072-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b072-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b072-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b072-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b072-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b072-134">-DefaultProfile</span></span>
<span data-ttu-id="6b072-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b072-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b072-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b072-136">CommonParameters</span></span>
<span data-ttu-id="6b072-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b072-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b072-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b072-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b072-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b072-139">INPUTS</span></span>

## <span data-ttu-id="6b072-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b072-140">OUTPUTS</span></span>

### <span data-ttu-id="6b072-141">Microsoft. Azure. commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="6b072-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="6b072-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b072-142">NOTES</span></span>
* <span data-ttu-id="6b072-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, Server, MSSQL, rådgivare, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="6b072-143">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="6b072-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b072-144">RELATED LINKS</span></span>

[<span data-ttu-id="6b072-145">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="6b072-145">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="6b072-146">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="6b072-146">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="6b072-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6b072-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="6b072-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6b072-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="6b072-149">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6b072-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
