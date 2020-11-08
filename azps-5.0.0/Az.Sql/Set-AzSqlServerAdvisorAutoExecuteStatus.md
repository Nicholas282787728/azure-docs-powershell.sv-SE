---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270190"
---
# <span data-ttu-id="22ebf-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="22ebf-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="22ebf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="22ebf-103">Uppdaterar status för automatisk körning för en Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="22ebf-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="22ebf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22ebf-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ebf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="22ebf-106">Cmdleten **set-AzSqlServerAdvisorAutoExecuteStatus** anger egenskapen AutoExecute för en Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="22ebf-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="22ebf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="22ebf-108">Exempel 1: Aktivera automatisk körning för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="22ebf-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="22ebf-109">Det här kommandot aktiverar statusen Autostart för en rådgivare som heter CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="22ebf-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="22ebf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22ebf-110">PARAMETERS</span></span>

### <span data-ttu-id="22ebf-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="22ebf-111">-AdvisorName</span></span>
<span data-ttu-id="22ebf-112">Anger namnet på den rådgivare för vilken denna cmdlet uppdaterar statusen för automatisk körning.</span><span class="sxs-lookup"><span data-stu-id="22ebf-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="22ebf-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="22ebf-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="22ebf-114">Anger det värde som denna cmdlet uppdaterar status för automatisk körning för.</span><span class="sxs-lookup"><span data-stu-id="22ebf-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="22ebf-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="22ebf-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22ebf-116">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="22ebf-116">Enabled</span></span>
- <span data-ttu-id="22ebf-117">Aktiv</span><span class="sxs-lookup"><span data-stu-id="22ebf-117">Disabled</span></span>
- <span data-ttu-id="22ebf-118">Vis</span><span class="sxs-lookup"><span data-stu-id="22ebf-118">Default</span></span>

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

### <span data-ttu-id="22ebf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ebf-119">-DefaultProfile</span></span>
<span data-ttu-id="22ebf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="22ebf-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22ebf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ebf-121">-ResourceGroupName</span></span>
<span data-ttu-id="22ebf-122">Anger namnet på serverns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="22ebf-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="22ebf-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22ebf-123">-ServerName</span></span>
<span data-ttu-id="22ebf-124">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="22ebf-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="22ebf-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22ebf-125">-Confirm</span></span>
<span data-ttu-id="22ebf-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22ebf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ebf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ebf-127">-WhatIf</span></span>
<span data-ttu-id="22ebf-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22ebf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ebf-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22ebf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ebf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ebf-130">CommonParameters</span></span>
<span data-ttu-id="22ebf-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ebf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ebf-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22ebf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ebf-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22ebf-133">INPUTS</span></span>

### <span data-ttu-id="22ebf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22ebf-134">System.String</span></span>

### <span data-ttu-id="22ebf-135">Microsoft. Azure. commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="22ebf-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="22ebf-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22ebf-136">OUTPUTS</span></span>

### <span data-ttu-id="22ebf-137">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="22ebf-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="22ebf-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22ebf-138">NOTES</span></span>
* <span data-ttu-id="22ebf-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, Server, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="22ebf-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="22ebf-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22ebf-140">RELATED LINKS</span></span>

[<span data-ttu-id="22ebf-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="22ebf-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="22ebf-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="22ebf-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
