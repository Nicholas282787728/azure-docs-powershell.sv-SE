---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325643"
---
# <span data-ttu-id="2338d-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2338d-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="2338d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2338d-102">SYNOPSIS</span></span>
<span data-ttu-id="2338d-103">Startar en samling av IIS-loggar från datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2338d-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="2338d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2338d-104">SYNTAX</span></span>

### <span data-ttu-id="2338d-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="2338d-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2338d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2338d-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2338d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2338d-107">DESCRIPTION</span></span>
<span data-ttu-id="2338d-108">Cmdleten **Enable-AzOperationalInsightsIISLogCollection** startar en samling av Internet Information Services (IIS)-loggar från anslutna datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2338d-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="2338d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2338d-109">EXAMPLES</span></span>

## <span data-ttu-id="2338d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2338d-110">PARAMETERS</span></span>

### <span data-ttu-id="2338d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2338d-111">-DefaultProfile</span></span>
<span data-ttu-id="2338d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2338d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2338d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2338d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2338d-114">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="2338d-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="2338d-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="2338d-115">-Workspace</span></span>
<span data-ttu-id="2338d-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2338d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2338d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2338d-117">-WorkspaceName</span></span>
<span data-ttu-id="2338d-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2338d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2338d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2338d-119">-Confirm</span></span>
<span data-ttu-id="2338d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2338d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2338d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2338d-121">-WhatIf</span></span>
<span data-ttu-id="2338d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2338d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2338d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2338d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2338d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2338d-124">CommonParameters</span></span>
<span data-ttu-id="2338d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2338d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2338d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2338d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2338d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2338d-127">INPUTS</span></span>

### <span data-ttu-id="2338d-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2338d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2338d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2338d-129">System.String</span></span>

## <span data-ttu-id="2338d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2338d-130">OUTPUTS</span></span>

### <span data-ttu-id="2338d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2338d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2338d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2338d-132">NOTES</span></span>

## <span data-ttu-id="2338d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2338d-133">RELATED LINKS</span></span>

[<span data-ttu-id="2338d-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2338d-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


