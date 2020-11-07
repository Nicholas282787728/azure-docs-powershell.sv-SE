---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 8eaf2ff99fe7f3ea49d73af95eb4482c645be59f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756864"
---
# <span data-ttu-id="ba51d-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba51d-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="ba51d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba51d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba51d-103">Tar bort auktoriseringsregeln för en HybridConnection från angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ba51d-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba51d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba51d-104">SYNTAX</span></span>

### <span data-ttu-id="ba51d-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ba51d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba51d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba51d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba51d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba51d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba51d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba51d-108">DESCRIPTION</span></span>
<span data-ttu-id="ba51d-109">Cmdleten **Remove-AzureRmRelayAuthorizationRule** tar bort auktoriseringsregeln för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ba51d-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ba51d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba51d-110">EXAMPLES</span></span>

### <span data-ttu-id="ba51d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ba51d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="ba51d-112">Tar bort auktoriseringsregeln `AuthoRule1` för namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ba51d-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="ba51d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ba51d-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="ba51d-114">Tar bort auktoriseringsregeln `AuthoRule1` för WcfRelay `TestWcfRelay` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ba51d-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="ba51d-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ba51d-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="ba51d-116">Tar bort auktoriseringsregeln `AuthoRule1` för HybridConnection `TestHybridConnection` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ba51d-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ba51d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba51d-117">PARAMETERS</span></span>

### <span data-ttu-id="ba51d-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba51d-118">-Confirm</span></span>
<span data-ttu-id="ba51d-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba51d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba51d-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ba51d-120">-HybridConnection</span></span>
<span data-ttu-id="ba51d-121">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="ba51d-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba51d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba51d-122">-Name</span></span>
<span data-ttu-id="ba51d-123">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="ba51d-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba51d-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ba51d-124">-Namespace</span></span>
<span data-ttu-id="ba51d-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ba51d-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba51d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba51d-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba51d-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ba51d-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba51d-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ba51d-128">-WcfRelay</span></span>
<span data-ttu-id="ba51d-129">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="ba51d-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba51d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba51d-130">-WhatIf</span></span>
<span data-ttu-id="ba51d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba51d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba51d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ba51d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba51d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba51d-133">-DefaultProfile</span></span>
<span data-ttu-id="ba51d-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba51d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba51d-135">-Force</span><span class="sxs-lookup"><span data-stu-id="ba51d-135">-Force</span></span>
<span data-ttu-id="ba51d-136">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ba51d-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ba51d-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba51d-137">-PassThru</span></span>
<span data-ttu-id="ba51d-138">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ba51d-138">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ba51d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba51d-139">CommonParameters</span></span>
<span data-ttu-id="ba51d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba51d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba51d-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba51d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba51d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba51d-142">INPUTS</span></span>

### <span data-ttu-id="ba51d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ba51d-143">System.String</span></span>

## <span data-ttu-id="ba51d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba51d-144">OUTPUTS</span></span>

### <span data-ttu-id="ba51d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba51d-145">System.Boolean</span></span>

## <span data-ttu-id="ba51d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba51d-146">NOTES</span></span>

## <span data-ttu-id="ba51d-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba51d-147">RELATED LINKS</span></span>

