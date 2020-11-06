---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576913"
---
# <span data-ttu-id="df829-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="df829-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="df829-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df829-102">SYNOPSIS</span></span>
<span data-ttu-id="df829-103">Get-AzureRmInterfaceEndpoint cmdleten får en gränssnitts slut punkt.</span><span class="sxs-lookup"><span data-stu-id="df829-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df829-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df829-104">SYNTAX</span></span>

### <span data-ttu-id="df829-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="df829-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df829-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df829-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df829-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df829-107">DESCRIPTION</span></span>
<span data-ttu-id="df829-108">Cmdleten **Get-AzureRmInterfaceEndpoint** får en gränssnitts slut punkt.</span><span class="sxs-lookup"><span data-stu-id="df829-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="df829-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df829-109">EXAMPLES</span></span>

### <span data-ttu-id="df829-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="df829-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df829-111">Det här kommandot hämtar gränssnitts slut punkten med namnet InterfaceEndpoint1 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $interfaceendpoint variabeln.</span><span class="sxs-lookup"><span data-stu-id="df829-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="df829-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="df829-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="df829-113">Det här kommandot hämtar gränssnitts slut punkten med resourceId-/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 och lagrar den i variabeln $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="df829-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="df829-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df829-114">PARAMETERS</span></span>

### <span data-ttu-id="df829-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df829-115">-DefaultProfile</span></span>
<span data-ttu-id="df829-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df829-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df829-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="df829-117">-Name</span></span>
<span data-ttu-id="df829-118">Namnet på gränssnittets slut punkt</span><span class="sxs-lookup"><span data-stu-id="df829-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df829-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df829-119">-ResourceGroupName</span></span>
<span data-ttu-id="df829-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="df829-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df829-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df829-121">-ResourceId</span></span>
<span data-ttu-id="df829-122">{{Fill ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="df829-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df829-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df829-123">-Confirm</span></span>
<span data-ttu-id="df829-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df829-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df829-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df829-125">-WhatIf</span></span>
<span data-ttu-id="df829-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df829-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df829-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df829-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df829-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df829-128">CommonParameters</span></span>
<span data-ttu-id="df829-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df829-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="df829-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df829-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df829-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df829-131">INPUTS</span></span>

### <span data-ttu-id="df829-132">System. String</span><span class="sxs-lookup"><span data-stu-id="df829-132">System.String</span></span>


## <span data-ttu-id="df829-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df829-133">OUTPUTS</span></span>

### <span data-ttu-id="df829-134">Microsoft. Azure. commands. Networks. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="df829-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="df829-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df829-135">NOTES</span></span>

## <span data-ttu-id="df829-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df829-136">RELATED LINKS</span></span>
