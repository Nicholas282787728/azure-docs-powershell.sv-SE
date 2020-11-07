---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 75cf6bac1913a2baa55a28135ba2d59f5ceaa07f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919478"
---
# <span data-ttu-id="75f9e-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="75f9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="75f9e-103">Uppdaterar en policy för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="75f9e-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="75f9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75f9e-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75f9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75f9e-105">DESCRIPTION</span></span>
<span data-ttu-id="75f9e-106">Cmdleten **set-AzServiceEndpointPolicy** skapar en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="75f9e-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="75f9e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75f9e-107">EXAMPLES</span></span>

### <span data-ttu-id="75f9e-108">Exempel 1: anger en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="75f9e-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="75f9e-109">Det här kommandot uppdaterar en tjänst slut punkts princip med namnet Policy1 som definieras av objektet $serviceEndpointPolicy tillhör resourcegroup "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="75f9e-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="75f9e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75f9e-110">PARAMETERS</span></span>

### <span data-ttu-id="75f9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f9e-111">-DefaultProfile</span></span>
<span data-ttu-id="75f9e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75f9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75f9e-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="75f9e-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="75f9e-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75f9e-115">-Confirm</span></span>
<span data-ttu-id="75f9e-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75f9e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f9e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f9e-117">-WhatIf</span></span>
<span data-ttu-id="75f9e-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75f9e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75f9e-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75f9e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f9e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f9e-120">CommonParameters</span></span>
<span data-ttu-id="75f9e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f9e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f9e-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f9e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f9e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75f9e-123">INPUTS</span></span>

### <span data-ttu-id="75f9e-124">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="75f9e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75f9e-125">OUTPUTS</span></span>

### <span data-ttu-id="75f9e-126">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="75f9e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75f9e-127">NOTES</span></span>

## <span data-ttu-id="75f9e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75f9e-128">RELATED LINKS</span></span>

[<span data-ttu-id="75f9e-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="75f9e-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="75f9e-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75f9e-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
