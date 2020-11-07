---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 7b9e6aa5a9879e0f7abb281810d80a6900198ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755975"
---
# <span data-ttu-id="d2d2d-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2d2d-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="d2d2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d2d-103">Startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2d2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2d2d-104">SYNTAX</span></span>

### <span data-ttu-id="d2d2d-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="d2d2d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d2d-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d2d2d-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d2d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2d2d-107">DESCRIPTION</span></span>
<span data-ttu-id="d2d2d-108">Cmdleten **Start-AzureRmVM** startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="d2d2d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2d2d-109">EXAMPLES</span></span>

### <span data-ttu-id="d2d2d-110">Exempel 1: starta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="d2d2d-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d2d2d-111">Det här kommandot startar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="d2d2d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2d2d-112">PARAMETERS</span></span>

### <span data-ttu-id="d2d2d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2d2d-113">-AsJob</span></span>
<span data-ttu-id="d2d2d-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d2d2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d2d-115">-DefaultProfile</span></span>
<span data-ttu-id="d2d2d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d2d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d2d2d-117">-Id</span></span>
<span data-ttu-id="d2d2d-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-118">The resource group name.</span></span>

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

### <span data-ttu-id="d2d2d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2d2d-119">-Name</span></span>
<span data-ttu-id="d2d2d-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="d2d2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="d2d2d-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d2d2d-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2d2d-123">-Confirm</span></span>
<span data-ttu-id="d2d2d-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d2d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d2d-125">-WhatIf</span></span>
<span data-ttu-id="d2d2d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2d2d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d2d-128">CommonParameters</span></span>
<span data-ttu-id="d2d2d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d2d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d2d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d2d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2d2d-131">INPUTS</span></span>

### <span data-ttu-id="d2d2d-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="d2d2d-132">None</span></span>
<span data-ttu-id="d2d2d-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d2d2d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2d2d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2d2d-134">OUTPUTS</span></span>

### <span data-ttu-id="d2d2d-135">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d2d2d-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="d2d2d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2d2d-136">NOTES</span></span>

## <span data-ttu-id="d2d2d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2d2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="d2d2d-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2d2d-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d2d2d-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2d2d-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="d2d2d-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2d2d-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="d2d2d-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2d2d-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="d2d2d-142">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2d2d-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="d2d2d-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d2d2d-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


