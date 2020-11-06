---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581703"
---
# <span data-ttu-id="8a1cc-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a1cc-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8a1cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1cc-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="8a1cc-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a1cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a1cc-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a1cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a1cc-105">DESCRIPTION</span></span>
<span data-ttu-id="8a1cc-106">Cmdleten **Get-AzureRmServiceEndpointPolicyDefinition** hämtar en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="8a1cc-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="8a1cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a1cc-107">EXAMPLES</span></span>

### <span data-ttu-id="8a1cc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a1cc-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="8a1cc-109">Det här kommandot hämtar princip definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1 i ServiceEndpointPolicy $Policy lagrar den i $policydef-variabeln.</span><span class="sxs-lookup"><span data-stu-id="8a1cc-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="8a1cc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a1cc-110">PARAMETERS</span></span>

### <span data-ttu-id="8a1cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1cc-111">-DefaultProfile</span></span>
<span data-ttu-id="8a1cc-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a1cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1cc-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a1cc-113">-Name</span></span>
<span data-ttu-id="8a1cc-114">Namnet på princip definitionen för tjänste slut punkten</span><span class="sxs-lookup"><span data-stu-id="8a1cc-114">The name of the service endpoint policy definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1cc-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a1cc-115">-ResourceId</span></span>
<span data-ttu-id="8a1cc-116">{{Fill ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="8a1cc-116">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="8a1cc-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8a1cc-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="8a1cc-118">Policy för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="8a1cc-118">The Service endpoint policy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a1cc-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a1cc-119">-Confirm</span></span>
<span data-ttu-id="8a1cc-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a1cc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a1cc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a1cc-121">-WhatIf</span></span>
<span data-ttu-id="8a1cc-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a1cc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a1cc-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a1cc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a1cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1cc-124">CommonParameters</span></span>
<span data-ttu-id="8a1cc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a1cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1cc-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a1cc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1cc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a1cc-127">INPUTS</span></span>

### <span data-ttu-id="8a1cc-128">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8a1cc-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8a1cc-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a1cc-129">OUTPUTS</span></span>

### <span data-ttu-id="8a1cc-130">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a1cc-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8a1cc-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a1cc-131">NOTES</span></span>

## <span data-ttu-id="8a1cc-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a1cc-132">RELATED LINKS</span></span>
