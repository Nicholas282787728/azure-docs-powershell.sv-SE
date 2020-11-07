---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923042"
---
# <span data-ttu-id="2b056-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b056-101">Stop-AzVM</span></span>

## <span data-ttu-id="2b056-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b056-102">SYNOPSIS</span></span>
<span data-ttu-id="2b056-103">Stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="2b056-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2b056-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b056-104">SYNTAX</span></span>

### <span data-ttu-id="2b056-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="2b056-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b056-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b056-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b056-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b056-107">DESCRIPTION</span></span>
<span data-ttu-id="2b056-108">Cmdleten **Stop-AzVM** stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="2b056-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2b056-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b056-109">EXAMPLES</span></span>

### <span data-ttu-id="2b056-110">Exempel 1: stoppa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="2b056-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2b056-111">Det här kommandot stoppar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2b056-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2b056-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b056-112">PARAMETERS</span></span>

### <span data-ttu-id="2b056-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b056-113">-AsJob</span></span>
<span data-ttu-id="2b056-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="2b056-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2b056-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b056-115">-DefaultProfile</span></span>
<span data-ttu-id="2b056-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b056-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b056-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2b056-117">-Force</span></span>
<span data-ttu-id="2b056-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2b056-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b056-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2b056-119">-Id</span></span>
<span data-ttu-id="2b056-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2b056-120">The resource group name.</span></span>

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

### <span data-ttu-id="2b056-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b056-121">-Name</span></span>
<span data-ttu-id="2b056-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="2b056-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b056-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b056-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b056-124">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2b056-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2b056-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="2b056-125">-StayProvisioned</span></span>
<span data-ttu-id="2b056-126">Cmdleten stoppar alla virtuella datorer i VMSS, men avdelar dem inte.</span><span class="sxs-lookup"><span data-stu-id="2b056-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="2b056-127">Kontot debiteras för de stoppade virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="2b056-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="2b056-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b056-128">-Confirm</span></span>
<span data-ttu-id="2b056-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b056-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b056-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b056-130">-WhatIf</span></span>
<span data-ttu-id="2b056-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b056-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b056-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b056-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b056-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b056-133">CommonParameters</span></span>
<span data-ttu-id="2b056-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b056-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b056-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b056-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b056-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b056-136">INPUTS</span></span>

### <span data-ttu-id="2b056-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b056-137">None</span></span>
<span data-ttu-id="2b056-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2b056-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b056-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b056-139">OUTPUTS</span></span>

### <span data-ttu-id="2b056-140">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2b056-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="2b056-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b056-141">NOTES</span></span>

## <span data-ttu-id="2b056-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b056-142">RELATED LINKS</span></span>

[<span data-ttu-id="2b056-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b056-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2b056-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b056-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="2b056-145">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b056-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="2b056-146">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b056-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="2b056-147">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b056-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="2b056-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b056-148">Update-AzVM</span></span>](./Update-AzVM.md)


