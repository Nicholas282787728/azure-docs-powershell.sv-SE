---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: b76e17169bdea8e25c1b861cd7de802d877455f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575180"
---
# <span data-ttu-id="2d847-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2d847-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="2d847-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d847-102">SYNOPSIS</span></span>
<span data-ttu-id="2d847-103">Startar en samling av IIS-loggar från datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2d847-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d847-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d847-104">SYNTAX</span></span>

### <span data-ttu-id="2d847-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="2d847-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d847-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d847-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d847-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d847-107">DESCRIPTION</span></span>
<span data-ttu-id="2d847-108">Cmdleten **Enable-AzureRmOperationalInsightsIISLogCollection** startar en samling av Internet Information Services (IIS)-loggar från anslutna datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2d847-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="2d847-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d847-109">EXAMPLES</span></span>

## <span data-ttu-id="2d847-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d847-110">PARAMETERS</span></span>

### <span data-ttu-id="2d847-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d847-111">-DefaultProfile</span></span>
<span data-ttu-id="2d847-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2d847-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d847-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d847-113">-ResourceGroupName</span></span>
<span data-ttu-id="2d847-114">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="2d847-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="2d847-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="2d847-115">-Workspace</span></span>
<span data-ttu-id="2d847-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2d847-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d847-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d847-117">-WorkspaceName</span></span>
<span data-ttu-id="2d847-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2d847-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d847-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d847-119">-Confirm</span></span>
<span data-ttu-id="2d847-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d847-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d847-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d847-121">-WhatIf</span></span>
<span data-ttu-id="2d847-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d847-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d847-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d847-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d847-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d847-124">CommonParameters</span></span>
<span data-ttu-id="2d847-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d847-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d847-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d847-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d847-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d847-127">INPUTS</span></span>

### <span data-ttu-id="2d847-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d847-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="2d847-129">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d847-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="2d847-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d847-130">System.String</span></span>

## <span data-ttu-id="2d847-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d847-131">OUTPUTS</span></span>

### <span data-ttu-id="2d847-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2d847-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2d847-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d847-133">NOTES</span></span>

## <span data-ttu-id="2d847-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d847-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d847-135">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2d847-135">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


