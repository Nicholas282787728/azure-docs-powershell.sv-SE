---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258780"
---
# <span data-ttu-id="d4737-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4737-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="d4737-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4737-102">SYNOPSIS</span></span>
<span data-ttu-id="d4737-103">Hämtar en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="d4737-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="d4737-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4737-104">SYNTAX</span></span>

### <span data-ttu-id="d4737-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d4737-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4737-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4737-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4737-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4737-107">DESCRIPTION</span></span>
<span data-ttu-id="d4737-108">Cmdleten **Get-AzServiceEndpointPolicy** hämtar en policy för tjänst slut punkter.</span><span class="sxs-lookup"><span data-stu-id="d4737-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="d4737-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4737-109">EXAMPLES</span></span>

### <span data-ttu-id="d4737-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4737-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d4737-111">Det här kommandot hämtar tjänste slut punkts principen med namnet ServiceEndpointPolicy1 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policy variabel.</span><span class="sxs-lookup"><span data-stu-id="d4737-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="d4737-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d4737-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d4737-113">Det här kommandot får en lista över alla tjänste slut punkts principer i resurs gruppen som heter ResourceGroup01 och lagrar den i $policyList variabeln.</span><span class="sxs-lookup"><span data-stu-id="d4737-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="d4737-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d4737-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="d4737-115">Det här kommandot får en lista över alla tjänst slut punkts principer som börjar med "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="d4737-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="d4737-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4737-116">PARAMETERS</span></span>

### <span data-ttu-id="d4737-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4737-117">-DefaultProfile</span></span>
<span data-ttu-id="d4737-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4737-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4737-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4737-119">-Name</span></span>
<span data-ttu-id="d4737-120">Namnet på tjänstens slut punkts princip</span><span class="sxs-lookup"><span data-stu-id="d4737-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d4737-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4737-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4737-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d4737-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d4737-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4737-123">-ResourceId</span></span>
<span data-ttu-id="d4737-124">ID för tjänste slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="d4737-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4737-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4737-125">-Confirm</span></span>
<span data-ttu-id="d4737-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4737-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4737-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4737-127">-WhatIf</span></span>
<span data-ttu-id="d4737-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4737-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4737-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4737-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4737-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4737-130">CommonParameters</span></span>
<span data-ttu-id="d4737-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4737-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4737-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4737-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4737-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4737-133">INPUTS</span></span>

### <span data-ttu-id="d4737-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d4737-134">System.String</span></span>

## <span data-ttu-id="d4737-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4737-135">OUTPUTS</span></span>

### <span data-ttu-id="d4737-136">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4737-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d4737-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4737-137">NOTES</span></span>

## <span data-ttu-id="d4737-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4737-138">RELATED LINKS</span></span>

[<span data-ttu-id="d4737-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4737-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d4737-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4737-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d4737-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4737-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
