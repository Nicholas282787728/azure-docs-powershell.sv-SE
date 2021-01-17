---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404523"
---
# <span data-ttu-id="c780d-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c780d-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="c780d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c780d-102">SYNOPSIS</span></span>
<span data-ttu-id="c780d-103">Får en eller flera rådgivare till en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c780d-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="c780d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c780d-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c780d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c780d-105">DESCRIPTION</span></span>
<span data-ttu-id="c780d-106">Cmdleten **Get-AzSqlServerAdvisor** hämtar en eller flera Azure SQL Server-rådgivare för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c780d-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="c780d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c780d-107">EXAMPLES</span></span>

### <span data-ttu-id="c780d-108">Exempel 1: lista alla rådgivare för servern</span><span class="sxs-lookup"><span data-stu-id="c780d-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
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

<span data-ttu-id="c780d-109">Det här kommandot får en lista över alla rådgivare för servern med namnet WiFi-öst som tillhör resurs gruppen WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="c780d-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="c780d-110">Exempel 2: skaffa en enda rådgivare för servern</span><span class="sxs-lookup"><span data-stu-id="c780d-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="c780d-111">Det här kommandot får rådgivaren med namnet CreateIndex för servern med namnet WiFi-öst.</span><span class="sxs-lookup"><span data-stu-id="c780d-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="c780d-112">Exempel 3: Visa alla rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="c780d-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

<span data-ttu-id="c780d-113">Det här kommandot får alla rådgivare för servern med namnet WiFi-öst.</span><span class="sxs-lookup"><span data-stu-id="c780d-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="c780d-114">Eftersom parametern *ExpandRecommendedActions* används i kommandot, får de rådgivare som rekommenderas i svaret.</span><span class="sxs-lookup"><span data-stu-id="c780d-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="c780d-115">Exempel 4: skaffa en enda rådgivare med de rekommenderade åtgärderna i svaret</span><span class="sxs-lookup"><span data-stu-id="c780d-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="c780d-116">Det här kommandot får rådgivaren CreateIndex från servern med namnet Wi-löpare-öst, med de rekommenderade åtgärderna i svaret.</span><span class="sxs-lookup"><span data-stu-id="c780d-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="c780d-117">Exempel 5: lista alla rådgivare för servern med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="c780d-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
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
```

<span data-ttu-id="c780d-118">Det här kommandot får en lista över alla rådgivare för servern med namnet WiFi-öst som tillhör resurs gruppen WIRunnersProd som börjar med bokstaven "d".</span><span class="sxs-lookup"><span data-stu-id="c780d-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="c780d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c780d-119">PARAMETERS</span></span>

### <span data-ttu-id="c780d-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="c780d-120">-AdvisorName</span></span>
<span data-ttu-id="c780d-121">Anger namnet på den rådgivare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c780d-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c780d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c780d-122">-DefaultProfile</span></span>
<span data-ttu-id="c780d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c780d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c780d-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="c780d-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="c780d-125">Anger att cmdleten innehåller de rekommenderade åtgärderna för de rådgivare som ingår i svaret.</span><span class="sxs-lookup"><span data-stu-id="c780d-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="c780d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c780d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c780d-127">Anger namnet på Server gruppen.</span><span class="sxs-lookup"><span data-stu-id="c780d-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="c780d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c780d-128">-ServerName</span></span>
<span data-ttu-id="c780d-129">Anger namnet på servern för den rådgivare som denna cmdlet begär.</span><span class="sxs-lookup"><span data-stu-id="c780d-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="c780d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c780d-130">CommonParameters</span></span>
<span data-ttu-id="c780d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c780d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c780d-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c780d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c780d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c780d-133">INPUTS</span></span>

### <span data-ttu-id="c780d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c780d-134">System.String</span></span>

### <span data-ttu-id="c780d-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c780d-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c780d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c780d-136">OUTPUTS</span></span>

### <span data-ttu-id="c780d-137">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="c780d-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="c780d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c780d-138">NOTES</span></span>
* <span data-ttu-id="c780d-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, Server, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="c780d-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="c780d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c780d-140">RELATED LINKS</span></span>

[<span data-ttu-id="c780d-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="c780d-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="c780d-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="c780d-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="c780d-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c780d-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="c780d-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c780d-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c780d-145">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="c780d-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

