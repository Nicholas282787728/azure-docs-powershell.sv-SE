---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 634beeaf33515ac5e89011ab47eaea34eccaa581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748001"
---
# <span data-ttu-id="70a78-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a78-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="70a78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70a78-102">SYNOPSIS</span></span>
<span data-ttu-id="70a78-103">Skapar en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="70a78-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="70a78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70a78-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70a78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70a78-105">DESCRIPTION</span></span>
<span data-ttu-id="70a78-106">**New-AzServiceEndpointPolicyDefinition-** cmdleten skapa en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="70a78-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="70a78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70a78-107">EXAMPLES</span></span>

### <span data-ttu-id="70a78-108">Exempel 1: skapar en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="70a78-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="70a78-109">Det här kommandot skapar princip definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1, service Microsoft. Storage, tjänst resurser prenumerationer/sub1 och beskrivning "ny definition" som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policydef variabeln.</span><span class="sxs-lookup"><span data-stu-id="70a78-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="70a78-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70a78-110">PARAMETERS</span></span>

### <span data-ttu-id="70a78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a78-111">-DefaultProfile</span></span>
<span data-ttu-id="70a78-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70a78-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70a78-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="70a78-113">-Description</span></span>
<span data-ttu-id="70a78-114">Beskrivning av definitionen</span><span class="sxs-lookup"><span data-stu-id="70a78-114">The description of the definition</span></span>

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

### <span data-ttu-id="70a78-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="70a78-115">-Name</span></span>
<span data-ttu-id="70a78-116">Namnet på tjänstens slut punkts princip</span><span class="sxs-lookup"><span data-stu-id="70a78-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="70a78-117">-Service</span><span class="sxs-lookup"><span data-stu-id="70a78-117">-Service</span></span>
<span data-ttu-id="70a78-118">Namn på tjänsten</span><span class="sxs-lookup"><span data-stu-id="70a78-118">Name of the service</span></span>

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

### <span data-ttu-id="70a78-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="70a78-119">-ServiceResource</span></span>
<span data-ttu-id="70a78-120">Lista över tjänst resurser</span><span class="sxs-lookup"><span data-stu-id="70a78-120">List of service resources</span></span>

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

### <span data-ttu-id="70a78-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70a78-121">-Confirm</span></span>
<span data-ttu-id="70a78-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70a78-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a78-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70a78-123">-WhatIf</span></span>
<span data-ttu-id="70a78-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70a78-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70a78-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70a78-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a78-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a78-126">CommonParameters</span></span>
<span data-ttu-id="70a78-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a78-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a78-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70a78-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a78-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70a78-129">INPUTS</span></span>

### <span data-ttu-id="70a78-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="70a78-130">None</span></span>

## <span data-ttu-id="70a78-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70a78-131">OUTPUTS</span></span>

### <span data-ttu-id="70a78-132">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a78-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="70a78-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70a78-133">NOTES</span></span>

## <span data-ttu-id="70a78-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70a78-134">RELATED LINKS</span></span>

[<span data-ttu-id="70a78-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a78-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="70a78-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a78-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="70a78-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a78-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="70a78-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a78-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
