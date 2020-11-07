---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f816be5d3c024e43074d6a75c5ba79df4b2fdb3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929466"
---
# <span data-ttu-id="63155-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63155-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="63155-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63155-102">SYNOPSIS</span></span>
<span data-ttu-id="63155-103">Tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="63155-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63155-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63155-104">SYNTAX</span></span>

### <span data-ttu-id="63155-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="63155-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63155-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="63155-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63155-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63155-107">DESCRIPTION</span></span>
<span data-ttu-id="63155-108">Cmdleten **Remove-AzureRmVM** tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="63155-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="63155-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63155-109">EXAMPLES</span></span>

### <span data-ttu-id="63155-110">Exempel 1: ta bort en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="63155-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="63155-111">Det här kommandot tar bort den virtuella datorn med namnet VirtualMachine07 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="63155-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="63155-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63155-112">PARAMETERS</span></span>

### <span data-ttu-id="63155-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63155-113">-AsJob</span></span>
<span data-ttu-id="63155-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="63155-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="63155-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63155-115">-DefaultProfile</span></span>
<span data-ttu-id="63155-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63155-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63155-117">-Force</span><span class="sxs-lookup"><span data-stu-id="63155-117">-Force</span></span>
<span data-ttu-id="63155-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="63155-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63155-119">-ID</span><span class="sxs-lookup"><span data-stu-id="63155-119">-Id</span></span>
<span data-ttu-id="63155-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="63155-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63155-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="63155-121">-Name</span></span>
<span data-ttu-id="63155-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="63155-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63155-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63155-123">-ResourceGroupName</span></span>
<span data-ttu-id="63155-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="63155-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63155-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63155-125">-Confirm</span></span>
<span data-ttu-id="63155-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63155-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63155-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63155-127">-WhatIf</span></span>
<span data-ttu-id="63155-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63155-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="63155-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63155-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63155-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63155-130">CommonParameters</span></span>
<span data-ttu-id="63155-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63155-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63155-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63155-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63155-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63155-133">INPUTS</span></span>

### <span data-ttu-id="63155-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="63155-134">None</span></span>
<span data-ttu-id="63155-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="63155-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63155-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63155-136">OUTPUTS</span></span>

### <span data-ttu-id="63155-137">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="63155-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="63155-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63155-138">NOTES</span></span>

## <span data-ttu-id="63155-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63155-139">RELATED LINKS</span></span>

[<span data-ttu-id="63155-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63155-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="63155-141">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63155-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="63155-142">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63155-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="63155-143">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63155-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="63155-144">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63155-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="63155-145">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="63155-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


