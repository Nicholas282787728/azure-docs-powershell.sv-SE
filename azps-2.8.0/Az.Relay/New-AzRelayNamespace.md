---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: 37e641516ffc21a0984f97cb84f94d2564033fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920131"
---
# <span data-ttu-id="3270d-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="3270d-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="3270d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3270d-102">SYNOPSIS</span></span>
<span data-ttu-id="3270d-103">Skapar ett nytt relä namn.</span><span class="sxs-lookup"><span data-stu-id="3270d-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="3270d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3270d-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3270d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3270d-105">DESCRIPTION</span></span>
<span data-ttu-id="3270d-106">Cmdleten **New-AzRelayNamespace** skapar ett nytt relä namn.</span><span class="sxs-lookup"><span data-stu-id="3270d-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="3270d-107">När namn rymds resursens manifest har skapats är det oföränderligt.</span><span class="sxs-lookup"><span data-stu-id="3270d-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="3270d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3270d-108">EXAMPLES</span></span>

### <span data-ttu-id="3270d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3270d-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="3270d-110">Skapar ett nytt relä namn område i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3270d-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="3270d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3270d-111">PARAMETERS</span></span>

### <span data-ttu-id="3270d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3270d-112">-DefaultProfile</span></span>
<span data-ttu-id="3270d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3270d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3270d-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="3270d-114">-Location</span></span>
<span data-ttu-id="3270d-115">Plats för relä namn.</span><span class="sxs-lookup"><span data-stu-id="3270d-115">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3270d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="3270d-116">-Name</span></span>
<span data-ttu-id="3270d-117">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="3270d-117">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3270d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3270d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3270d-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3270d-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3270d-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3270d-120">-Tag</span></span>
<span data-ttu-id="3270d-121">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="3270d-121">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3270d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3270d-122">-Confirm</span></span>
<span data-ttu-id="3270d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3270d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3270d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3270d-124">-WhatIf</span></span>
<span data-ttu-id="3270d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3270d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3270d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3270d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3270d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3270d-127">CommonParameters</span></span>
<span data-ttu-id="3270d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3270d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3270d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3270d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3270d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3270d-130">INPUTS</span></span>

### <span data-ttu-id="3270d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3270d-131">System.String</span></span>

### <span data-ttu-id="3270d-132">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3270d-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3270d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3270d-133">OUTPUTS</span></span>

### <span data-ttu-id="3270d-134">Microsoft. Azure. commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3270d-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="3270d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3270d-135">NOTES</span></span>

## <span data-ttu-id="3270d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3270d-136">RELATED LINKS</span></span>
