---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399672"
---
# <span data-ttu-id="463c9-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="463c9-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="463c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="463c9-102">SYNOPSIS</span></span>
<span data-ttu-id="463c9-103">Hämtar en policy definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="463c9-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="463c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="463c9-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="463c9-105">DESCRIPTION</span></span>
<span data-ttu-id="463c9-106">Cmdleten **Get-AzServiceEndpointPolicyDefinition** hämtar en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="463c9-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="463c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="463c9-107">EXAMPLES</span></span>

### <span data-ttu-id="463c9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="463c9-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="463c9-109">Det här kommandot hämtar princip definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1 i ServiceEndpointPolicy $Policy lagrar den i $policydef-variabeln.</span><span class="sxs-lookup"><span data-stu-id="463c9-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="463c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="463c9-110">PARAMETERS</span></span>

### <span data-ttu-id="463c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463c9-111">-DefaultProfile</span></span>
<span data-ttu-id="463c9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="463c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="463c9-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="463c9-113">-Name</span></span>
<span data-ttu-id="463c9-114">Namnet på princip definitionen för tjänste slut punkten</span><span class="sxs-lookup"><span data-stu-id="463c9-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="463c9-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="463c9-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="463c9-116">Policy för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="463c9-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="463c9-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="463c9-117">-Confirm</span></span>
<span data-ttu-id="463c9-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="463c9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463c9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463c9-119">-WhatIf</span></span>
<span data-ttu-id="463c9-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="463c9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="463c9-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="463c9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463c9-122">CommonParameters</span></span>
<span data-ttu-id="463c9-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463c9-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="463c9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463c9-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="463c9-125">INPUTS</span></span>

### <span data-ttu-id="463c9-126">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="463c9-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="463c9-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="463c9-127">OUTPUTS</span></span>

### <span data-ttu-id="463c9-128">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="463c9-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="463c9-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="463c9-129">NOTES</span></span>

## <span data-ttu-id="463c9-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="463c9-130">RELATED LINKS</span></span>

[<span data-ttu-id="463c9-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="463c9-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="463c9-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="463c9-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="463c9-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="463c9-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="463c9-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="463c9-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
