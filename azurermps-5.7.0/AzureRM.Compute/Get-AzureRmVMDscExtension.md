---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574370"
---
# <span data-ttu-id="170eb-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="170eb-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="170eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="170eb-102">SYNOPSIS</span></span>
<span data-ttu-id="170eb-103">Hämtar inställningarna för DSC-tillägget på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="170eb-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="170eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="170eb-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="170eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="170eb-105">DESCRIPTION</span></span>
<span data-ttu-id="170eb-106">Cmdleten **Get-AzureRmVMDscExtension** hämtar inställningarna för tillägget DSC (önskad State Configuration) på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="170eb-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="170eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="170eb-107">EXAMPLES</span></span>

### <span data-ttu-id="170eb-108">Exempel 1: Hämta inställningar för en DSC-anknytning</span><span class="sxs-lookup"><span data-stu-id="170eb-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="170eb-109">Det här kommandot får inställningar för tillägget DSC på den virtuella datorn med namnet VM07.</span><span class="sxs-lookup"><span data-stu-id="170eb-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="170eb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="170eb-110">PARAMETERS</span></span>

### <span data-ttu-id="170eb-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="170eb-111">-Name</span></span>
<span data-ttu-id="170eb-112">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="170eb-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="170eb-113">Set-AzureRmVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, som är samma värde som används av **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="170eb-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="170eb-114">Ange endast den här parametern om du har ändrat standard namnet i cmdleten **set-AzureRmVMDscExtension** eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="170eb-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="170eb-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="170eb-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="170eb-117">-Status</span><span class="sxs-lookup"><span data-stu-id="170eb-117">-Status</span></span>
<span data-ttu-id="170eb-118">Anger att denna cmdlet får instans vyn av DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="170eb-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170eb-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="170eb-119">-VMName</span></span>
<span data-ttu-id="170eb-120">Anger namnet på en virtuell dator för vilken denna cmdlet får DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="170eb-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170eb-121">CommonParameters</span></span>
<span data-ttu-id="170eb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170eb-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170eb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170eb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="170eb-124">INPUTS</span></span>

### <span data-ttu-id="170eb-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="170eb-125">None</span></span>
<span data-ttu-id="170eb-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="170eb-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="170eb-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="170eb-127">OUTPUTS</span></span>

### <span data-ttu-id="170eb-128">Microsoft. Azure. commands. Compute. extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="170eb-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="170eb-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="170eb-129">NOTES</span></span>

## <span data-ttu-id="170eb-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="170eb-130">RELATED LINKS</span></span>

[<span data-ttu-id="170eb-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="170eb-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="170eb-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="170eb-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


