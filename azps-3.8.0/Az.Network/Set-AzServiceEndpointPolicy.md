---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928053"
---
# <span data-ttu-id="c1cb3-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="c1cb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cb3-103">Uppdaterar en policy för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="c1cb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1cb3-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1cb3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="c1cb3-106">Cmdleten **set-AzServiceEndpointPolicy** skapar en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="c1cb3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1cb3-107">EXAMPLES</span></span>

### <span data-ttu-id="c1cb3-108">Exempel 1: anger en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="c1cb3-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="c1cb3-109">Det här kommandot uppdaterar en tjänst slut punkts princip med namnet Policy1 som definieras av objektet $serviceEndpointPolicy tillhör resourcegroup "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="c1cb3-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="c1cb3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1cb3-110">PARAMETERS</span></span>

### <span data-ttu-id="c1cb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cb3-111">-DefaultProfile</span></span>
<span data-ttu-id="c1cb3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1cb3-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c1cb3-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb3-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1cb3-115">-Confirm</span></span>
<span data-ttu-id="c1cb3-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1cb3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1cb3-117">-WhatIf</span></span>
<span data-ttu-id="c1cb3-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1cb3-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1cb3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cb3-120">CommonParameters</span></span>
<span data-ttu-id="c1cb3-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cb3-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1cb3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cb3-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1cb3-123">INPUTS</span></span>

### <span data-ttu-id="c1cb3-124">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c1cb3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1cb3-125">OUTPUTS</span></span>

### <span data-ttu-id="c1cb3-126">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c1cb3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1cb3-127">NOTES</span></span>

## <span data-ttu-id="c1cb3-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1cb3-128">RELATED LINKS</span></span>

[<span data-ttu-id="c1cb3-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="c1cb3-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="c1cb3-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1cb3-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)