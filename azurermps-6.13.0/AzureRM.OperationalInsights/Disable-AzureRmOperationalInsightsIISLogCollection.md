---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 085aa91321f9e263e4fa5620f982beb01eab2b16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755470"
---
# <span data-ttu-id="26887-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="26887-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="26887-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26887-102">SYNOPSIS</span></span>
<span data-ttu-id="26887-103">Stoppar insamling av IIS-loggar från datorer.</span><span class="sxs-lookup"><span data-stu-id="26887-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26887-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26887-104">SYNTAX</span></span>

### <span data-ttu-id="26887-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="26887-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26887-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="26887-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26887-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26887-107">DESCRIPTION</span></span>
<span data-ttu-id="26887-108">Cmdleten **disable-AzureRmOperationalInsightsIISLogCollection** stoppar samlingen Internet Information Services (IIS)-loggar från anslutna datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="26887-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="26887-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26887-109">EXAMPLES</span></span>

## <span data-ttu-id="26887-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26887-110">PARAMETERS</span></span>

### <span data-ttu-id="26887-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26887-111">-DefaultProfile</span></span>
<span data-ttu-id="26887-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26887-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26887-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26887-113">-ResourceGroupName</span></span>
<span data-ttu-id="26887-114">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="26887-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="26887-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="26887-115">-Workspace</span></span>
<span data-ttu-id="26887-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="26887-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="26887-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26887-117">-WorkspaceName</span></span>
<span data-ttu-id="26887-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="26887-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="26887-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26887-119">-Confirm</span></span>
<span data-ttu-id="26887-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26887-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26887-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26887-121">-WhatIf</span></span>
<span data-ttu-id="26887-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26887-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26887-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26887-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26887-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26887-124">CommonParameters</span></span>
<span data-ttu-id="26887-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26887-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26887-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26887-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26887-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26887-127">INPUTS</span></span>

### <span data-ttu-id="26887-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="26887-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="26887-129">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26887-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="26887-130">System. String</span><span class="sxs-lookup"><span data-stu-id="26887-130">System.String</span></span>

## <span data-ttu-id="26887-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26887-131">OUTPUTS</span></span>

### <span data-ttu-id="26887-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="26887-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="26887-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26887-133">NOTES</span></span>
* <span data-ttu-id="26887-134">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="26887-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="26887-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26887-135">RELATED LINKS</span></span>

[<span data-ttu-id="26887-136">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="26887-136">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


