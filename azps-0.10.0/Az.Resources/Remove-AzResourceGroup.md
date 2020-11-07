---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 232f8de58bb6026a2932631ac2f9e3ed77c71b91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923813"
---
# <span data-ttu-id="3bf23-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3bf23-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="3bf23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bf23-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf23-103">Tar bort en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3bf23-103">Removes a resource group.</span></span>

## <span data-ttu-id="3bf23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bf23-104">SYNTAX</span></span>

### <span data-ttu-id="3bf23-105">RemoveByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="3bf23-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bf23-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="3bf23-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bf23-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bf23-107">DESCRIPTION</span></span>
<span data-ttu-id="3bf23-108">Cmdleten **Remove-AzResourceGroup** tar bort en Azure resurs grupp och dess resurser från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3bf23-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="3bf23-109">Använd Remove-AzResource cmdlet för att ta bort en resurs, men lämna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3bf23-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="3bf23-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bf23-110">EXAMPLES</span></span>

### <span data-ttu-id="3bf23-111">Exempel 1: ta bort en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="3bf23-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="3bf23-112">Det här kommandot tar bort resurs gruppen ContosoRG01 från prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3bf23-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="3bf23-113">Cmdleten uppmanar dig att bekräfta och returnerar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3bf23-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="3bf23-114">Exempel 2: ta bort en resurs grupp utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="3bf23-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="3bf23-115">Det här kommandot använder cmdleten Get-AzResourceGroup för att hämta resurs gruppen ContosoRG01 och skickar den sedan till **Remove-AzResourceGroup** genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="3bf23-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="3bf23-116">Den *utförliga* gemensamma parametern får statusinformation om åtgärden och *Force* -parametern gör att uppmaningen inte bekräftas.</span><span class="sxs-lookup"><span data-stu-id="3bf23-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="3bf23-117">Exempel 3: ta bort alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="3bf23-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="3bf23-118">Det här kommandot använder cmdleten **Get-AzResourceGroup** för att hämta alla resurs grupper och skickar dem sedan för att **ta bort-AzResourceGroup** med operatören.</span><span class="sxs-lookup"><span data-stu-id="3bf23-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="3bf23-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bf23-119">PARAMETERS</span></span>

### <span data-ttu-id="3bf23-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3bf23-120">-ApiVersion</span></span>
<span data-ttu-id="3bf23-121">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="3bf23-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3bf23-122">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="3bf23-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf23-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bf23-123">-AsJob</span></span>
<span data-ttu-id="3bf23-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3bf23-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3bf23-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf23-125">-DefaultProfile</span></span>
<span data-ttu-id="3bf23-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3bf23-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf23-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3bf23-127">-Force</span></span>
<span data-ttu-id="3bf23-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3bf23-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3bf23-129">-ID</span><span class="sxs-lookup"><span data-stu-id="3bf23-129">-Id</span></span>
<span data-ttu-id="3bf23-130">Anger ID för resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3bf23-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="3bf23-131">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="3bf23-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf23-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bf23-132">-Name</span></span>
<span data-ttu-id="3bf23-133">Anger namnen på de resurs grupper som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3bf23-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="3bf23-134">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="3bf23-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf23-135">-För</span><span class="sxs-lookup"><span data-stu-id="3bf23-135">-Pre</span></span>
<span data-ttu-id="3bf23-136">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3bf23-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3bf23-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3bf23-137">-Confirm</span></span>
<span data-ttu-id="3bf23-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3bf23-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bf23-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bf23-139">-WhatIf</span></span>
<span data-ttu-id="3bf23-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3bf23-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bf23-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3bf23-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bf23-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf23-142">CommonParameters</span></span>
<span data-ttu-id="3bf23-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf23-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf23-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bf23-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf23-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bf23-145">INPUTS</span></span>

## <span data-ttu-id="3bf23-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bf23-146">OUTPUTS</span></span>

## <span data-ttu-id="3bf23-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bf23-147">NOTES</span></span>

## <span data-ttu-id="3bf23-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bf23-148">RELATED LINKS</span></span>

[<span data-ttu-id="3bf23-149">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3bf23-149">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="3bf23-150">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3bf23-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="3bf23-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3bf23-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


