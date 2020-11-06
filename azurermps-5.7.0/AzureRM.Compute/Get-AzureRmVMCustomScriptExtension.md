---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576613"
---
# <span data-ttu-id="cda95-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cda95-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="cda95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cda95-102">SYNOPSIS</span></span>
<span data-ttu-id="cda95-103">Hämtar information om ett anpassat skript tillägg.</span><span class="sxs-lookup"><span data-stu-id="cda95-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cda95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cda95-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="cda95-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cda95-105">DESCRIPTION</span></span>
<span data-ttu-id="cda95-106">Cmdleten **Get-AzureRmVMCustomScriptExtension** hämtar information om ett anpassat namn för en virtuell dator för skript för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="cda95-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="cda95-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cda95-107">EXAMPLES</span></span>

### <span data-ttu-id="cda95-108">Exempel 1: Hämta ett anpassat skript tillägg</span><span class="sxs-lookup"><span data-stu-id="cda95-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="cda95-109">Det här kommandot hämtar det anpassade skript tillägget med namnet ContosoCustomScript för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="cda95-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="cda95-110">Exempel 2: Hämta instans visningen av ett anpassat skript tillägg</span><span class="sxs-lookup"><span data-stu-id="cda95-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="cda95-111">Det här kommandot hämtar instans vyn för det anpassade skript tillägget med namnet ContosoCustomScript för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="cda95-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="cda95-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cda95-112">PARAMETERS</span></span>

### <span data-ttu-id="cda95-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cda95-113">-Name</span></span>
<span data-ttu-id="cda95-114">Anger namnet på det anpassade skript tillägget som innehåller information om den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cda95-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="cda95-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda95-115">-ResourceGroupName</span></span>
<span data-ttu-id="cda95-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cda95-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cda95-117">-Status</span><span class="sxs-lookup"><span data-stu-id="cda95-117">-Status</span></span>
<span data-ttu-id="cda95-118">Anger att denna cmdlet får instans vyn för det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="cda95-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="cda95-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="cda95-119">-VMName</span></span>
<span data-ttu-id="cda95-120">Anger namnet på en virtuell dator för vilken denna cmdlet får det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="cda95-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="cda95-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda95-121">CommonParameters</span></span>
<span data-ttu-id="cda95-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda95-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda95-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda95-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda95-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cda95-124">INPUTS</span></span>

### <span data-ttu-id="cda95-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="cda95-125">None</span></span>
<span data-ttu-id="cda95-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cda95-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cda95-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cda95-127">OUTPUTS</span></span>

## <span data-ttu-id="cda95-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cda95-128">NOTES</span></span>

## <span data-ttu-id="cda95-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cda95-129">RELATED LINKS</span></span>

[<span data-ttu-id="cda95-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cda95-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="cda95-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="cda95-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="cda95-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="cda95-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


