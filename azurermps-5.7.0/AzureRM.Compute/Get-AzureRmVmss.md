---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584432"
---
# <span data-ttu-id="da986-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="da986-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da986-102">SYNOPSIS</span></span>
<span data-ttu-id="da986-103">Hämtar egenskaperna för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="da986-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da986-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da986-104">SYNTAX</span></span>

### <span data-ttu-id="da986-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="da986-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="da986-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="da986-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## <span data-ttu-id="da986-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da986-107">DESCRIPTION</span></span>
<span data-ttu-id="da986-108">Cmdleten **Get-AzureRmVmss** hämtar modellen och instans vyn för en virtuell dators skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="da986-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="da986-109">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="da986-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="da986-110">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="da986-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="da986-111">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="da986-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="da986-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da986-112">EXAMPLES</span></span>

### <span data-ttu-id="da986-113">Exempel 1: Hämta egenskaper för en VMSS</span><span class="sxs-lookup"><span data-stu-id="da986-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="da986-114">Det här kommandot får egenskaperna för VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="da986-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="da986-115">Eftersom kommandot inte anger parameter för *InstanceView* , får cmdleten modellen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="da986-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="da986-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da986-116">PARAMETERS</span></span>

### <span data-ttu-id="da986-117">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="da986-117">-InstanceView</span></span>
<span data-ttu-id="da986-118">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="da986-118">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da986-119">-ResourceGroupName</span></span>
<span data-ttu-id="da986-120">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="da986-120">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="da986-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="da986-121">-VMScaleSetName</span></span>
<span data-ttu-id="da986-122">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="da986-122">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="da986-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da986-123">CommonParameters</span></span>
<span data-ttu-id="da986-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da986-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da986-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da986-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da986-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da986-126">INPUTS</span></span>

### <span data-ttu-id="da986-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="da986-127">None</span></span>
<span data-ttu-id="da986-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="da986-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da986-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da986-129">OUTPUTS</span></span>

### <span data-ttu-id="da986-130">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="da986-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="da986-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da986-131">NOTES</span></span>

## <span data-ttu-id="da986-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da986-132">RELATED LINKS</span></span>

[<span data-ttu-id="da986-133">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="da986-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="da986-135">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="da986-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="da986-137">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="da986-138">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="da986-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da986-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


