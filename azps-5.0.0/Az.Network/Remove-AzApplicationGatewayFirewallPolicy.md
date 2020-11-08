---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271476"
---
# <span data-ttu-id="0b217-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0b217-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="0b217-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b217-102">SYNOPSIS</span></span>
<span data-ttu-id="0b217-103">Tar bort en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b217-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="0b217-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b217-104">SYNTAX</span></span>

### <span data-ttu-id="0b217-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="0b217-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b217-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0b217-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b217-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b217-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b217-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b217-108">DESCRIPTION</span></span>
<span data-ttu-id="0b217-109">Cmdleten **Remove-AzApplicationGatewayFirewallPolicy** tar bort en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b217-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="0b217-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b217-110">EXAMPLES</span></span>

### <span data-ttu-id="0b217-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0b217-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0b217-112">Det här kommandot tar bort den brand Väggs princip för Application Gateway som heter ApplicationGatewayFirewallPolicy01 i resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0b217-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0b217-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b217-113">PARAMETERS</span></span>

### <span data-ttu-id="0b217-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b217-114">-AsJob</span></span>
<span data-ttu-id="0b217-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0b217-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b217-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b217-116">-DefaultProfile</span></span>
<span data-ttu-id="0b217-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b217-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b217-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0b217-118">-Force</span></span>
<span data-ttu-id="0b217-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0b217-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0b217-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b217-120">-InputObject</span></span>
<span data-ttu-id="0b217-121">Firewall-principobjektet</span><span class="sxs-lookup"><span data-stu-id="0b217-121">The firewall policy object</span></span>

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

### <span data-ttu-id="0b217-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b217-122">-Name</span></span>
<span data-ttu-id="0b217-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0b217-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b217-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b217-124">-PassThru</span></span>
<span data-ttu-id="0b217-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0b217-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b217-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0b217-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b217-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b217-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b217-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0b217-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b217-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b217-129">-ResourceId</span></span>
<span data-ttu-id="0b217-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="0b217-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0b217-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b217-131">-Confirm</span></span>
<span data-ttu-id="0b217-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b217-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b217-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b217-133">-WhatIf</span></span>
<span data-ttu-id="0b217-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b217-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b217-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b217-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b217-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b217-136">CommonParameters</span></span>
<span data-ttu-id="0b217-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b217-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b217-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b217-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b217-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b217-139">INPUTS</span></span>

### <span data-ttu-id="0b217-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0b217-140">System.String</span></span>

## <span data-ttu-id="0b217-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b217-141">OUTPUTS</span></span>

### <span data-ttu-id="0b217-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b217-142">System.Boolean</span></span>

## <span data-ttu-id="0b217-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b217-143">NOTES</span></span>

## <span data-ttu-id="0b217-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b217-144">RELATED LINKS</span></span>
