---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 8d24aadd185a58472268fc4edf9ca504e7592bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575713"
---
# <span data-ttu-id="1c583-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="1c583-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="1c583-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c583-102">SYNOPSIS</span></span>
<span data-ttu-id="1c583-103">Hämtar egenskaperna för en VMSS-virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1c583-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c583-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c583-104">SYNTAX</span></span>

### <span data-ttu-id="1c583-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="1c583-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c583-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="1c583-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [<CommonParameters>]
```

## <span data-ttu-id="1c583-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c583-107">DESCRIPTION</span></span>
<span data-ttu-id="1c583-108">Cmdleten **Get-AzureRmVmssVM** hämtar modellen vy och instans för en virtuell dator med skalnings uppsättning (virtuell dator).</span><span class="sxs-lookup"><span data-stu-id="1c583-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="1c583-109">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1c583-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="1c583-110">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="1c583-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="1c583-111">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1c583-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="1c583-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c583-112">EXAMPLES</span></span>

### <span data-ttu-id="1c583-113">Exempel 1: Hämta egenskaper för en VMSS virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1c583-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="1c583-114">Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS001 som tillhör resurs gruppen VMSS.</span><span class="sxs-lookup"><span data-stu-id="1c583-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="1c583-115">Eftersom kommandot inte anger parameter för *InstanceView* , får cmdleten modellen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1c583-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="1c583-116">Exempel 2: Hämta modell visnings egenskaperna för en VMSS-virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1c583-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="1c583-117">Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS004 som tillhör resurs gruppen VMSS.</span><span class="sxs-lookup"><span data-stu-id="1c583-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="1c583-118">Kommandot hämtar det instans-ID som lagras i variabeln $ID vars modell vy ska visas.</span><span class="sxs-lookup"><span data-stu-id="1c583-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="1c583-119">Exempel 3: Hämta instans Visa egenskaper för en VMSS-virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1c583-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="1c583-120">Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS004 som tillhör resurs gruppen VMSS.</span><span class="sxs-lookup"><span data-stu-id="1c583-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="1c583-121">Eftersom kommandot *InstanceView* parameter anges i cmdlet hämtas instans visningen av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1c583-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="1c583-122">Med kommandot hämtas instans-ID som lagras i variabeln $ID som instans-vyn ska hämtas för.</span><span class="sxs-lookup"><span data-stu-id="1c583-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="1c583-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c583-123">PARAMETERS</span></span>

### <span data-ttu-id="1c583-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1c583-124">-InstanceId</span></span>
<span data-ttu-id="1c583-125">Anger det instans-ID som modell läget ska visas för.</span><span class="sxs-lookup"><span data-stu-id="1c583-125">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c583-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="1c583-126">-InstanceView</span></span>
<span data-ttu-id="1c583-127">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="1c583-127">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c583-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c583-128">-ResourceGroupName</span></span>
<span data-ttu-id="1c583-129">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="1c583-129">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c583-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1c583-130">-VMScaleSetName</span></span>
<span data-ttu-id="1c583-131">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="1c583-131">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c583-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c583-132">CommonParameters</span></span>
<span data-ttu-id="1c583-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c583-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c583-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c583-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c583-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c583-135">INPUTS</span></span>

### <span data-ttu-id="1c583-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="1c583-136">None</span></span>
<span data-ttu-id="1c583-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1c583-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c583-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c583-138">OUTPUTS</span></span>

### <span data-ttu-id="1c583-139">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1c583-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1c583-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c583-140">NOTES</span></span>

## <span data-ttu-id="1c583-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c583-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c583-142">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="1c583-142">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="1c583-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1c583-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


