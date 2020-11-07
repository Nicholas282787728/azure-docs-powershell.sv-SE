---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924982"
---
# <span data-ttu-id="4bcfc-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bcfc-101">Remove-AzVM</span></span>

## <span data-ttu-id="4bcfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bcfc-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcfc-103">Tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="4bcfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bcfc-104">SYNTAX</span></span>

### <span data-ttu-id="4bcfc-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="4bcfc-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bcfc-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4bcfc-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bcfc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bcfc-107">DESCRIPTION</span></span>
<span data-ttu-id="4bcfc-108">Cmdleten **Remove-AzVM** tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="4bcfc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bcfc-109">EXAMPLES</span></span>

### <span data-ttu-id="4bcfc-110">Exempel 1: ta bort en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4bcfc-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="4bcfc-111">Det här kommandot tar bort den virtuella datorn med namnet VirtualMachine07 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="4bcfc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bcfc-112">PARAMETERS</span></span>

### <span data-ttu-id="4bcfc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bcfc-113">-AsJob</span></span>
<span data-ttu-id="4bcfc-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4bcfc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcfc-115">-DefaultProfile</span></span>
<span data-ttu-id="4bcfc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bcfc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4bcfc-117">-Force</span></span>
<span data-ttu-id="4bcfc-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bcfc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="4bcfc-119">-Id</span></span>
<span data-ttu-id="4bcfc-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-120">The resource group name.</span></span>

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

### <span data-ttu-id="4bcfc-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4bcfc-121">-Name</span></span>
<span data-ttu-id="4bcfc-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-122">The resource name.</span></span>

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

### <span data-ttu-id="4bcfc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcfc-123">-ResourceGroupName</span></span>
<span data-ttu-id="4bcfc-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4bcfc-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bcfc-125">-Confirm</span></span>
<span data-ttu-id="4bcfc-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bcfc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcfc-127">-WhatIf</span></span>
<span data-ttu-id="4bcfc-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4bcfc-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bcfc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcfc-130">CommonParameters</span></span>
<span data-ttu-id="4bcfc-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcfc-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcfc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcfc-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bcfc-133">INPUTS</span></span>

### <span data-ttu-id="4bcfc-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="4bcfc-134">None</span></span>
<span data-ttu-id="4bcfc-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4bcfc-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bcfc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bcfc-136">OUTPUTS</span></span>

### <span data-ttu-id="4bcfc-137">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="4bcfc-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="4bcfc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bcfc-138">NOTES</span></span>

## <span data-ttu-id="4bcfc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bcfc-139">RELATED LINKS</span></span>

[<span data-ttu-id="4bcfc-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bcfc-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4bcfc-141">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bcfc-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="4bcfc-142">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bcfc-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="4bcfc-143">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bcfc-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="4bcfc-144">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bcfc-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="4bcfc-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bcfc-145">Update-AzVM</span></span>](./Update-AzVM.md)


