---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 09c601e2ecfddf417e90efd60b58bcdd1a51ff5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575543"
---
# <span data-ttu-id="a3c20-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a3c20-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="a3c20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3c20-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c20-103">Uppdaterar beskrivningen av ett befintligt namn område för en relä.</span><span class="sxs-lookup"><span data-stu-id="a3c20-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3c20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3c20-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c20-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3c20-105">DESCRIPTION</span></span>
<span data-ttu-id="a3c20-106">Cmdleten **set-AzureRmRelayNamespace** uppdaterar beskrivningen av angivet relä namn område i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a3c20-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="a3c20-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3c20-107">EXAMPLES</span></span>

### <span data-ttu-id="a3c20-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3c20-108">Example 1</span></span>
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

<span data-ttu-id="a3c20-109">Uppdaterar namn området för relät med en ny beskrivning.</span><span class="sxs-lookup"><span data-stu-id="a3c20-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="a3c20-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3c20-110">PARAMETERS</span></span>

### <span data-ttu-id="a3c20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c20-111">-DefaultProfile</span></span>
<span data-ttu-id="a3c20-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3c20-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3c20-113">-InputObject</span></span>
<span data-ttu-id="a3c20-114">Objekt i relä namn</span><span class="sxs-lookup"><span data-stu-id="a3c20-114">Relay Namespace object</span></span>

```yaml
Type: RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c20-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3c20-115">-Name</span></span>
<span data-ttu-id="a3c20-116">Namn område för relä</span><span class="sxs-lookup"><span data-stu-id="a3c20-116">Relay Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c20-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3c20-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a3c20-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c20-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a3c20-119">-Tag</span></span>
<span data-ttu-id="a3c20-120">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a3c20-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a3c20-121">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="a3c20-121">For example:</span></span>

<span data-ttu-id="a3c20-122">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a3c20-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c20-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3c20-123">-Confirm</span></span>
<span data-ttu-id="a3c20-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3c20-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c20-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c20-125">-WhatIf</span></span>
<span data-ttu-id="a3c20-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3c20-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c20-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3c20-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c20-128">CommonParameters</span></span>
<span data-ttu-id="a3c20-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c20-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3c20-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c20-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3c20-131">INPUTS</span></span>

### <span data-ttu-id="a3c20-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c20-132">-ResourceGroupName</span></span>
 <span data-ttu-id="a3c20-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a3c20-133">System.String</span></span>

### <span data-ttu-id="a3c20-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a3c20-134">-NamespaceName</span></span>
 <span data-ttu-id="a3c20-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a3c20-135">System.String</span></span>

### <span data-ttu-id="a3c20-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="a3c20-136">-Location</span></span>
 <span data-ttu-id="a3c20-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a3c20-137">System.String</span></span>

### <span data-ttu-id="a3c20-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a3c20-138">-Tag</span></span>
 <span data-ttu-id="a3c20-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a3c20-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a3c20-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3c20-140">OUTPUTS</span></span>

### <span data-ttu-id="a3c20-141">Microsoft. Azure. commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a3c20-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="a3c20-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3c20-142">NOTES</span></span>

## <span data-ttu-id="a3c20-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3c20-143">RELATED LINKS</span></span>

