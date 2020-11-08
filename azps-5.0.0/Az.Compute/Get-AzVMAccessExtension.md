---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263349"
---
# <span data-ttu-id="22b91-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b91-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="22b91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22b91-102">SYNOPSIS</span></span>
<span data-ttu-id="22b91-103">Hämtar information om VMAccess-tillägget.</span><span class="sxs-lookup"><span data-stu-id="22b91-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="22b91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22b91-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b91-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22b91-105">DESCRIPTION</span></span>
<span data-ttu-id="22b91-106">Cmdleten **Get-AzVMAccessExtension** hämtar information om tillägget virtuell dator åtkomst (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="22b91-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="22b91-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22b91-107">EXAMPLES</span></span>

### <span data-ttu-id="22b91-108">Exempel 1: skaffa VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="22b91-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="22b91-109">Det här kommandot får tillägget VMAccess med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="22b91-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="22b91-110">Exempel 2: Hämta instans vyn för VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="22b91-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="22b91-111">Det här kommandot hämtar instans vyn för VMAccess-tillägget med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="22b91-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="22b91-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22b91-112">PARAMETERS</span></span>

### <span data-ttu-id="22b91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b91-113">-DefaultProfile</span></span>
<span data-ttu-id="22b91-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22b91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b91-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="22b91-115">-Name</span></span>
<span data-ttu-id="22b91-116">Anger namnet på den fil ändelse som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="22b91-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b91-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b91-117">-ResourceGroupName</span></span>
<span data-ttu-id="22b91-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="22b91-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b91-119">-Status</span><span class="sxs-lookup"><span data-stu-id="22b91-119">-Status</span></span>
<span data-ttu-id="22b91-120">Anger att denna cmdlet endast får instans vyn av tillägget.</span><span class="sxs-lookup"><span data-stu-id="22b91-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b91-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="22b91-121">-VMName</span></span>
<span data-ttu-id="22b91-122">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="22b91-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="22b91-123">Denna cmdlet hämtar information om VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="22b91-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b91-124">CommonParameters</span></span>
<span data-ttu-id="22b91-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b91-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22b91-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b91-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22b91-127">INPUTS</span></span>

### <span data-ttu-id="22b91-128">System. String</span><span class="sxs-lookup"><span data-stu-id="22b91-128">System.String</span></span>

### <span data-ttu-id="22b91-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22b91-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22b91-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22b91-130">OUTPUTS</span></span>

### <span data-ttu-id="22b91-131">Microsoft. Azure. commands. Compute. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="22b91-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="22b91-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22b91-132">NOTES</span></span>

## <span data-ttu-id="22b91-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22b91-133">RELATED LINKS</span></span>

[<span data-ttu-id="22b91-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b91-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="22b91-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="22b91-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="22b91-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="22b91-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


