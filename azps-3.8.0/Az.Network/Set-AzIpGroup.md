---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090234"
---
# <span data-ttu-id="a95c9-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a95c9-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="a95c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a95c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a95c9-103">Sparar en modifierad brand vägg.</span><span class="sxs-lookup"><span data-stu-id="a95c9-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="a95c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a95c9-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a95c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a95c9-105">DESCRIPTION</span></span>
<span data-ttu-id="a95c9-106">Cmdleten **set-AzIpGroup** uppdaterar en Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="a95c9-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="a95c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a95c9-107">EXAMPLES</span></span>

### <span data-ttu-id="a95c9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a95c9-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="a95c9-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a95c9-109">PARAMETERS</span></span>

### <span data-ttu-id="a95c9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a95c9-110">-AsJob</span></span>
<span data-ttu-id="a95c9-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a95c9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a95c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95c9-112">-DefaultProfile</span></span>
<span data-ttu-id="a95c9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a95c9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95c9-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="a95c9-114">-IpGroup</span></span>
<span data-ttu-id="a95c9-115">IpGroup</span><span class="sxs-lookup"><span data-stu-id="a95c9-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95c9-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a95c9-116">-Confirm</span></span>
<span data-ttu-id="a95c9-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a95c9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95c9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95c9-118">-WhatIf</span></span>
<span data-ttu-id="a95c9-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a95c9-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a95c9-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a95c9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95c9-121">CommonParameters</span></span>
<span data-ttu-id="a95c9-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95c9-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a95c9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95c9-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a95c9-124">INPUTS</span></span>

### <span data-ttu-id="a95c9-125">Microsoft. Azure. commands. Networks. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a95c9-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a95c9-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a95c9-126">OUTPUTS</span></span>

### <span data-ttu-id="a95c9-127">Microsoft. Azure. commands. Networks. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a95c9-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a95c9-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a95c9-128">NOTES</span></span>

## <span data-ttu-id="a95c9-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a95c9-129">RELATED LINKS</span></span>