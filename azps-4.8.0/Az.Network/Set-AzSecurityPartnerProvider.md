---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258145"
---
# <span data-ttu-id="1e75b-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1e75b-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="1e75b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e75b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e75b-103">Sparar en ändrad Azure-SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="1e75b-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="1e75b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e75b-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e75b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e75b-105">DESCRIPTION</span></span>
<span data-ttu-id="1e75b-106">Cmdleten **set-AzSecurityPartnerProvider** uppdaterar en Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1e75b-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="1e75b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e75b-107">EXAMPLES</span></span>

### <span data-ttu-id="1e75b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1e75b-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="1e75b-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e75b-109">PARAMETERS</span></span>

### <span data-ttu-id="1e75b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e75b-110">-AsJob</span></span>
<span data-ttu-id="1e75b-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1e75b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e75b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e75b-112">-DefaultProfile</span></span>
<span data-ttu-id="1e75b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e75b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e75b-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1e75b-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="1e75b-115">SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1e75b-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e75b-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e75b-116">-Confirm</span></span>
<span data-ttu-id="1e75b-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e75b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e75b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e75b-118">-WhatIf</span></span>
<span data-ttu-id="1e75b-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e75b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e75b-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e75b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e75b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e75b-121">CommonParameters</span></span>
<span data-ttu-id="1e75b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e75b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e75b-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e75b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e75b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e75b-124">INPUTS</span></span>

### <span data-ttu-id="1e75b-125">Microsoft. Azure. commands. Networks. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1e75b-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="1e75b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e75b-126">OUTPUTS</span></span>

### <span data-ttu-id="1e75b-127">Microsoft. Azure. commands. Networks. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1e75b-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="1e75b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e75b-128">NOTES</span></span>

## <span data-ttu-id="1e75b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e75b-129">RELATED LINKS</span></span>