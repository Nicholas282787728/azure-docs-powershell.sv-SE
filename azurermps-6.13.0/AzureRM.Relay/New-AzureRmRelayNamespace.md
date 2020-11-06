---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: a809d563c4fe633669e9b1cf9d3bbb39770bfd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575132"
---
# <span data-ttu-id="165e6-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="165e6-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="165e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="165e6-102">SYNOPSIS</span></span>
<span data-ttu-id="165e6-103">Skapar ett nytt relä namn.</span><span class="sxs-lookup"><span data-stu-id="165e6-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="165e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="165e6-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="165e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="165e6-105">DESCRIPTION</span></span>
<span data-ttu-id="165e6-106">Cmdleten **New-AzureRmRelayNamespace** skapar ett nytt relä namn.</span><span class="sxs-lookup"><span data-stu-id="165e6-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="165e6-107">När namn rymds resursens manifest har skapats är det oföränderligt.</span><span class="sxs-lookup"><span data-stu-id="165e6-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="165e6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="165e6-108">EXAMPLES</span></span>

### <span data-ttu-id="165e6-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="165e6-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="165e6-110">Skapar ett nytt relä namn område i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="165e6-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="165e6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="165e6-111">PARAMETERS</span></span>

### <span data-ttu-id="165e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165e6-112">-DefaultProfile</span></span>
<span data-ttu-id="165e6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="165e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165e6-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="165e6-114">-Location</span></span>
<span data-ttu-id="165e6-115">Plats för relä namn.</span><span class="sxs-lookup"><span data-stu-id="165e6-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="165e6-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="165e6-116">-Name</span></span>
<span data-ttu-id="165e6-117">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="165e6-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="165e6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="165e6-118">-ResourceGroupName</span></span>
<span data-ttu-id="165e6-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="165e6-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="165e6-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="165e6-120">-Tag</span></span>
<span data-ttu-id="165e6-121">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="165e6-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="165e6-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="165e6-122">-Confirm</span></span>
<span data-ttu-id="165e6-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="165e6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="165e6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="165e6-124">-WhatIf</span></span>
<span data-ttu-id="165e6-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="165e6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="165e6-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="165e6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="165e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165e6-127">CommonParameters</span></span>
<span data-ttu-id="165e6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="165e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="165e6-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="165e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165e6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="165e6-130">INPUTS</span></span>

### <span data-ttu-id="165e6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="165e6-131">System.String</span></span>
<span data-ttu-id="165e6-132">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="165e6-132">System.Collections.Hashtable</span></span>


## <span data-ttu-id="165e6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="165e6-133">OUTPUTS</span></span>

### <span data-ttu-id="165e6-134">Microsoft. Azure. commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="165e6-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="165e6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="165e6-135">NOTES</span></span>

## <span data-ttu-id="165e6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="165e6-136">RELATED LINKS</span></span>
