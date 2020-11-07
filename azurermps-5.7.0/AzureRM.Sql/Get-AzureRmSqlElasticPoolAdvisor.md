---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3bb8292c872c02c5d6b092e5e721b15eab24e493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579331"
---
# <span data-ttu-id="1d131-101">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="1d131-101">Get-AzureRmSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="1d131-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d131-102">SYNOPSIS</span></span>
<span data-ttu-id="1d131-103">Hämtar en eller flera rådgivare för en elastisk Azure SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="1d131-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d131-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d131-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d131-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d131-105">DESCRIPTION</span></span>
<span data-ttu-id="1d131-106">Cmdleten **Get-AzureRmSqlElasticPoolAdvisor** har en eller flera Azure SQL-Elastic pool rådgivare för en Azure SQL elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="1d131-106">The **Get-AzureRmSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="1d131-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d131-107">EXAMPLES</span></span>

### <span data-ttu-id="1d131-108">Exempel 1: lista alla rådgivare för angiven elastisk pool</span><span class="sxs-lookup"><span data-stu-id="1d131-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -PoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1d131-109">Kommandot hämtar alla rådgivare för den Elastic pool som heter WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="1d131-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="1d131-110">Exempel 2: skaffa en enda rådgivare för angiven elastiska pool</span><span class="sxs-lookup"><span data-stu-id="1d131-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1d131-111">Det här kommandot får rådgivaren med namnet CreateIndex för den elastiska poolen med namnet WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="1d131-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="1d131-112">Exempel 3: Visa alla rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="1d131-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1d131-113">Det här kommandot får alla rådgivare för den elastiska poolen med de rekommenderade åtgärderna i svaret.</span><span class="sxs-lookup"><span data-stu-id="1d131-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="1d131-114">Exempel 4: skaffa en enda rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="1d131-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="1d131-115">Det här kommandot får rådgivaren CreateIndex från servern med namnet Wi-löpare-öst, med de rekommenderade åtgärderna i svaret.</span><span class="sxs-lookup"><span data-stu-id="1d131-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="1d131-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d131-116">PARAMETERS</span></span>

### <span data-ttu-id="1d131-117">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1d131-117">-AdvisorName</span></span>
<span data-ttu-id="1d131-118">Anger namnet på den rådgivare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="1d131-118">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1d131-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d131-119">-DefaultProfile</span></span>
<span data-ttu-id="1d131-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1d131-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d131-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1d131-121">-ElasticPoolName</span></span>
<span data-ttu-id="1d131-122">Anger namnet på den Elastic pool som denna cmdlet begär rådgivare för.</span><span class="sxs-lookup"><span data-stu-id="1d131-122">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="1d131-123">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="1d131-123">-ExpandRecommendedActions</span></span>
<span data-ttu-id="1d131-124">Anger att cmdleten innehåller de rekommenderade åtgärderna för klassificeringen i svaret.</span><span class="sxs-lookup"><span data-stu-id="1d131-124">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="1d131-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d131-125">-ResourceGroupName</span></span>
<span data-ttu-id="1d131-126">Anger namnet på resurs gruppen för den server som innehåller den här elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="1d131-126">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="1d131-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d131-127">-ServerName</span></span>
<span data-ttu-id="1d131-128">Anger namnet på den server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="1d131-128">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="1d131-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d131-129">CommonParameters</span></span>
<span data-ttu-id="1d131-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d131-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d131-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d131-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d131-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d131-132">INPUTS</span></span>

### <span data-ttu-id="1d131-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="1d131-133">None</span></span>
<span data-ttu-id="1d131-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1d131-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d131-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d131-135">OUTPUTS</span></span>

### <span data-ttu-id="1d131-136">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="1d131-136">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="1d131-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d131-137">NOTES</span></span>
* <span data-ttu-id="1d131-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, elasticpool, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="1d131-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="1d131-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d131-139">RELATED LINKS</span></span>

[<span data-ttu-id="1d131-140">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="1d131-140">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="1d131-141">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="1d131-141">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="1d131-142">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1d131-142">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="1d131-143">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1d131-143">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="1d131-144">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="1d131-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)