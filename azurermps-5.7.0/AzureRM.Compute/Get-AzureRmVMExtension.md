---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574366"
---
# <span data-ttu-id="805d2-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="805d2-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="805d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="805d2-102">SYNOPSIS</span></span>
<span data-ttu-id="805d2-103">Hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="805d2-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="805d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="805d2-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="805d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="805d2-105">DESCRIPTION</span></span>
<span data-ttu-id="805d2-106">Cmdleten **Get-AzureRmVMExtension** hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="805d2-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="805d2-107">Ange namnet på ett tillägg som du vill hämta egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="805d2-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="805d2-108">Om du bara vill få instans visningen av ett fil namn anger du en status parameter.</span><span class="sxs-lookup"><span data-stu-id="805d2-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="805d2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="805d2-109">EXAMPLES</span></span>

### <span data-ttu-id="805d2-110">Exempel 1: Hämta egenskaper för ett tillägg</span><span class="sxs-lookup"><span data-stu-id="805d2-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="805d2-111">Det här kommandot får egenskaper för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="805d2-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="805d2-112">Exempel 2: Hämta instans visning av ett tillägg</span><span class="sxs-lookup"><span data-stu-id="805d2-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="805d2-113">Med det här kommandot hämtas instans-vyn för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="805d2-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="805d2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="805d2-114">PARAMETERS</span></span>

### <span data-ttu-id="805d2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="805d2-115">-Name</span></span>
<span data-ttu-id="805d2-116">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="805d2-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="805d2-117">Denna cmdlet hämtar egenskaper för tillägget som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="805d2-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="805d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="805d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="805d2-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="805d2-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="805d2-120">-Status</span><span class="sxs-lookup"><span data-stu-id="805d2-120">-Status</span></span>
<span data-ttu-id="805d2-121">Anger att denna cmdlet bara får instans vyn av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="805d2-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="805d2-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="805d2-122">-VMName</span></span>
<span data-ttu-id="805d2-123">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="805d2-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="805d2-124">Denna cmdlet hämtar egenskaper för ett tillägg från den virtuella dator som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="805d2-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="805d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805d2-125">CommonParameters</span></span>
<span data-ttu-id="805d2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="805d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805d2-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805d2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805d2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="805d2-128">INPUTS</span></span>

### <span data-ttu-id="805d2-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="805d2-129">None</span></span>
<span data-ttu-id="805d2-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="805d2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="805d2-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="805d2-131">OUTPUTS</span></span>

## <span data-ttu-id="805d2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="805d2-132">NOTES</span></span>

## <span data-ttu-id="805d2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="805d2-133">RELATED LINKS</span></span>

[<span data-ttu-id="805d2-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="805d2-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="805d2-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="805d2-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


