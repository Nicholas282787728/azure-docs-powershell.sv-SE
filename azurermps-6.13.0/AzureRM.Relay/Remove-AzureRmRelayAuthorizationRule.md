---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: cebc4680e4c24bb7e19342d32e4aedd57b960e55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755322"
---
# <span data-ttu-id="121d4-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="121d4-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="121d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="121d4-102">SYNOPSIS</span></span>
<span data-ttu-id="121d4-103">Tar bort auktoriseringsregeln för en HybridConnection från angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="121d4-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="121d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="121d4-104">SYNTAX</span></span>

### <span data-ttu-id="121d4-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="121d4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="121d4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="121d4-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="121d4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="121d4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="121d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="121d4-108">DESCRIPTION</span></span>
<span data-ttu-id="121d4-109">Cmdleten **Remove-AzureRmRelayAuthorizationRule** tar bort auktoriseringsregeln för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="121d4-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="121d4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="121d4-110">EXAMPLES</span></span>

### <span data-ttu-id="121d4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="121d4-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="121d4-112">Tar bort auktoriseringsregeln `AuthoRule1` för namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="121d4-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="121d4-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="121d4-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="121d4-114">Tar bort auktoriseringsregeln `AuthoRule1` för WcfRelay `TestWcfRelay` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="121d4-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="121d4-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="121d4-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="121d4-116">Tar bort auktoriseringsregeln `AuthoRule1` för HybridConnection `TestHybridConnection` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="121d4-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="121d4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="121d4-117">PARAMETERS</span></span>

### <span data-ttu-id="121d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121d4-118">-DefaultProfile</span></span>
<span data-ttu-id="121d4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="121d4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="121d4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="121d4-120">-Force</span></span>
<span data-ttu-id="121d4-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="121d4-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="121d4-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="121d4-122">-HybridConnection</span></span>
<span data-ttu-id="121d4-123">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="121d4-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="121d4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="121d4-124">-Name</span></span>
<span data-ttu-id="121d4-125">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="121d4-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="121d4-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="121d4-126">-Namespace</span></span>
<span data-ttu-id="121d4-127">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="121d4-127">Namespace Name.</span></span>

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

### <span data-ttu-id="121d4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="121d4-128">-PassThru</span></span>
<span data-ttu-id="121d4-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="121d4-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="121d4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="121d4-130">-ResourceGroupName</span></span>
<span data-ttu-id="121d4-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="121d4-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="121d4-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="121d4-132">-WcfRelay</span></span>
<span data-ttu-id="121d4-133">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="121d4-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="121d4-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="121d4-134">-Confirm</span></span>
<span data-ttu-id="121d4-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="121d4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="121d4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="121d4-136">-WhatIf</span></span>
<span data-ttu-id="121d4-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="121d4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="121d4-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="121d4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="121d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121d4-139">CommonParameters</span></span>
<span data-ttu-id="121d4-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="121d4-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="121d4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121d4-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="121d4-142">INPUTS</span></span>

### <span data-ttu-id="121d4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="121d4-143">System.String</span></span>


## <span data-ttu-id="121d4-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="121d4-144">OUTPUTS</span></span>

### <span data-ttu-id="121d4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="121d4-145">System.Boolean</span></span>


## <span data-ttu-id="121d4-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="121d4-146">NOTES</span></span>

## <span data-ttu-id="121d4-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="121d4-147">RELATED LINKS</span></span>
