---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323802"
---
# <span data-ttu-id="fa732-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fa732-101">New-AzIpGroup</span></span>

## <span data-ttu-id="fa732-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa732-102">SYNOPSIS</span></span>
<span data-ttu-id="fa732-103">Skapar en Azure-IpGroup.</span><span class="sxs-lookup"><span data-stu-id="fa732-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="fa732-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa732-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa732-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa732-105">DESCRIPTION</span></span>
<span data-ttu-id="fa732-106">Cmdleten **New-AzIpGroup** skapar en Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="fa732-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="fa732-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa732-107">EXAMPLES</span></span>

### <span data-ttu-id="fa732-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa732-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="fa732-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fa732-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="fa732-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa732-110">PARAMETERS</span></span>

### <span data-ttu-id="fa732-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa732-111">-AsJob</span></span>
<span data-ttu-id="fa732-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fa732-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa732-113">-DefaultProfile</span></span>
<span data-ttu-id="fa732-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa732-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fa732-115">-Force</span></span>
<span data-ttu-id="fa732-116">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="fa732-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="fa732-117">-IpAddress</span></span>
<span data-ttu-id="fa732-118">IP-adresser definierade i IpGroup</span><span class="sxs-lookup"><span data-stu-id="fa732-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="fa732-119">-Location</span></span>
<span data-ttu-id="fa732-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="fa732-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa732-121">-Name</span></span>
<span data-ttu-id="fa732-122">Namnet på ipgroup.</span><span class="sxs-lookup"><span data-stu-id="fa732-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa732-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa732-124">Resurs grupps namnet för ipgroup.</span><span class="sxs-lookup"><span data-stu-id="fa732-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fa732-125">-Tag</span></span>
<span data-ttu-id="fa732-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="fa732-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa732-127">-Confirm</span></span>
<span data-ttu-id="fa732-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa732-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa732-129">-WhatIf</span></span>
<span data-ttu-id="fa732-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa732-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa732-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa732-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa732-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa732-132">CommonParameters</span></span>
<span data-ttu-id="fa732-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa732-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa732-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa732-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa732-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa732-135">INPUTS</span></span>

### <span data-ttu-id="fa732-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fa732-136">System.String</span></span>

### <span data-ttu-id="fa732-137">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fa732-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fa732-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="fa732-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fa732-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa732-139">OUTPUTS</span></span>

### <span data-ttu-id="fa732-140">Microsoft. Azure. commands. Networks. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="fa732-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="fa732-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa732-141">NOTES</span></span>

## <span data-ttu-id="fa732-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa732-142">RELATED LINKS</span></span>
