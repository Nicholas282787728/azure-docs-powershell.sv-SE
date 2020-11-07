---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: d8ec5eed1b6c955720822e28bf54da68e9aefcac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919611"
---
# <span data-ttu-id="adfbb-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="adfbb-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="adfbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adfbb-102">SYNOPSIS</span></span>
<span data-ttu-id="adfbb-103">Tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="adfbb-103">Deletes a data source.</span></span>

## <span data-ttu-id="adfbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adfbb-104">SYNTAX</span></span>

### <span data-ttu-id="adfbb-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="adfbb-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adfbb-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="adfbb-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adfbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adfbb-107">DESCRIPTION</span></span>
<span data-ttu-id="adfbb-108">Cmdleten **Remove-AzOperationalInsightsDataSource** tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="adfbb-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="adfbb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adfbb-109">EXAMPLES</span></span>

## <span data-ttu-id="adfbb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adfbb-110">PARAMETERS</span></span>

### <span data-ttu-id="adfbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfbb-111">-DefaultProfile</span></span>
<span data-ttu-id="adfbb-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="adfbb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adfbb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="adfbb-113">-Force</span></span>
<span data-ttu-id="adfbb-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="adfbb-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfbb-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="adfbb-115">-Name</span></span>
<span data-ttu-id="adfbb-116">Anger namnet på den data källa som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="adfbb-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adfbb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adfbb-117">-ResourceGroupName</span></span>
<span data-ttu-id="adfbb-118">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="adfbb-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adfbb-119">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="adfbb-119">-Workspace</span></span>
<span data-ttu-id="adfbb-120">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="adfbb-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adfbb-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="adfbb-121">-WorkspaceName</span></span>
<span data-ttu-id="adfbb-122">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="adfbb-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adfbb-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="adfbb-123">-Confirm</span></span>
<span data-ttu-id="adfbb-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adfbb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adfbb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adfbb-125">-WhatIf</span></span>
<span data-ttu-id="adfbb-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="adfbb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adfbb-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="adfbb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adfbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfbb-128">CommonParameters</span></span>
<span data-ttu-id="adfbb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adfbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adfbb-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adfbb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfbb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adfbb-131">INPUTS</span></span>

### <span data-ttu-id="adfbb-132">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="adfbb-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="adfbb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="adfbb-133">System.String</span></span>

## <span data-ttu-id="adfbb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adfbb-134">OUTPUTS</span></span>

### <span data-ttu-id="adfbb-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="adfbb-135">System.Void</span></span>

## <span data-ttu-id="adfbb-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adfbb-136">NOTES</span></span>
* <span data-ttu-id="adfbb-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="adfbb-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="adfbb-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adfbb-138">RELATED LINKS</span></span>

[<span data-ttu-id="adfbb-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="adfbb-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="adfbb-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="adfbb-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


