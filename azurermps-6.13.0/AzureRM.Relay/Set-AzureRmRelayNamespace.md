---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 6bb333de426236099bed7402fc4756181415c4ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755522"
---
# <span data-ttu-id="4e1b0-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="4e1b0-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="4e1b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1b0-103">Uppdaterar beskrivningen av ett befintligt namn område för en relä.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e1b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e1b0-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e1b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e1b0-105">DESCRIPTION</span></span>
<span data-ttu-id="4e1b0-106">Cmdleten **set-AzureRmRelayNamespace** uppdaterar beskrivningen av angivet relä namn område i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="4e1b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e1b0-107">EXAMPLES</span></span>

### <span data-ttu-id="4e1b0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4e1b0-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="4e1b0-109">Uppdaterar namn området för relät med en ny beskrivning.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="4e1b0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e1b0-110">PARAMETERS</span></span>

### <span data-ttu-id="4e1b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1b0-111">-DefaultProfile</span></span>
<span data-ttu-id="4e1b0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e1b0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e1b0-113">-InputObject</span></span>
<span data-ttu-id="4e1b0-114">Objekt i relä namn området.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e1b0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e1b0-115">-Name</span></span>
<span data-ttu-id="4e1b0-116">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="4e1b0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e1b0-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e1b0-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e1b0-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4e1b0-119">-Tag</span></span>
<span data-ttu-id="4e1b0-120">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="4e1b0-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e1b0-121">-Confirm</span></span>
<span data-ttu-id="4e1b0-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e1b0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e1b0-123">-WhatIf</span></span>
<span data-ttu-id="4e1b0-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e1b0-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e1b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1b0-126">CommonParameters</span></span>
<span data-ttu-id="4e1b0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4e1b0-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e1b0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1b0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e1b0-129">INPUTS</span></span>

### <span data-ttu-id="4e1b0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4e1b0-130">System.String</span></span>
<span data-ttu-id="4e1b0-131">System. Collection. hash Microsoft. Azure. commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="4e1b0-131">System.Collections.Hashtable Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>


## <span data-ttu-id="4e1b0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e1b0-132">OUTPUTS</span></span>

### <span data-ttu-id="4e1b0-133">Microsoft. Azure. commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4e1b0-133">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="4e1b0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e1b0-134">NOTES</span></span>

## <span data-ttu-id="4e1b0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e1b0-135">RELATED LINKS</span></span>
