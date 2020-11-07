---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3677b580629360a9f38d808af8df9ec0694bcc61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748414"
---
# <span data-ttu-id="d48e1-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d48e1-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="d48e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d48e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d48e1-103">Lägger till en princip definition för tjänste slut punkter till en angiven princip.</span><span class="sxs-lookup"><span data-stu-id="d48e1-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="d48e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d48e1-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d48e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d48e1-105">DESCRIPTION</span></span>
<span data-ttu-id="d48e1-106">Cmdleten **Add-AzServiceEndpointPolicyDefinition** lägger till en definition för tjänste slut punkter till principen.</span><span class="sxs-lookup"><span data-stu-id="d48e1-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="d48e1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d48e1-107">EXAMPLES</span></span>

### <span data-ttu-id="d48e1-108">Exempel 1: uppdaterar en princip definition för tjänste slut punkter i en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="d48e1-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="d48e1-109">Det här kommandot uppdaterade policy definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1, service Microsoft. Storage, tjänst resurser prenumerationer/sub1 och beskrivning "ny definition" som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policydef variabeln.</span><span class="sxs-lookup"><span data-stu-id="d48e1-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="d48e1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d48e1-110">PARAMETERS</span></span>

### <span data-ttu-id="d48e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d48e1-111">-DefaultProfile</span></span>
<span data-ttu-id="d48e1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d48e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d48e1-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d48e1-113">-Description</span></span>
<span data-ttu-id="d48e1-114">Beskrivning av definitionen</span><span class="sxs-lookup"><span data-stu-id="d48e1-114">The description of the definition</span></span>

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

### <span data-ttu-id="d48e1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d48e1-115">-Name</span></span>
<span data-ttu-id="d48e1-116">Namnet på princip definitionen för tjänste slut punkten</span><span class="sxs-lookup"><span data-stu-id="d48e1-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="d48e1-117">-Service</span><span class="sxs-lookup"><span data-stu-id="d48e1-117">-Service</span></span>
<span data-ttu-id="d48e1-118">Namn på tjänsten</span><span class="sxs-lookup"><span data-stu-id="d48e1-118">Name of the service</span></span>

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

### <span data-ttu-id="d48e1-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d48e1-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d48e1-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d48e1-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="d48e1-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="d48e1-121">-ServiceResource</span></span>
<span data-ttu-id="d48e1-122">Lista över tjänst resurser</span><span class="sxs-lookup"><span data-stu-id="d48e1-122">List of service resources</span></span>

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

### <span data-ttu-id="d48e1-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d48e1-123">-Confirm</span></span>
<span data-ttu-id="d48e1-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d48e1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d48e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d48e1-125">-WhatIf</span></span>
<span data-ttu-id="d48e1-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d48e1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d48e1-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d48e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d48e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48e1-128">CommonParameters</span></span>
<span data-ttu-id="d48e1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d48e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48e1-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48e1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48e1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d48e1-131">INPUTS</span></span>

### <span data-ttu-id="d48e1-132">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d48e1-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d48e1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d48e1-133">OUTPUTS</span></span>

### <span data-ttu-id="d48e1-134">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d48e1-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d48e1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d48e1-135">NOTES</span></span>

## <span data-ttu-id="d48e1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d48e1-136">RELATED LINKS</span></span>

[<span data-ttu-id="d48e1-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d48e1-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="d48e1-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d48e1-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="d48e1-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d48e1-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="d48e1-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d48e1-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)