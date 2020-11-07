---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748289"
---
# <span data-ttu-id="5bf1e-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bf1e-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="5bf1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bf1e-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf1e-103">Get-AzInterfaceEndpoint cmdleten får en gränssnitts slut punkt.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="5bf1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bf1e-104">SYNTAX</span></span>

### <span data-ttu-id="5bf1e-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5bf1e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf1e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bf1e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bf1e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bf1e-107">DESCRIPTION</span></span>
<span data-ttu-id="5bf1e-108">Cmdleten **Get-AzInterfaceEndpoint** får en gränssnitts slut punkt.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="5bf1e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bf1e-109">EXAMPLES</span></span>

### <span data-ttu-id="5bf1e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5bf1e-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5bf1e-111">Det här kommandot hämtar gränssnitts slut punkten med namnet InterfaceEndpoint1 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $interfaceendpoint variabeln.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="5bf1e-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5bf1e-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="5bf1e-113">Det här kommandot hämtar gränssnitts slut punkten med resourceId-/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 och lagrar den i variabeln $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="5bf1e-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5bf1e-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="5bf1e-115">Det här kommandot får de gränssnitts slut punkter som börjar med "InterfaceEndpoint"</span><span class="sxs-lookup"><span data-stu-id="5bf1e-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="5bf1e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bf1e-116">PARAMETERS</span></span>

### <span data-ttu-id="5bf1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf1e-117">-DefaultProfile</span></span>
<span data-ttu-id="5bf1e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf1e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5bf1e-119">-Name</span></span>
<span data-ttu-id="5bf1e-120">Namnet på gränssnittets slut punkt</span><span class="sxs-lookup"><span data-stu-id="5bf1e-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5bf1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="5bf1e-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5bf1e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bf1e-123">-ResourceId</span></span>
<span data-ttu-id="5bf1e-124">ID för gränssnittets slut punkt.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-124">The ID of the interface endpoint.</span></span>

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

### <span data-ttu-id="5bf1e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5bf1e-125">-Confirm</span></span>
<span data-ttu-id="5bf1e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf1e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf1e-127">-WhatIf</span></span>
<span data-ttu-id="5bf1e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf1e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf1e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf1e-130">CommonParameters</span></span>
<span data-ttu-id="5bf1e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf1e-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bf1e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf1e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bf1e-133">INPUTS</span></span>

### <span data-ttu-id="5bf1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf1e-134">System.String</span></span>

## <span data-ttu-id="5bf1e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bf1e-135">OUTPUTS</span></span>

### <span data-ttu-id="5bf1e-136">Microsoft. Azure. commands. Networks. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bf1e-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="5bf1e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bf1e-137">NOTES</span></span>

## <span data-ttu-id="5bf1e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bf1e-138">RELATED LINKS</span></span>
