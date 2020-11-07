---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa3aff9a1e471445c49cbfb23b5799a97c54025d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746485"
---
# <span data-ttu-id="94473-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="94473-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="94473-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94473-102">SYNOPSIS</span></span>
<span data-ttu-id="94473-103">Uppdaterar status för automatisk körning för en Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="94473-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="94473-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94473-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94473-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94473-105">DESCRIPTION</span></span>
<span data-ttu-id="94473-106">Cmdleten **set-AzSqlServerAdvisorAutoExecuteStatus** anger egenskapen AutoExecute för en Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="94473-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="94473-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94473-107">EXAMPLES</span></span>

### <span data-ttu-id="94473-108">Exempel 1: Aktivera automatisk körning för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="94473-108">Example 1: Enable auto execute for an Advisor</span></span>
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

<span data-ttu-id="94473-109">Det här kommandot aktiverar statusen Autostart för en rådgivare som heter CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="94473-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="94473-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94473-110">PARAMETERS</span></span>

### <span data-ttu-id="94473-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="94473-111">-AdvisorName</span></span>
<span data-ttu-id="94473-112">Anger namnet på den rådgivare för vilken denna cmdlet uppdaterar statusen för automatisk körning.</span><span class="sxs-lookup"><span data-stu-id="94473-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="94473-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="94473-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="94473-114">Anger det värde som denna cmdlet uppdaterar status för automatisk körning för.</span><span class="sxs-lookup"><span data-stu-id="94473-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="94473-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="94473-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94473-116">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="94473-116">Enabled</span></span>
- <span data-ttu-id="94473-117">Aktiv</span><span class="sxs-lookup"><span data-stu-id="94473-117">Disabled</span></span>
- <span data-ttu-id="94473-118">Vis</span><span class="sxs-lookup"><span data-stu-id="94473-118">Default</span></span>

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

### <span data-ttu-id="94473-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94473-119">-DefaultProfile</span></span>
<span data-ttu-id="94473-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="94473-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94473-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94473-121">-ResourceGroupName</span></span>
<span data-ttu-id="94473-122">Anger namnet på serverns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="94473-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="94473-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94473-123">-ServerName</span></span>
<span data-ttu-id="94473-124">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="94473-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="94473-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94473-125">-Confirm</span></span>
<span data-ttu-id="94473-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94473-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94473-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94473-127">-WhatIf</span></span>
<span data-ttu-id="94473-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94473-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94473-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94473-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94473-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94473-130">CommonParameters</span></span>
<span data-ttu-id="94473-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94473-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94473-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94473-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94473-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94473-133">INPUTS</span></span>

### <span data-ttu-id="94473-134">System. String</span><span class="sxs-lookup"><span data-stu-id="94473-134">System.String</span></span>

### <span data-ttu-id="94473-135">Microsoft. Azure. commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="94473-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="94473-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94473-136">OUTPUTS</span></span>

### <span data-ttu-id="94473-137">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="94473-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="94473-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94473-138">NOTES</span></span>
* <span data-ttu-id="94473-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, Server, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="94473-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="94473-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94473-140">RELATED LINKS</span></span>

[<span data-ttu-id="94473-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="94473-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="94473-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="94473-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)