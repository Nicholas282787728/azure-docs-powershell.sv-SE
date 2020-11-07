---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 92720cd486abd5f79be7f044e3fe98d038976a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755466"
---
# <span data-ttu-id="38412-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="38412-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="38412-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38412-102">SYNOPSIS</span></span>
<span data-ttu-id="38412-103">Uppdaterar status för automatisk körning av en Azure SQL-Elastic pool rådgivare.</span><span class="sxs-lookup"><span data-stu-id="38412-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38412-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38412-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38412-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38412-105">DESCRIPTION</span></span>
<span data-ttu-id="38412-106">Cmdleten **set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** ställer in egenskapen autoexecuting för en Azure SQL-pool med Elastic-resurspool.</span><span class="sxs-lookup"><span data-stu-id="38412-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="38412-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38412-107">EXAMPLES</span></span>

### <span data-ttu-id="38412-108">Exempel 1: Aktivera automatisk körning för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="38412-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="38412-109">Det här kommandot anger statusen för automatisk körning för en rådgivare med namnet CreateIndex till Enabled.</span><span class="sxs-lookup"><span data-stu-id="38412-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="38412-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38412-110">PARAMETERS</span></span>

### <span data-ttu-id="38412-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="38412-111">-AdvisorName</span></span>
<span data-ttu-id="38412-112">Anger namnet på den rådgivare för vilken denna cmdlet uppdaterar statusen för automatisk körning.</span><span class="sxs-lookup"><span data-stu-id="38412-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="38412-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="38412-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="38412-114">Anger ett nytt värde som denna cmdlet uppdaterar status för automatisk körning till.</span><span class="sxs-lookup"><span data-stu-id="38412-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="38412-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="38412-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38412-116">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="38412-116">Enabled</span></span>
- <span data-ttu-id="38412-117">Aktiv</span><span class="sxs-lookup"><span data-stu-id="38412-117">Disabled</span></span>
- <span data-ttu-id="38412-118">Vis</span><span class="sxs-lookup"><span data-stu-id="38412-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38412-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38412-119">-DefaultProfile</span></span>
<span data-ttu-id="38412-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="38412-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38412-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="38412-121">-ElasticPoolName</span></span>
<span data-ttu-id="38412-122">Anger namnet på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="38412-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="38412-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38412-123">-ResourceGroupName</span></span>
<span data-ttu-id="38412-124">Anger namnet på resurs gruppen för den server som innehåller den här elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="38412-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="38412-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38412-125">-ServerName</span></span>
<span data-ttu-id="38412-126">Anger namnet på den server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="38412-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="38412-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38412-127">-Confirm</span></span>
<span data-ttu-id="38412-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38412-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38412-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38412-129">-WhatIf</span></span>
<span data-ttu-id="38412-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38412-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38412-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38412-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38412-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38412-132">CommonParameters</span></span>
<span data-ttu-id="38412-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38412-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38412-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38412-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38412-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38412-135">INPUTS</span></span>

### <span data-ttu-id="38412-136">System. String</span><span class="sxs-lookup"><span data-stu-id="38412-136">System.String</span></span>

### <span data-ttu-id="38412-137">Microsoft. Azure. commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="38412-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="38412-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38412-138">OUTPUTS</span></span>

### <span data-ttu-id="38412-139">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="38412-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="38412-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38412-140">NOTES</span></span>
* <span data-ttu-id="38412-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, elastisk pool, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="38412-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="38412-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38412-142">RELATED LINKS</span></span>

[<span data-ttu-id="38412-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="38412-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="38412-144">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="38412-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
