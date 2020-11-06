---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 74178c9818cb5782c105e5566fd5e5dc44ef6526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585083"
---
# <span data-ttu-id="58777-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="58777-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="58777-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58777-102">SYNOPSIS</span></span>
<span data-ttu-id="58777-103">Startar en samling med anpassade loggar från Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="58777-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58777-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58777-104">SYNTAX</span></span>

### <span data-ttu-id="58777-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="58777-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58777-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="58777-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58777-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58777-107">DESCRIPTION</span></span>
<span data-ttu-id="58777-108">Cmdleten **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** startar en samling med anpassade loggar från anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="58777-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="58777-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58777-109">EXAMPLES</span></span>

## <span data-ttu-id="58777-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58777-110">PARAMETERS</span></span>

### <span data-ttu-id="58777-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58777-111">-DefaultProfile</span></span>
<span data-ttu-id="58777-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="58777-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58777-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58777-113">-ResourceGroupName</span></span>
<span data-ttu-id="58777-114">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="58777-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="58777-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="58777-115">-Workspace</span></span>
<span data-ttu-id="58777-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="58777-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="58777-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58777-117">-WorkspaceName</span></span>
<span data-ttu-id="58777-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="58777-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="58777-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58777-119">-Confirm</span></span>
<span data-ttu-id="58777-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58777-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58777-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58777-121">-WhatIf</span></span>
<span data-ttu-id="58777-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58777-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58777-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58777-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58777-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58777-124">CommonParameters</span></span>
<span data-ttu-id="58777-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58777-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58777-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58777-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58777-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58777-127">INPUTS</span></span>

### <span data-ttu-id="58777-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="58777-128">PSWorkspace</span></span>
<span data-ttu-id="58777-129">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="58777-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="58777-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58777-130">OUTPUTS</span></span>

### <span data-ttu-id="58777-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="58777-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="58777-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58777-132">NOTES</span></span>
* <span data-ttu-id="58777-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="58777-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="58777-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58777-134">RELATED LINKS</span></span>

[<span data-ttu-id="58777-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="58777-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


