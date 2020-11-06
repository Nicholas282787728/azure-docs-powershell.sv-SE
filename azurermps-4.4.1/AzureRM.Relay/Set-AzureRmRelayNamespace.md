---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575870"
---
# <span data-ttu-id="4327c-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="4327c-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="4327c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4327c-102">SYNOPSIS</span></span>
<span data-ttu-id="4327c-103">Uppdaterar beskrivningen av ett befintligt namn område för en relä.</span><span class="sxs-lookup"><span data-stu-id="4327c-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4327c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4327c-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4327c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4327c-105">DESCRIPTION</span></span>
<span data-ttu-id="4327c-106">Cmdleten **set-AzureRmRelayNamespace** uppdaterar beskrivningen av angivet relä namn område i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4327c-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="4327c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4327c-107">EXAMPLES</span></span>

### <span data-ttu-id="4327c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4327c-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="4327c-109">Uppdaterar namn området för relät med en ny beskrivning.</span><span class="sxs-lookup"><span data-stu-id="4327c-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="4327c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4327c-110">PARAMETERS</span></span>

### <span data-ttu-id="4327c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4327c-111">-ResourceGroupName</span></span>
<span data-ttu-id="4327c-112">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4327c-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="4327c-113">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4327c-113">-Tag</span></span>
<span data-ttu-id="4327c-114">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4327c-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4327c-115">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="4327c-115">For example:</span></span>

<span data-ttu-id="4327c-116">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="4327c-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4327c-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4327c-117">-Confirm</span></span>
<span data-ttu-id="4327c-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4327c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4327c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4327c-119">-WhatIf</span></span>
<span data-ttu-id="4327c-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4327c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4327c-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4327c-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4327c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4327c-122">-DefaultProfile</span></span>
<span data-ttu-id="4327c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4327c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4327c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4327c-124">-InputObject</span></span>
<span data-ttu-id="4327c-125">Objekt i relä namn området.</span><span class="sxs-lookup"><span data-stu-id="4327c-125">Relay Namespace object.</span></span>

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

### <span data-ttu-id="4327c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="4327c-126">-Name</span></span>
<span data-ttu-id="4327c-127">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="4327c-127">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="4327c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4327c-128">CommonParameters</span></span>
<span data-ttu-id="4327c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4327c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4327c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4327c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4327c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4327c-131">INPUTS</span></span>

### <span data-ttu-id="4327c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4327c-132">-ResourceGroupName</span></span>
 <span data-ttu-id="4327c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4327c-133">System.String</span></span>

### <span data-ttu-id="4327c-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4327c-134">-NamespaceName</span></span>
 <span data-ttu-id="4327c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4327c-135">System.String</span></span>

### <span data-ttu-id="4327c-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="4327c-136">-Location</span></span>
 <span data-ttu-id="4327c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4327c-137">System.String</span></span>

### <span data-ttu-id="4327c-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4327c-138">-Tag</span></span>
 <span data-ttu-id="4327c-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4327c-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4327c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4327c-140">OUTPUTS</span></span>

### <span data-ttu-id="4327c-141">Microsoft. Azure. commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4327c-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="4327c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4327c-142">NOTES</span></span>

## <span data-ttu-id="4327c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4327c-143">RELATED LINKS</span></span>

