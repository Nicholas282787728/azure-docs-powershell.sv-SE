---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 9a22c275064068cff7d97d58a69e17548c764439
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575925"
---
# <span data-ttu-id="5239b-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5239b-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="5239b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5239b-102">SYNOPSIS</span></span>
<span data-ttu-id="5239b-103">Stoppar insamling av IIS-loggar från datorer.</span><span class="sxs-lookup"><span data-stu-id="5239b-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5239b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5239b-104">SYNTAX</span></span>

### <span data-ttu-id="5239b-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="5239b-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5239b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5239b-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5239b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5239b-107">DESCRIPTION</span></span>
<span data-ttu-id="5239b-108">Cmdleten **disable-AzureRmOperationalInsightsIISLogCollection** stoppar samlingen Internet Information Services (IIS)-loggar från anslutna datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="5239b-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="5239b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5239b-109">EXAMPLES</span></span>

## <span data-ttu-id="5239b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5239b-110">PARAMETERS</span></span>

### <span data-ttu-id="5239b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5239b-111">-ResourceGroupName</span></span>
<span data-ttu-id="5239b-112">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="5239b-112">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5239b-113">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="5239b-113">-Workspace</span></span>
<span data-ttu-id="5239b-114">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="5239b-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5239b-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5239b-115">-WorkspaceName</span></span>
<span data-ttu-id="5239b-116">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="5239b-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5239b-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5239b-117">-Confirm</span></span>
<span data-ttu-id="5239b-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5239b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5239b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5239b-119">-WhatIf</span></span>
<span data-ttu-id="5239b-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5239b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5239b-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5239b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5239b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5239b-122">-DefaultProfile</span></span>
<span data-ttu-id="5239b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5239b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5239b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5239b-124">CommonParameters</span></span>
<span data-ttu-id="5239b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5239b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5239b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5239b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5239b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5239b-127">INPUTS</span></span>

### <span data-ttu-id="5239b-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5239b-128">PSWorkspace</span></span>
<span data-ttu-id="5239b-129">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5239b-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="5239b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5239b-130">OUTPUTS</span></span>

### <span data-ttu-id="5239b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5239b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5239b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5239b-132">NOTES</span></span>
* <span data-ttu-id="5239b-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="5239b-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5239b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5239b-134">RELATED LINKS</span></span>

[<span data-ttu-id="5239b-135">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5239b-135">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


