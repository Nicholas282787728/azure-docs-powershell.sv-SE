---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: e7025a48fd1d83a0018ac18de01673b0deeed742
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748003"
---
# <span data-ttu-id="22c95-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="22c95-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="22c95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22c95-102">SYNOPSIS</span></span>
<span data-ttu-id="22c95-103">Skapar en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="22c95-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="22c95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22c95-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22c95-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22c95-105">DESCRIPTION</span></span>
<span data-ttu-id="22c95-106">**New-AzServiceEndpointPolicy-** cmdleten skapa en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="22c95-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="22c95-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22c95-107">EXAMPLES</span></span>

### <span data-ttu-id="22c95-108">Exempel 1: skapar en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="22c95-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="22c95-109">Det här kommandot skapar en tjänst slut punkts princip med namnet Policy1 med definitioner definierade av objektet $serviceEndpointDefinition och lagrar dem i $serviceEndpointPolicy variabeln.</span><span class="sxs-lookup"><span data-stu-id="22c95-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="22c95-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22c95-110">PARAMETERS</span></span>

### <span data-ttu-id="22c95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c95-111">-DefaultProfile</span></span>
<span data-ttu-id="22c95-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22c95-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22c95-113">-Force</span><span class="sxs-lookup"><span data-stu-id="22c95-113">-Force</span></span>
<span data-ttu-id="22c95-114">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="22c95-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c95-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="22c95-115">-Location</span></span>
<span data-ttu-id="22c95-116">plats.</span><span class="sxs-lookup"><span data-stu-id="22c95-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c95-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="22c95-117">-Name</span></span>
<span data-ttu-id="22c95-118">Namnet på under nätet</span><span class="sxs-lookup"><span data-stu-id="22c95-118">The name of the subnet</span></span>

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

### <span data-ttu-id="22c95-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c95-119">-ResourceGroupName</span></span>
<span data-ttu-id="22c95-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="22c95-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c95-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22c95-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="22c95-122">Lista över definitioner för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="22c95-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c95-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22c95-123">-Confirm</span></span>
<span data-ttu-id="22c95-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22c95-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c95-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c95-125">-WhatIf</span></span>
<span data-ttu-id="22c95-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22c95-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c95-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22c95-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c95-128">CommonParameters</span></span>
<span data-ttu-id="22c95-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c95-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c95-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c95-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22c95-131">INPUTS</span></span>

### <span data-ttu-id="22c95-132">System. String</span><span class="sxs-lookup"><span data-stu-id="22c95-132">System.String</span></span>

## <span data-ttu-id="22c95-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22c95-133">OUTPUTS</span></span>

### <span data-ttu-id="22c95-134">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="22c95-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="22c95-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22c95-135">NOTES</span></span>

## <span data-ttu-id="22c95-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22c95-136">RELATED LINKS</span></span>

[<span data-ttu-id="22c95-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="22c95-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="22c95-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="22c95-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="22c95-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="22c95-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)