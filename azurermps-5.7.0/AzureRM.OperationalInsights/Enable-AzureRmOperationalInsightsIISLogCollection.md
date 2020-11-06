---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 417bc080d707c3da02dd8a0083fb707f79d0a999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577112"
---
# <span data-ttu-id="2854b-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2854b-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="2854b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2854b-102">SYNOPSIS</span></span>
<span data-ttu-id="2854b-103">Startar en samling av IIS-loggar från datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2854b-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2854b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2854b-104">SYNTAX</span></span>

### <span data-ttu-id="2854b-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="2854b-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2854b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2854b-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2854b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2854b-107">DESCRIPTION</span></span>
<span data-ttu-id="2854b-108">Cmdleten **Enable-AzureRmOperationalInsightsIISLogCollection** startar en samling av Internet Information Services (IIS)-loggar från anslutna datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2854b-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="2854b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2854b-109">EXAMPLES</span></span>

## <span data-ttu-id="2854b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2854b-110">PARAMETERS</span></span>

### <span data-ttu-id="2854b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2854b-111">-DefaultProfile</span></span>
<span data-ttu-id="2854b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2854b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2854b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2854b-113">-ResourceGroupName</span></span>
<span data-ttu-id="2854b-114">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="2854b-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2854b-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="2854b-115">-Workspace</span></span>
<span data-ttu-id="2854b-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2854b-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2854b-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2854b-117">-WorkspaceName</span></span>
<span data-ttu-id="2854b-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2854b-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2854b-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2854b-119">-Confirm</span></span>
<span data-ttu-id="2854b-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2854b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2854b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2854b-121">-WhatIf</span></span>
<span data-ttu-id="2854b-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2854b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2854b-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2854b-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2854b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2854b-124">CommonParameters</span></span>
<span data-ttu-id="2854b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2854b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2854b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2854b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2854b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2854b-127">INPUTS</span></span>

### <span data-ttu-id="2854b-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2854b-128">PSWorkspace</span></span>
<span data-ttu-id="2854b-129">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2854b-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="2854b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2854b-130">OUTPUTS</span></span>

### <span data-ttu-id="2854b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2854b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2854b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2854b-132">NOTES</span></span>

## <span data-ttu-id="2854b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2854b-133">RELATED LINKS</span></span>

[<span data-ttu-id="2854b-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2854b-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


