---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754445"
---
# <span data-ttu-id="91109-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="91109-101">Start-AzVM</span></span>

## <span data-ttu-id="91109-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91109-102">SYNOPSIS</span></span>
<span data-ttu-id="91109-103">Startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="91109-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="91109-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91109-104">SYNTAX</span></span>

### <span data-ttu-id="91109-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="91109-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91109-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="91109-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91109-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91109-107">DESCRIPTION</span></span>
<span data-ttu-id="91109-108">Cmdleten **Start-AzVM** startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="91109-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="91109-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91109-109">EXAMPLES</span></span>

### <span data-ttu-id="91109-110">Exempel 1: starta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="91109-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="91109-111">Det här kommandot startar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="91109-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="91109-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91109-112">PARAMETERS</span></span>

### <span data-ttu-id="91109-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91109-113">-AsJob</span></span>
<span data-ttu-id="91109-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="91109-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="91109-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91109-115">-DefaultProfile</span></span>
<span data-ttu-id="91109-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91109-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91109-117">-ID</span><span class="sxs-lookup"><span data-stu-id="91109-117">-Id</span></span>
<span data-ttu-id="91109-118">ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="91109-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91109-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="91109-119">-Name</span></span>
<span data-ttu-id="91109-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="91109-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91109-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91109-121">-ResourceGroupName</span></span>
<span data-ttu-id="91109-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="91109-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91109-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91109-123">-Confirm</span></span>
<span data-ttu-id="91109-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91109-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91109-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91109-125">-WhatIf</span></span>
<span data-ttu-id="91109-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91109-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91109-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91109-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91109-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91109-128">CommonParameters</span></span>
<span data-ttu-id="91109-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91109-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91109-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91109-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91109-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91109-131">INPUTS</span></span>

### <span data-ttu-id="91109-132">System. String</span><span class="sxs-lookup"><span data-stu-id="91109-132">System.String</span></span>

## <span data-ttu-id="91109-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91109-133">OUTPUTS</span></span>

### <span data-ttu-id="91109-134">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="91109-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="91109-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91109-135">NOTES</span></span>

## <span data-ttu-id="91109-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91109-136">RELATED LINKS</span></span>

[<span data-ttu-id="91109-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="91109-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="91109-138">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="91109-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="91109-139">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="91109-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="91109-140">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="91109-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="91109-141">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="91109-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="91109-142">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="91109-142">Update-AzVM</span></span>](./Update-AzVM.md)


