---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089128"
---
# <span data-ttu-id="00e9b-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="00e9b-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="00e9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="00e9b-103">Uppdaterar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="00e9b-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="00e9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00e9b-104">SYNTAX</span></span>

### <span data-ttu-id="00e9b-105">ByFactoryObject (standard)</span><span class="sxs-lookup"><span data-stu-id="00e9b-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e9b-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="00e9b-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e9b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00e9b-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00e9b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00e9b-108">DESCRIPTION</span></span>
<span data-ttu-id="00e9b-109">Cmdleten **set-AzApplicationGatewayFirewallPolicy** uppdaterar en Azure Application Gateway-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="00e9b-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="00e9b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00e9b-110">EXAMPLES</span></span>

### <span data-ttu-id="00e9b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="00e9b-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="00e9b-112">Det här kommandot uppdaterar brand Väggs principen för Application Gateway med inställningarna i $AppGwFirewallPolicy variabel och lagrar den uppdaterade gatewayen i $UpdatedAppGwFirewallPolicy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="00e9b-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="00e9b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00e9b-113">PARAMETERS</span></span>

### <span data-ttu-id="00e9b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00e9b-114">-AsJob</span></span>
<span data-ttu-id="00e9b-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="00e9b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00e9b-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="00e9b-116">-CustomRule</span></span>
<span data-ttu-id="00e9b-117">Listan med CustomRules</span><span class="sxs-lookup"><span data-stu-id="00e9b-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e9b-118">-DefaultProfile</span></span>
<span data-ttu-id="00e9b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00e9b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00e9b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00e9b-120">-InputObject</span></span>
<span data-ttu-id="00e9b-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="00e9b-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00e9b-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="00e9b-122">-ManagedRule</span></span>
<span data-ttu-id="00e9b-123">ManagedRules för brand Väggs princip</span><span class="sxs-lookup"><span data-stu-id="00e9b-123">ManagedRules of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e9b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="00e9b-124">-Name</span></span>
<span data-ttu-id="00e9b-125">Namnet på brand Väggs principen.</span><span class="sxs-lookup"><span data-stu-id="00e9b-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e9b-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="00e9b-126">-PolicySetting</span></span>
<span data-ttu-id="00e9b-127">Policysettings för brand Väggs princip</span><span class="sxs-lookup"><span data-stu-id="00e9b-127">Policysettings of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e9b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e9b-128">-ResourceGroupName</span></span>
<span data-ttu-id="00e9b-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="00e9b-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e9b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00e9b-130">-ResourceId</span></span>
<span data-ttu-id="00e9b-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="00e9b-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e9b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00e9b-132">-Confirm</span></span>
<span data-ttu-id="00e9b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00e9b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00e9b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00e9b-134">-WhatIf</span></span>
<span data-ttu-id="00e9b-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00e9b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00e9b-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00e9b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00e9b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e9b-137">CommonParameters</span></span>
<span data-ttu-id="00e9b-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e9b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e9b-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00e9b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e9b-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00e9b-140">INPUTS</span></span>

### <span data-ttu-id="00e9b-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="00e9b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="00e9b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00e9b-142">OUTPUTS</span></span>

### <span data-ttu-id="00e9b-143">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="00e9b-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="00e9b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00e9b-144">NOTES</span></span>

## <span data-ttu-id="00e9b-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00e9b-145">RELATED LINKS</span></span>
