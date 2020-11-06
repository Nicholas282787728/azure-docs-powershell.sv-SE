---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576232"
---
# <span data-ttu-id="74efa-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="74efa-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="74efa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74efa-102">SYNOPSIS</span></span>
<span data-ttu-id="74efa-103">Hämtar ett virtuellt nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="74efa-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74efa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74efa-104">SYNTAX</span></span>

### <span data-ttu-id="74efa-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="74efa-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74efa-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74efa-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74efa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74efa-107">DESCRIPTION</span></span>
<span data-ttu-id="74efa-108">Cmdleten **Get-AzureRmVirtualNetworkTap** får ett Azure Virtual Network-tryck eller en lista över de virtuella Azure-nätverks knackningarna i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="74efa-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="74efa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74efa-109">EXAMPLES</span></span>

### <span data-ttu-id="74efa-110">Exempel 1: Hämta ett virtuellt nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="74efa-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="74efa-111">Det här kommandot får en VirtualNetwork för att trycka på "VirtualTap1" i "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="74efa-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="74efa-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74efa-112">PARAMETERS</span></span>

### <span data-ttu-id="74efa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74efa-113">-DefaultProfile</span></span>
<span data-ttu-id="74efa-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74efa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74efa-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="74efa-115">-Name</span></span>
<span data-ttu-id="74efa-116">Namnet på tryckningen.</span><span class="sxs-lookup"><span data-stu-id="74efa-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74efa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74efa-117">-ResourceGroupName</span></span>
<span data-ttu-id="74efa-118">Resurs grupps namnet för det virtuella nätverkets tryck.</span><span class="sxs-lookup"><span data-stu-id="74efa-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74efa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74efa-119">-ResourceId</span></span>
<span data-ttu-id="74efa-120">ResourceId för VirtualNetworkTap-resursen</span><span class="sxs-lookup"><span data-stu-id="74efa-120">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74efa-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74efa-121">-Confirm</span></span>
<span data-ttu-id="74efa-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74efa-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74efa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74efa-123">-WhatIf</span></span>
<span data-ttu-id="74efa-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74efa-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74efa-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74efa-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74efa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74efa-126">CommonParameters</span></span>
<span data-ttu-id="74efa-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74efa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74efa-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74efa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74efa-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74efa-129">INPUTS</span></span>

### <span data-ttu-id="74efa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74efa-130">System.String</span></span>

## <span data-ttu-id="74efa-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74efa-131">OUTPUTS</span></span>

### <span data-ttu-id="74efa-132">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="74efa-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="74efa-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74efa-133">NOTES</span></span>

## <span data-ttu-id="74efa-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74efa-134">RELATED LINKS</span></span>
