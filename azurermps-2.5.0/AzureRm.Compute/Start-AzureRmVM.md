---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930262"
---
# <span data-ttu-id="483bd-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bd-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="483bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="483bd-102">SYNOPSIS</span></span>
<span data-ttu-id="483bd-103">Startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="483bd-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="483bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="483bd-104">SYNTAX</span></span>

### <span data-ttu-id="483bd-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="483bd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483bd-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="483bd-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="483bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="483bd-107">DESCRIPTION</span></span>
<span data-ttu-id="483bd-108">Cmdleten **Start-AzureRmVM** startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="483bd-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="483bd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="483bd-109">EXAMPLES</span></span>

### <span data-ttu-id="483bd-110">Exempel 1: starta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="483bd-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="483bd-111">Det här kommandot startar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="483bd-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="483bd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="483bd-112">PARAMETERS</span></span>

### <span data-ttu-id="483bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="483bd-113">-AsJob</span></span>
<span data-ttu-id="483bd-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="483bd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="483bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483bd-115">-DefaultProfile</span></span>
<span data-ttu-id="483bd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="483bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="483bd-117">-ID</span><span class="sxs-lookup"><span data-stu-id="483bd-117">-Id</span></span>
<span data-ttu-id="483bd-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="483bd-118">The resource group name.</span></span>

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

### <span data-ttu-id="483bd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="483bd-119">-Name</span></span>
<span data-ttu-id="483bd-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="483bd-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="483bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="483bd-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="483bd-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="483bd-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="483bd-123">-Confirm</span></span>
<span data-ttu-id="483bd-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="483bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483bd-125">-WhatIf</span></span>
<span data-ttu-id="483bd-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="483bd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="483bd-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="483bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483bd-128">CommonParameters</span></span>
<span data-ttu-id="483bd-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483bd-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483bd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483bd-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="483bd-131">INPUTS</span></span>

### <span data-ttu-id="483bd-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="483bd-132">None</span></span>
<span data-ttu-id="483bd-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="483bd-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="483bd-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="483bd-134">OUTPUTS</span></span>

### <span data-ttu-id="483bd-135">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="483bd-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="483bd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="483bd-136">NOTES</span></span>

## <span data-ttu-id="483bd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="483bd-137">RELATED LINKS</span></span>

[<span data-ttu-id="483bd-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bd-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="483bd-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bd-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="483bd-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bd-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="483bd-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bd-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="483bd-142">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bd-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="483bd-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="483bd-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


