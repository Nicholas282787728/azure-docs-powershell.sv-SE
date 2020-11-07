---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927414"
---
# <span data-ttu-id="a11e7-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a11e7-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="a11e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a11e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a11e7-103">Uppdaterar beskrivningen av ett befintligt namn område för en relä.</span><span class="sxs-lookup"><span data-stu-id="a11e7-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="a11e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a11e7-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a11e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a11e7-105">DESCRIPTION</span></span>
<span data-ttu-id="a11e7-106">Cmdleten **set-AzRelayNamespace** uppdaterar beskrivningen av angivet relä namn område i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a11e7-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="a11e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a11e7-107">EXAMPLES</span></span>

### <span data-ttu-id="a11e7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a11e7-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="a11e7-109">Uppdaterar namn området för relät med en ny beskrivning.</span><span class="sxs-lookup"><span data-stu-id="a11e7-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="a11e7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a11e7-110">PARAMETERS</span></span>

### <span data-ttu-id="a11e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11e7-111">-DefaultProfile</span></span>
<span data-ttu-id="a11e7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a11e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a11e7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a11e7-113">-InputObject</span></span>
<span data-ttu-id="a11e7-114">Objekt i relä namn området.</span><span class="sxs-lookup"><span data-stu-id="a11e7-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="a11e7-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a11e7-115">-Name</span></span>
<span data-ttu-id="a11e7-116">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="a11e7-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a11e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="a11e7-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a11e7-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="a11e7-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a11e7-119">-Tag</span></span>
<span data-ttu-id="a11e7-120">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="a11e7-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="a11e7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a11e7-121">-Confirm</span></span>
<span data-ttu-id="a11e7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a11e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a11e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11e7-123">-WhatIf</span></span>
<span data-ttu-id="a11e7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a11e7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11e7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a11e7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a11e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11e7-126">CommonParameters</span></span>
<span data-ttu-id="a11e7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a11e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11e7-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a11e7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11e7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a11e7-129">INPUTS</span></span>

### <span data-ttu-id="a11e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a11e7-130">System.String</span></span>

### <span data-ttu-id="a11e7-131">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a11e7-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a11e7-132">Microsoft. Azure. commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="a11e7-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="a11e7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a11e7-133">OUTPUTS</span></span>

### <span data-ttu-id="a11e7-134">Microsoft. Azure. commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a11e7-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="a11e7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a11e7-135">NOTES</span></span>

## <span data-ttu-id="a11e7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a11e7-136">RELATED LINKS</span></span>
