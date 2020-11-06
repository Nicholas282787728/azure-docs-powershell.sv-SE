---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e9d5a7443c8a758cdc839826025d51fe57d55420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578792"
---
# <span data-ttu-id="3ca6f-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3ca6f-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="3ca6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ca6f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca6f-103">Tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ca6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ca6f-104">SYNTAX</span></span>

### <span data-ttu-id="3ca6f-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="3ca6f-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca6f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3ca6f-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca6f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ca6f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ca6f-108">Cmdleten **Remove-AzureRmOperationalInsightsDataSource** tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="3ca6f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ca6f-109">EXAMPLES</span></span>

## <span data-ttu-id="3ca6f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ca6f-110">PARAMETERS</span></span>

### <span data-ttu-id="3ca6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca6f-111">-DefaultProfile</span></span>
<span data-ttu-id="3ca6f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3ca6f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ca6f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ca6f-113">-Force</span></span>
<span data-ttu-id="3ca6f-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ca6f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ca6f-115">-Name</span></span>
<span data-ttu-id="3ca6f-116">Anger namnet på den data källa som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="3ca6f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca6f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ca6f-118">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="3ca6f-119">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="3ca6f-119">-Workspace</span></span>
<span data-ttu-id="3ca6f-120">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ca6f-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ca6f-121">-WorkspaceName</span></span>
<span data-ttu-id="3ca6f-122">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ca6f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ca6f-123">-Confirm</span></span>
<span data-ttu-id="3ca6f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca6f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca6f-125">-WhatIf</span></span>
<span data-ttu-id="3ca6f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca6f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca6f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca6f-128">CommonParameters</span></span>
<span data-ttu-id="3ca6f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca6f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca6f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca6f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca6f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ca6f-131">INPUTS</span></span>

### <span data-ttu-id="3ca6f-132">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ca6f-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="3ca6f-133">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ca6f-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="3ca6f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca6f-134">System.String</span></span>

## <span data-ttu-id="3ca6f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ca6f-135">OUTPUTS</span></span>

### <span data-ttu-id="3ca6f-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="3ca6f-136">System.Void</span></span>

## <span data-ttu-id="3ca6f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ca6f-137">NOTES</span></span>
* <span data-ttu-id="3ca6f-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="3ca6f-138">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3ca6f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ca6f-139">RELATED LINKS</span></span>

[<span data-ttu-id="3ca6f-140">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3ca6f-140">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="3ca6f-141">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3ca6f-141">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


