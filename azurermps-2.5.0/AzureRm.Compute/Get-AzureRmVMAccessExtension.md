---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929478"
---
# <span data-ttu-id="6db8c-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6db8c-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="6db8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6db8c-102">SYNOPSIS</span></span>
<span data-ttu-id="6db8c-103">Hämtar information om VMAccess-tillägget.</span><span class="sxs-lookup"><span data-stu-id="6db8c-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6db8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6db8c-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6db8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6db8c-105">DESCRIPTION</span></span>
<span data-ttu-id="6db8c-106">Cmdleten **Get-AzureRmVMAccessExtension** hämtar information om tillägget virtuell dator åtkomst (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="6db8c-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="6db8c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6db8c-107">EXAMPLES</span></span>

### <span data-ttu-id="6db8c-108">Exempel 1: skaffa VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="6db8c-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="6db8c-109">Det här kommandot får tillägget VMAccess med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6db8c-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="6db8c-110">Exempel 2: Hämta instans vyn för VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="6db8c-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="6db8c-111">Det här kommandot hämtar instans vyn för VMAccess-tillägget med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6db8c-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="6db8c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6db8c-112">PARAMETERS</span></span>

### <span data-ttu-id="6db8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db8c-113">-DefaultProfile</span></span>
<span data-ttu-id="6db8c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6db8c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6db8c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6db8c-115">-Name</span></span>
<span data-ttu-id="6db8c-116">Anger namnet på den fil ändelse som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6db8c-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6db8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6db8c-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6db8c-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6db8c-119">-Status</span><span class="sxs-lookup"><span data-stu-id="6db8c-119">-Status</span></span>
<span data-ttu-id="6db8c-120">Anger att denna cmdlet endast får instans vyn av tillägget.</span><span class="sxs-lookup"><span data-stu-id="6db8c-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="6db8c-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="6db8c-121">-VMName</span></span>
<span data-ttu-id="6db8c-122">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6db8c-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6db8c-123">Denna cmdlet hämtar information om VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6db8c-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6db8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db8c-124">CommonParameters</span></span>
<span data-ttu-id="6db8c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db8c-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db8c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db8c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6db8c-127">INPUTS</span></span>

### <span data-ttu-id="6db8c-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="6db8c-128">None</span></span>
<span data-ttu-id="6db8c-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6db8c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6db8c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6db8c-130">OUTPUTS</span></span>

### <span data-ttu-id="6db8c-131">Microsoft. Azure. commands. Compute. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="6db8c-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="6db8c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6db8c-132">NOTES</span></span>

## <span data-ttu-id="6db8c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6db8c-133">RELATED LINKS</span></span>

[<span data-ttu-id="6db8c-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6db8c-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="6db8c-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6db8c-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="6db8c-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6db8c-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


