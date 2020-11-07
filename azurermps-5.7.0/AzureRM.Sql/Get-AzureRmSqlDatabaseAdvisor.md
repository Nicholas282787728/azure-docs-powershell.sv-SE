---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: 75e584ba9eab2c43aba5fc6a9b5d3cd3b39adc5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575487"
---
# <span data-ttu-id="7726b-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="7726b-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="7726b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7726b-102">SYNOPSIS</span></span>
<span data-ttu-id="7726b-103">Får en eller flera rådgivare till en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7726b-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7726b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7726b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7726b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7726b-105">DESCRIPTION</span></span>
<span data-ttu-id="7726b-106">Cmdleten **Get-AzureRmSqlDatabaseAdvisor** hämtar en eller flera Azure SQL-databas rådgivare för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7726b-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="7726b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7726b-107">EXAMPLES</span></span>

### <span data-ttu-id="7726b-108">Exempel 1: lista alla rådgivare för den angivna databasen</span><span class="sxs-lookup"><span data-stu-id="7726b-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="7726b-109">Med det här kommandot får du en lista med alla rådgivare för databasen med namnet WIRunner som tillhör servern med namnet WiFi-öst.</span><span class="sxs-lookup"><span data-stu-id="7726b-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="7726b-110">Exempel 2: skaffa en enda rådgivare för den angivna databasen</span><span class="sxs-lookup"><span data-stu-id="7726b-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="7726b-111">Det här kommandot får rådgivaren CreateIndex för databasen med namnet WIRunner.</span><span class="sxs-lookup"><span data-stu-id="7726b-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="7726b-112">Exempel 3: Visa alla rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="7726b-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="7726b-113">Det här kommandot får alla rådgivare för databasen ' WIRunner ' med de rekommenderade åtgärderna i svaret.</span><span class="sxs-lookup"><span data-stu-id="7726b-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="7726b-114">Eftersom parametern *ExpandRecommendedActions* används i kommandot får cmdleten de rekommenderade åtgärderna med svaret.</span><span class="sxs-lookup"><span data-stu-id="7726b-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="7726b-115">Exempel 4: skaffa en enda rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="7726b-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="7726b-116">Det här kommandot får den rådgivare som heter CreateIndex från databasen med namnet WIRunner med de rekommenderade åtgärderna i svaret.</span><span class="sxs-lookup"><span data-stu-id="7726b-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="7726b-117">Eftersom parametern *ExpandRecommendedActions* används i kommandot får cmdleten de rekommenderade åtgärderna med svaret.</span><span class="sxs-lookup"><span data-stu-id="7726b-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="7726b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7726b-118">PARAMETERS</span></span>

### <span data-ttu-id="7726b-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="7726b-119">-AdvisorName</span></span>
<span data-ttu-id="7726b-120">Anger namnet på den rådgivare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="7726b-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7726b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7726b-121">-DatabaseName</span></span>
<span data-ttu-id="7726b-122">Anger namnet på den databas där denna cmdlet begär rådgivare.</span><span class="sxs-lookup"><span data-stu-id="7726b-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="7726b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7726b-123">-DefaultProfile</span></span>
<span data-ttu-id="7726b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7726b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7726b-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="7726b-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="7726b-126">Anger att denna cmdlet får de rekommenderade åtgärderna med svaret.</span><span class="sxs-lookup"><span data-stu-id="7726b-126">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7726b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7726b-127">-ResourceGroupName</span></span>
<span data-ttu-id="7726b-128">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="7726b-128">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="7726b-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7726b-129">-ServerName</span></span>
<span data-ttu-id="7726b-130">Anger namnet på den server som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="7726b-130">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="7726b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7726b-131">CommonParameters</span></span>
<span data-ttu-id="7726b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7726b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7726b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7726b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7726b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7726b-134">INPUTS</span></span>

### <span data-ttu-id="7726b-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="7726b-135">None</span></span>
<span data-ttu-id="7726b-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7726b-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7726b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7726b-137">OUTPUTS</span></span>

### <span data-ttu-id="7726b-138">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="7726b-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="7726b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7726b-139">NOTES</span></span>
* <span data-ttu-id="7726b-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="7726b-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="7726b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7726b-141">RELATED LINKS</span></span>

[<span data-ttu-id="7726b-142">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="7726b-142">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="7726b-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="7726b-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="7726b-144">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="7726b-144">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="7726b-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="7726b-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="7726b-146">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="7726b-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)