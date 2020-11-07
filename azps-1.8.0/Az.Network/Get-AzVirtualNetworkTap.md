---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: df4da43c1a8edf0c3c887e4acdd009593984c048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748191"
---
# <span data-ttu-id="7db12-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7db12-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="7db12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7db12-102">SYNOPSIS</span></span>
<span data-ttu-id="7db12-103">Hämtar ett virtuellt nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="7db12-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="7db12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7db12-104">SYNTAX</span></span>

### <span data-ttu-id="7db12-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7db12-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db12-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db12-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7db12-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7db12-107">DESCRIPTION</span></span>
<span data-ttu-id="7db12-108">Cmdleten **Get-AzVirtualNetworkTap** får ett Azure Virtual Network-tryck eller en lista över de virtuella Azure-nätverks knackningarna i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7db12-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="7db12-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7db12-109">EXAMPLES</span></span>

### <span data-ttu-id="7db12-110">Exempel 1: Hämta ett virtuellt nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="7db12-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="7db12-111">Det här kommandot får en VirtualNetwork för att trycka på "VirtualTap1" i "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="7db12-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="7db12-112">Exempel 2: få igång alla virtuella nätverk genom att använda filtrering</span><span class="sxs-lookup"><span data-stu-id="7db12-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="7db12-113">Det här kommandot får alla VirtualNetwork tryck referenser som börjar med "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="7db12-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="7db12-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7db12-114">PARAMETERS</span></span>

### <span data-ttu-id="7db12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db12-115">-DefaultProfile</span></span>
<span data-ttu-id="7db12-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7db12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7db12-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7db12-117">-Name</span></span>
<span data-ttu-id="7db12-118">Namnet på tryckningen.</span><span class="sxs-lookup"><span data-stu-id="7db12-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7db12-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db12-119">-ResourceGroupName</span></span>
<span data-ttu-id="7db12-120">Resurs grupps namnet för det virtuella nätverkets tryck.</span><span class="sxs-lookup"><span data-stu-id="7db12-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7db12-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7db12-121">-ResourceId</span></span>
<span data-ttu-id="7db12-122">ResourceId för VirtualNetworkTap-resursen</span><span class="sxs-lookup"><span data-stu-id="7db12-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="7db12-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7db12-123">-Confirm</span></span>
<span data-ttu-id="7db12-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7db12-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db12-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db12-125">-WhatIf</span></span>
<span data-ttu-id="7db12-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7db12-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7db12-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7db12-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db12-128">CommonParameters</span></span>
<span data-ttu-id="7db12-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db12-130">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7db12-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db12-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7db12-131">INPUTS</span></span>

### <span data-ttu-id="7db12-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7db12-132">System.String</span></span>

## <span data-ttu-id="7db12-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7db12-133">OUTPUTS</span></span>

### <span data-ttu-id="7db12-134">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7db12-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="7db12-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7db12-135">NOTES</span></span>

## <span data-ttu-id="7db12-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7db12-136">RELATED LINKS</span></span>

[<span data-ttu-id="7db12-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7db12-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="7db12-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7db12-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="7db12-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7db12-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)