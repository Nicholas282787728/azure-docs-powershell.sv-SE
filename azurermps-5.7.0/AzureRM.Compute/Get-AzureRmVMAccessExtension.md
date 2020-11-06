---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575718"
---
# <span data-ttu-id="037ea-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="037ea-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="037ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="037ea-102">SYNOPSIS</span></span>
<span data-ttu-id="037ea-103">Hämtar information om VMAccess-tillägget.</span><span class="sxs-lookup"><span data-stu-id="037ea-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="037ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="037ea-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="037ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="037ea-105">DESCRIPTION</span></span>
<span data-ttu-id="037ea-106">Cmdleten **Get-AzureRmVMAccessExtension** hämtar information om tillägget virtuell dator åtkomst (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="037ea-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="037ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="037ea-107">EXAMPLES</span></span>

### <span data-ttu-id="037ea-108">Exempel 1: skaffa VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="037ea-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="037ea-109">Det här kommandot får tillägget VMAccess med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="037ea-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="037ea-110">Exempel 2: Hämta instans vyn för VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="037ea-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="037ea-111">Det här kommandot hämtar instans vyn för VMAccess-tillägget med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="037ea-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="037ea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="037ea-112">PARAMETERS</span></span>

### <span data-ttu-id="037ea-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="037ea-113">-Name</span></span>
<span data-ttu-id="037ea-114">Anger namnet på den fil ändelse som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="037ea-114">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="037ea-115">-ResourceGroupName</span></span>
<span data-ttu-id="037ea-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="037ea-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ea-117">-Status</span><span class="sxs-lookup"><span data-stu-id="037ea-117">-Status</span></span>
<span data-ttu-id="037ea-118">Anger att denna cmdlet endast får instans vyn av tillägget.</span><span class="sxs-lookup"><span data-stu-id="037ea-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ea-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="037ea-119">-VMName</span></span>
<span data-ttu-id="037ea-120">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="037ea-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="037ea-121">Denna cmdlet hämtar information om VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="037ea-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037ea-122">CommonParameters</span></span>
<span data-ttu-id="037ea-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037ea-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="037ea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037ea-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="037ea-125">INPUTS</span></span>

### <span data-ttu-id="037ea-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="037ea-126">None</span></span>
<span data-ttu-id="037ea-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="037ea-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="037ea-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="037ea-128">OUTPUTS</span></span>

## <span data-ttu-id="037ea-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="037ea-129">NOTES</span></span>

## <span data-ttu-id="037ea-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="037ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="037ea-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="037ea-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="037ea-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="037ea-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="037ea-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="037ea-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


