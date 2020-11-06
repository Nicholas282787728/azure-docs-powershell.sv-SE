---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582587"
---
# <span data-ttu-id="36fa2-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="36fa2-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="36fa2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="36fa2-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="36fa2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36fa2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36fa2-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36fa2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="36fa2-106">**New-AzureRmServiceEndpointPolicy-** cmdleten skapa en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="36fa2-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="36fa2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="36fa2-108">Exempel 1: skapar en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="36fa2-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="36fa2-109">Det här kommandot skapar en tjänst slut punkts princip med namnet Policy1 med definitioner definierade av objektet $serviceEndpointDefinition och lagrar dem i $serviceEndpointPolicy variabeln.</span><span class="sxs-lookup"><span data-stu-id="36fa2-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="36fa2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36fa2-110">PARAMETERS</span></span>

### <span data-ttu-id="36fa2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fa2-111">-DefaultProfile</span></span>
<span data-ttu-id="36fa2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36fa2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36fa2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="36fa2-113">-Force</span></span>
<span data-ttu-id="36fa2-114">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="36fa2-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="36fa2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="36fa2-115">-Name</span></span>
<span data-ttu-id="36fa2-116">Namnet på under nätet</span><span class="sxs-lookup"><span data-stu-id="36fa2-116">The name of the subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fa2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36fa2-117">-ResourceGroupName</span></span>
<span data-ttu-id="36fa2-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="36fa2-118">The resource group name.</span></span>

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

### <span data-ttu-id="36fa2-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="36fa2-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="36fa2-120">Lista över definitioner för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="36fa2-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fa2-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36fa2-121">-Confirm</span></span>
<span data-ttu-id="36fa2-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36fa2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36fa2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36fa2-123">-WhatIf</span></span>
<span data-ttu-id="36fa2-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36fa2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36fa2-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36fa2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36fa2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fa2-126">CommonParameters</span></span>
<span data-ttu-id="36fa2-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36fa2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="36fa2-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36fa2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fa2-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36fa2-129">INPUTS</span></span>

### <span data-ttu-id="36fa2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="36fa2-130">System.String</span></span>


## <span data-ttu-id="36fa2-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36fa2-131">OUTPUTS</span></span>

### <span data-ttu-id="36fa2-132">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="36fa2-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="36fa2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36fa2-133">NOTES</span></span>

## <span data-ttu-id="36fa2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36fa2-134">RELATED LINKS</span></span>
