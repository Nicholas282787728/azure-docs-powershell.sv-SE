---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269321"
---
# <span data-ttu-id="ef5f3-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ef5f3-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ef5f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5f3-103">Tar bort en regel samlings grupp för Azure Firewall i en Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="ef5f3-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="ef5f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef5f3-104">SYNTAX</span></span>

### <span data-ttu-id="ef5f3-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ef5f3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5f3-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5f3-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef5f3-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5f3-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef5f3-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5f3-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef5f3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef5f3-109">DESCRIPTION</span></span>
<span data-ttu-id="ef5f3-110">Cmdleten **Remove-AzFirewallPolicyRuleCollectionGroup** tar bort en regel samlings grupp från en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ef5f3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef5f3-111">EXAMPLES</span></span>

### <span data-ttu-id="ef5f3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef5f3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="ef5f3-113">I det här exemplet tas brand Väggs princip regeln för colelction grupp med namnet "testRcGroup" bort i Firewall-principobjektet $fp</span><span class="sxs-lookup"><span data-stu-id="ef5f3-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="ef5f3-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ef5f3-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="ef5f3-115">Det här exemplet tar bort brand Väggs princip regeln colelction gruppen "testRcGroup" i brand väggen med namnet "fpName" frpm resourcegroup namnen "testRg"</span><span class="sxs-lookup"><span data-stu-id="ef5f3-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="ef5f3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef5f3-116">PARAMETERS</span></span>

### <span data-ttu-id="ef5f3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef5f3-117">-AsJob</span></span>
<span data-ttu-id="ef5f3-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ef5f3-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5f3-119">-DefaultProfile</span></span>
<span data-ttu-id="ef5f3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="ef5f3-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="ef5f3-122">Namnet på brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="ef5f3-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ef5f3-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="ef5f3-124">Brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ef5f3-125">-Force</span></span>
<span data-ttu-id="ef5f3-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef5f3-127">-InputObject</span></span>
<span data-ttu-id="ef5f3-128">Grupp objekt för gruppen för brand Väggs policy</span><span class="sxs-lookup"><span data-stu-id="ef5f3-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef5f3-129">-Name</span></span>
<span data-ttu-id="ef5f3-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef5f3-131">-PassThru</span></span>
<span data-ttu-id="ef5f3-132">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef5f3-133">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5f3-134">-ResourceGroupName</span></span>
<span data-ttu-id="ef5f3-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef5f3-136">-ResourceId</span></span>
<span data-ttu-id="ef5f3-137">Resurs-ID för regel samlings gruppen</span><span class="sxs-lookup"><span data-stu-id="ef5f3-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef5f3-138">-Confirm</span></span>
<span data-ttu-id="ef5f3-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef5f3-140">-WhatIf</span></span>
<span data-ttu-id="ef5f3-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef5f3-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5f3-143">CommonParameters</span></span>
<span data-ttu-id="ef5f3-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5f3-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef5f3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5f3-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef5f3-146">INPUTS</span></span>

### <span data-ttu-id="ef5f3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ef5f3-147">System.String</span></span>

### <span data-ttu-id="ef5f3-148">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ef5f3-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="ef5f3-149">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="ef5f3-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="ef5f3-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef5f3-150">OUTPUTS</span></span>

### <span data-ttu-id="ef5f3-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef5f3-151">System.Boolean</span></span>

## <span data-ttu-id="ef5f3-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef5f3-152">NOTES</span></span>

## <span data-ttu-id="ef5f3-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef5f3-153">RELATED LINKS</span></span>