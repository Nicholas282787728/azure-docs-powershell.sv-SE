---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 91d99188d1a93ff3719d9229961cbb673666c14a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755568"
---
# <span data-ttu-id="66f42-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66f42-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="66f42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66f42-102">SYNOPSIS</span></span>
<span data-ttu-id="66f42-103">Uppdaterar tillståndet för en rekommenderad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="66f42-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66f42-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66f42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66f42-105">DESCRIPTION</span></span>
<span data-ttu-id="66f42-106">Cmdleten **set-AzureRmSqlDatabaseRecommendedActionState** uppdaterar tillståndet för en rekommenderad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="66f42-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="66f42-107">Då kan en Rekommenderad åtgärd tillämpas, återkallas eller ignoreras baserat på det nya läget.</span><span class="sxs-lookup"><span data-stu-id="66f42-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="66f42-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66f42-108">EXAMPLES</span></span>

### <span data-ttu-id="66f42-109">Exempel 1: tillämpa ett rekommenderat åtgärds tillstånd på väntande</span><span class="sxs-lookup"><span data-stu-id="66f42-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

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

<span data-ttu-id="66f42-110">Det här kommandot uppdaterar tillståndet för den rekommenderade åtgärden som heter IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 som tillhör databasen som heter WIRunner till Pending.</span><span class="sxs-lookup"><span data-stu-id="66f42-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="66f42-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66f42-111">PARAMETERS</span></span>

### <span data-ttu-id="66f42-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="66f42-112">-AdvisorName</span></span>
<span data-ttu-id="66f42-113">Anger namnet på den rådgivare som den rekommenderade åtgärden tillhör.</span><span class="sxs-lookup"><span data-stu-id="66f42-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66f42-114">-DatabaseName</span></span>
<span data-ttu-id="66f42-115">Anger namnet på den databas som den här cmdleten ställer in det rekommenderade åtgärds tillståndet för.</span><span class="sxs-lookup"><span data-stu-id="66f42-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f42-116">-DefaultProfile</span></span>
<span data-ttu-id="66f42-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="66f42-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="66f42-118">-RecommendedActionName</span></span>
<span data-ttu-id="66f42-119">Anger namnet på den rekommenderade åtgärd för vilken status uppdateras.</span><span class="sxs-lookup"><span data-stu-id="66f42-119">Specifies the name of the recommended action for which state is being updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f42-120">-ResourceGroupName</span></span>
<span data-ttu-id="66f42-121">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="66f42-121">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66f42-122">-ServerName</span></span>
<span data-ttu-id="66f42-123">Anger namnet på den server som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="66f42-123">Specifies the name of the server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-124">-State</span><span class="sxs-lookup"><span data-stu-id="66f42-124">-State</span></span>
<span data-ttu-id="66f42-125">Anger det nya värde som den här cmdleten uppdaterar det rekommenderade åtgärds tillståndet för.</span><span class="sxs-lookup"><span data-stu-id="66f42-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="66f42-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="66f42-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66f42-127">Aktiva</span><span class="sxs-lookup"><span data-stu-id="66f42-127">Active</span></span>
- <span data-ttu-id="66f42-128">OAvsluta</span><span class="sxs-lookup"><span data-stu-id="66f42-128">Pending</span></span>
- <span data-ttu-id="66f42-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="66f42-129">PendingRevert</span></span>
- <span data-ttu-id="66f42-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="66f42-130">RevertCancelled</span></span>
- <span data-ttu-id="66f42-131">Ignorera</span><span class="sxs-lookup"><span data-stu-id="66f42-131">Ignored</span></span>
- <span data-ttu-id="66f42-132">Matchar</span><span class="sxs-lookup"><span data-stu-id="66f42-132">Resolved</span></span>

```yaml
Type: RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66f42-133">-Confirm</span></span>
<span data-ttu-id="66f42-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66f42-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f42-135">-WhatIf</span></span>
<span data-ttu-id="66f42-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66f42-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66f42-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66f42-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f42-138">CommonParameters</span></span>
<span data-ttu-id="66f42-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f42-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f42-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f42-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f42-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66f42-141">INPUTS</span></span>

### <span data-ttu-id="66f42-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="66f42-142">None</span></span>
<span data-ttu-id="66f42-143">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="66f42-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66f42-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66f42-144">OUTPUTS</span></span>

### <span data-ttu-id="66f42-145">Microsoft. Azure. commands. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="66f42-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="66f42-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66f42-146">NOTES</span></span>
* <span data-ttu-id="66f42-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL, rådgivare, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="66f42-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="66f42-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66f42-148">RELATED LINKS</span></span>

[<span data-ttu-id="66f42-149">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="66f42-149">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="66f42-150">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="66f42-150">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="66f42-151">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="66f42-151">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="66f42-152">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="66f42-152">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="66f42-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66f42-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="66f42-154">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="66f42-154">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="66f42-155">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66f42-155">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="66f42-156">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66f42-156">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="66f42-157">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="66f42-157">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="66f42-158">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="66f42-158">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="66f42-159">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="66f42-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
