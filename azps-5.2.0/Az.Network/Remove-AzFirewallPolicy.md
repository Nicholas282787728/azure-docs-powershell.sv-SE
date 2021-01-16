---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409739"
---
# <span data-ttu-id="b226c-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b226c-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="b226c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b226c-102">SYNOPSIS</span></span>
<span data-ttu-id="b226c-103">Tar bort en Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="b226c-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="b226c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b226c-104">SYNTAX</span></span>

### <span data-ttu-id="b226c-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b226c-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b226c-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b226c-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b226c-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b226c-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b226c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b226c-108">DESCRIPTION</span></span>
<span data-ttu-id="b226c-109">Cmdleten **Remove-AzFirewallPolicy** tar bort en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="b226c-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="b226c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b226c-110">EXAMPLES</span></span>

### <span data-ttu-id="b226c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b226c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="b226c-112">I det här exemplet tas brand Väggs principen "firewallpolicy" bort i resourcegroup "TestRg"</span><span class="sxs-lookup"><span data-stu-id="b226c-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="b226c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b226c-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="b226c-114">I det här exemplet tas brand Väggs principen bort med ID.</span><span class="sxs-lookup"><span data-stu-id="b226c-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="b226c-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b226c-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="b226c-116">Det här exemplet tar bort brand Väggs princip $fp</span><span class="sxs-lookup"><span data-stu-id="b226c-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="b226c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b226c-117">PARAMETERS</span></span>

### <span data-ttu-id="b226c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b226c-118">-AsJob</span></span>
<span data-ttu-id="b226c-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b226c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b226c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b226c-120">-DefaultProfile</span></span>
<span data-ttu-id="b226c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b226c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b226c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b226c-122">-Force</span></span>
<span data-ttu-id="b226c-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b226c-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b226c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b226c-124">-InputObject</span></span>
<span data-ttu-id="b226c-125">AzureFirewall policy</span><span class="sxs-lookup"><span data-stu-id="b226c-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b226c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b226c-126">-Name</span></span>
<span data-ttu-id="b226c-127">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b226c-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b226c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b226c-128">-PassThru</span></span>
<span data-ttu-id="b226c-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b226c-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b226c-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b226c-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b226c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b226c-131">-ResourceGroupName</span></span>
<span data-ttu-id="b226c-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b226c-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b226c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b226c-133">-ResourceId</span></span>
<span data-ttu-id="b226c-134">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b226c-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b226c-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b226c-135">-Confirm</span></span>
<span data-ttu-id="b226c-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b226c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b226c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b226c-137">-WhatIf</span></span>
<span data-ttu-id="b226c-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b226c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b226c-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b226c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b226c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b226c-140">CommonParameters</span></span>
<span data-ttu-id="b226c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b226c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b226c-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b226c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b226c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b226c-143">INPUTS</span></span>

### <span data-ttu-id="b226c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b226c-144">System.String</span></span>

### <span data-ttu-id="b226c-145">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b226c-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="b226c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b226c-146">OUTPUTS</span></span>

### <span data-ttu-id="b226c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b226c-147">System.Boolean</span></span>

## <span data-ttu-id="b226c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b226c-148">NOTES</span></span>

## <span data-ttu-id="b226c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b226c-149">RELATED LINKS</span></span>
