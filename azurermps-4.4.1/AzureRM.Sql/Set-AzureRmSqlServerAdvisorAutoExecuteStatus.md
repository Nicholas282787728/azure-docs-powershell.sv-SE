---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579704"
---
# <span data-ttu-id="3d9c7-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3d9c7-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="3d9c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9c7-103">Uppdaterar status för automatisk körning för en Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d9c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d9c7-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d9c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d9c7-105">DESCRIPTION</span></span>
<span data-ttu-id="3d9c7-106">Cmdleten **set-AzureRmSqlServerAdvisorAutoExecuteStatus** anger egenskapen AutoExecute för en Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="3d9c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d9c7-107">EXAMPLES</span></span>

### <span data-ttu-id="3d9c7-108">Exempel 1: Aktivera automatisk körning för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="3d9c7-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="3d9c7-109">Det här kommandot aktiverar statusen Autostart för en rådgivare som heter CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="3d9c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d9c7-110">PARAMETERS</span></span>

### <span data-ttu-id="3d9c7-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="3d9c7-111">-AdvisorName</span></span>
<span data-ttu-id="3d9c7-112">Anger namnet på den rådgivare för vilken denna cmdlet uppdaterar statusen för automatisk körning.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="3d9c7-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3d9c7-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="3d9c7-114">Anger det värde som denna cmdlet uppdaterar status för automatisk körning för.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="3d9c7-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3d9c7-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d9c7-116">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="3d9c7-116">Enabled</span></span>
- <span data-ttu-id="3d9c7-117">Aktiv</span><span class="sxs-lookup"><span data-stu-id="3d9c7-117">Disabled</span></span>
- <span data-ttu-id="3d9c7-118">Vis</span><span class="sxs-lookup"><span data-stu-id="3d9c7-118">Default</span></span>

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

### <span data-ttu-id="3d9c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d9c7-120">Anger namnet på serverns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="3d9c7-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d9c7-121">-ServerName</span></span>
<span data-ttu-id="3d9c7-122">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3d9c7-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d9c7-123">-Confirm</span></span>
<span data-ttu-id="3d9c7-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d9c7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d9c7-125">-WhatIf</span></span>
<span data-ttu-id="3d9c7-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d9c7-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d9c7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9c7-128">-DefaultProfile</span></span>
<span data-ttu-id="3d9c7-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d9c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9c7-130">CommonParameters</span></span>
<span data-ttu-id="3d9c7-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9c7-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9c7-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d9c7-133">INPUTS</span></span>

## <span data-ttu-id="3d9c7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d9c7-134">OUTPUTS</span></span>

### <span data-ttu-id="3d9c7-135">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="3d9c7-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="3d9c7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d9c7-136">NOTES</span></span>
* <span data-ttu-id="3d9c7-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, Server, MSSQL, rådgivare</span><span class="sxs-lookup"><span data-stu-id="3d9c7-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="3d9c7-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d9c7-138">RELATED LINKS</span></span>

[<span data-ttu-id="3d9c7-139">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="3d9c7-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="3d9c7-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3d9c7-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)