---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 2ac1e336161d4cfad1bbef37ec98716456a8143c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745150"
---
# <span data-ttu-id="7c3c2-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="7c3c2-101">Get-AzVMSize</span></span>

## <span data-ttu-id="7c3c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c3c2-103">Hämtar tillgängliga storlekar på virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="7c3c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c3c2-104">SYNTAX</span></span>

### <span data-ttu-id="7c3c2-105">ListVirtualMachineSizeParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7c3c2-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c3c2-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7c3c2-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c3c2-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7c3c2-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c3c2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c3c2-108">DESCRIPTION</span></span>
<span data-ttu-id="7c3c2-109">Cmdleten **Get-AzVMSize** hämtar tillgängliga storlekar på virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="7c3c2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c3c2-110">EXAMPLES</span></span>

### <span data-ttu-id="7c3c2-111">Exempel 1: Hämta storlekar på en virtuell dator för en plats</span><span class="sxs-lookup"><span data-stu-id="7c3c2-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="7c3c2-112">Det här kommandot får de tillgängliga storlekarna för virtuella datorer på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="7c3c2-113">Exempel 2: Hämta storlekar för en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="7c3c2-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="7c3c2-114">Det här kommandot får tillgängliga storlekar för virtuella datorer som du kan distribuera i tillgänglighets uppsättningen med namnet AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="7c3c2-115">Exempel 3: skapa storlekar för en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7c3c2-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="7c3c2-116">Det här kommandot får tillgängliga storlekar för den befintliga virtuella datorn med namnet VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="7c3c2-117">Du kan ändra storlek på den virtuella datorn till de storlekar det här kommandot får.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="7c3c2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c3c2-118">PARAMETERS</span></span>

### <span data-ttu-id="7c3c2-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="7c3c2-119">-AvailabilitySetName</span></span>
<span data-ttu-id="7c3c2-120">Anger namnet på den tillgänglighets uppsättning för vilken denna cmdlet får de tillgängliga virtuella dator storlekarna.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c3c2-121">-DefaultProfile</span></span>
<span data-ttu-id="7c3c2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c3c2-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="7c3c2-123">-Location</span></span>
<span data-ttu-id="7c3c2-124">Anger platsen för vilken denna cmdlet får de tillgängliga virtuella dator storlekarna.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c3c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c3c2-126">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c2-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c3c2-127">-VMName</span></span>
<span data-ttu-id="7c3c2-128">Anger namnet på den virtuella dator där den här cmdleten får de tillgängliga storlekarna för storleks ändring.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c3c2-129">CommonParameters</span></span>
<span data-ttu-id="7c3c2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c3c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c3c2-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c3c2-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c3c2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c3c2-132">INPUTS</span></span>

### <span data-ttu-id="7c3c2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7c3c2-133">System.String</span></span>

## <span data-ttu-id="7c3c2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c3c2-134">OUTPUTS</span></span>

### <span data-ttu-id="7c3c2-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="7c3c2-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="7c3c2-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c3c2-136">NOTES</span></span>

## <span data-ttu-id="7c3c2-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c3c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="7c3c2-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7c3c2-138">Get-AzVM</span></span>](./Get-AzVM.md)

