---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 889bd206566b9c722aa187f9e32a76c1711af337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755546"
---
# <span data-ttu-id="f7a8a-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f7a8a-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="f7a8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a8a-103">Hämtar information om VMAccess-tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7a8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7a8a-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7a8a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a8a-106">Cmdleten **Get-AzureRmVMAccessExtension** hämtar information om tillägget virtuell dator åtkomst (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="f7a8a-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="f7a8a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7a8a-107">EXAMPLES</span></span>

### <span data-ttu-id="f7a8a-108">Exempel 1: skaffa VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="f7a8a-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="f7a8a-109">Det här kommandot får tillägget VMAccess med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="f7a8a-110">Exempel 2: Hämta instans vyn för VMAccess-tillägget</span><span class="sxs-lookup"><span data-stu-id="f7a8a-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="f7a8a-111">Det här kommandot hämtar instans vyn för VMAccess-tillägget med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="f7a8a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7a8a-112">PARAMETERS</span></span>

### <span data-ttu-id="f7a8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a8a-113">-DefaultProfile</span></span>
<span data-ttu-id="f7a8a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a8a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7a8a-115">-Name</span></span>
<span data-ttu-id="f7a8a-116">Anger namnet på den fil ändelse som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f7a8a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a8a-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7a8a-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f7a8a-119">-Status</span><span class="sxs-lookup"><span data-stu-id="f7a8a-119">-Status</span></span>
<span data-ttu-id="f7a8a-120">Anger att denna cmdlet endast får instans vyn av tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="f7a8a-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="f7a8a-121">-VMName</span></span>
<span data-ttu-id="f7a8a-122">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f7a8a-123">Denna cmdlet hämtar information om VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7a8a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a8a-124">CommonParameters</span></span>
<span data-ttu-id="f7a8a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7a8a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a8a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a8a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a8a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7a8a-127">INPUTS</span></span>

### <span data-ttu-id="f7a8a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f7a8a-128">System.String</span></span>

### <span data-ttu-id="f7a8a-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7a8a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7a8a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7a8a-130">OUTPUTS</span></span>

### <span data-ttu-id="f7a8a-131">Microsoft. Azure. commands. Compute. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f7a8a-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="f7a8a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7a8a-132">NOTES</span></span>

## <span data-ttu-id="f7a8a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7a8a-133">RELATED LINKS</span></span>

[<span data-ttu-id="f7a8a-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f7a8a-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f7a8a-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f7a8a-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f7a8a-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f7a8a-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


