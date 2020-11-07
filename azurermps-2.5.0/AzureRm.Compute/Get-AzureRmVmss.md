---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930357"
---
# <span data-ttu-id="15b52-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="15b52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15b52-102">SYNOPSIS</span></span>
<span data-ttu-id="15b52-103">Hämtar egenskaperna för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="15b52-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15b52-104">SYNTAX</span></span>

### <span data-ttu-id="15b52-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="15b52-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b52-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="15b52-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15b52-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15b52-107">DESCRIPTION</span></span>
<span data-ttu-id="15b52-108">Cmdleten **Get-AzureRmVmss** hämtar modellen och instans vyn för en virtuell dators skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="15b52-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="15b52-109">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="15b52-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="15b52-110">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="15b52-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="15b52-111">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="15b52-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="15b52-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15b52-112">EXAMPLES</span></span>

### <span data-ttu-id="15b52-113">Exempel 1: Hämta egenskaper för en VMSS</span><span class="sxs-lookup"><span data-stu-id="15b52-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="15b52-114">Det här kommandot får egenskaperna för VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="15b52-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="15b52-115">Eftersom kommandot inte anger parameter för *InstanceView* , får cmdleten modellen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="15b52-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="15b52-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15b52-116">PARAMETERS</span></span>

### <span data-ttu-id="15b52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b52-117">-DefaultProfile</span></span>
<span data-ttu-id="15b52-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15b52-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b52-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="15b52-119">-InstanceView</span></span>
<span data-ttu-id="15b52-120">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="15b52-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b52-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b52-121">-ResourceGroupName</span></span>
<span data-ttu-id="15b52-122">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="15b52-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="15b52-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="15b52-123">-VMScaleSetName</span></span>
<span data-ttu-id="15b52-124">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="15b52-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="15b52-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b52-125">CommonParameters</span></span>
<span data-ttu-id="15b52-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b52-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b52-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b52-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b52-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15b52-128">INPUTS</span></span>

### <span data-ttu-id="15b52-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="15b52-129">None</span></span>
<span data-ttu-id="15b52-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="15b52-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15b52-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15b52-131">OUTPUTS</span></span>

### <span data-ttu-id="15b52-132">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="15b52-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="15b52-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15b52-133">NOTES</span></span>

## <span data-ttu-id="15b52-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15b52-134">RELATED LINKS</span></span>

[<span data-ttu-id="15b52-135">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="15b52-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="15b52-137">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="15b52-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="15b52-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="15b52-140">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="15b52-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="15b52-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


