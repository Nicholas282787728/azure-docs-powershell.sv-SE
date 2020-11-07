---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 43c6f96556cb283ef21f24df00d6a6ddb9c5397a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925122"
---
# <span data-ttu-id="125af-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="125af-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="125af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="125af-102">SYNOPSIS</span></span>
<span data-ttu-id="125af-103">Hämtar egenskaperna för en VMSS-virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="125af-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="125af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="125af-104">SYNTAX</span></span>

### <span data-ttu-id="125af-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="125af-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="125af-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="125af-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="125af-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="125af-107">DESCRIPTION</span></span>
<span data-ttu-id="125af-108">Cmdleten **Get-AzVmssVM** hämtar modellen vy och instans för en virtuell dator med skalnings uppsättning (virtuell dator).</span><span class="sxs-lookup"><span data-stu-id="125af-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="125af-109">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="125af-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="125af-110">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="125af-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="125af-111">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="125af-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="125af-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="125af-112">EXAMPLES</span></span>

### <span data-ttu-id="125af-113">Exempel 1: Hämta egenskaper för en VMSS virtuell dator</span><span class="sxs-lookup"><span data-stu-id="125af-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="125af-114">Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS001 som tillhör resurs gruppen VMSS.</span><span class="sxs-lookup"><span data-stu-id="125af-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="125af-115">Eftersom kommandot inte anger parameter för *InstanceView* , får cmdleten modellen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="125af-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="125af-116">Exempel 2: Hämta modell visnings egenskaperna för en VMSS-virtuell dator</span><span class="sxs-lookup"><span data-stu-id="125af-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="125af-117">Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS004 som tillhör resurs gruppen VMSS.</span><span class="sxs-lookup"><span data-stu-id="125af-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="125af-118">Kommandot hämtar det instans-ID som lagras i variabeln $ID vars modell vy ska visas.</span><span class="sxs-lookup"><span data-stu-id="125af-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="125af-119">Exempel 3: Hämta instans Visa egenskaper för en VMSS-virtuell dator</span><span class="sxs-lookup"><span data-stu-id="125af-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="125af-120">Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS004 som tillhör resurs gruppen VMSS.</span><span class="sxs-lookup"><span data-stu-id="125af-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="125af-121">Eftersom kommandot *InstanceView* parameter anges i cmdlet hämtas instans visningen av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="125af-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="125af-122">Med kommandot hämtas instans-ID som lagras i variabeln $ID som instans-vyn ska hämtas för.</span><span class="sxs-lookup"><span data-stu-id="125af-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="125af-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="125af-123">PARAMETERS</span></span>

### <span data-ttu-id="125af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125af-124">-DefaultProfile</span></span>
<span data-ttu-id="125af-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="125af-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="125af-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="125af-126">-InstanceId</span></span>
<span data-ttu-id="125af-127">Anger det instans-ID som modell läget ska visas för.</span><span class="sxs-lookup"><span data-stu-id="125af-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="125af-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="125af-128">-InstanceView</span></span>
<span data-ttu-id="125af-129">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="125af-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="125af-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125af-130">-ResourceGroupName</span></span>
<span data-ttu-id="125af-131">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="125af-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="125af-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="125af-132">-VMScaleSetName</span></span>
<span data-ttu-id="125af-133">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="125af-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="125af-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125af-134">CommonParameters</span></span>
<span data-ttu-id="125af-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="125af-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125af-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="125af-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125af-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="125af-137">INPUTS</span></span>

### <span data-ttu-id="125af-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="125af-138">None</span></span>
<span data-ttu-id="125af-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="125af-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="125af-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="125af-140">OUTPUTS</span></span>

### <span data-ttu-id="125af-141">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="125af-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="125af-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="125af-142">NOTES</span></span>

## <span data-ttu-id="125af-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="125af-143">RELATED LINKS</span></span>

[<span data-ttu-id="125af-144">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="125af-144">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="125af-145">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="125af-145">Get-AzVmss</span></span>](./Get-AzVmss.md)


