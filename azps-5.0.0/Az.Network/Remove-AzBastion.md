---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325265"
---
# <span data-ttu-id="ecaf9-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="ecaf9-101">Remove-AzBastion</span></span>

## <span data-ttu-id="ecaf9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecaf9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecaf9-103">Tar bort en Bastion-resurs.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="ecaf9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecaf9-104">SYNTAX</span></span>

### <span data-ttu-id="ecaf9-105">ByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="ecaf9-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecaf9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecaf9-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecaf9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecaf9-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecaf9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecaf9-108">DESCRIPTION</span></span>
<span data-ttu-id="ecaf9-109">Tar bort en Bastion-resurs. Example1 tar bort Bastion med dess ResourceGroupName och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="ecaf9-110">Example2 tar bort Bastion med dess objekt med pipelinan.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="ecaf9-111">Example3 tar bort Bastion med dess objekt.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="ecaf9-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecaf9-112">EXAMPLES</span></span>

### <span data-ttu-id="ecaf9-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ecaf9-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="ecaf9-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ecaf9-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="ecaf9-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ecaf9-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="ecaf9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecaf9-116">PARAMETERS</span></span>

### <span data-ttu-id="ecaf9-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecaf9-117">-Confirm</span></span>
<span data-ttu-id="ecaf9-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecaf9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecaf9-119">-DefaultProfile</span></span>
<span data-ttu-id="ecaf9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecaf9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ecaf9-121">-Force</span></span>
<span data-ttu-id="ecaf9-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ecaf9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecaf9-123">-InputObject</span></span>
<span data-ttu-id="ecaf9-124">Bastion-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecaf9-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecaf9-125">-Name</span></span>
<span data-ttu-id="ecaf9-126">Bastion resurs namn som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecaf9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecaf9-127">-PassThru</span></span>
<span data-ttu-id="ecaf9-128">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ecaf9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecaf9-129">-ResourceGroupName</span></span>
<span data-ttu-id="ecaf9-130">Resurs grupps namnet där Bastion finns.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecaf9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecaf9-131">-ResourceId</span></span>
<span data-ttu-id="ecaf9-132">Azure Resource ID för Bastion ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecaf9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecaf9-133">-WhatIf</span></span>
<span data-ttu-id="ecaf9-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecaf9-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecaf9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecaf9-136">CommonParameters</span></span>
<span data-ttu-id="ecaf9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecaf9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecaf9-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecaf9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecaf9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecaf9-139">INPUTS</span></span>

### <span data-ttu-id="ecaf9-140">Microsoft. Azure. commands. Networks. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="ecaf9-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="ecaf9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ecaf9-141">System.String</span></span>

## <span data-ttu-id="ecaf9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecaf9-142">OUTPUTS</span></span>

### <span data-ttu-id="ecaf9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecaf9-143">System.Boolean</span></span>

## <span data-ttu-id="ecaf9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecaf9-144">NOTES</span></span>

## <span data-ttu-id="ecaf9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecaf9-145">RELATED LINKS</span></span>
[<span data-ttu-id="ecaf9-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="ecaf9-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="ecaf9-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="ecaf9-147">New-AzBastion</span></span>](./New-AzBastion.md)