---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
ms.openlocfilehash: a77119e653f3d4e6155fbe98e85a583eca50c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757022"
---
# <span data-ttu-id="fa929-101">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="fa929-101">Get-AzureRmSqlServerAdvisor</span></span>

## <span data-ttu-id="fa929-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa929-102">SYNOPSIS</span></span>
<span data-ttu-id="fa929-103">Får en eller flera rådgivare till en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fa929-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa929-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa929-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa929-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa929-105">DESCRIPTION</span></span>
<span data-ttu-id="fa929-106">Cmdleten **Get-AzureRmSqlServerAdvisor** hämtar en eller flera Azure SQL Server-rådgivare för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fa929-106">The **Get-AzureRmSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="fa929-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa929-107">EXAMPLES</span></span>

### <span data-ttu-id="fa929-108">Exempel 1: lista alla rådgivare för servern</span><span class="sxs-lookup"><span data-stu-id="fa929-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="fa929-109">Det här kommandot får en lista över alla rådgivare för servern med namnet WiFi-öst som tillhör resurs gruppen WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="fa929-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="fa929-110">Exempel 2: skaffa en enda rådgivare för servern</span><span class="sxs-lookup"><span data-stu-id="fa929-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="fa929-111">Det här kommandot får rådgivaren med namnet CreateIndex för servern med namnet WiFi-öst.</span><span class="sxs-lookup"><span data-stu-id="fa929-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="fa929-112">Exempel 3: Visa alla rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="fa929-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="fa929-113">Det här kommandot får alla rådgivare för servern med namnet WiFi-öst.</span><span class="sxs-lookup"><span data-stu-id="fa929-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="fa929-114">Eftersom parametern *ExpandRecommendedActions* används i kommandot, får de rådgivare som rekommenderas i svaret.</span><span class="sxs-lookup"><span data-stu-id="fa929-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="fa929-115">Exempel 4: skaffa en enda rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="fa929-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="fa929-116">Det här kommandot får rådgivaren CreateIndex från servern med namnet Wi-löpare-öst, med de rekommenderade åtgärderna i svaret.</span><span class="sxs-lookup"><span data-stu-id="fa929-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="fa929-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa929-117">PARAMETERS</span></span>

### <span data-ttu-id="fa929-118">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="fa929-118">-AdvisorName</span></span>
<span data-ttu-id="fa929-119">Anger namnet på den rådgivare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="fa929-119">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fa929-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa929-120">-DefaultProfile</span></span>
<span data-ttu-id="fa929-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fa929-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa929-122">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="fa929-122">-ExpandRecommendedActions</span></span>
<span data-ttu-id="fa929-123">Anger att cmdleten innehåller de rekommenderade åtgärderna för de rådgivare som ingår i svaret.</span><span class="sxs-lookup"><span data-stu-id="fa929-123">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa929-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa929-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa929-125">Anger namnet på Server gruppen.</span><span class="sxs-lookup"><span data-stu-id="fa929-125">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="fa929-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fa929-126">-ServerName</span></span>
<span data-ttu-id="fa929-127">Anger namnet på servern för den rådgivare som denna cmdlet begär.</span><span class="sxs-lookup"><span data-stu-id="fa929-127">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="fa929-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa929-128">CommonParameters</span></span>
<span data-ttu-id="fa929-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa929-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa929-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa929-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa929-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa929-131">INPUTS</span></span>

### <span data-ttu-id="fa929-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fa929-132">System.String</span></span>

### <span data-ttu-id="fa929-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa929-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa929-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa929-134">OUTPUTS</span></span>

### <span data-ttu-id="fa929-135">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="fa929-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="fa929-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa929-136">NOTES</span></span>
* <span data-ttu-id="fa929-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, Server, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="fa929-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="fa929-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa929-138">RELATED LINKS</span></span>

[<span data-ttu-id="fa929-139">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="fa929-139">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="fa929-140">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="fa929-140">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="fa929-141">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="fa929-141">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="fa929-142">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fa929-142">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="fa929-143">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fa929-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
