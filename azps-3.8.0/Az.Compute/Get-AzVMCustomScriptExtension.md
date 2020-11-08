---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092779"
---
# <span data-ttu-id="af16b-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="af16b-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="af16b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af16b-102">SYNOPSIS</span></span>
<span data-ttu-id="af16b-103">Hämtar information om ett anpassat skript tillägg.</span><span class="sxs-lookup"><span data-stu-id="af16b-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="af16b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af16b-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af16b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af16b-105">DESCRIPTION</span></span>
<span data-ttu-id="af16b-106">Cmdleten **Get-AzVMCustomScriptExtension** hämtar information om ett anpassat namn för en virtuell dator för skript för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="af16b-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="af16b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af16b-107">EXAMPLES</span></span>

### <span data-ttu-id="af16b-108">Exempel 1: Hämta ett anpassat skript tillägg</span><span class="sxs-lookup"><span data-stu-id="af16b-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="af16b-109">Det här kommandot hämtar det anpassade skript tillägget med namnet ContosoCustomScript för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="af16b-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="af16b-110">Exempel 2: Hämta instans visningen av ett anpassat skript tillägg</span><span class="sxs-lookup"><span data-stu-id="af16b-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="af16b-111">Det här kommandot hämtar instans vyn för det anpassade skript tillägget med namnet ContosoCustomScript för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="af16b-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="af16b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af16b-112">PARAMETERS</span></span>

### <span data-ttu-id="af16b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af16b-113">-DefaultProfile</span></span>
<span data-ttu-id="af16b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af16b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af16b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="af16b-115">-Name</span></span>
<span data-ttu-id="af16b-116">Anger namnet på det anpassade skript tillägget som innehåller information om den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af16b-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="af16b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af16b-117">-ResourceGroupName</span></span>
<span data-ttu-id="af16b-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="af16b-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="af16b-119">-Status</span><span class="sxs-lookup"><span data-stu-id="af16b-119">-Status</span></span>
<span data-ttu-id="af16b-120">Anger att denna cmdlet får instans vyn för det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="af16b-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="af16b-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="af16b-121">-VMName</span></span>
<span data-ttu-id="af16b-122">Anger namnet på en virtuell dator för vilken denna cmdlet får det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="af16b-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="af16b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af16b-123">CommonParameters</span></span>
<span data-ttu-id="af16b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af16b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af16b-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af16b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af16b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af16b-126">INPUTS</span></span>

### <span data-ttu-id="af16b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="af16b-127">System.String</span></span>

### <span data-ttu-id="af16b-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af16b-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af16b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af16b-129">OUTPUTS</span></span>

### <span data-ttu-id="af16b-130">Microsoft. Azure. commands. Compute. Models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="af16b-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="af16b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af16b-131">NOTES</span></span>

## <span data-ttu-id="af16b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af16b-132">RELATED LINKS</span></span>

[<span data-ttu-id="af16b-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="af16b-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="af16b-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="af16b-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="af16b-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="af16b-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

