---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 27124aa859fc9c97a74a3ed401c67de328d93884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090973"
---
# <span data-ttu-id="c8057-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8057-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c8057-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8057-102">SYNOPSIS</span></span>
<span data-ttu-id="c8057-103">Skapar en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="c8057-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="c8057-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8057-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8057-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8057-105">DESCRIPTION</span></span>
<span data-ttu-id="c8057-106">**New-AzServiceEndpointPolicyDefinition-** cmdleten skapa en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="c8057-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="c8057-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8057-107">EXAMPLES</span></span>

### <span data-ttu-id="c8057-108">Exempel 1: skapar en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="c8057-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="c8057-109">Det här kommandot skapar princip definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1, service Microsoft. Storage, tjänst resurser prenumerationer/sub1 och beskrivning "ny definition" som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policydef variabeln.</span><span class="sxs-lookup"><span data-stu-id="c8057-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="c8057-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8057-110">PARAMETERS</span></span>

### <span data-ttu-id="c8057-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8057-111">-DefaultProfile</span></span>
<span data-ttu-id="c8057-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8057-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8057-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c8057-113">-Description</span></span>
<span data-ttu-id="c8057-114">Beskrivning av definitionen</span><span class="sxs-lookup"><span data-stu-id="c8057-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8057-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8057-115">-Name</span></span>
<span data-ttu-id="c8057-116">Namnet på tjänstens slut punkts princip</span><span class="sxs-lookup"><span data-stu-id="c8057-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8057-117">-Service</span><span class="sxs-lookup"><span data-stu-id="c8057-117">-Service</span></span>
<span data-ttu-id="c8057-118">Namn på tjänsten</span><span class="sxs-lookup"><span data-stu-id="c8057-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8057-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="c8057-119">-ServiceResource</span></span>
<span data-ttu-id="c8057-120">Lista över tjänst resurser</span><span class="sxs-lookup"><span data-stu-id="c8057-120">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8057-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8057-121">-Confirm</span></span>
<span data-ttu-id="c8057-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8057-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8057-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8057-123">-WhatIf</span></span>
<span data-ttu-id="c8057-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8057-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8057-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8057-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8057-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8057-126">CommonParameters</span></span>
<span data-ttu-id="c8057-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8057-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8057-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8057-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8057-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8057-129">INPUTS</span></span>

### <span data-ttu-id="c8057-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="c8057-130">None</span></span>

## <span data-ttu-id="c8057-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8057-131">OUTPUTS</span></span>

### <span data-ttu-id="c8057-132">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8057-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c8057-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8057-133">NOTES</span></span>

## <span data-ttu-id="c8057-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8057-134">RELATED LINKS</span></span>

[<span data-ttu-id="c8057-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8057-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c8057-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8057-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c8057-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8057-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c8057-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8057-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
