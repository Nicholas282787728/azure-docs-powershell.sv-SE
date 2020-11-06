---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580660"
---
# <span data-ttu-id="742e8-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="742e8-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="742e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="742e8-102">SYNOPSIS</span></span>
<span data-ttu-id="742e8-103">Stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="742e8-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="742e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="742e8-104">SYNTAX</span></span>

### <span data-ttu-id="742e8-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="742e8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="742e8-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="742e8-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="742e8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="742e8-107">DESCRIPTION</span></span>
<span data-ttu-id="742e8-108">Cmdleten **Stop-AzureRmVM** stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="742e8-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="742e8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="742e8-109">EXAMPLES</span></span>

### <span data-ttu-id="742e8-110">Exempel 1: stoppa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="742e8-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="742e8-111">Det här kommandot stoppar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="742e8-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="742e8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="742e8-112">PARAMETERS</span></span>

### <span data-ttu-id="742e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742e8-113">-DefaultProfile</span></span>
<span data-ttu-id="742e8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="742e8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="742e8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="742e8-115">-Force</span></span>
<span data-ttu-id="742e8-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="742e8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="742e8-117">-ID</span><span class="sxs-lookup"><span data-stu-id="742e8-117">-Id</span></span>
<span data-ttu-id="742e8-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="742e8-118">The resource group name.</span></span>

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

### <span data-ttu-id="742e8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="742e8-119">-Name</span></span>
<span data-ttu-id="742e8-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="742e8-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="742e8-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="742e8-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="742e8-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="742e8-123">-StayProvisioned</span></span>
<span data-ttu-id="742e8-124">Cmdleten stoppar alla virtuella datorer i VMSS, men avdelar dem inte.</span><span class="sxs-lookup"><span data-stu-id="742e8-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="742e8-125">Kontot debiteras för de stoppade virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="742e8-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="742e8-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="742e8-126">-Confirm</span></span>
<span data-ttu-id="742e8-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="742e8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="742e8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="742e8-128">-WhatIf</span></span>
<span data-ttu-id="742e8-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="742e8-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="742e8-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="742e8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="742e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742e8-131">CommonParameters</span></span>
<span data-ttu-id="742e8-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742e8-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742e8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742e8-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="742e8-134">INPUTS</span></span>

## <span data-ttu-id="742e8-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="742e8-135">OUTPUTS</span></span>

## <span data-ttu-id="742e8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="742e8-136">NOTES</span></span>

## <span data-ttu-id="742e8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="742e8-137">RELATED LINKS</span></span>

[<span data-ttu-id="742e8-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="742e8-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="742e8-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="742e8-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="742e8-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="742e8-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="742e8-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="742e8-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="742e8-142">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="742e8-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="742e8-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="742e8-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


