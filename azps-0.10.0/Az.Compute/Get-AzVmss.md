---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925133"
---
# <span data-ttu-id="df351-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-101">Get-AzVmss</span></span>

## <span data-ttu-id="df351-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df351-102">SYNOPSIS</span></span>
<span data-ttu-id="df351-103">Hämtar egenskaperna för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="df351-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="df351-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df351-104">SYNTAX</span></span>

### <span data-ttu-id="df351-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="df351-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df351-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="df351-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df351-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df351-107">DESCRIPTION</span></span>
<span data-ttu-id="df351-108">Cmdleten **Get-AzVmss** hämtar modellen och instans vyn för en virtuell dators skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="df351-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="df351-109">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="df351-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="df351-110">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="df351-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="df351-111">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="df351-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="df351-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df351-112">EXAMPLES</span></span>

### <span data-ttu-id="df351-113">Exempel 1: Hämta egenskaper för en VMSS</span><span class="sxs-lookup"><span data-stu-id="df351-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="df351-114">Det här kommandot får egenskaperna för VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="df351-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="df351-115">Eftersom kommandot inte anger parameter för *InstanceView* , får cmdleten modellen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="df351-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="df351-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df351-116">PARAMETERS</span></span>

### <span data-ttu-id="df351-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df351-117">-DefaultProfile</span></span>
<span data-ttu-id="df351-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df351-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df351-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="df351-119">-InstanceView</span></span>
<span data-ttu-id="df351-120">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="df351-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="df351-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df351-121">-ResourceGroupName</span></span>
<span data-ttu-id="df351-122">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="df351-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="df351-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="df351-123">-VMScaleSetName</span></span>
<span data-ttu-id="df351-124">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="df351-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="df351-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df351-125">CommonParameters</span></span>
<span data-ttu-id="df351-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df351-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df351-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df351-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df351-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df351-128">INPUTS</span></span>

### <span data-ttu-id="df351-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="df351-129">None</span></span>
<span data-ttu-id="df351-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="df351-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df351-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df351-131">OUTPUTS</span></span>

### <span data-ttu-id="df351-132">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="df351-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="df351-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df351-133">NOTES</span></span>

## <span data-ttu-id="df351-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df351-134">RELATED LINKS</span></span>

[<span data-ttu-id="df351-135">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="df351-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="df351-137">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="df351-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="df351-139">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="df351-140">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="df351-141">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df351-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


