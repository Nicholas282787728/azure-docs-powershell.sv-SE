---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524512"
---
# <span data-ttu-id="b4a5a-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="b4a5a-101">Get-AzVMSize</span></span>

## <span data-ttu-id="b4a5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a5a-103">Hämtar tillgängliga storlekar på virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="b4a5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4a5a-104">SYNTAX</span></span>

### <span data-ttu-id="b4a5a-105">ListVirtualMachineSizeParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b4a5a-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4a5a-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b4a5a-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4a5a-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b4a5a-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4a5a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4a5a-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a5a-109">Cmdleten **Get-AzVMSize** hämtar tillgängliga storlekar på virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="b4a5a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4a5a-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a5a-111">Exempel 1: Hämta storlekar på en virtuell dator för en plats</span><span class="sxs-lookup"><span data-stu-id="b4a5a-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="b4a5a-112">Det här kommandot får de tillgängliga storlekarna för virtuella datorer på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="b4a5a-113">Exempel 2: Hämta storlekar för en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="b4a5a-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="b4a5a-114">Det här kommandot får tillgängliga storlekar för virtuella datorer som du kan distribuera i tillgänglighets uppsättningen med namnet AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="b4a5a-115">Exempel 3: skapa storlekar för en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b4a5a-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="b4a5a-116">Det här kommandot får tillgängliga storlekar för den befintliga virtuella datorn med namnet VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="b4a5a-117">Du kan ändra storlek på den virtuella datorn till de storlekar det här kommandot får.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="b4a5a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4a5a-118">PARAMETERS</span></span>

### <span data-ttu-id="b4a5a-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="b4a5a-119">-AvailabilitySetName</span></span>
<span data-ttu-id="b4a5a-120">Anger namnet på den tillgänglighets uppsättning för vilken denna cmdlet får de tillgängliga virtuella dator storlekarna.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="b4a5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a5a-121">-DefaultProfile</span></span>
<span data-ttu-id="b4a5a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4a5a-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="b4a5a-123">-Location</span></span>
<span data-ttu-id="b4a5a-124">Anger platsen för vilken denna cmdlet får de tillgängliga virtuella dator storlekarna.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="b4a5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4a5a-126">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b4a5a-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="b4a5a-127">-VMName</span></span>
<span data-ttu-id="b4a5a-128">Anger namnet på den virtuella dator där den här cmdleten får de tillgängliga storlekarna för storleks ändring.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="b4a5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a5a-129">CommonParameters</span></span>
<span data-ttu-id="b4a5a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a5a-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4a5a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a5a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4a5a-132">INPUTS</span></span>

### <span data-ttu-id="b4a5a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b4a5a-133">System.String</span></span>

## <span data-ttu-id="b4a5a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4a5a-134">OUTPUTS</span></span>

### <span data-ttu-id="b4a5a-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="b4a5a-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="b4a5a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4a5a-136">NOTES</span></span>

## <span data-ttu-id="b4a5a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4a5a-137">RELATED LINKS</span></span>

[<span data-ttu-id="b4a5a-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b4a5a-138">Get-AzVM</span></span>](./Get-AzVM.md)


