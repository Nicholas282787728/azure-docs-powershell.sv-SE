---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EF6C862B-A89C-48AB-A590-92CFA387305F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
ms.openlocfilehash: fc54e470ed79593b40d25fdfc4cf655a0a8f44d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412691"
---
# <span data-ttu-id="7925a-101">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="7925a-101">Get-AzSqlDatabaseRecommendedAction</span></span>

## <span data-ttu-id="7925a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7925a-102">SYNOPSIS</span></span>
<span data-ttu-id="7925a-103">Hämtar en eller flera rekommenderade åtgärder för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="7925a-103">Gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="7925a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7925a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7925a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7925a-105">DESCRIPTION</span></span>
<span data-ttu-id="7925a-106">Cmdleten **Get-AzSqlDatabaseRecommendedAction** har en eller flera rekommenderade åtgärder för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="7925a-106">The **Get-AzSqlDatabaseRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="7925a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7925a-107">EXAMPLES</span></span>

### <span data-ttu-id="7925a-108">Exempel 1: lista alla rekommenderade åtgärder för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="7925a-108">Example 1: List all the recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="7925a-109">Det här kommandot får en lista över alla rekommenderade åtgärder hos den rådgivare som heter CreateIndex tillgänglig för databasen som heter Wi-löpare – Australien-öst.</span><span class="sxs-lookup"><span data-stu-id="7925a-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the database named wi-runner-australia-east.</span></span>

### <span data-ttu-id="7925a-110">Exempel 2: skaffa en enda Rekommenderad åtgärd för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="7925a-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="7925a-111">Med det här kommandot får du den rekommenderade åtgärden som heter IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 för rådgivaren CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="7925a-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 for the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="7925a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7925a-112">PARAMETERS</span></span>

### <span data-ttu-id="7925a-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="7925a-113">-AdvisorName</span></span>
<span data-ttu-id="7925a-114">Anger namnet på den rådgivare för vilken denna cmdlet begär rekommenderade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="7925a-114">Specifies the name of the Advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="7925a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7925a-115">-DatabaseName</span></span>
<span data-ttu-id="7925a-116">Anger namnet på den databas som den här cmdleten begär åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="7925a-116">Specifies the name of the database for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="7925a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7925a-117">-DefaultProfile</span></span>
<span data-ttu-id="7925a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7925a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7925a-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="7925a-119">-RecommendedActionName</span></span>
<span data-ttu-id="7925a-120">Anger namnet på den rekommenderade åtgärd som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="7925a-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7925a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7925a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7925a-122">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="7925a-122">Specifies name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="7925a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7925a-123">-ServerName</span></span>
<span data-ttu-id="7925a-124">Anger namnet på den server som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="7925a-124">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="7925a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7925a-125">CommonParameters</span></span>
<span data-ttu-id="7925a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7925a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7925a-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7925a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7925a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7925a-128">INPUTS</span></span>

### <span data-ttu-id="7925a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7925a-129">System.String</span></span>

## <span data-ttu-id="7925a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7925a-130">OUTPUTS</span></span>

### <span data-ttu-id="7925a-131">Microsoft. Azure. commands. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="7925a-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="7925a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7925a-132">NOTES</span></span>
* <span data-ttu-id="7925a-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL, rådgivare, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="7925a-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="7925a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7925a-134">RELATED LINKS</span></span>

[<span data-ttu-id="7925a-135">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="7925a-135">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="7925a-136">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="7925a-136">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="7925a-137">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="7925a-137">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="7925a-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="7925a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
