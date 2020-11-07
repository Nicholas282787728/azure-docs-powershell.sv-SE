---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 69a9fd259350238175016b3245d22022845a9f51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919476"
---
# <span data-ttu-id="e3016-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3016-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e3016-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3016-102">SYNOPSIS</span></span>
<span data-ttu-id="e3016-103">Uppdaterar en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="e3016-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="e3016-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3016-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3016-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3016-105">DESCRIPTION</span></span>
<span data-ttu-id="e3016-106">Cmdleten **set-AzServiceEndpointPolicyDefinition** skapa en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="e3016-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="e3016-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3016-107">EXAMPLES</span></span>

### <span data-ttu-id="e3016-108">Exempel 1: uppdaterar en princip definition för tjänste slut punkter i en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="e3016-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="e3016-109">Det här kommandot uppdaterar en princip definition för tjänste slut punkter med namnet Policydef1 i policyn för tjänste slut punkter som definieras av objektet $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="e3016-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="e3016-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3016-110">PARAMETERS</span></span>

### <span data-ttu-id="e3016-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3016-111">-DefaultProfile</span></span>
<span data-ttu-id="e3016-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3016-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3016-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e3016-113">-Description</span></span>
<span data-ttu-id="e3016-114">Beskrivning av definitionen</span><span class="sxs-lookup"><span data-stu-id="e3016-114">The description of the definition</span></span>

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

### <span data-ttu-id="e3016-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3016-115">-Name</span></span>
<span data-ttu-id="e3016-116">Namnet på regeln</span><span class="sxs-lookup"><span data-stu-id="e3016-116">The name of the rule</span></span>

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

### <span data-ttu-id="e3016-117">-Service</span><span class="sxs-lookup"><span data-stu-id="e3016-117">-Service</span></span>
<span data-ttu-id="e3016-118">Namn på tjänsten</span><span class="sxs-lookup"><span data-stu-id="e3016-118">Name of the service</span></span>

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

### <span data-ttu-id="e3016-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e3016-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e3016-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3016-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="e3016-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="e3016-121">-ServiceResource</span></span>
<span data-ttu-id="e3016-122">Lista över tjänst resurser</span><span class="sxs-lookup"><span data-stu-id="e3016-122">List of service resources</span></span>

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

### <span data-ttu-id="e3016-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3016-123">-Confirm</span></span>
<span data-ttu-id="e3016-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3016-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3016-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3016-125">-WhatIf</span></span>
<span data-ttu-id="e3016-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3016-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3016-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3016-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3016-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3016-128">CommonParameters</span></span>
<span data-ttu-id="e3016-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3016-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3016-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3016-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3016-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3016-131">INPUTS</span></span>

### <span data-ttu-id="e3016-132">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e3016-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e3016-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3016-133">OUTPUTS</span></span>

### <span data-ttu-id="e3016-134">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e3016-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e3016-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3016-135">NOTES</span></span>

## <span data-ttu-id="e3016-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3016-136">RELATED LINKS</span></span>

[<span data-ttu-id="e3016-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3016-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e3016-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3016-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e3016-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3016-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e3016-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3016-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
