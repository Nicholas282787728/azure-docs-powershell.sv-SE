---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573688"
---
# <span data-ttu-id="30001-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30001-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="30001-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30001-102">SYNOPSIS</span></span>
<span data-ttu-id="30001-103">Startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="30001-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30001-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30001-104">SYNTAX</span></span>

### <span data-ttu-id="30001-105">RestartResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="30001-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30001-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="30001-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30001-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="30001-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30001-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="30001-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30001-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30001-109">DESCRIPTION</span></span>
<span data-ttu-id="30001-110">Cmdleten **restart-AzureRmVM** startar om en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="30001-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="30001-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30001-111">EXAMPLES</span></span>

### <span data-ttu-id="30001-112">Exempel 1: starta om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="30001-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="30001-113">Det här kommandot startar om den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="30001-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="30001-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30001-114">PARAMETERS</span></span>

### <span data-ttu-id="30001-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30001-115">-DefaultProfile</span></span>
<span data-ttu-id="30001-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30001-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30001-117">-ID</span><span class="sxs-lookup"><span data-stu-id="30001-117">-Id</span></span>
<span data-ttu-id="30001-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="30001-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30001-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="30001-119">-Name</span></span>
<span data-ttu-id="30001-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="30001-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="30001-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="30001-121">-PerformMaintenance</span></span>
<span data-ttu-id="30001-122">För att utföra underhåll av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="30001-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30001-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30001-123">-ResourceGroupName</span></span>
<span data-ttu-id="30001-124">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="30001-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30001-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30001-125">-Confirm</span></span>
<span data-ttu-id="30001-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30001-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30001-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30001-127">-WhatIf</span></span>
<span data-ttu-id="30001-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30001-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30001-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30001-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30001-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30001-130">CommonParameters</span></span>
<span data-ttu-id="30001-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30001-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30001-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30001-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30001-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30001-133">INPUTS</span></span>

## <span data-ttu-id="30001-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30001-134">OUTPUTS</span></span>

## <span data-ttu-id="30001-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30001-135">NOTES</span></span>

## <span data-ttu-id="30001-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30001-136">RELATED LINKS</span></span>

[<span data-ttu-id="30001-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30001-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="30001-138">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30001-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="30001-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30001-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="30001-140">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30001-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="30001-141">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30001-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="30001-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="30001-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


