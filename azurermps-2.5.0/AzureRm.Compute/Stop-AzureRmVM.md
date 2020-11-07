---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4bf5ec5ccdbe79f5557cb2f400fbcc0b9baf5e5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931486"
---
# <span data-ttu-id="a96a6-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a96a6-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="a96a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a96a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a96a6-103">Stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="a96a6-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a96a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a96a6-104">SYNTAX</span></span>

### <span data-ttu-id="a96a6-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="a96a6-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96a6-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a96a6-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a96a6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a96a6-107">DESCRIPTION</span></span>
<span data-ttu-id="a96a6-108">Cmdleten **Stop-AzureRmVM** stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="a96a6-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="a96a6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a96a6-109">EXAMPLES</span></span>

### <span data-ttu-id="a96a6-110">Exempel 1: stoppa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="a96a6-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a96a6-111">Det här kommandot stoppar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a96a6-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a96a6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a96a6-112">PARAMETERS</span></span>

### <span data-ttu-id="a96a6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a96a6-113">-AsJob</span></span>
<span data-ttu-id="a96a6-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="a96a6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a96a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96a6-115">-DefaultProfile</span></span>
<span data-ttu-id="a96a6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a96a6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a96a6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a96a6-117">-Force</span></span>
<span data-ttu-id="a96a6-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a96a6-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a96a6-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a96a6-119">-Id</span></span>
<span data-ttu-id="a96a6-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a96a6-120">The resource group name.</span></span>

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

### <span data-ttu-id="a96a6-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a96a6-121">-Name</span></span>
<span data-ttu-id="a96a6-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="a96a6-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="a96a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="a96a6-124">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a96a6-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a96a6-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="a96a6-125">-StayProvisioned</span></span>
<span data-ttu-id="a96a6-126">Cmdleten stoppar alla virtuella datorer i VMSS, men avdelar dem inte.</span><span class="sxs-lookup"><span data-stu-id="a96a6-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="a96a6-127">Kontot debiteras för de stoppade virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="a96a6-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="a96a6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a96a6-128">-Confirm</span></span>
<span data-ttu-id="a96a6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a96a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96a6-130">-WhatIf</span></span>
<span data-ttu-id="a96a6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a96a6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a96a6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a96a6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96a6-133">CommonParameters</span></span>
<span data-ttu-id="a96a6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96a6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a96a6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96a6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a96a6-136">INPUTS</span></span>

### <span data-ttu-id="a96a6-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="a96a6-137">None</span></span>
<span data-ttu-id="a96a6-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a96a6-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a96a6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a96a6-139">OUTPUTS</span></span>

### <span data-ttu-id="a96a6-140">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a96a6-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a96a6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a96a6-141">NOTES</span></span>

## <span data-ttu-id="a96a6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a96a6-142">RELATED LINKS</span></span>

[<span data-ttu-id="a96a6-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a96a6-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a96a6-144">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a96a6-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="a96a6-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a96a6-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="a96a6-146">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a96a6-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="a96a6-147">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a96a6-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="a96a6-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a96a6-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


