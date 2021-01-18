---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524521"
---
# <span data-ttu-id="dfa36-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dfa36-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="dfa36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfa36-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa36-103">Hämtar inställningarna för DSC-tillägget på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dfa36-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="dfa36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfa36-104">SYNTAX</span></span>

### <span data-ttu-id="dfa36-105">GetDscExtension (standard)</span><span class="sxs-lookup"><span data-stu-id="dfa36-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfa36-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfa36-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfa36-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfa36-107">DESCRIPTION</span></span>
<span data-ttu-id="dfa36-108">Cmdleten **Get-AzVMDscExtension** hämtar inställningarna för tillägget DSC (önskad State Configuration) på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dfa36-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="dfa36-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfa36-109">EXAMPLES</span></span>

### <span data-ttu-id="dfa36-110">Exempel 1: Hämta inställningar för en DSC-anknytning</span><span class="sxs-lookup"><span data-stu-id="dfa36-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="dfa36-111">Det här kommandot får inställningar för tillägget DSC på den virtuella datorn med namnet VM07.</span><span class="sxs-lookup"><span data-stu-id="dfa36-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="dfa36-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfa36-112">PARAMETERS</span></span>

### <span data-ttu-id="dfa36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa36-113">-DefaultProfile</span></span>
<span data-ttu-id="dfa36-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfa36-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfa36-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfa36-115">-Name</span></span>
<span data-ttu-id="dfa36-116">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="dfa36-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="dfa36-117">Set-AzVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, som är samma värde som används av **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="dfa36-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="dfa36-118">Ange endast den här parametern om du har ändrat standard namnet i cmdleten **set-AzVMDscExtension** eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="dfa36-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa36-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa36-119">-ResourceGroupName</span></span>
<span data-ttu-id="dfa36-120">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dfa36-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa36-121">-Status</span><span class="sxs-lookup"><span data-stu-id="dfa36-121">-Status</span></span>
<span data-ttu-id="dfa36-122">Anger att denna cmdlet får instans vyn av DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="dfa36-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa36-123">-VM</span><span class="sxs-lookup"><span data-stu-id="dfa36-123">-VM</span></span>
<span data-ttu-id="dfa36-124">Anger det virtuella dator objekt som tillägget är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="dfa36-124">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa36-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="dfa36-125">-VMName</span></span>
<span data-ttu-id="dfa36-126">Anger namnet på en virtuell dator för vilken denna cmdlet får DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="dfa36-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa36-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa36-127">CommonParameters</span></span>
<span data-ttu-id="dfa36-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa36-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa36-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfa36-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa36-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfa36-130">INPUTS</span></span>

### <span data-ttu-id="dfa36-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dfa36-131">System.String</span></span>

### <span data-ttu-id="dfa36-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dfa36-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dfa36-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfa36-133">OUTPUTS</span></span>

### <span data-ttu-id="dfa36-134">Microsoft. Azure. commands. Compute. extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="dfa36-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="dfa36-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfa36-135">NOTES</span></span>

## <span data-ttu-id="dfa36-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfa36-136">RELATED LINKS</span></span>

[<span data-ttu-id="dfa36-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dfa36-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="dfa36-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dfa36-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


